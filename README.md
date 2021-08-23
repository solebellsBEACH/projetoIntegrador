# projetoIntegrador

ALTER TABLE Animal ADD CONSTRAINT FK_Animal_3
    FOREIGN KEY (fk_Tipo_Animais_codigo)
    REFERENCES Tipo_Animais (codigo)
    ON DELETE SET NULL;
 
ALTER TABLE Donatario ADD CONSTRAINT FK_Donatario_2
    FOREIGN KEY (fk_Animal_codigo)
    REFERENCES Animal (codigo)
    ON DELETE SET NULL;
    
  ALTER TABLE Animal ADD CONSTRAINT FK_Animal_2
    FOREIGN KEY (fk_Doador_codigo)
    REFERENCES Doador (codigo)
    ON DELETE RESTRICT;
    
   
ALTER TABLE Solicita_Doa ADD CONSTRAINT FK_Solicita_Doa_1
    FOREIGN KEY (fk_Donatario_codigo)
    REFERENCES Donatario (codigo)
    ON DELETE SET NULL;
 
ALTER TABLE Solicita_Doa ADD CONSTRAINT FK_Solicita_Doa_2
    FOREIGN KEY (fk_Doador_codigo)
    REFERENCES Doador (codigo)
    ON DELETE SET NULL;
 
ALTER TABLE Escolhe_Escolhidos ADD CONSTRAINT FK_Escolhe_Escolhidos_1
    FOREIGN KEY (fk_Donatario_codigo)
    REFERENCES Donatario (codigo)
    ON DELETE SET NULL;
 
ALTER TABLE Escolhe_Escolhidos ADD CONSTRAINT FK_Escolhe_Escolhidos_2
    FOREIGN KEY (fk_Animal_codigo)
    REFERENCES Animal (codigo)
    ON DELETE SET NULL;
 
ALTER TABLE Conter_Ser ADD CONSTRAINT FK_Conter_Ser_1
    FOREIGN KEY (fk_Tipo_Animais_Codigo)
    REFERENCES Tipo_Animais (Codigo)
    ON DELETE RESTRICT;
 
ALTER TABLE Conter_Ser ADD CONSTRAINT FK_Conter_Ser_2
    FOREIGN KEY (fk_Animal_codigo)
    REFERENCES Animal (codigo)
    ON DELETE SET NULL;
