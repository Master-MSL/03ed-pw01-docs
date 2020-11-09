Studio delle licenze open-source e loro compatibilità
=====================================================

In questa fase analizzeremo i diversi progetti open-source scelti e le
loro licenze verificando se possano esserci delle incompatibilità e se
questo possa determinare difficoltà nel riuscirli ad integrare e/o
rilasciare.

Si affronterà la necessità di capire se ci potrebbero essere dei vincoli
nell’adozione di ulteriori licenze open-source sui moduli da sviluppare
che non creino nuove problematiche con i software fino ad ora scelti.

Nella seguente tabella riassumiamo i dati raccolti:

+---------+---------+---------+---------+---------+---------+---------+
| S       | Licence | Com     | S       | Ap      | Comp    | C       |
| oftware |         | mercial | oftware | provata | atibile | opyleft |
|         |         | use     | libero  | OSI     | GPL     |         |
+---------+---------+---------+---------+---------+---------+---------+
| TheHive | AGP     | SI      | SI      | SI      | SI (con | SI      |
|         | L-3.0-o |         |         |         | p       |         |
|         | r-later |         |         |         | rogetti |         |
|         |         |         |         |         | GPLv3)  |         |
+---------+---------+---------+---------+---------+---------+---------+
| MISP    | AGP     | SI      | SI      | SI      | SI (con | SI      |
|         | L-3.0-o |         |         |         | p       |         |
|         | r-later |         |         |         | rogetti |         |
|         |         |         |         |         | GPLv3)  |         |
+---------+---------+---------+---------+---------+---------+---------+
| BSD     | SI      | SI      | SI      | SI      | NO      |         |
| 2       |         |         |         |         |         |         |
| -Clause |         |         |         |         |         |         |
| “Simp   |         |         |         |         |         |         |
| lified” |         |         |         |         |         |         |
| License |         |         |         |         |         |         |
+---------+---------+---------+---------+---------+---------+---------+
| Cortex  | AGP     | SI      | SI      | SI      | SI (con | SI      |
|         | L-3.0-o |         |         |         | p       |         |
|         | r-later |         |         |         | rogetti |         |
|         |         |         |         |         | GPLv3)  |         |
+---------+---------+---------+---------+---------+---------+---------+
| STIX    | GNU     | SI      | SI      | SI      | SI (con | SI      |
|         | General |         |         |         | p       |         |
|         | Public  |         |         |         | rogetti |         |
|         | License |         |         |         | GPLv3)  |         |
|         | v3.0    |         |         |         |         |         |
+---------+---------+---------+---------+---------+---------+---------+
| TAXII   | BSD     | SI      | SI      | SI      | SI      | NO      |
|         | 3       |         |         |         |         |         |
|         | -Clause |         |         |         |         |         |
|         | "New"   |         |         |         |         |         |
|         | or      |         |         |         |         |         |
|         | "R      |         |         |         |         |         |
|         | evised" |         |         |         |         |         |
|         | License |         |         |         |         |         |
+---------+---------+---------+---------+---------+---------+---------+

.. _section-6:

Licenze coinvolte
^^^^^^^^^^^^^^^^^

-  **Licenza Pubblica GNU versione 3 (GNU General Public License
   v3.0):** E’ una licenza che garantisce agli utenti finali come
   organizzazioni, imprese o semplici individui, di utilizzare,
   condividere e modificare il software. E’ una licenza copyleft, il che
   significa che le opere derivate possono essere distribuite solo sotto
   gli stessi termini di licenza. Questa licenza è progettata per essere
   applicata facilmente ai programmi se si è titolari dei relativi
   diritti. Per far questo, non bisogna modificarla ma solamente
   aggiungere nel programma una nota che vi faccia riferimento. [1]

-  **Licenza Pubblica Generica GNU Affero (GNU Affero General Public
   License, AGPL) versione 3**: E' una licenza di software libero ed è
   una licenza con copyleft. I termini d'uso sono effettivamente quelli
   della GPLv3 con un paragrafo aggiuntivo nella sezione 13, che
   permette agli utenti che interagiscono tramite una rete con il
   programma a cui si applica la licenza di ricevere il sorgente di quel
   programma. [2]
-  **Licenza BSD 3-Clause modificata**: Questa è la licenza BSD
   originale, modificata rimuovendo la clausola pubblicitaria. È una
   licenza per software libero debole e permissiva, senza copyleft,
   compatibile con la GNU GPLv3. Talvolta questa licenza è denominata
   "la licenza BSD con 3 clausole".[3]

Lo schema, di seguito, presentato può essere spiegato fornendo l’esempio
tratto dal sito sponsorizzato dalla Free Software Foundation
(http://www.gnu.org/):

“[...] Le frecce che vanno da una licenza all'altra indicano che la
prima licenza è compatibile con la seconda. Ciò rimane vero anche se per
arrivare da una licenza all'altra seguite più di una freccia; e così, ad
esempio, la licenza ISC è compatibile con la GPLv3. La GPLv2 è
compatibile con la GPLv3 se il programma vi permette di scegliere una
"versione successiva" della GPL, che è il caso della maggior parte del
software rilasciato con questa licenza. Questo diagramma non è completo
(si veda la nostra pagina sulle licenze per una lista più completa delle
licenze compatibili con le GPL versioni 2 e 3), ma illustra chiaramente
che la GPLv3 è compatibile con praticamente ogni cosa con la quale la
GPLv2 è compatibile, e anche qualcuna in più. […]”

|image25|

Considerando le licenze coinvolte questo permetterà una più facile
distribuzione dell’intera soluzione e, da i dati raccolti e dallo schema
presentato, è possibile determinare che tutte le licenze coinvolte sono
compatibili con la licenza GPLv3.

La licenza AGPLv3 è una licenza di software libero con copyleft. I
termini d'uso sono effettivamente quelli della GPLv3 con un paragrafo
aggiuntivo nella sezione 13, che permette agli utenti, che interagiscono
tramite una rete con il software, di ricevere il sorgente di quel
programma.

La Free Software Foundation raccomanda questa licenza per ogni software
che sia comunemente pensato per applicazioni web e che in generale siano
rese disponibili su una rete. La AGPL non è compatibile con la GPL 2.0
perché la sezione 13 rientra nella definizione di "restrizioni
aggiuntive" fornita dalla vecchia versione della GPL. È però pienamente
compatibile con la GPLv3, grazie a una sezione appositamente inserita in
essa.

L'introduzione della AGPL è dovuta al cosiddetto ASP loophole, cioè si
ha la possibilità di fornire servizi tramite software libero
modificandone il contenuto senza aver l’obbligo di dover distribuire le
modifiche effettuate, violando di fatto il concetto di software libero,
volto alla diffusione della conoscenza.

Infatti l'obbligo di rendere disponibile il codice sorgente modificato
nella GNU GPLv3 è legato alla circolazione del software, per cui non
sorge alcun obbligo in tal senso se il codice modificato non viene in
alcun modo distribuito.

Da qui si pone il problema in cui, invece di distribuire il codice, si
distribuiscono le funzionalità del codice rendendolo disponibile con
un'interfaccia remota. In questo caso, seppure la sezione della GNU
GPLv3 non viene violata, ne viene violato lo spirito in quanto ci si
avvale di materiale soggetto a copyright di altri senza rendere alla
comunità le modifiche effettuate.

Si noti che la GNU AGPLv3 non è compatibile con la GPLv2. Tecnicamente
non è compatibile nemmeno con la GPLv3: non si può prendere codice
rilasciato sotto GNU AGPL e distribuirlo o modificarlo alle condizioni
della GPLv3 o viceversa. Tuttavia, è possibile combinare in un unico
progetto moduli separati o file sorgente rilasciate sotto entrambe le
licenze, il che darà a molti programmatori tutte le libertà di cui
necessitano per realizzare il programma che desiderano.

Analizzando la sezione 13 di entrambe e licenze si ha un chiaro richiamo
tra le due licenze in maniera inequivocabile e senza ragionevoli dubbi.

**GNU General Public License (GPLv3)**

“[…]

13. Use with the GNU Affero General Public License.

Notwithstanding any other provision of this License, you have permission
to link or combine any covered work with a work licensed under version 3
of the GNU Affero General Public License into a single combined work,
and to convey the resulting work. The terms of this License will
continue to apply to the part which is the covered work, but the special
requirements of the GNU Affero General Public License, section 13,
concerning interaction through a network will apply to the combination
as such.

[...]”[1]

**GNU Affero General Public License (AGPLv3)**

“[...]13. Remote Network Interaction; Use with the GNU General Public
License.

Notwithstanding any other provision of this License, if you modify the
Program, your modified version must prominently offer all users
interacting with it remotely through a computer network (if your version
supports such interaction) an opportunity to receive the Corresponding
Source of your version by providing access to the Corresponding Source
from a network server at no charge, through some standard or customary
means of facilitating copying of software. This Corresponding Source
shall include the Corresponding Source for any work covered by version 3
of the GNU General Public License that is incorporated pursuant to the
following paragraph.

Notwithstanding any other provision of this License, you have permission
to link or combine any covered work with a work licensed under version 3
of the GNU General Public License into a single combined work, and to
convey the resulting work. The terms of this License will continue to
apply to the part which is the covered work, but the work with which it
is combined will remain governed by version 3 of the GNU General Public
License.

[...]”[2]

Analizzando il contesto non sembrano esserci particolari problematiche
legate alle licenze che intercorrono tra gli strumenti.

Questa considerazione è da considerarsi corretta fino a quando non si
decida di redistribuire a terze parti l’architettura creata se,
naturalmente, sono state apportate modifiche al software originale.

E’ necessario sicuramente calare il contesto delle licenze in gioco con
il contesto normativo italiano facendo riferimento all’ 68 del D.Lgs.
82/2005 (Codice dell’Amministrazione Digitale o CAD) in combinato
disposto con l’art. 69 CAD.

L’articolo 68 CAD, che tratta l’argomento dell’analisi comparativa del
software, prevede quanto segue:

“[…]

Art. 68. Analisi comparativa delle soluzioni

1. Le pubbliche amministrazioni acquisiscono programmi informatici o
parti di essi nel rispetto dei principi di economicità e di efficienza,
tutela degli investimenti, riuso e neutralità tecnologica, a seguito di
una valutazione comparativa di tipo tecnico ed economico tra le seguenti
soluzioni disponibili sul mercato:

a) software sviluppato per conto della pubblica amministrazione;

b) riutilizzo di software o parti di esso sviluppati per conto della
pubblica amministrazione;

c) software libero o a codice sorgente aperto;

d) software fruibile in modalità cloud computing;

e) software di tipo proprietario mediante ricorso a licenza d’uso;

f) software combinazione delle precedenti soluzioni.

1-bis. A tal fine, le pubbliche amministrazioni prima di procedere
all’acquisto, secondo le procedure di cui al codice di cui al decreto
legislativo n. 50 del 2016, effettuano una valutazione comparativa delle
diverse soluzioni disponibili sulla base dei seguenti criteri:

a) costo complessivo del programma o soluzione quale costo di acquisto,
di implementazione, di mantenimento e supporto;

b) livello di utilizzo di formati di dati e di interfacce di tipo aperto
nonché di standard in grado di assicurare l’interoperabilità e la
cooperazione applicativa tra i diversi sistemi informatici della
pubblica amministrazione;

c) garanzie del fornitore in materia di livelli di sicurezza, conformità
alla normativa in materia di protezione dei dati personali, livelli di
servizio tenuto conto della tipologia di software acquisito.

1-ter. Ove dalla valutazione comparativa di tipo tecnico ed economico,
secondo i criteri di cui al comma 1-bis, risulti motivatamente
l’impossibilità di accedere a soluzioni già disponibili all’interno
della pubblica amministrazione, o a software liberi o a codici sorgente
aperto, adeguati alle esigenze da soddisfare, è consentita
l’acquisizione di programmi informatici di tipo proprietario mediante
ricorso a licenza d’uso. La valutazione di cui al presente comma è
effettuata secondo le modalità e i criteri definiti dall’AgID. [...]“[4]

La nostra soluzione comparativa ha cercato di fornire elementi di
fattibilità con soluzioni a riuso fornite dalla CERT-PA e, vista
l’impossibilità momentanea di approfondire la soluzione da loro
proposta, è stato necessario trovare alternative open-source che
avrebbero potuto soddisfare le nostre esigenze.

La soluzione open-source individuata è sicuramente di interesse per il
dominio dell’argomento trattato e quindi non si è ritenuto necessario
approfondire ulteriori software proprietari.

Naturalmente la soluzione individuata dovrà essere conforme e rispettare
l’art. 69 CAD, che dice:

“[…]

Art. 69. Riuso delle soluzioni e standard aperti

1. Le pubbliche amministrazioni che siano titolari di soluzioni e
programmi informatici realizzati su specifiche indicazioni del
committente pubblico, hanno l’obbligo di rendere disponibile il relativo
codice sorgente, completo della documentazione e rilasciato in
repertorio pubblico sotto licenza aperta, in uso gratuito ad altre
pubbliche amministrazioni o ai soggetti giuridici che intendano
adattarli alle proprie esigenze, salvo motivate ragioni di ordine e
sicurezza pubblica, difesa nazionale e consultazioni elettorali.

2. Al fine di favorire il riuso dei programmi informatici di proprietà
delle pubbliche amministrazioni, ai sensi del comma 1, nei capitolati o
nelle specifiche di progetto è previsto, salvo che ciò risulti
eccessivamente oneroso per comprovate ragioni di carattere
tecnico-economico, che l’amministrazione committente sia sempre titolare
di tutti i diritti sui programmi e i servizi delle tecnologie
dell’informazione e della comunicazione, appositamente sviluppati per
essa.

2-bis. Al medesimo fine di cui al comma 2, il codice sorgente, la
documentazione e la relativa descrizione tecnico funzionale di tutte le
soluzioni informatiche di cui al comma 1 sono pubblicati attraverso una
o più piattaforme individuate dall’AgID con proprie Linee guida.

[...]”[5]

che di fatto prevede di considerare e, quindi, di favorire il riuso del
software stesso tra più amministrazioni.

È dunque necessario che la prima considerazione in ordine di importanza
nella scelta della licenza sia quella di valutare l’impatto che il testo
della licenza ha sulla possibilità di riuso da parte di altre
amministrazioni.

“[…] Una licenza aperta, così come intesa nell’Art. 69 del CAD, è una
licenza che garantisca all’utente di un software le seguenti libertà:

-  Libertà di eseguire il software come si desidera, per qualsiasi
   scopo, senza ulteriori costi o restrizioni;
-  Libertà di studiare come funziona il software e di modificarlo in
   modo da adattarlo alle proprie necessità;
-  Libertà di ridistribuire copie del software;
-  Libertà di modificare il software e distribuirne pubblicamente le
   versioni modificate.

*L’accesso al codice sorgente, o parimenti al formato necessario per
riprodurre e modificare un’opera, è un prerequisito per rispettare tali
libertà. […]” [6]*

Visto tutte le considerazioni fatte in precedenza e viste le indicazioni
sopra riportate dell’Art. 69 del CAD, il punto più critico su cui è
necessario fare un approfondimento è sicuramente quello riportato come
ultimo punto dell’Art. 69 del CAD, sarà necessario quindi verificare
che, se avvenisse un arricchimento della soluzione proposta da parte di
una Pubblica Amministrazione, questa dovrà e potrà rispettare le licenze
open-source dei sistemi integrati se solo se ripubblicasse il progetto
di integrazione mantenendo la licenza AGPLv3 e converrebbe pensare a
migliorare la soluzione definitiva introducendo nuovi componenti
software che possano interagire via rete piuttosto che modificare il
codice sorgente di uno dei software scelti.

La licenza AGPLv3 è una licenza consigliata da Agid e Team digitale come
riportato nel paragrafo 3.5 del documento “Linee guida su acquisizione e
riuso di software per le pubbliche amministrazioni “ *[6]*\ che tratta
questo argomento fornendo un vademecum su come e quale licenza
open-source scegliere.

Una considerazione interessante è legata al progetto in riuso proposto
da CERT-PA analizzata nel paragrafo “Ambito tecnologico” che propone una
soluzione open-source facendo uso di altri strumenti e l’aggiunta di una
componente software: CNTI. Questa componente ha una interazione via
network con gli altri strumenti selezionati. Pur non avendo ulteriori
dettagli in merito è presumibile che anche loro abbiano scelto una
soluzione con licenza AGPLv3 per poter avere una interazione con gli
altri strumenti selezionati, questo approccio avvalla le considerazioni
fatte in precedenza e su come poter approcciare un eventuale
arricchimento della soluzione definitiva.

.. _section-7:
