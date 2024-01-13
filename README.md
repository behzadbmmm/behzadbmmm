import math
class Mostatil:
    def __init__(self, arz, tol):
        self.arz = arz
        self.tol = tol
        if arz == tol:
            raise ("نمیشه توی مستطیل طول و عرض یکی باشه")

    def __repr__(self):
        return f"mostatil ba arz {self.arz} va tol {self.tol}"

    def __eq__(self, other):
        return self.masahat() == other.masahat()

    def __gt__(self, other):
        return self.masahat() > other.masahat()

    def masahat(self):
        return self.arz * self.tol

    def mohit(self):
        return (self.arz * 2) + (self.tol * 2)


class Moraba:
    def __init__(self, zele):
        self.zele = zele

    def __repr__(self):
        return f"moraba ba zele {self.zele}"

    def __eq__(self, other):
        return self.masahat() == other.masahat()

    def __gt__(self, other):
        return self.masahat() > other.masahat()

    def masahat(self):
        return self.zele * self.zele

    def mohit(self):
        return self.zele * 4


class Mosalas:
    def __init__(self, ghaede, ertefa):
        self.ghaede = ghaede
        self.ertefa = ertefa

    def __repr__(self):
        return f"mosalas ba ertefa {self.ertefa} va ghaede {self.ghaede}"

    def __eq__(self, other):
        return self.masahat() == other.masahat()

    def __gt__(self, other):
        return self.masahat() > other.masahat()

    def masahat(self):
        return (self.ghaede * self.ertefa) / 2

    def mohit(self):
        return "من اندازه ضلع های شما را ندارم لظفا سه ضلع را در هم جمع کنید"


class Zozanaghe:
    def __init__(self, ghaede_kochick, ghaede_bozorg, ertefa):
        self.ghaede_kochick = ghaede_kochick
        self.ghaede_bozorg = ghaede_bozorg
        self.ertefa = ertefa
        if self.ghaede_kochick > self.ghaede_bozorg:
            raise ("قاعده بزرگ نمیشه از قاعده کوچک کوچک تر باشه")

    def __repr__(self):
        return f"zozanagh ba ghaede kochak{self.ghaede_kochick} va ghaede bozorg{self.ghaede_bozorg} va ertefa {self.ertefa}"

    def __eq__(self, other):
        return self.masahat() == other.masahat()

    def __gt__(self, other):
        return self.masahat() > other.masahat()

    def masahat(self):
        return (self.ghaede_bozorg + self.ghaede_kochick) * self.ertefa / 2

    def mohit(self):
        return ("من اندازه ضلع های شما را ندارم لظفا ضلع ها را در هم جمع کنید")


class Lozi:
    def __init__(self, ghotr_kochik, ghotr_bozorg, zele):
        self.ghotr_kochik = ghotr_kochik
        self.ghotr_bozorg = ghotr_bozorg
        self.zele = zele
        if self.ghotr_kochik > self.ghotr_bozorg:
            raise ("نمیشه قطر بزرگ از کوچک کوچک تر باشه")

    def __repr__(self):
        return f"lozi ba ghotr kochick {self.ghotr_kochik} va ghotr bozorg {self.ghotr_bozorg} va zele {self.zele}"

    def __eq__(self, other):
        return self.masahat() == other.masahat()

    def __gt__(self, other):
        return self.masahat() > other.masahat()

    def masahat(self):
        return (self.ghotr_bozorg + self.ghotr_kochik) / 2

    def mohit(self):
        return self.zele * 4


class Daiere:
    def __init__(self, ghotr):
        self.ghotr = ghotr

    def __repr__(self):
        return f"daiere ba ghotr {self.ghotr}"

    def __eq__(self, other):
        return self.masahat() == other.masahat

    def __gt__(self, other):
        return self.masahat() > other.masahat

    def masahat(self):
        return (self.ghotr / 2) * (self.ghotr / 2) * 3.14

    def mohit(self):
        return self.ghotr * 3.14


class Motavaziol_azla:
    def __init__(self, ghaede, ertefa):
        self.ghaede = ghaede
        self.ertefa = ertefa

    def __repr__(self):
        return f"Motavaziol_azla ba ghaede {self.ghaede} va ertefa {self.ertefa}"

    def __eq__(self, other):
        return self.masahat() == other.masahat

    def __gt__(self, other):
        return self.masahat() > other.masahat

    def masahat(self):
        return self.ghaede * self.ertefa

    def mohit(self):
        return "من اندازه ضلع های شما را ندارم لظفا سه ضلع را در هم جمع کنید"


class Kore:
    def __init__(self, shoa):
        self.shoa = shoa

    def __repr__(self):
        return f"kore ba shoa {self.shoa}"

    def __eq__(self, other):
        return self.masahat() == other.masahat()

    def __gt__(self, other):
        return self.masahat() > other.masahat()

    def masahat(self):
        return 4 * 3.14 * self.shoa ** 2

    def hajm(self):
        return (4 / 3) * 3.14 * self.shoa * self.shoa * self.shoa


class Mokaab_mostatil:
    def __init__(self, arz, tol, ertefa):
        self.arz = arz
        self.tol = tol
        self.ertefa = ertefa

    def __repr__(self):
        return f"mokaab_mostatil ba arz {self.arz} va tol {self.tol} va ertefa {self.ertefa}"

    def __eq__(self, other):
        return self.masahat() == other.masahat()

    def __gt__(self, other):
        return self.masahat() > other.masahat()

    def masahat(self):
        return ((self.arz * self.tol) * 2) + ((self.ertefa * self.arz) * 2) + ((self.ertefa * self.tol) * 2)

    def hajm(self):
        return self.tol * self.arz * self.ertefa


class Mokaab_moraba:
    def __init__(self, zele):
        self.zele = zele

    def __repr__(self):
        return f"mokaab_moraba ba  zele {self.zele}"

    def __eq__(self, other):
        return self.masahat() == other.masahat()

    def __gt__(self, other):
        return self.masahat() > other.masahat()

    def masahat(self):
        return (self.zele * self.zele) * 6

    def hajm(self):
        return (self.zele * self.zele) * self.zele


class Heram_morabai_motenazer:
    def __init__(self, ghaede_mosalas, ertefa_mosalas, ertefa_heram):
        self.ghaede_mosalas = ghaede_mosalas
        self.ertefa_mosalas = ertefa_mosalas
        self.ertefa_heram = ertefa_heram

    def __repr__(self):
        return f"Heram morabai motenazer ba ghaede mosalas {self.ghaede_mosalas} va ertefa mosalas {self.ertefa_mosalas} va ertefa heram {self.ertefa_heram}"

    def __eq__(self, other):
        return self.masahat() == other.masahat()

    def __gt__(self, other):
        return self.masahat() > other.masahat()

    def masahat(self):
        return (self.ghaede_mosalas * self.ghaede_mosalas) + (self.ghaede_mosalas * self.ertefa_mosalas / 2) * 4

    def masahat_ghaede(self):
        return self.ghaede_mosalas * self.ghaede_mosalas

    def hajm(self):
        return (self.ertefa_heram * self.masahat_ghaede()) * (1 / 3)


class Estakhr:
    def __init__(self, ertefa_k,ertfa_b,arz,tol_k,tol_b):
        self.ertefa_k=ertefa_k
        self.ertefa_b=ertfa_b
        self.arz=arz
        self.tol_k=tol_k
        self.tol_b=tol_b
        if self.ertefa_k>ertfa_b:
            raise "نمیشه ارتفاع کوچیک از بزرگ بزرگتر باشه"
        if self.tol_k>tol_b:
            raise "نمیشه طول کوچیک از بزرگ بزرگتر باشه"
    def __repr__(self):
        return f"estakhr ba ertefa kochik {self.ertefa_k} va ertefa bozorg {self.ertefa_b} va arz {self.arz} va tol kochik {self.tol_k} va tol bozorg {self.tol_b}"

    def __eq__(self, other):
        return self.masahat() == other.masahat()

    def __gt__(self, other):
        return self.masahat() > other.masahat()

    def j1 (self):
        return (self.tol_k*self.arz+(self.ertefa_k*self.arz))

    def m2 (self):
        return ((self.tol_b-self.tol_k)**2)+((self.ertefa_b-self.ertefa_k)**2)
    def m3 (self):
        return math.sqrt(self.m2())

    def j2 (self):
        return self.m3()*self.arz
    def j3 (self):
        return self.ertefa_b*self.arz
    def m4 (self):
        return (self.tol_b-self.tol_k)*(self.ertefa_b-self.ertefa_k)/2
    def m5 (self):
        return (self.ertefa_k*self.tol_b)+self.m4()
    def j4 (self):
        return (self.m5()*2)
    def masahat(self):
        return self.j1()+self.j2()+self.j3()+self.j4()

    def n1(self):
        return self.tol_b*self.ertefa_k*self.arz
    def n2(self):
        return (1/2*(self.ertefa_b-self.ertefa_k)*(self.tol_b-self.tol_k))*self.arz
    def hajm(self):
        return (self.n1())+(self.n2())

class Estahkr_mazrae:
    def __init__(self,gh_k_zk,gh_b_zk,gh_k_zb,gh_b_zb,ertefa):
        self.gh_k_zk=gh_k_zk
        self.gh_b_zk=gh_b_zk
        self.gh_k_zb=gh_k_zb
        self.gh_b_zb=gh_b_zb
        self.ertefa=ertefa
    def m1(self):
        return (((self.gh_k_zk+self.gh_b_zk)*self.ertefa)/2)*2
    def m2(self):
        return (((self.gh_k_zb+self.gh_b_zb)*self.ertefa)/2)*2
    def m3(self):
        return (self.gh_b_zb*self.gh_b_zk)
    def m4 (self):
        return (self.gh_k_zk*self.gh_k_zb)
    def masahat(self):
        return self.m1()+self.m2()+self.m4()
    def hajm(self):
        return (self.m4()+self.m3()+math.sqrt(self.m4()*self.m3()))*(self.ertefa/3)






