# ativos_TO.py

class AMVMovimentacao:
    def __init__(self):
        self.status = "Desligado"

    def iniciar(self):
        self.status = "Ligado"
        print("AMV Movimentação iniciado")

    def parar(self):
        self.status = "Desligado"
        print("AMV Movimentação parado")

class Hotbox:
    def __init__(self):
        self.temperatura = 0

    def aquecer(self, temperatura):
        self.temperatura = temperatura
        print(f"Hotbox aquecido a {temperatura} graus")

    def desligar(self):
        self.temperatura = 0
        print("Hotbox desligado")

class Coldwheel:
    def __init__(self):
        self.status = "Desligado"

    def ligar(self):
        self.status = "Ligado"
        print("Coldwheel ligado")

    def desligar(self):
        self.status = "Desligado"
        print("Coldwheel desligado")

class AMVMola:
    def __init__(self):
        self.tensao = 0

    def ajustar_tensao(self, valor):
        self.tensao = valor
        print(f"AMV Mola ajustado para {valor} unidades de tensão")

class Gerador:
    def __init__(self):
        self.status = "Desligado"

    def ligar(self):
        self.status = "Ligado"
        print("Gerador ligado")

    def desligar(self):
        self.status = "Desligado"
        print("Gerador desligado")

class Nobreak:
    def __init__(self):
        self.bateria = 100

    def status_bateria(self):
        print(f"Status da bateria: {self.bateria}%")

    def descarregar(self, valor):
        self.bateria -= valor
        if self.bateria < 0:
            self.bateria = 0
        print(f"Bateria descarregada para {self.bateria}%")

if __name__ == "__main__":
    # Testando os módulos

    # AMV Movimentação
    amv = AMVMovimentacao()
    amv.iniciar()
    amv.parar()

    # Hotbox
    hotbox = Hotbox()
    hotbox.aquecer(100)
    hotbox.desligar()

    # Coldwheel
    coldwheel = Coldwheel()
    coldwheel.ligar()
    coldwheel.desligar()

    # AMV Mola
    amv_mola = AMVMola()
    amv_mola.ajustar_tensao(50)

    # Gerador
    gerador = Gerador()
    gerador.ligar()
    gerador.desligar()

    # Nobreak
    nobreak = Nobreak()
    nobreak.status_bateria()
    nobreak.descarregar(20)
