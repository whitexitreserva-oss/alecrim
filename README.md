model Projeto {
  id          Int      @id @default(autoincrement())
  titulo      String
  destaque    Boolean  @default(false)
  perfil      Perfil   @relation(fields: [perfilId], references: [id])
  perfilId    Int
  habilidades ProjetoHabilidade[]
}
model pessoa {
    id Int   @id @default(autoincrement())
    nome  String
    itens  adress[]
    pessoal int @iddefault
}

model endereço {
    id          Int      @id @default(autoincrement())
    Cidade  String
    Estado  String
    Pais    String 
    Cep     Number       @relation(fields: [pessoaID],
    references: [id])
    pessoaId Int
}
