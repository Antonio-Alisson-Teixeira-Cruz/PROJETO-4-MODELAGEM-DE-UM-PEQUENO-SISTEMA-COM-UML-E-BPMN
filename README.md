Análise e projeto de sistemas - projeto 4 - Modelagem de um pequeno sistema com UML e BPMN

Alunos: Anna Beatryz Gomes Gurgel e Antônio Alisson Teixeira Cruz Sala: 2-ds

Escola: Escola Estadual de Educação Profissional Deputado Roberto Mesquita
Professor: Everson


BPMN do sistema de reserva de sala:

[inicio] -> [receber pedido de cadastro] -> [verificar disponibilidade] -> {sala disponível?}<br>
                                                    -> [sim]<br>
                                                        -> [fazer a reserva da sala, para o usuário]<br>
                                                    -> [não]<br>
                                                        -> [informar o cliente que não será possível a reserva]<br>


UML do sistema de reserva de salas:


+----------------------------+
         CLIENTE
+----------------------------+                  
  - id: int                                           
  - nome: string                  
  - email: sring                    
+----------------------------+
  + realizarPedidoDeReserva()    
+----------------------------+


+-----------------------------+
 RESERVA
+-----------------------------+
 - id: int
 - dataHora: dateTime
 - status: string
- duração: int  
+-----------------------------+
   + verificarDisponibilidade()
   + confirmarPedido()
   + informarCliente()
+-----------------------------+

 
+----------------------+
SALA
+----------------------+
- id: int
- nome:string
- capacidade
+----------------------+


cliente 1 ------ 0 reservas                                 reserva 0 ------ 1 sala
  - Um CLIENTE pode ter várias RESERVAS.                      -Várias RESERVAS equivalem a apenas uma SALA.
  - Várias RESERVAS podem pertencer a um único CLIENTE        -Uma SALA pode ter várias RESERVAS
