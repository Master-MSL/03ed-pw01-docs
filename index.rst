#########################################################################
Studio di fattibilità per soluzioni Cyber Threat Intelligence Open Source
#########################################################################

**Sommario**

Questo progetto riguarda l'analisi e la scelta di una soluzione Open Source che risponda alle esigenze di comunicazione, condivisione di eventi critici in ambito Cyber Security. Si affronterà un percorso che permetterà di scegliere da un punto di vista organizzativo, economico, tecnologico e legale la scelta effettuata. 

Nel Capitolo 1 vengono presentati gli aspetti organizzativi: analisi dell'ambiente esterno, ambiente interno, la stuttura organizzativo, la mission e possibili strategie organizzative.

Nel Capitolo 2 vengono presentati gli aspetti economici: i work package individuati, un piano di implementaizione e GANTT e la SWOT analisi.

Nel Capitolo 3 vengono presentati gli aspetti tecnologici: le analisi delle soluzioni indiduate: in riuso e usando progetti di terze parti con licenza Open Source

Nel Capitolo 4 vengono presentati gli aspetti legali: approfondendo l'uso di quali licence Open Source utilizzato dalla soluzione individuata e possibili vincoli, criticità e/o opportunità che emergono dall'uso di questi strumenti da un punto di vista legale.

Nel Capitolo 5 vengono presentate le conclusioni emerse dal contesto analizzato.

=====================
Analisi Organizzativa
=====================

In questo sezione analizzeremo gli aspetti organizzativi che riguardano
il Project Work in oggetto con l’obbiettivo di far emergere opportunità
ed eventuali problematiche che potremmo incontrare nel corso del
progetto ed eventuali soluzioni che si potrebbero applicare.

Ambiente Esterno
----------------

Negli ultimi anni gli attacchi informatici sono sempre meglio
strutturati ed efficaci.

Dal 2000 ad oggi il CLUSIT (Associazione Italiana per la Sicurezza
Informatica) presenta annualmente un rapporto sulle minacce informatiche
che sono avvenute facendo emergere una situazione sempre più critica
sulla capacità delle organizzazioni criminali di poter aggirare e
attaccare infrastrutture informatiche non adeguatamente protette.

In questo modo possono farne uso per i più disparati scopi:
dall’attivismo alla vendita di dati recuperati da queste azioni, fino a
creare dei veri e propri disservizi dei sistemi informativi che possono
portare a bloccare intere aziende nella loro normale operatività con
ingenti perdite economiche, di immagine e di produttività delle stesse.

|image1|\ Nel grafo è riportato l’andamento degli ultimi sei anni e di
come questo fenomeno stia aumentando.

Questo fenomeno è naturalmente esteso a livello internazionale in tutte
quelle nazioni che ad oggi presentano un minimo livello di
digitalizzazione.

Ci soffermeremo nel descrivere la situazione Europea attuale in modo da
capire esattamente cosa è stato fatto e cosa si sta facendo a tale
proposito.

La Comunità Europea ha approvato nel 2016 la **Direttiva NIS 2016/1148**
(*Network and Information Security*) che è volta a stabilire le misure
per la realizzazione in Europa di un ambiente digitale sicuro e
affidabile.

E' stata recepita col Decreto Legislativo 18 maggio 2018, n. 65,
pubblicato sulla Gazzetta Ufficiale n. 132 del 9 giugno 2018 (entrato in
vigore il 24 giugno 2018).

La Direttiva impone agli Stati Membri dell'Unione europea l'adozione di
una serie di misure di sicurezza comuni ed adeguate, imponendo nel
contempo la notifica degli incidenti all'Autorità nazionale istituita
allo scopo.

Gli Stati dovranno anche promuovere la nascita di CSIRT (**Computer
Security Incident Response Team**) nazionali, sulla base del CERT-UE,
per realizzare un network europeo che si occupi della sicurezza delle
reti critiche.

Gli obiettivi sono, quindi:

-  gestione dei rischi di sicurezza;
-  protezione contro i cyber attacchi;
-  individuazione di incidenti di cyber sicurezza;
-  riduzione dell'impatto degli incidenti di cyber sicurezza.

La Direttiva NIS, e il decreto di attuazione, si rivolgono a due
categorie:

-  **Operatori di servizi essenziali**\ (OES) stabiliti nell'Unione
   europea, cioè i soggetti, pubblici o privati, che forniscono servizi
   essenziali per la società e l'economia nei settori sanitario,
   dell'energia, dei trasporti, bancario, delle infrastrutture dei
   mercati finanziari, della fornitura e distribuzione di acqua potabile
   e delle infrastrutture digitali;
-  **Digital Service Provide**\ r (DSP), cioè le persone giuridiche che
   forniscono servizi della società dell'informazione (e-commerce,
   social network, cloud computing, motori di ricerca, financial
   provider, ecc...); le persone giuridiche che forniscono servizi di
   e-commerce, cloud computing o motori di ricerca, con stabilimento
   principale, sede sociale o rappresentante designato sul territorio
   nazionale.
   Non sono soggetti alla normativa i DSP con meno di 50 dipendenti o
   con fatturato inferiore ai 10 milioni l'anno (piccole e micro
   imprese).

Si tratta di soggetti che sono essenziali per la vita di tutti i giorni
dei cittadini dell’Unione. A tali soggetti la direttiva impone specifici
oneri:

-  **adozione di misure tecniche e organizzative** adeguate alle
   gestione dei rischi e a prevenire e minimizzare l'impatto degli
   incidenti di sicurezza delle reti e dei sistemi informativi, al fine
   di assicurare la continuità del servizio;
-  **obbligo di notifica**, senza ingiustificato ritardo, degli
   incidenti di sicurezza con impatto rilevante, rispettivamente sulla
   continuità e la fornitura del servizio.

La notifica va fatta al **Computer Security Incident Response
Team**\ (CSIRT) italiano, informandone anche l’Autorità competente NIS
di riferimento.

Il CSIRT italiano è istituito presso la Presidenza del Consiglio dei
Ministri mediante unificazione del Computer Emergency Response Team
(CERT) Nazionale e del CERT-PA. Si occupa di:

-  definire le procedure per la prevenzione e la gestione degli
   incidenti informatici;

-  ricevere le notifiche di incidente, informandone il **DIS
   (Dipartimento informazioni per la sicurezza)**\ che coordina i
   servizi segreti:

   -  fornire al notificante le informazioni utili per le gestione
      efficace dell’incidente;
   -  informare gli altri Stati membri dell’UE eventualmente coinvolti
      dall’incidente, tutelando la sicurezza e gli interessi commerciali
      dell’OSE o del FSD nonché la riservatezza delle informazioni
      fornite.

Inoltre la Commissione Europea ha fissato i criteri e le soglie per
stabilire la **rilevanza degli incidenti** da parte dei DSP.

Un incidente è rilevante se si verifica almeno una condizione:

-  indisponibilità del servizio fornito per oltre 5.000.000 di ore
   utente;
-  perdita di integrità, autenticità o riservatezza dei dati per oltre
   100.000 utenti dell’UE;
-  rischio per la sicurezza e/o l’incolumità pubblica, o in termini di
   perdite di vite umane;
-  danni materiali superiori a 1.000.000 di EUR per almeno un utente
   nell’UE.

Il recepimento in Italia della Direttiva NIS può essere riassunta in
questo diagramma:

|image2|

Diversi aspetti di questa Direttiva risultano rilevanti al mantenimento
delle infrastrutture, dei servizi informatici, in particolare:

-  **notifica degli incidenti informatici**: **gli operatori di servizi
   essenziali dovranno inoltrare al CSIRT** (e per conoscenza all’
   autorità competente NIS del proprio settore) **le** **notifiche di
   incidenti informatici**\ con impatto rilevante sui servizi forniti,
   Il decreto non fissa un limite temporale rigido per le notifiche, ma
   specifica che le stesse vanno effettuate “senza ingiustificato
   ritardo”;
-  **trattamento dei dati personali:** il decreto attuativo precisa che
   il trattamento dei dati personali in applicazione del decreto sia
   effettuato ai sensi del D.Lgs. 196/2003. Tale riferimento è diventato
   (almeno in parte) obsoleto con l’entrata in vigore definitiva del
   Regolazione Generale sulla protezione dei dati (GDPR);
-  **regime sanzionatorio:**\ la Direttiva NIS lascia agli Stati membri
   un margine di discrezionalità riguardo al tipo e alla natura delle
   sanzioni applicabili, a condizione che siano effettive, proporzionate
   e dissuasive. Nell’esercitare tale discrezionalità, il governo ha
   ritenuto di stabilire che le autorità competenti potranno applicare
   sanzioni amministrative fino a 150.000 Euro.

Per quanto riguarda il regime sanzionatorio è necessario aggiungere alla
sanzione prevista dalla Direttiva NIS quella introdotta dal GDPR che può
prevedere **m\ ulte** che potranno arrivare **fino a 20 milioni** di
euro e saranno pari al **2% o al 4% del fatturato** per le imprese.

Da questa prima esamina di quello che ad oggi lo scenario rivolto
all’argomento della sicurezza informatica fa emergere diversi aspetti
interessanti da affrontare e approfondire.

Sicuramente questi aspetti necessitano di tempi medio/lunghi per essere
elaborati e devono permeare all’interno della società per accrescere la
cultura generale sotto questi aspetti. La nostra società ci permette di
avere servizi sempre più efficienti ed efficaci ma questo non può
diminuire la l’affidabilità e la certezza che certe operazioni critiche
non vadano a buon fine. Quindi è necessario che i sistemi informativi
forniscano servizi agli utenti sempre più efficienti e sicuri.

E’ necessario quindi, oltre ad investimenti ingenti per migliorare i
sistemi informativi ed infrastrutture, aumentare la cultura generale in
modo da prevenire eventuali problemi e diverrà fondamentale intervenire
in tempi utili riducendo i tempi di notifica prevista dalla Direttiva
NIS.

L’aspetto normativo non è l’unico che è necessario considerare per
affrontare la seguente problematica della sicurezza informatica.

Un altro aspetto importante è la razionalizzazione dei data center
pubblici.

Il processo è distinto in tre fasi ben distinte che hanno avuto inizio
nel 2017 con la pubblicazione da parte dell’Agenzia per l’Italia
Digitale della circolare n. 5 del 30 novembre 2017.

La finalità di questo censimento era\ **l’individuazione delle
infrastrutture candidate a ricoprire il ruolo di PSN** (Poli Strategici
Nazionali) o classificabili nelle categorie:

-  nel Gruppo A rientreranno le amministrazioni che dispongono di data
   center di **qualità intermedia**;
-  nel Gruppo B rientreranno le amministrazioni con\ **infrastrutture
   carenti**;
-  nella categoria candidabile a Polo strategico nazionale (PSN) saranno
   inseriti i **soggetti con data center caratterizzati da elevati
   standard di qualità**.

Con la conclusione della seconda fase, avvenuta il 20 giugno 2018, ha
visto la partecipazione di:

-  778 Amministrazioni,
-  625 amministrazioni hanno dichiarato di possedere Data Center
-  153 amministrazioni hanno dichiarato di non possedere oppure di
   avvalersi di servizi IT erogati da altri soggetti
-  4154 applicazioni critiche

Per un totale di 927 Data Center censiti.

Dal 14 giugno 2019 sta procedendo la Fase 3 del Censimento del
Patrimonio ICT della PA\ **che\ si propone di rilevare i dati necessari
per delineare il quadro informativo/statistico sulle principali
installazioni informatiche a livello nazionale, regionale e locale**,
raccogliendo informazioni circa l’insieme delle principali componenti
hardware e software in uso dalle amministrazioni pubbliche.

Come previsto dalla nuova Circolare AGID n. 1/2019 pubblicata in
Gazzetta Ufficiale (GU Serie Generale n. 152 del 01 luglio 2019) e con
riferimento ai **requisiti** riportati nella tabella dell’Allegato A
della stessa Circolare, ogni singola infrastruttura quindi potrà essere
classificata in una delle seguenti categorie:

-  **Infrastrutture candidabili all’utilizzo da parte di un PSN**, se
   soddisfa tutti i requisiti riportati nella colonna Candidabilità
   all’uso da PSN;
-  **Gruppo A**, se non soddisfa tutti i requisiti riportati nella
   colonna Candidabilità all’uso da PSN ma soddisfa tutti i requisiti
   riportati nella colonna Gruppo A;
-  **Gruppo B**, se non soddisfa i requisiti di cui alle categorie
   precedenti e nel caso di mancata partecipazione alla rilevazione.

Queste fasi e questi cambiamenti fanno parte del **piano triennale per
la pubblica amministrazione 2019 – 2021**\ che indica le linee di azione
per promuovere la trasformazione digitale del settore pubblico e del
Paese.

In questo scenario e nell’attuale processo di trasformazione che sta
avvenendo si possono notare aspetti di forte miglioramento ma anche di
forte responsabilizzazione per strutture informatiche che rispondano ai
requisiti richiesti.

Questo comporterà un’attenzione maggiore verso questi PSN che possiamo
semplificare in due aspetti coerenti al Project Work che stiamo
affrontando:

1. **Economico:** dovuto alla riduzione e semplificazione dell’attuale
   scenario dei data center in Italia che permetterà alle PA italiane di
   ridurre i costi di gestione di data center piccoli e non adeguati.
2. **Sicurezza**: pochi e ben strutturati PSN porteranno a un maggior
   controllo e ridurranno il perimetro migliorandone l’efficacia delle
   protezioni messe in atto.

In questo scenario ricco di cambiamenti e miglioramenti il Project Work
vuole avere un suo ruolo fondamentale: quello di aggregare, correlare e
trasmettere informazioni di attacchi informatici che possono interessare
gli attori coinvolti in questo cambiamento.

In questo contesto tutti gli stakeholder sarebbero parte attiva e
contribuirebbero a mitigare eventuali situazioni critiche che si
potrebbero presentare in ogni instante della normale operatività dei
servizi forniti dalla PA verso i concittadini.

Ad oggi questa operazione è fornita, come dicevamo in precedenza, dal
CERT e CERT-PA con un meccanismo di notifica efficace ed efficiente ma
non sufficientemente celere a bloccare situazioni critiche in atto.

Se consideriamo il fatto che in ogni istante del giorno un attacco
informatico può mettere in crisi le infrastrutture portando alla
paralisi dell’intero data center si ritiene necessario migliorare
l’aspetto di comunicazione tra i vari attori per avere una difesa
globale più efficace, riducendo drasticamente i tempi di comunicazione e
quindi di reazione di tutti i partecipanti.

Ambiente Interno
----------------

Lo scenario che si è presentato finora fa emergere aspetti organizzativi
interessanti e ha delineato cosa può essere considerato come ambiente
esterno e quali possono essere i punti di forza del Project Work e
delinea un ambiente interno molto interessante legato al fatto che tutti
i punti affrontati sono di sicuro interesse da parte di tutti gli attori
che potrebbero essere coinvolti e che potrebbero presentare alcune
caratteristiche particolari anche sotto questo punto di vista.

Uno degli aspetti che emergono con maggiore determinazione è quello
della Community: attori differenti che hanno interessi comuni e
problematiche comuni da affrontare.

Questo aspetto è necessario che venga mantenuto nel tempo ed è
fondamentale che l’interesse e la partecipazione si mantenga almeno
costante nel tempo in modo da permettere uno scambio continuo di idee,
problematiche, metodi di azioni.

La Community è, su questo Project Work, uno degli aspetti fondamentali
perché possa avere successo nel tempo. Questo aspetto dovrà essere
mantenuto arricchendolo di vari contributi che arriveranno all’interno
del gruppo fornendo la giusta visibilità da parte di chi ha fornito
notizia, di chi lo dovrà recepire ed analizzare ed un adeguato ritorno
positivo o negativo sul contributo fornito.

Questo modo potrebbe portare ad una maggiore coesione all’interno della
Community e maggior appartenenza con l’effetto sperato del non
abbandono.

Analizzando i possibili attori della Community è possibile individuare
Enti Nazionali ben distinti che possono portare il loro contributo alla
riuscita del progetto, ad esempio: PSN, Ministero dell’informazione,
Agid, CERT, CERT-PA, Polizia Postale di Stato.

Da questo breve elenco, che non vuole considerarsi esaustivo, emerge una
situazione molto eterogenea di come questi attori sono strutturati al
loro interno e nei loro processi, e si rende necessario quindi pensare
ad un modello di governo dell’intero Project Work che non abbia la
presunzione di entrare nel merito di ogni singola realtà ma che possa
portare a termine gli obiettivi preposti mantenendo il più possibile la
coerenza con le modalità esistenti ad oggi all’interno della singola
struttura.

Per la grande maggioranza tutti gli attori della Community avranno una
propria struttura non solo organizzativa, di processo ma anche di propri
sistemi informativi che ad oggi li supportino nelle loro attività.

Struttura Organizzativa
-----------------------

Una struttura divisionale integrata è di fatto lo schema classico che
più si addice a questa analisi di contesto:

-  **Azienda**: parliamo dell’intera Nazione coinvolta e di fatto
   potremmo considerare come una sola e grande azienda;
-  **Ambiente**: visti i cambiamenti in atto possiamo considerare
   l’ambiente dinamico e complesso;
-  **Raggruppamento**: sicuramente una specializzazione degli output
   forniti e insita all’interno della struttura coinvolta;
-  **Livelli gerarchici**: saranno previsti quattro livelli gerarchici:
   Direzione Generale, Direzione di business; Direzioni di funzioni;
   Unità operative.
-  **Accentramento/Decentramento**: è necessario un’autonomia e delega
   totale alle direzioni di Business e un accentramento al vertice per
   decisioni strategiche e allocazioni di risorse.
-  **Formalizzazione**: è di fatto molto sviluppata all’interno delle
   divisioni ma sarà necessario spostare questo aspetto anche a livelli
   più alti per aumentare e mantenere uno standard qualitativo molto
   alto.
-  **Organi di staff:** necessario maggiori approfondimenti.
-  **Sistemi Operativi**: sarà necessario sviluppare un sistema
   informativo per mantenere un coordinamento sulle attività.

I punti di forza di questa struttura sono sicuramente: la gestione
integrata e unitaria del business, una maggior rapidità dei processi
decisionali e una maggior risposta ai cambiamenti in un ambiente in
continua evoluzione coadiuvata da una flessibilità strategica nella
definizione del business.

I punti deboli su cui sarà necessario intervenire con maggior controllo
potrebbero essere quello dell’orientamento all’efficienza che però
potrebbero essere irrisori nel caso di molta coesione e partecipazione
della Community.

Gli altri punti di debolezza che si potrebbero presentare con questa
tipo di struttura, sono:

-  Perdita di economia di scala e di specializzazione
-  Rivalità conflittualità inter-divisionali
-  Eccessivo orientamento al raggiungimento di performance di breve
   periodo

Sono da considerarsi poco rilevanti per come questo progetto dovrà
portare a compimento il risultato previsto. L’ambiente infatti non è
assolutamente quello di una grande azienda orientata agli utili ma sarà
quello di mettere a fattor comune l’esperienza di tutti gli attori per
un obiettivo comune e, quindi, i tre aspetti sopra elencati possono
essere per il momento considerati come non critici.

Uno degli aspetti critici che invece dovranno essere tenuti sotto
controllo e sicuramente l’aspetto del coordinamento che dovrà
preoccuparsi di mantenere viva la Community, suddividendo i compiti e le
attività tra gli attori coinvolti definendo processi idonei sia in fase
di raccolta requisiti che di realizzazione di un Security Information
and Event Management (SIEM) a livello nazionale.

Una rappresentazione iniziale dell’organigramma aziendale è riportata
nel grafico sottostante:

|image3|

.. _section-1:

.. _section-2:

.. _section-3:

Mission
-------

Il project work ha come obbiettivo l’integrazione di eventi di sicurezza
che ogni infrastruttura partecipante al progetto possa fornire
permettendo così che ogni attore diventi fornitore dei propri eventi che
potranno essere consumati dagli attori restanti. Questo permetterà un
accrescimento da parte di tutti sull’apprendimento e sulle modalità di
gestione di eventi critici creando una base di conoscenza noto a tutti e
porterà alla definizione di standard comportamentali per la risoluzione
di problematiche legate al mondo della cybersecurity.

Sarà necessario sviluppare una sovra infrastruttura il cui scopo
principale sarà quello di armonizzare e velocizzare la comunicazione tra
gli attori condividendo gli eventi critici per renderli immediatamente
utili ai partecipanti.

Questa infrastruttura vuole migliorare alcune problematiche che
riguarderanno in particolare:

-  incrementare l’efficacia delle comunicazioni tra strutture critiche;
-  incremento della conoscenza sulla sicurezza informatica;
-  armonizzazione di processi tra enti;
-  abbattimento di costi nel gestire problematiche di sicurezza
   informatiche;
-  permettere agli attori di diventare parti attive nell’individuazione
   e risoluzione di aspetti di sicurezza informatica;
-  confrontarsi con altre realtà per capire come risolvere una nuova
   problematica e condividerla.

Strategia corporate
~~~~~~~~~~~~~~~~~~~

La quasi totalità delle aziende nazionali, per il momento possiamo
limitarci al nostro perimetro ma in realtà potremmo tranquillamente
estenderlo a quelle internazionali, stanno approcciando il problema
della sicurezza informatica con grande apprensione e ancor poca
dimestichezza.

E’ continua la ricerca di personale specializzato in questo ambito così
vasto e in continua crescita. Sicuramente argomenti così impattanti e
con poca cultura sono di grande preoccupazione per tutte le aziende che
trattano prodotti e servizi basati su sistemi informativi.

Sia per etica aziendale che per effetto di ingenti multe si rende
necessario adeguare la propria infrastruttura e limitare quanto più
possibile i danni che potrebbero essere causati da un eventuale attacco
informatico.

Il settore in cui andiamo ad operare è di fatto un settore dove la
richiesta di protezione è alta e quindi l’interesse è elevato.

Essendo un argomento di interesse comune sarà necessario veicolare e
promuovere l’iniziativa verso la più ampia platea possibile.

Strategia di business
~~~~~~~~~~~~~~~~~~~~~

Il coinvolgimento di un’ampia platea darà la possibilità di recepire la
maggior parte di casi d’uso possibile che permetteranno di creare uno
strumento informatico atto a coprire la le esigenze raccolte.

La creazione di un Sistema Informativo Open Source atto a raccogliere e
condividere problematiche sull’argomento, porterà diversi vantaggi:

-  condivisione della conoscenza sull’argomento;
-  condivisione di risorse umane;
-  condivisione di obbiettivi comuni;
-  riduzione di costi;
-  standardizzazione di processi complessi;

Su questi punti è necessario elaborare una strategia che mantenga nel
lungo periodo la possibilità di mantenere il progetto dal punto di vista
di esigenze, performance e interesse.

Si dovrà puntare alla formazione e al supporto nell’uso e installazione
del sistema informativo e proporre servizi di controllo e monitoraggio
in caso in cui si abbia a che fare con un cliente finale che abbia
necessità di essere protetto ma non abbia personale preparato o adeguato
a farlo.

Essendo di interesse nazionale andrà vagliata la possibilità di avere
incentivi statali o condizioni di sottoscrizione, utili a mantenere nel
tempo la Community, le infrastrutture e il software necessario a gestire
questo progetto.

Strategia funzionale
~~~~~~~~~~~~~~~~~~~~

Essendo l’argomento e l’ambiente esterno molto complessi è necessario
coordinare le attività fin dall’inizio e ogni aspetto decisionale andrà
vagliato, approvato e controllato.

Sarà necessario avere una unità dedicata a questo aspetto che dovrà
svolgere principalmente i compiti di cui sopra.

Sarà necessario un gruppo in grado di espandere e cogliere l’esigenza da
parte di nuovi partner e promuovere le attività svolte fino a quel
momento e dovrà promuovere la roadmap delle attività svolte e che si
dovranno svolgere.

E’ opportuno che queste attività vengano gestite sia da un punto
commerciale che economico mantenendo il controllo dei costi e ricavi che
si avranno durante le fasi del progetto e si prevederà un gruppo a
gestire questi aspetti.

Le singole unità organizzative potranno dividersi in diverse tipologie
di attività definite preliminarmente e potranno esserci unità
organizzative atte allo sviluppo e progettazione della soluzione e altre
dedicate a fasi di test e collaudo.

A causa delle peculiarità della soluzione e dei dati trattati sarà
necessario dare enfasi alle sezioni di test e collaudo garantendo nel
tempo la trasparenza dei risultati ottenuti e aumentando la fiducia
verso il cliente finale.

Naturalmente le strategie di alto livello saranno gestite dalla
direzione generale.

Ambito Economico
================

Vista la mission e l’organizzazione aziendale si è ipotizzata una
possibile WBS (Work Breakdown Structure) suddiviso in sei WP (Work
Project), ogni WP sarà di responsabilità di gruppi specifici che
dovranno occuparsi delle macro attività indicate.

WP1: Coordinamento
~~~~~~~~~~~~~~~~~~

-  **Definizione del partnership strategico**: fase strategica per
   determinare e definire i partner strategici che potrebbe determinare
   valore aggiunto nella definizione ed esecuzione del progetto.

WP2: Community
~~~~~~~~~~~~~~

-  **Definizione delle regole**: è necessario definire e determinare
   regole e modalità di utilizzo della community. Come in ogni community
   sarà necessario individuare profili di utenti e gruppi, i loro
   compiti e le loro modalità operative all’interno della community.
-  **Definizione dei ruoli**: verranno determinati i ruoli dei gruppi di
   utenti che dovranno soddisfare le esigenze del progetto e finalità
   della community
-  **Coinvolgimento dei partner**: si dovrà capire in quale modalità e
   tempi coinvolgere i partner per migliorare e permettere una piena
   collaborazione degli stessi
-  **Avvio community**: fase operativa nel creare e rendere operativo la
   community definita nei punti precedenti. In questa fase sarà
   necessario determinare le parti tecniche sul come e dove questo
   servizio deve essere erogato.

WP3: Raccolta Requisiti
~~~~~~~~~~~~~~~~~~~~~~~

-  **Intervista partner**: partendo da un elenco di requisiti generici,
   che potrebbero essere considerati la base comune su cui partire il
   progetto, è necessario coinvolgere i partner fin dalle prime fasi per
   raccogliere requisiti essenziali arricchendo i requisiti di base di
   dettagli che ogni partner potrebbe avere necessità di arricchire e
   approfondire in base alle proprie peculiarità.
-  Definizione del perimetro di azione: la raccolta dei requisiti
   determinerà un ulteriori fase di analisi di quanto raccolto e
   determinerà le priorità di svolgimento e realizzazione degli stessi.
-  **Stesura documentazione dei requisiti e casi d’uso**: è necessario
   creare documentazione dei requisiti raccolti e discussi e
   realizzazione di casi d’uso.
-  **Calcolo della dimensioni del prodotto**: raccolti i requisiti e
   casi d’uso che si vogliono realizzare sarà possibile determinare,
   facendo uso di Function Point e SNAP Point, una dimensione più
   adeguata e un calcolo dei costi di realizzazione più in linea con
   quanto determinato inizialmente. Questo permetterà di definire con
   più dettaglio e maggiore affidabilità l’esecuzione e il
   coinvolgimento delle risorse che dovranno essere coinvolte nei passi
   successivi. Questo fase di progetto potrebbe portare ad una revisione
   dal punto di vista delle tempistiche e dei costi.

WP4: Sviluppo del prodotto
~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Sviluppo nuove funzionalità:
-  Sviluppo delle componenti di monitoraggio
-  Sviluppo delle componenti di gestione
-  Sviluppo big data
-  Integrazione tra le parti

WP5: Test del prodotto
~~~~~~~~~~~~~~~~~~~~~~

-  Verifica e rispetto dei requisiti
-  Test funzionali

WP6: Collaudo
~~~~~~~~~~~~~

-  Verifica di installabilità
-  Verifica rispetto dei requisiti di sicurezza
-  Verifica di High Affidability (HA)
-  Verifica di Disaster Recovery (DR)

WP7: Marketing e Formazione
~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  **Definizione di strategie**: necessaria per affrontare in modo
   organizzato le fasi di marketing e formazione. Argomento fondamentale
   per trasmettere i vantaggi nell’adottare questa soluzione permettendo
   alle strutture aderenti di trarne i più ampi benefici di utilizzo. In
   questa fase si determinerà il modo più efficace per raggiungere
   l’obiettivo prefissato. La fase di marketing dovrà determinare il
   modo in cui pubblicizzare e promuovere l’iniziativa in modo da
   permettere il più ampio coinvolgimento al di fuori dei partner già
   coinvolti
-  **Formazione**: necessario per trasmettere la conoscenza e
   coinvolgimento di tutte le parti interessate. Sarà necessario
   suddividere i corsi formativi per tipo di utenti: dirigenti,
   responsabili, operatori. Questo permetterà una maggiore efficacia e
   attenzione nei confronti degli utenti in base alle loro
   caratteristiche formative e conoscitive.
-  **Installazione**: prevedere documentazione necessaria
   all’installazione e metodi per agevolare la configurazione del
   sistema e , ove necessario, prevedere installazioni personalizzate.
   In questa fase potrebbe emergere una esigenza di installazione della
   soluzione con affiancamento di un operatore.

Implementation Plan
~~~~~~~~~~~~~~~~~~~

Analizzando le diverse attività è stato definito un GANTT che
rappresenta le macro attività che dovremmo affrontare durante la
creazione del progetto.

|image4|

Ipotizzando inoltre un costo a risorsa è possibile una prima
determinazione dei costi di progetto e il legame tra le attività e la
OBS.

Per i costi di progetto è stato ipotizzato un costo di 30 €/h si è
ottenuto la seguente RBS

|image5|

con una stima di costo complessivo pari a 156.720 € come si può evincere
dal Gantt.

.. _section-4:

SWOT
~~~~

In questa sezione si vuole evidenziare e schematizzare l’analisi SWOT
inerente al Project Work.

======= ============================ ==============================
\       Vantaggi e opportunità       Rischi e Pericoli
Interno Strenght – Punti di forza:   Weakness – Punti di debolezza:
\                                    
Esterno Opportunities – Opportunità: Threats – Minacce:
\                                    
======= ============================ ==============================

**Strategie SO:** è necessario condividere e formare ad ogni livello
aziendale i punti di forza e le opportunità che si avrebbero
nell’adottare questo modo di lavorare. Questo fase è molto delicata e
molto importante perché permetterà di ottenere consensi su gli aspetti
più critici e meno positivi dell’intera SWOT Analisys. Questo permetterà
una maggiore consapevolezza, condivisione e partecipazione di tutti gli
stakeholder e renderà più agevole l’affrontare i punti di debolezza e
minacce

**Strategie WT:** le problematiche elencate in questa visione
necessitano di attività parallele per essere arginate. Sarà necessario
costruire o aggiornare l’intero asset aziendale e definire policy di
sicurezza coerenti con l’esistente mostrando i punti di forza e
debolezza dell’intera infrastruttura. Potrebbero esserci punti critici
non sfruttabili facilmente dall’esterno mentre potrebbero esserci casi
meno critici ad un prima analisi ma facilmente sfruttabili. Anche in
questa fase per calmierare le eventuali resistenze al cambiamento sarà
necessario un coinvolgimento sia formativo che lavorativo.

Strategie WO: in questo caso è possibile cogliere una certa
compensazione tra opportunità e minacce. Le minacce rimangono dei punti
di attenzione ma le opportunità potrebbero compensare senza alcun
problema le stesse annullandole.

**Strategie ST:**\ in questo caso i punti di forza possono compensare,
cogliendone i benefici, le minacce individuate.

Ambito Tecnologico
==================

L’aspetto tecnologico prevede sicuramente una fase di esplorazione del
AS-IS sui sistemi Open Source e commerciali già esistenti per capire se
sistemi già consolidati sulla tematica preposta possano essere di aiuto
a addirittura coprire in parte o totalmente i requisiti preposti.

Sia i CISO (Chief Information Security Officer) che i direttori
dell’area Risk&Compliance stanno valutando funzionalità e
caratteristiche offerte dai servizi di CTI (Cyber Threat Intelligence)
inserendoli nei piani di rafforzamento per l’aspetto di sicurezza delle
proprie aziende.

Questo trend è dettato dal fatto che entro il 2022, il 20% delle grandi
imprese utilizzerà servizi CTI per definire le proprie strategie alla
lotta contro attacchi informatici.

Ad oggi i maggiori fruitori dei servizi CTI commerciali sono i servizi
governativi e finanziari ma si incomincia a notare un aumento anche in
altri settori, causato sia da una maggiore maturità dei programmi di
sicurezza che dall’aumento esponenziale di attacchi informatici negli
ultimi anni hanno fatto emergere diverse lacune.

La CTI è una caratteristica importante e fondamentale di un programma di
Cybersecurity in particolare per le aziende che lavorano nel mercato
digitale.

Ad alto livello, i servizi CTI possono essere utilizzati in due
modalità:

-  fornire informazioni solo alle macchine o ai sistemi di elaborazione
   automatica, vale a dire MRTI (Machine-Readable Threat Intelligence)
-  fornire informazioni prodotti da team di specialisti, al TOP
   Management

Informazioni leggibili da una macchina/sistema di sicurezza
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Sono informazioni principalmente di monitoraggio e/o notifica in tempo
reale, generalmente chiamati Indicator Of Compromise abbreviato in IoC
che sono artefatti ricavati in rete o in un sistema informatico che sono
correlabili a manomissioni o intrusioni.

Tipici IoC sono un indirizzo IP, un indice hash che identifica
univocamente un file malevolo, una URL, un dominio WEB da cui è stato
veicolato un attacco.

La determinazione degli IoC è una fase fondamentale per determinare in
modo organico, scientifico e ripetibile il tipo di attacco esaminato e
per capire le proporzioni del danno subito.

Gli IoC sono ricavati per lo più da fonti esterne e utilizzati per
arricchire i sistemi di sicurezza interna. Spesso includono anche
informazioni sull’attività operativa che si sta verificando (fonti
esterne) o si è già verificata (fonti interne) ma con approcci e
obiettivi puramente tecnici.

Informazioni prodotto da un team di specialisti
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Sono informazioni acquisite da diverse fonti (Commerciali o Open
Source), contenenti elementi come TTP (Tactics, Techniques and
Procedures), Threat Actor o report prodotti da analisti umani. Queste
informazioni includono generalmente un’analisi su misura per il cliente,
con dettagli delle azioni di rimedio da effettuare.

Tutte queste informazioni sono generate utilizzando standard come
STIX/TAXII, JSON, etc. ed elaborate da piattaforme commerciali chiamate
TIP (commerciali) od Open Source come MISP utilizzate per effettuare una
corretta Cyber Threat Information Sharing e, in particolare, per
svolgere un’attività di Cyber Threat Hunting.

La Cyber Threat Information Sharing è un ecosistema dove esiste una
condivisione real-time di un’informazione utilizzabile di Cyber Threat,
in grado di incrementare le difese di un’organizzazione (privata o
pubblica) in ottica di prevenzione, identificazione e mitigazione della
Cyber Threat prima che possa esserci un impatto reale
sull’organizzazione stessa.

**Il mercato si divide tra tecnologie/piattaforme di Cyber Threat
Intelligence commerciali e open source.** Entrambe le
tecnologie/piattaforme sono usate per la gestione delle Cyber Threat, ma
applicate in modi diversi.

Esistono diversi elementi da considerare per effettuare un confronto tra
le diverse tecnologie da adottare nel mondo della CTI. In particolare
possiamo distinguere cinque principali elementi caratterizzanti, che
sono:

-  gestione dei feed e fusione di diverse fonti;
-  capacità di arricchimento, analisi e discovery dei dati;
-  etichettatura dei dati e delle fonti e information sharing;
-  gestione degli utenti e collaborazione tra i team;
-  scalabilità e supporto.

Da uno studio fatto nel 2019 sulle principali differenze tra le maggiori
tecnologie/piattaforme commerciali e opensource disponibili sul mercato
rispetto alle diverse categorie di elementi (category) e caratteristiche
tecnica per ogni singola categoria (features) si è ottenuto quanto
segue:

|image6|

Come si può notare nel 2019 il confronto tra prodotti OpenSource e
commerciali mostrava una carenza negli aspetti legati a:

-  possibilità di generazione di report ad hoc
-  possibilità di effettuare un’opportuna etichettatura delle fonti
-  Manutenzione e supporto

Osservando l’evoluzione dei progetti OpenSource, in particolare del
protetto OpenSource MISP, si è potuto notare come parte di queste
mancanze siano state colmate nel tempo fornendo una soluzione sempre più
ricca e maggiormente confrontabile con soluzioni commerciali, ad esempio
MISP è in grado ad oggi di effettuare una valida etichettatura delle
fonti.

Esistono diversi prodotti che potrebbero soddisfare le esigenze di
condivisione di informazioni riguardanti attacchi informatici e questo è
un elenco delle principali soluzioni CTI OpenSource e Commerciali
esistenti sul mercato:

+---------+---------+---------+---------+---------+---------+---------+
| *       | *       | *       | **      | **      | Licence | Last    |
| *Name** | *Type** | *Year** | Owner** | Project |         | Update  |
|         |         |         |         | si      |         |         |
|         |         |         |         | te(s)** |         |         |
+---------+---------+---------+---------+---------+---------+---------+
| Collab  | Open    | 2014    | MITRE   | `link   | MIT     | 29/     |
| orative | Source  |         |         | 1 <ht   | Licence | 07/2019 |
| R       |         |         |         | tp://li |         |         |
| esearch |         |         |         | nk/>`__ |         |         |
| Into    |         |         |         |         |         |         |
| Threats |         |         |         | `link   |         |         |
| (CRITs) |         |         |         | 2 <     |         |         |
|         |         |         |         | https:/ |         |         |
|         |         |         |         | /github |         |         |
|         |         |         |         | .com/cr |         |         |
|         |         |         |         | its>`__ |         |         |
+---------+---------+---------+---------+---------+---------+---------+
| Col     | Open    | 2012    | CSIRT   | `link   | Mozilla | 07/     |
| lective | Source  |         | Gadgets | 1 <     | Public  | 06/2020 |
| Intel   |         |         |         | http:// | License |         |
| ligence |         |         | Fou     | csirtga | Version |         |
| Fr      |         |         | ndation | dgets.o | 2.0     |         |
| amework |         |         |         | rg/>`__ |         |         |
| (CIF)   |         |         |         |         |         |         |
|         |         |         |         | `link   |         |         |
|         |         |         |         | 2 <     |         |         |
|         |         |         |         | https:/ |         |         |
|         |         |         |         | /github |         |         |
|         |         |         |         | .com/cs |         |         |
|         |         |         |         | irtgadg |         |         |
|         |         |         |         | ets>`__ |         |         |
+---------+---------+---------+---------+---------+---------+---------+
| GOSINT  | Open    | 2017    | Cisco   | l\ `ink | Co      | 04/     |
|         | Source  |         |         | 1       | pyright | 08/2018 |
|         |         |         |         |  <https | (c)     |         |
|         |         |         |         | ://gith | 2017,   |         |
|         |         |         |         | ub.com/ | Cisco   |         |
|         |         |         |         | ciscocs | S       |         |
|         |         |         |         | irt/GOS | ystems, |         |
|         |         |         |         | INT>`__ | Inc.    |         |
|         |         |         |         |         | All     |         |
|         |         |         |         | `link   | rights  |         |
|         |         |         |         | 2 <ht   | re      |         |
|         |         |         |         | tps://g | served. |         |
|         |         |         |         | osint.r |         |         |
|         |         |         |         | eadthed |         |         |
|         |         |         |         | ocs.io/ |         |         |
|         |         |         |         | en/late |         |         |
|         |         |         |         | st/>`__ |         |         |
+---------+---------+---------+---------+---------+---------+---------+
| MANTIS  | Open    | 2013    | SIEMENS | `l      | GNU     | 29/     |
| Cyber   | Source  |         |         | ink <ht | General | 11/2013 |
| Threat  |         |         |         | tps://g | Public  |         |
| Intel   |         |         |         | ithub.c | License |         |
| ligence |         |         |         | om/siem | v2.0    |         |
| Man     |         |         |         | ens/dja |         |         |
| agement |         |         |         | ngo-man |         |         |
| Fr      |         |         |         | tis>`__ |         |         |
| amework |         |         |         |         |         |         |
+---------+---------+---------+---------+---------+---------+---------+
| Malware | Open    | 2012    | CIRCL   | `link   | GNU     | 14/     |
| Info    | Source  |         |         | 1 <http | Affero  | 07/2020 |
| rmation |         |         |         | ://www. | General |         |
| Sharing |         |         |         | misp-pr | Public  |         |
| P       |         |         |         | oject.o | License |         |
| latform |         |         |         | rg/>`__ | v3.0    |         |
| (MISP)  |         |         |         |         |         |         |
|         |         |         |         | `link   |         |         |
|         |         |         |         | 2       |         |         |
|         |         |         |         | <https: |         |         |
|         |         |         |         | //githu |         |         |
|         |         |         |         | b.com/M |         |         |
|         |         |         |         | ISP>`__ |         |         |
|         |         |         |         |         |         |         |
|         |         |         |         | `link   |         |         |
|         |         |         |         | 3 <htt  |         |         |
|         |         |         |         | ps://ww |         |         |
|         |         |         |         | w.misp- |         |         |
|         |         |         |         | project |         |         |
|         |         |         |         | .org/co |         |         |
|         |         |         |         | mmuniti |         |         |
|         |         |         |         | es/>`__ |         |         |
+---------+---------+---------+---------+---------+---------+---------+
| M       | Open    | 2016    | Palo    | `link   | Apache  | 13/     |
| ineMeld | Source  |         | Alto    | <https: | License | 05/2020 |
|         |         |         |         | //githu | 2.0     |         |
|         |         |         |         | b.com/P |         |         |
|         |         |         |         | aloAlto |         |         |
|         |         |         |         | Network |         |         |
|         |         |         |         | s/minem |         |         |
|         |         |         |         | eld>`__ |         |         |
+---------+---------+---------+---------+---------+---------+---------+
| Yeti    | Open    | 2017    | Yeti    | `link   | Apache  | 27/     |
|         | Source  |         |         | 1 <h    | License | 05/2020 |
|         |         |         |         | ttps:// | 2.0     |         |
|         |         |         |         | yeti-pl |         |         |
|         |         |         |         | atform. |         |         |
|         |         |         |         | github. |         |         |
|         |         |         |         | io/>`__ |         |         |
|         |         |         |         |         |         |         |
|         |         |         |         | `link   |         |         |
|         |         |         |         | 2 <h    |         |         |
|         |         |         |         | ttps:// |         |         |
|         |         |         |         | github. |         |         |
|         |         |         |         | com/yet |         |         |
|         |         |         |         | i-platf |         |         |
|         |         |         |         | orm>`__ |         |         |
+---------+---------+---------+---------+---------+---------+---------+
| TheHive | Open    | 2014    | TheHive | `li     | GNU     | 25/     |
|         | Source  |         |         | nk <htt | Affero  | 04/2020 |
|         |         |         |         | ps://gi | General |         |
|         |         |         |         | thub.co |         |         |
|         |         |         |         | m/TheHi | Public  |         |
|         |         |         |         | ve-Proj | Licence |         |
|         |         |         |         | ect>`__ | v3.0    |         |
+---------+---------+---------+---------+---------+---------+---------+
| Cortex  | Open    | 2014    | TheHive | `li     | GNU     | 20/     |
|         | Source  |         |         | nk <htt | Affero  | 01/2020 |
|         |         |         |         | ps://gi | General |         |
|         |         |         |         | thub.co |         |         |
|         |         |         |         | m/TheHi | Public  |         |
|         |         |         |         | ve-Proj | Licence |         |
|         |         |         |         | ect>`__ | v3.0    |         |
+---------+---------+---------+---------+---------+---------+---------+
| Threa   | Com     | 2013    | Anomali | `       |         | n.a.    |
| tStream | mercial |         |         | link <h |         |         |
|         |         |         |         | ttps:// |         |         |
|         |         |         |         | www.ano |         |         |
|         |         |         |         | mali.co |         |         |
|         |         |         |         | m/platf |         |         |
|         |         |         |         | orm>`__ |         |         |
+---------+---------+---------+---------+---------+---------+---------+
| Ecl     | Com     | 2014    | Ecl     | `lin    |         | n.a.    |
| ecticIQ | mercial |         | ecticIQ | k <http |         |         |
| P       |         |         |         | s://www |         |         |
| latform |         |         |         | .eclect |         |         |
|         |         |         |         | iciq.co |         |         |
|         |         |         |         | m/platf |         |         |
|         |         |         |         | orm>`__ |         |         |
+---------+---------+---------+---------+---------+---------+---------+
| Looki   | Com     | 2015    | Looki   | `lin    |         | n.a.    |
| ngGlass | mercial |         | ngGlass | k <http |         |         |
|         |         |         |         | s://www |         |         |
|         |         |         |         | .lookin |         |         |
|         |         |         |         | gglassc |         |         |
|         |         |         |         | yber.co |         |         |
|         |         |         |         | m/produ |         |         |
|         |         |         |         | cts/man |         |         |
|         |         |         |         | age-int |         |         |
|         |         |         |         | elligen |         |         |
|         |         |         |         | ce/>`__ |         |         |
+---------+---------+---------+---------+---------+---------+---------+
| C       | Com     | 2019    | C       | `       |         | n.a.    |
| elerium | mercial |         | elerium | link <h |         |         |
|         |         |         |         | ttps:// |         |         |
|         |         |         |         | www.cel |         |         |
|         |         |         |         | erium.c |         |         |
|         |         |         |         | om/>`__ |         |         |
+---------+---------+---------+---------+---------+---------+---------+
| Threat  | Com     | 2013    | Threat  | `link   |         | n.a.    |
| Connect | mercial |         | Connect | <https: |         |         |
|         |         |         |         | //www.t |         |         |
|         |         |         |         | hreatco |         |         |
|         |         |         |         | nnect.c |         |         |
|         |         |         |         | om/>`__ |         |         |
+---------+---------+---------+---------+---------+---------+---------+
| ThreatQ | Com     | 2015    | ThreatQ | `       |         | n.a.    |
| P       | mercial |         | uotient | link <h |         |         |
| latform |         |         |         | ttps:// |         |         |
|         |         |         |         | www.thr |         |         |
|         |         |         |         | eatq.co |         |         |
|         |         |         |         | m/threa |         |         |
|         |         |         |         | tq/>`__ |         |         |
+---------+---------+---------+---------+---------+---------+---------+
| TruSTAR | Com     | 2014    | TruSTAR | `l      |         | n.a.    |
|         | mercial |         | Techn   | ink <ht |         |         |
|         |         |         | ologies | tps://t |         |         |
|         |         |         |         | rustar. |         |         |
|         |         |         |         | co/>`__ |         |         |
+---------+---------+---------+---------+---------+---------+---------+
| Open    | Co      | 2012    | Ali     | `l      |         | n.a.    |
| Threat  | mmunity |         | enVault | ink <ht |         |         |
|         |         |         |         | tps://w |         |         |
| E       |         |         |         | ww.alie |         |         |
| xchange |         |         |         | nvault. |         |         |
| (OTX)   |         |         |         | com/ope |         |         |
|         |         |         |         | n-threa |         |         |
|         |         |         |         | t-excha |         |         |
|         |         |         |         | nge>`__ |         |         |
+---------+---------+---------+---------+---------+---------+---------+
| ThreatE | Co      | 2015    | F       | `lin    |         | n.a.    |
| xchange | mmunity |         | acebook | k <http |         |         |
|         |         |         |         | s://dev |         |         |
|         |         |         |         | elopers |         |         |
|         |         |         |         | .facebo |         |         |
|         |         |         |         | ok.com/ |         |         |
|         |         |         |         | product |         |         |
|         |         |         |         | s/threa |         |         |
|         |         |         |         | t-excha |         |         |
|         |         |         |         | nge>`__ |         |         |
+---------+---------+---------+---------+---------+---------+---------+
| X-Force | Co      | 2015    | IBM     | `link   |         | n.a.    |
| E       | mmunity |         |         | <https: |         |         |
| xchange |         |         |         | //excha |         |         |
|         |         |         |         | nge.xfo |         |         |
|         |         |         |         | rce.ibm |         |         |
|         |         |         |         | cloud.c |         |         |
|         |         |         |         | om/>`__ |         |         |
+---------+---------+---------+---------+---------+---------+---------+
| Threat  | Co      | 2015    | Micro   | `lin    |         | n.a.    |
| Central | mmunity |         | Focus   | k <http |         |         |
|         |         |         |         | s://www |         |         |
|         |         |         |         | .microf |         |         |
|         |         |         |         | ocus.co |         |         |
|         |         |         |         | m/it-it |         |         |
|         |         |         |         | /soluti |         |         |
|         |         |         |         | ons/app |         |         |
|         |         |         |         | licatio |         |         |
|         |         |         |         | n-secur |         |         |
|         |         |         |         | ity>`__ |         |         |
+---------+---------+---------+---------+---------+---------+---------+

Come si può notare nell’ambito della Cyber Security l’aspetto e la
gestione dei fenomeni legati ad attacchi informatici è in continua
crescita e denotano una caratteristica comune che è quella di
condividere le informazioni per aumentare l’efficacia della difesa.

Dal piano triennale ICT 2019-2021 sulla sicurezza informatica AGID ha
attivato un progetto per la sperimentazione delle modalità di scambio
automatico di informazioni operative (indicatori di compromissione) tra
strutture di sicurezza mediante protocolli STIX e TAXII tramite
piattaforme per la raccolta, l'archiviazione, la distribuzione e la
condivisione di indicatori di sicurezza informatica e minacce relative
all'analisi degli incidenti.

Tale sperimentazione, che comprende due Gruppi di lavoro dedicati
rispettivamente agli aspetti tecnici ed alla definizione di una
tassonomia ad hoc, ha lo scopo di produrre le specifiche tecniche ed
organizzative che verranno emanate come standard per la realizzazione di
un sistema nazionale di interscambio automatico di indicatori di
compromissione qualificati tra operatori

accreditati.

La proposta coinvolge tre strumenti open-source e la realizzazione da
parte della CERT-PA di un modulo software che permette l’integrazione di
queste tre soluzioni.

Nella loro soluzione propongono l’uso dei seguenti strumenti
open-source:

-  **MineMeld:**\ applicazione open-source che semplifica
   l'aggregazione, l'applicazione e la condivisione di minacce
   informatiche.

   -  Nativamente collegato a Palo Alto Firewall
   -  Licence: Apache License Version 2.0
   -  Repository: https://github.com/PaloAltoNetworks/minemeld

-  **MISP:**\ piattaforma per la condivisione di minacce informatiche,
   l'archiviazione e la correlazione degli indicatori di compromissione
   di attacchi mirati, informazioni sulle minacce, informazioni sulla
   frode finanziaria, informazioni sulla vulnerabilità o persino
   informazioni antiterrorismo.

   -  Licence: AGPL-3.0-or-later , BSD 2-Clause “Simplified” License ,
      CC0-1.0 or BSD 2-Clause “Simplified” License
   -  Repository: https://github.com/MISP/MISP

-  **CABBY:**\ libreria Python per interagire con server che utilizzano
   il protocollo TAXII.

   -  Licence: BSD 3-Clause
   -  https://github.com/eclecticiq/cabby/blob/master/LICENSE.rst
   -  Repository: https://github.com/EclecticIQ/cabby

-  **CNTI:**\ agevolare la ricezione delle informazioni tramite
   differenti servizi – come i framework MineMeld e l’istanza MISP del
   CERT-PA, del client CNTI o della libreria Cabby di EclecticIQ –
   garantisce interoperabilità con i sistemi e prodotti di terze parti
   già in uso dalle organizzazioni.

   -  Licence: non trovato
   -  Repository: non trovato

In questa fase la CERT-PA sta subendo profondi cambiamenti organizzativi
che non ci permettono al momento di approfondire ulteriormente la
soluzioni da loro proposta.

Da questo studio di mercato emerge un enorme interesse sull’argomento e
importanti lavori effettuati da parte di società commerciali e anche
dalle comunità open-source che stanno aggiungendo servizi di supporto
agli strumenti realizzati per sopperire alle carenze in questo senso e
soddisfare le esigenze richieste dai clienti.

L’approccio che è emerso al momento più interessante è l’uso di tre
prodotti open-source per ottenere un sistema CTI il più completo
possibile, questi strumenti nascono dal più conosciuto MISP e aggiungono
funzionalità al MISP attuale fornendo un più completo ecosistema
nell’effettuare analisi e gestione dei casi anomali riscontrati. Inoltre
gli strumenti prevedono una completa integrazione con il MISP ricavando
e/o arricchendo le informazioni ottenute dallo stesso.

La soluzione prevede l’uso di questi strumenti:

-  TheHive
-  Cortex
-  MISP

TheHive
~~~~~~~

E’ una piattaforma di Security Incident Response scalabile open source
completamente integrata con il MISP (Malware Information Sharing
Platform) disegnata per agevolare il lavoro di SOC, CSIRT, CERT e
qualsiasi altro fruitore/forniture che gestisca informazioni di
sicurezza che necessitano di analizzare e agire rapidamente a fronte di
attacchi informatici.

L’approccio di TheHive è quello di fornire una piattaforma che possa
garantire un modello collaborativo sull’analisi e risoluzione di un
attacco informatico.

Grazie al flusso di lavoro integrato è possibile inserire e gestire
informazioni in tempo reale relative a casi nuovi o esistenti, attività,
osservabili e IOC e queste sono rese disponibili per tutti i membri del
team.

Inoltre è possibile grazie a notifiche speciali gestire o assegnare
nuove attività e visualizzare in anteprima nuovi eventi e avvisi forniti
dal MISP.

TheHive permette inoltre di aggiungere metriche e campi personalizzabili
che permettono di guidare le attività di un team, e gli analisti possono
registrare i loro progressi e allegare prove e file degni di nota,
aggiungere tag e importare archivi ZIP protetti da password contenenti
malware o dati sospetti senza aprirli.

Inoltre è possibile partire da un evento fornito dal MISP, effettuare il
triage usando le potenzialità di Cortex, per analizzare in maniera più
completa e così ottenere risposte sul IOC analizzato nel più breve tempo
possibile.

Una volta completate le indagini, esportare IOC in una o più istanze
MISP.

Cortex
~~~~~~

Cortex è uno strumento capace di interagire con numerosi altri servizi,
ad oggi ne sono disponibili 147, tra cui alcuni gratuiti e alcuni a
pagamento per una analisi più completa del IOC che si sta analizzando
questo strumento permette di diminuire i tempi di analisi e avere un
unico punto come raccolta di informazioni forniti dai molteplici servizi
ad oggi a disposizione sul Web.

Inoltre permette la creazione di analizzatori o responder personalizzati
utilizzando qualsiasi linguaggio di programmazione supportato da Linux,
permettendo di condividere i risultati con tutto il team o, meglio, con
tutta la comunità.

Inoltre è possibile eseguire più interrogazioni contemporanee su più
instanze MISP a disposizione.

Cortex, nato dallo stesso gruppo di TheHive, permette una integrazione
nativa con quest’ultimo fornendo a TheHive uno strumento aggiuntivo che
permette di eseguire centinaia di controlli su più instanze di Cortex
contemporaneamente fornendo a quest’ultimo i risultati ottenuti e grazie
al motore di report di TheHive è possibile visualizzarlo nel modo
desiderato.

MISP
~~~~

Una piattaforma di intelligence per la condivisione delle minacce,
l'archiviazione e la correlazione degli indicatori di compromissione
(IOC) di attacchi mirati, informazioni sulle minacce, informazioni sulla
frode finanziaria, informazioni sulla vulnerabilità o persino
informazioni antiterrorismo.

MISP viene utilizzato oggi in più organizzazioni non solo per
archiviare, condividere, collaborare su indicatori di sicurezza
informatica, analisi di malware, ma anche per utilizzare gli IOC e le
informazioni per rilevare e prevenire attacchi, frodi o minacce contro
le infrastrutture, le organizzazioni o le persone ICT.

Questo sistema permette di:

-  avere un database di IoC e indicatori efficienti che consentono di
   archiviare informazioni tecniche e non tecniche su campioni di
   malware, incidenti, aggressori e informazioni di intelligence.
-  Correlazione automatica per trovare relazioni tra attributi e
   indicatori di malware, campagne di attacchi o analisi. Il motore di
   correlazione include la correlazione tra attributi e correlazioni più
   avanzate come la correlazione hash Fuzzy (ad esempio ssdeep) o la
   corrispondenza dei blocchi CIDR. La correlazione può anche essere
   abilitata o l'evento disabilitato per attributo.
-  Un modello di dati flessibile in cui oggetti complessi possono essere
   espressi e collegati tra loro per esprimere informazioni sulle
   minacce, incidenti o elementi connessi.
-  Funzionalità di condivisione integrata per facilitare la condivisione
   dei dati utilizzando diversi modelli di distribuzioni. MISP può
   sincronizzare automaticamente eventi e attributi tra diversi MISP.
   Funzionalità di filtro avanzate possono essere utilizzate per
   soddisfare ogni politica di condivisione di un'organizzazione tra cui
   una capacità di gruppo di condivisione flessibile e meccanismi di
   distribuzione a livello di attributo.
-  Un'interfaccia utente intuitiva per gli utenti finali per creare,
   aggiornare e collaborare su eventi e attributi / indicatori.
   Un'interfaccia grafica per navigare senza soluzione di continuità tra
   gli eventi e le loro correlazioni. Una funzionalità del grafico degli
   eventi per creare e visualizzare relazioni tra oggetti e attributi.
   Funzionalità di filtro avanzate ed elenco di avvisi per aiutare gli
   analisti a contribuire con eventi e attributi.
-  archiviare i dati in un formato strutturato (che consente l'uso
   automatizzato del database per vari scopi) con un ampio supporto di
   indicatori di sicurezza informatica insieme a indicatori di frode
   come nel settore finanziario.
-  esportazione: generazione di IDS (Suricata, Snort e Bro sono
   supportati per impostazione predefinita), OpenIOC, output in testo
   normale, CSV, MISP XML o JSON per l'integrazione con altri sistemi
   (ID di rete, ID host, strumenti personalizzati)
-  importazione: importazione in blocco, importazione in batch,
   importazione in testo libero, importazione da OpenIOC, sandbox GFI,
   ThreatConnect CSV o formato MISP.
-  Strumento flessibile di importazione di testo libero per facilitare
   l'integrazione di report non strutturati in MISP.
-  Un sistema gentile per collaborare su eventi e attributi che consente
   agli utenti MISP di proporre modifiche o aggiornamenti ad attributi /
   indicatori.
-  condivisione dei dati: scambio e sincronizzazione automatici con
   altre parti e gruppi di fiducia mediante MISP.
-  importazione di feed: strumento flessibile per importare e integrare
   feed di MISP e qualsiasi feed di minacce o OSINT da terze parti.
   Molti feed predefiniti sono inclusi nell'installazione MISP standard.
-  delega della condivisione: consente un semplice meccanismo
   pseudo-anonimo per delegare la pubblicazione di eventi / indicatori a
   un'altra organizzazione.
-  API flessibile per integrare MISP con le altre soluzioni. MISP è in
   bundle con PyMISP che è una libreria Python flessibile per
   recuperare, aggiungere o aggiornare gli attributi degli eventi,
   gestire campioni di malware o cercare attributi.
-  tassonomia regolabile per classificare e taggare gli eventi seguendo
   i propri schemi di classificazione o tassonomie esistenti. La
   tassonomia può essere locale per il tuo MISP ma anche condivisibile
   tra le istanze MISP. MISP viene fornito con un set predefinito di
   tassonomie e schemi di classificazione noti per supportare la
   classificazione standard utilizzata da ENISA, Europol, DHS, CSIRT o
   molte altre organizzazioni.
-  i vocabolari dell'intelligence chiamati galassia MISP e in bundle con
   attori della minaccia esistenti, malware, RAT, ransomware o MITRE
   ATT&CK che possono essere facilmente collegati agli eventi in MISP.
-  moduli di espansione in Python per espandere MISP con i propri
   servizi o attivare moduli di errore già disponibili.
-  supporto di avvistamento per ottenere osservazioni da organizzazioni
   riguardanti indicatori e attributi condivisi. L'avvistamento può
   essere fornito tramite l'interfaccia utente MISP, API come documento
   MISP o documenti di avvistamento STIX.
-  Supporto STIX: esportazione dei dati nel formato STIX (XML e JSON)
   inclusa esportazione/importazione nel formato STIX 2.0.
-  crittografia integrata e firma delle notifiche tramite PGP e/o S/MIME
   a seconda delle preferenze dell'utente.
-  Canale di abbonamento di pubblicazione in tempo reale all'interno di
   MISP per ottenere automaticamente tutte le modifiche.

Condividere con gli umani
'''''''''''''''''''''''''

I dati archiviati sono immediatamente disponibili per colleghi e
partner. Memorizza l'ID evento nel tuo sistema di biglietteria o sarai
informato dalle notifiche e-mail firmate e crittografate.

Condivisione con le macchine
''''''''''''''''''''''''''''

Generando regole Snort/Suricata/Bro/Zeek IDS, le esportazioni STIX,
OpenIOC, text o csv MISP consente di importare automaticamente i dati
nei sistemi di rilevamento con conseguente rilevamento migliore e più
rapido delle intrusioni.

L'importazione dei dati può anche essere eseguita in vari modi:
importazione di testo libero, OpenIOC, importazione batch, importazione
di risultati sandbox o utilizzo di modelli preconfigurati o
personalizzati.

Se si esegue MISP internamente, i dati possono anche essere caricati e
scaricati automaticamente da e verso istanze MISP ospitate esternamente.
Grazie a questa automazione e allo sforzo degli altri, ora si è in
possesso di preziosi indicatori di compromesso senza lavoro aggiuntivo.

Condivisione collaborativa di analisi e correlazione
''''''''''''''''''''''''''''''''''''''''''''''''''''

Quando vengono aggiunti nuovi dati, MISP mostrerà immediatamente le
relazioni con altri osservabili e indicatori esitenti. Ciò si traduce in
un'analisi più efficiente, ma consente anche di avere un quadro migliore
dei TTP, delle campagne correlate e dell'attribuzione.

La funzione di discussione consentirà anche conversazioni tra più
analisti con conseguente beneficio per tutti.

Architettura
~~~~~~~~~~~~

Sia TheHive che Cortex forniscono librerie per essere integrate con
strumenti di terze parti, queste librerie, chiamate: TheHive4py e
Cortex4py permettono di fornire interfacce e servizi per una più facile
integrazione.

TheHive e Cortex nascono dal progetto open source che è consultabile su
questo link https://thehive-project.org/ inoltre forniscono, ad oggi, un
supporto professionale nel caso in cui fosse necessario.

Un possibile schema architetturale di questo ecosistema potrebbe essere
il seguente:

Questo ecosistema risulta interessante per diversi aspetti non solo
funzionali ma anche di interoperabilità con soluzioni proposte perché è
possibile sfruttare il MISP per mantenere e agevolare la condivisione
delle informazioni ottenute da una analisi di un incidente informatico.

La presenza del MISP infatti permette di interagire con altre proposte
che ne fanno già uso come quella descritta in precedenza e proposta
dalla CERT-PA in collaborazione con Agid.

Tutti gli strumenti permettono una comunicazione sicura in HTTPS l’una
con l’altra e un sistema di autenticazione e profilazione su ogni
singolo strumento permettendo di gestire con accuratezza anche aspetti
di privacy.

Caso d’uso
~~~~~~~~~~

Senza entrare nel merito delle singole piattaforme e delle diverse
caratteristiche che ognuno può offrire che demandiamo alle
documentazioni ufficiali, analizzeremo un caso d’uso pratico di come
queste piattaforme possano fornire un valido sostegno nell’analisi di
problematiche di sicurezza e nella modalità di condivisione tra le parti
e eventualmente la possibilità di condivisione dell’analisi fatte con
altre organizzazioni.

Una volta eseguito il login su TheHive si ottiene accesso alla dashboard
corrispondente in grado di riassumere le attività ancora da svolgere o
nuove attività che possono essere state assegnate.

|image7|

essendo il primo accesso e non avendo casi da analizzare se ne può
creare uno nuovo nel quale è possibile aggiungere macro informazioni su
quello che si vorrà fare in seguito.

Una volta creato il caso d’uso sarà possibile aggiungere delle attività
da demandare a gruppi specifici di analisti e aggiungere le azioni
osservabili su cui si potrà chiedere aiuto a Cortex per ottenere
informazioni più dettagliate a loro riguardo.

|image8|

Come si può notare dalla schermata in questo caso d’uso è stato
richiesto di effettuare dei controlli su un file specifico, una url e un
indirizzo IP.

Una volta inseriti gli elementi da controllare è possibile sia
simultaneamente che singolarmente richiedere a Cortex un’analisi più
dettagliata specificando quali servizi utilizzare in base alla
configurazione di Cortex effettuata.

Una volta selezionati gli oggetti che si vuole osservare è possibile
tramite il pulsante “Action” richiedere l’inizio dell’analisi
selezionando gli opportuni servizi, come mostrato nell’immagine
sottostante.

|image9|

Una volta selezionati e premuto il pulsante “Run selected analyzers” si
otterrà dopo pochi istanti il risultato dell’analisi svolta per ogni
oggetto selezionato.

Per una più facile visualizzazione i vari oggetti osservati verranno
arricchiti di “Tag” che conterranno informazioni sia testuale che visivo
mostrando delle colorazioni diverse in base alle analisi fatte.

|image10|

Per capire cosa sia avvenuto realmente a fronte di pochi passaggi è
necessario collegarsi a Cortex per rendersi conto del lavoro effettuato.

Nella schermata seguente si può notare come Cortex abbia semplificato il
lavoro che andrebbe fatto a mano su singoli quesiti e che ha svolto in
parallelo.

|image11|

Una volta effettuata l’analisi sfruttando TheHive e il motore Cortex per
ottenere le informazioni necessarie è possibile pubblicare questo caso
di studio a MISP dicendo a TheHive di condividerlo con il MISP, premendo
il tasto “Share”

|image12|

Collegandosi al MISP è infine possibile osservare l’avvenuta
comunicazione tra TheHive e MISP.

|image13|

A questo punto è possibile come per ogni altro evento presente su MISP
poterlo condividere con altre organizzazioni e ad altri MISP esistenti.

.. _section-5:

Interoperabilità e tipi di dati
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

L'interoperabilità tra i sistemi è assicurata da collegamenti punto a
punto così facendo è possibile ottenere altri casi d’uso interessanti in
aggiunto a quello appena descritto, come ad esempio:

-  TheHive rimane in ascolto di nuovi eventi presenti sul MISP
   eventualmente filtrandoli a seconda dell’interesse da cui si può
   iniziare o proseguire un analisi sull’evento
-  il MISP è collegabile direttamente a Cortex permettendo di utilizzare
   direttamente le API fornitegli e arricchendo il proprio evento con
   ulteriori dettagli senza essere obbligati a usare TheHive.

L’intercomunicazione tra i sistemi è gestita tramite API di tipo REST
con collegamenti HTTP/HTTPS il che permette uno scambio di messaggi
interpretabili e di tipo JSON e, inoltre, i sistemi necessitano della
creazione di particolari utenti per comunicare fra di loro.

Questo permette una gestione sicura del dato e dell’impossibilità di
avere interferenze esterne sui tipi di analisi fatte mantenendo sicuro e
configurabile l’intero ecosistema.

Sia MISP che Cortex, pur avendo obbiettivi diversi, permettono
l’integrazione con sistemi esterni facendo uso di protocolli STIX/TAXII.

STIX
~~~~

Con STIX, tutti gli aspetti di sospetto, compromesso e attribuzione
possono essere rappresentati chiaramente con oggetti e relazioni
descrittive. Le informazioni STIX possono essere rappresentate
visivamente per un analista o archiviate come JSON per essere
rapidamente leggibili dal computer. L'apertura di STIX consente
l'integrazione in strumenti e prodotti esistenti o utilizzati per
esigenze specifiche dell'analista o della rete.

Gli oggetti STIX categorizzano ogni informazione con attributi specifici
da popolare. Il concatenamento di più oggetti attraverso relazioni
consente rappresentazioni semplici o complesse di CTI.

Di seguito è riportato un elenco di ciò che può essere rappresentato
tramite STIX che è un linguaggio ed un formato di serializzazione
open-source, usato per scambiare cyber threat intelligence in maniera
consistente e machine-readable, in modo da essere di supporto
all'analisi

collaborativa delle minacce e lo scambio automatizzato di informazioni
di intelligence.

Definisce 12 oggetti (STIX Domain Objects, SDOs) e due tipi di relazioni
(STIX Relationship Objects, SROs).

Gli oggetti sono:

-  **Attack Pattern**: Un tipo di TTP che descrive i modi in cui gli
   attaccanti cercano di compromettere un obiettivo

-  **Campaign**: Un insieme di comportamenti degli attaccanti che
   descrivono un gruppo di attività malevole o attacchi che succedono in
   un determinato periodo e contro uno specifico insieme di obiettivi
-  **Course of Action**: Un'azione presa per prevenire o rispondere ad
   un attacco
-  **Identity**: Individui, organizzazioni o gruppi
-  **Indicator**: Una caratteristica che permette di rilevare attivita
   informatiche malevole o sospette
-  **Intrusion Set**: Un gruppo di comportamenti e risorse con proprieta
   comuni che si crede siano governate da un singolo attore
-  **Malware**: Un tipo di TTP, conosciuto anche come codice o programma
   malevolo, usato per compromettere confidenzialità, integrità o
   disponibilità delle informazioni o dei sistemi della vittima
-  **Observer Data**: Rappresenta informazioni osservate in un sistema o
   in una rete (ad esempio un indirizzo IP)
-  **Report**: Collezione di threat intelligence focalizzata su uno o
   più temi, come la descrizione di un threat actor, un malware o una
   tecnica d'attacco, includendo i relativi dettagli
-  **Threat Actor**: Individui, gruppi o organizzazioni che si crede
   stiano operando con intenzioni malevole

|image14|

TAXII
~~~~~

E' un protocollo a livello applicativo utilizzato per scambiare
informazioni di threat intelligence in HTTPS.

TAXII definisce un API RESTful (un set di servizi e scambi di messaggi)
e un set di requisiti per client e server TAXII. Come illustrato di
seguito, TAXII definisce due servizi primari per supportare una varietà
di modelli di condivisione comuni:

-  **Collection**: è un'interfaccia con un repository logico di oggetti
   CTI forniti da un server TAXII che consente a un produttore di
   ospitare una serie di dati CTI che possono essere richiesti dai
   consumatori: i clienti e i server TAXII si scambiano informazioni in
   un modello di richiesta-risposta.
-  **Channel**: gestito da un server TAXII, un canale consente ai
   produttori di inviare dati a molti consumatori e consumatori per
   ricevere dati da molti produttori: i clienti TAXII scambiano
   informazioni con altri clienti TAXII in un modello di abbonamento di
   pubblicazione.

Collection e channel possono essere organizzati in diversi modi. Ad
esempio, possono essere raggruppati per supportare le esigenze di un
determinato gruppo di fiducia.

` <https://exchange.xforce.ibmcloud.com/>`__

Un'istanza del server TAXII può supportare una o più radici API. Le
radici API sono raggruppamenti logici di canali.

` <https://exchange.xforce.ibmcloud.com/>`__

TAXII utilizza HTTPS come trasporto per tutte le comunicazioni e
utilizza HTTP per la negoziazione e l'autenticazione dei contenuti.

` <https://exchange.xforce.ibmcloud.com/>`__

TAXII è stato appositamente progettato per supportare lo scambio di CTI
rappresentati in STIX e il supporto per lo scambio di contenuti STIX 2.1
è obbligatorio da implementare.

Tuttavia, TAXII può anche essere utilizzato per condividere dati in
altri formati. È importante notare che STIX e TAXII sono standard
indipendenti: le strutture e le serializzazioni di STIX non si basano su
alcun meccanismo di trasporto specifico e TAXII può essere utilizzato
per trasportare dati non STIX.

` <https://exchange.xforce.ibmcloud.com/>`__

I principi di progettazione di TAXII comprendono la riduzione al minimo
delle modifiche operative necessarie per l'adozione; facile integrazione
con gli accordi di condivisione esistenti e supporto per tutti i modelli
di condivisione delle minacce ampiamente utilizzati: hub-and-speak,
peer-to-peer, fonte-abbonato.

I server TAXII sono rilevati grazie a query DNS ed usa HTTPS per tutte
le comunicazioni e permettono di scegliere due modalità di
comunicazione:

-  modalità “push”
-  modalità “pull”

e diversi tipi di messaggi, ad esempio di sottoscrizione, pausa di
trasmissione, modica iscrizione. E' stato sviluppato appositamente per
scambiare CTI rappresentata in formato STIX.

|image15|

Studio dei Repository
---------------------

La soluzione applicativa individuata è di sicuro interesse per
semplificare l’analisi e la tracciatura degli IoC e per agevolare un
interscambio di queste informazioni in maniera continua ed efficace.

In questa sezione si analizzerà lo stato di salute delle soluzioni
trovate da un punto di vista organizzativo, interesse e di
movimentazione da parte degli sviluppatori e di chi sta portando avanti
le community per valutare se questi progetti possono avere un seguito ed
eventuali lock-in tecnologici e di processo che potrebbero introdurre
problematiche nella loro adozione.

Si utilizzeranno gli strumenti messi a disposizione dai repository
utilizzati da questi strumenti che ad oggi, fanno capo tutti a GitHub
per la loro pubblicazione del software libero. Si faranno considerazioni
sul loro uso da parte di altri utenti.

GitHub mette a disposizione uno strumento, chiamato Insight, che
permette ad ognuno di tenere sotto controllo l’andamento del progetto
fornendo importanti informazioni sullo stato di longevità e lavoro sul
progetto analizzato fornendo importanti indici che potrebbero
influenzare o meno la scelta dei progetti.

Prenderemo come parametri di Insights i seguenti:

-  **Pulse**: fornisce indicazioni sulle attività fino all’ultimo mese
   di chi ha partecipato al progetto questa indicazione permette di
   capire nell’immediato l’interesse verso il progetto osservato.
-  **Contributors**: fornisce l’elenco dei collaboratori al progetto e
   una rappresentazione grafica di cosa è avvenuto nell’ultimo anno sul
   progetto.
-  **Network**: fornisce in formato grafico l’andamento delle attività
   svolte sui progetti e i momenti di rilascio di versioni.

Si andranno ad analizzare le seguenti informazioni per ottenere una
visione più completa sullo stato dei singoli progetti.

Questi parametri sicuramente potranno subire dei cambiamenti nel tempo e
vogliono indicare lo stato attuale del progetto.

.. _misp-1:

MISP
~~~~

url: https://github.com/MISP/MISP

============ =========
Pulse        |image16|
Contributors |image17|
Network      |image18|
============ =========

.. _thehive-1:

TheHive
~~~~~~~

url: https://github.com/TheHive-Project/TheHive

============ =========
Pulse        |image19|
Contributors |image20|
Network      |image21|
============ =========

.. _cortex-1:

Cortex
~~~~~~

url: https://github.com/TheHive-Project/Cortex

============ =========
Pulse        |image22|
Contributors |image23|
Network      |image24|
============ =========

Da questi tre grafici per progetto fornitoci da GitHub è possibile
osservare lo stato attuale dei progetti, questo permetterà di prendere
decisioni in merito nell’adottare lo strumento individuato o doverlo
abbandonare per evitare problemi futuri.

Si valuteranno le singole situazioni verrà dato un voto da 1 a 5 in
merito all’andamento del grafico giustificando tale valore nelle note.

+---------+-------+--------------+---------+--------------------+
|         | Pulse | Contributors | Network | Note               |
+---------+-------+--------------+---------+--------------------+
| MISP    | 5     | 5            | 5       | Il progetto        |
|         |       |              |         | risulta essere in  |
|         |       |              |         | ottima salute in   |
|         |       |              |         | quanto ha          |
|         |       |              |         | un’ottima attività |
|         |       |              |         | di rilasci da      |
|         |       |              |         | diverse decine di  |
|         |       |              |         | sviluppatori che   |
|         |       |              |         | mantengono la      |
|         |       |              |         | soluzione. Dal     |
|         |       |              |         | grafico            |
|         |       |              |         | Contributors si    |
|         |       |              |         | evince come la     |
|         |       |              |         | quantità di commit |
|         |       |              |         | nell’ultimo anno   |
|         |       |              |         | sia cresciuto in   |
|         |       |              |         | maniera lineare    |
|         |       |              |         | dando concretezza  |
|         |       |              |         | al progetto        |
|         |       |              |         | stesso. La parte   |
|         |       |              |         | Network fa         |
|         |       |              |         | emergere un buon   |
|         |       |              |         | lavoro di          |
|         |       |              |         | teamworking dove   |
|         |       |              |         | tutti i contributi |
|         |       |              |         | hanno trovato      |
|         |       |              |         | seguito            |
|         |       |              |         | nell’ultimo        |
|         |       |              |         | rilascio.          |
+---------+-------+--------------+---------+--------------------+
| TheHive | 4     | 3            | 5       | Il progetto        |
|         |       |              |         | risulta essere in  |
|         |       |              |         | discreta salute e  |
|         |       |              |         | pur non avendo un  |
|         |       |              |         | notevole numero di |
|         |       |              |         | contributori si    |
|         |       |              |         | può notare come    |
|         |       |              |         | alcune attività    |
|         |       |              |         | siano state svolte |
|         |       |              |         | nell’ultimo mese.  |
|         |       |              |         | Si evince dal      |
|         |       |              |         | grafico fornito da |
|         |       |              |         | GitHub che le      |
|         |       |              |         | attività si sono   |
|         |       |              |         | affievolite nel    |
|         |       |              |         | tempo e questo può |
|         |       |              |         | portare a pensare  |
|         |       |              |         | ad un progressivo  |
|         |       |              |         | abbandono e/o      |
|         |       |              |         | perdita di         |
|         |       |              |         | interesse al       |
|         |       |              |         | progetto. La parte |
|         |       |              |         | che fornisce un    |
|         |       |              |         | ulteriore punto di |
|         |       |              |         | vista importante e |
|         |       |              |         | il Forks dal quale |
|         |       |              |         | si evince che il   |
|         |       |              |         | progetto non è     |
|         |       |              |         | stato abbandonato  |
|         |       |              |         | ma stanno nascendo |
|         |       |              |         | nuove versioni e   |
|         |       |              |         | quindi mitigando   |
|         |       |              |         | il senso di un     |
|         |       |              |         | eventuale          |
|         |       |              |         | abbandono del      |
|         |       |              |         | progetto, facendo  |
|         |       |              |         | ben pensare sul    |
|         |       |              |         | proseguo dello     |
|         |       |              |         | stesso.            |
+---------+-------+--------------+---------+--------------------+
| Cortex  | 2     | 3            | 5       | Questo progetto,   |
|         |       |              |         | costola di         |
|         |       |              |         | TheHive, ha uno    |
|         |       |              |         | stato di salute    |
|         |       |              |         | più critico del    |
|         |       |              |         | precedente e anche |
|         |       |              |         | questo dovrà       |
|         |       |              |         | essere tenuto      |
|         |       |              |         | sotto osservazione |
|         |       |              |         | nei prossimi mesi  |
|         |       |              |         | per vederne        |
|         |       |              |         | l’evoluzione.      |
|         |       |              |         | Anche in questo    |
|         |       |              |         | caso il grafico    |
|         |       |              |         | ottenuto dalla     |
|         |       |              |         | parte Forks        |
|         |       |              |         | risulta            |
|         |       |              |         | interessante in    |
|         |       |              |         | quanto si evince   |
|         |       |              |         | che il progetto è  |
|         |       |              |         | in evoluzione e si |
|         |       |              |         | stanno portando    |
|         |       |              |         | avanti attività in |
|         |       |              |         | parallelo per      |
|         |       |              |         | aggiungere nuove   |
|         |       |              |         | funzionalità.      |
+---------+-------+--------------+---------+--------------------+

Analizzando i tre grafici emerge un interesse di miglioramento da parte
dei singoli progetti nel voler continuare a portarli avanti. Sicuramente
le componenti TheHive e Cortex fanno emergere dei dubbi sul loro
proseguo. Sono progetti giovani e sicuramente sarà necessario tenerli
sotto controllo pur rilevandone l’effettiva utilità nei sistemi fino ad
oggi sviluppati da questo gruppo.

E’ necessario considerare in questa fase eventuali LOCK-IN che
porteremmo nella nostra infrastruttura se applicassimo queste soluzioni
e se queste soluzioni non dovessero decollare nell’immediato.

Da questo punto di vista si è consapevoli del fatto che questi sistemi
siano indipendenti l’uno dall’altro e che la presenza di uno dei
progetti non inibisca la propria efficacia e le proprie funzionalità.

Security Policy
~~~~~~~~~~~~~~~

Un aspetto importante è capire come è implementato e come sono gestiti
all’interno del progetto gli aspetti di sicurezza.

Per un utilizzatore è importante che sia a conoscenza di come poter
fornire indicazioni in merito alla scoperta di un problema di sicurezza
e come questo debba essere comunicato.

Il fornire codice aperto a tutti, appunto open-source, non significa
esclusivamente condividere il lavoro ma anche la conoscenza con tutti
permettendo a chiunque di entrare nel merito di come è stato fatto il
progetto e poter suggerire miglioramenti o nuovi casi d’uso da
implementare.

Un aspetto fondamentale è appunto la gestione dei problemi di sicurezza
riscontrati per rendere il progetto più stabile e sicuramente meno
sfruttabile da male intenzionati.

La gestione di questo aspetto è indice di un grado di maturità, di etica
e responsabilità dell’intero progetto.

Inoltre la presenza di indicazioni complete su come comunicare la
presenza di problemi di questo tipo indica la solidità dell’intera
community che assicura un buon livello di interazione tra utente finale
e gruppo di lavoro rendendolo più solido e sicuramente forniscono
all’utente finale la percezione di un progetto presidiato e quindi un
aumento del grado di fiducia e di affidabilità dell’intero progetto
verso terzi.

Questo aspetto all’interno della community, per essere efficace,
sicuramente dovrà essere gestito con un presidio costante e potrebbe non
essere chiaro fino a che livello questo venga fatto.

La presenza però di una politica di gestione su questo aspetto è un
aspetto importante che aumenterà il grado di fiducia verso il progetto
open-source considerato.

Osservando i repository dei progetti emerge la situazione riassunta in
tabella

+-----------------+----------+------------------+------------------+
|                 | MISP     | TheHive          | Cortex           |
+-----------------+----------+------------------+------------------+
| Security Policy | Presente | Non presente     | Non presente     |
|                 |          | (supporto        | (supporto        |
|                 |          | presente)        | presente)        |
+-----------------+----------+------------------+------------------+

MISP riporta nella sezione dedicata alle politiche di sicurezza in
maniera chiara cosa e come fornire indicazioni su questi aspetti
sensibili, mentre, sia TheHive che Cortex, non seguono i suggerimenti
forniti dal repository su dove e come inserire queste policy, ma è
possibile trovare indicazioni su come notificare al supporto qualsiasi
tipo di problema.

Questo aspetto sicuramente andrebbe migliorato nei progetti TheHive e
Cortex ma la presenza di un supporto presidiato permette
all’utilizzatore finale di aver maggior fiducia verso questi progetti.

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

Conclusioni
===========

L’aspetto della sicurezza informatica è uno dei temi fondamentali per un
consolidamento e un incremento della fiducia da parte degli utenti
finali per spingerli verso l’uso di strumenti digitali. E’ necessario
quindi cercare di salvaguardare le infrastrutture e il software messo a
disposizione.

La continua operatività di questi strumenti è necessaria ed è necessario
che eventuali attacchi informatici non causino blocchi generali dei
servizi forniti, per questo motivo il miglioramento sia nei processi che
nell’operatività nell’ambito della cyber-security deve essere costante e
in continua evoluzione.

Il percorso fatto all’interno di questo Project Work ha portato ad un
interessante considerazione: anche nell’ambito cyber-security si sta
incominciando a dare risposte percorribili anche dal punto di vista
open-source.

La cyber-security ha ancora una forte componente legata a sistemi a
supporto proprietari anche legato al fatto che la competenza su questo
argomento è ancora molto limitata. Negli ultimi anni stanno nascendo
organizzazioni trasversali che aiuteranno ad aumentare la cultura
sull’argomento e la risposta open-source sull’argomento è sicuramente un
aiuto alla divulgazione della materia.

La presenza di software open-source in ambito cyber-security permetterà
di perseguire in maniera condivisa verso ad una efficace riduzione degli
effetti di attacchi informatici.

Inoltre l’aumento di capacità di calcolo dei sistemi coinvolti e quindi
un progressivo abbandono di soluzione hardware verso macchine virtuali,
capaci di eseguire la stessa quantità di elaborazioni senza fare perdere
prestazioni all’infrastruttura, permetterà di realizzare soluzioni
software-base, altamente scalabili, anche totalmente open-source
permettendo una gestione ad ulteriori problematiche di lock-in ed a una
rivisitazione della spesa complessiva ad oggi ancora molto elevata.

.. |image1| image:: Pictures/1000000000000300000001B012DB9774AD3657B9.jpg
   :width: 17cm
   :height: 9.562cm
.. |image2| image:: Pictures/10000000000006290000049FE24F4713C77950D3.jpg
   :width: 14.626cm
   :height: 10.971cm
.. |image3| image:: Pictures/10003DCE0001FFE00001800019F36F495E205B5B.pdf
   :width: 16.013cm
   :height: 12.012cm
.. |image4| image:: Pictures/100000000000043500000295F5080D8E5C58336F.png
   :width: 17cm
   :height: 10.433cm
.. |image5| image:: Pictures/100000000000050F000000548D4124038A44129E.png
   :width: 17cm
   :height: 1.984cm
.. |image6| image:: Pictures/100000000000038E0000049622FCC8E83421356A.jpg
   :width: 10.074cm
   :height: 16.116cm
.. |image7| image:: Pictures/1000020100000591000002F6071A0D7BDF5DB3C9.png
   :width: 15.723cm
   :height: 8.363cm
.. |image8| image:: Pictures/10000201000005910000030FB8C0BFA4BAF30CB5.png
   :width: 15.699cm
   :height: 8.625cm
.. |image9| image:: Pictures/1000020100000591000002F648603CB986381A67.png
   :width: 16.032cm
   :height: 8.527cm
.. |image10| image:: Pictures/10000201000005910000032D1AE5514D9F92C6B7.png
   :width: 16.053cm
   :height: 9.158cm
.. |image11| image:: Pictures/1000020100000591000004039F8FF09C3BEDF7EE.png
   :width: 16.452cm
   :height: 11.857cm
.. |image12| image:: Pictures/1000020100000591000003606FF93CAF39D1B52F.png
   :width: 16.723cm
   :height: 10.139cm
.. |image13| image:: Pictures/1000020100000591000002F6A130B71276FDE8EA.png
   :width: 17cm
   :height: 9.042cm
.. |image14| image:: Pictures/10000000000004660000037C562A5C2349443969.png
   :width: 17cm
   :height: 13.467cm
.. |image15| image:: Pictures/100000000000042F0000017D68186EAE385F4ED3.png
   :width: 17cm
   :height: 6.047cm
.. |image16| image:: Pictures/10000000000003A4000001DF2232A7CC6ED2A8BF.png
   :width: 14.002cm
   :height: 7.195cm
.. |image17| image:: Pictures/10000000000003B700000154895A4964DEC3EC8B.png
   :width: 14.002cm
   :height: 5.004cm
.. |image18| image:: Pictures/100000000000039C000002FA30FD5D0A792B17AA.png
   :width: 14.002cm
   :height: 11.546cm
.. |image19| image:: Pictures/10000000000003A6000001DD27C780AF168255DC.png
   :width: 14.002cm
   :height: 7.149cm
.. |image20| image:: Pictures/10000000000003AC00000150FD97254C39AD9463.png
   :width: 14.002cm
   :height: 5.004cm
.. |image21| image:: Pictures/100000000000039F000002FD5D03EB4AB8FB2640.png
   :width: 14.002cm
   :height: 11.553cm
.. |image22| image:: Pictures/10000000000003A200000141A0B9C44ABFD55F9D.png
   :width: 14.002cm
   :height: 4.831cm
.. |image23| image:: Pictures/10000000000003A00000014C2B1026D97C3FE43D.png
   :width: 14.002cm
   :height: 5.008cm
.. |image24| image:: Pictures/10000000000003AC000002FB437CA2DABB6ECDA2.png
   :width: 14.002cm
   :height: 11.365cm
.. |image25| image:: Pictures/1000000000000252000001F21A16020B973D5A40.png
   :width: 13.028cm
   :height: 10.922cm

