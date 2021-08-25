---
title: Protocollo di servizi di indicizzazione del contenuto
description: Questo documento è una specifica del protocollo del servizio di indicizzazione del contenuto.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df48db5dd1b19983b12daeb6747dce92eedcd78674553f11af2e335f08e7de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481149"
---
# <a name="content-indexing-services-protocol"></a>Protocollo di servizi di indicizzazione del contenuto

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows ricerca.](../search/-search-3x-wds-overview.md)

Specifica del protocollo, versione 0.12

-   [1 Introduzione](#1-introduction)
    -   [1.1 Glossario](#11-glossary)
    -   [1.2 Riferimenti](#12-references)
    -   [1.3 Panoramica del protocollo (Synopsis)](#13-protocol-overview-synopsis)
    -   [1.4 Relazione con altri protocolli](#14-relationship-to-other-protocols)
    -   [1.5 Prerequisiti e precondizioni](#15-prerequisites-and-preconditions)
    -   [1.6 Dichiarazione di applicabilità](#16-applicability-statement)
    -   [1.7 Controllo delle versioni e negoziazione dalla capacità](#17-versioning-and-capability-negotiation)
    -   [1.8 Campi estendibili dal fornitore](#18-vendor-extensible-fields)
    -   [1.9 Assegnazioni degli standard](#19-standards-assignments)
-   [2 Messaggi](#2-messages)
    -   [2.1 Trasporto](#21-transport)
    -   [2.2 Sintassi dei messaggi](#22-message-syntax)
-   [3 Dettagli del protocollo](#3-protocol-details)
    -   [3.1 Dettagli server](#31-server-details)
    -   [3.2 Dettagli client](#32-client-details)
-   [4 Esempi di protocollo](#4-protocol-examples)
    -   [4.1 Esempio 1](#41-example-1)
    -   [4.2 Esempio 2](#42-example-2)
-   [5 Sicurezza](#5-security)
    -   [5.1 Considerazioni sulla sicurezza per i responsabili dell'implementazione](#51-security-considerations-for-implementers)
    -   [5.2 Indice dei parametri di sicurezza](#52-index-of-security-parameters)
-   [6 Indice del comportamento specifico della versione](#6-index-of-version-specific-behavior)

Questo documento è una specifica del protocollo del servizio di indicizzazione del contenuto.

La documentazione del programma WSPP (Workgroup Server Protocol Program) è destinata all'uso in combinazione con i concetti relativi alla documentazione relativa agli standard pubblici, alla programmazione di rete e ai sistemi distribuiti del gruppo di lavoro Windows e presuppone che il lettore abbia familiarità con il materiale di cui si fa riferimento o abbia accesso immediato.

Una specifica del protocollo WSPP non richiede l'uso di strumenti di programmazione o ambienti di programmazione Microsoft per consentire a un licensee di sviluppare un'implementazione. I licenziateri che hanno accesso agli strumenti e agli ambienti di programmazione Microsoft sono liberi di sfruttarli.

## <a name="1-introduction"></a>1 Introduzione

-   [1.1 Glossario](#11-glossary)
-   [1.2 Riferimenti](#12-references)
-   [1.3 Panoramica del protocollo (Synopsis)](#13-protocol-overview-synopsis)
-   [1.4 Relazione con altri protocolli](#14-relationship-to-other-protocols)
-   [1.5 Prerequisiti e precondizioni](#15-prerequisites-and-preconditions)
-   [1.6 Dichiarazione di applicabilità](#16-applicability-statement)
-   [1.7 Controllo delle versioni e negoziazione dalla capacità](#17-versioning-and-capability-negotiation)
-   [1.8 Campi estendibili dal fornitore](#18-vendor-extensible-fields)
-   [1.9 Assegnazioni degli standard](#19-standards-assignments)

### <a name="11-glossary"></a>1.1 Glossario

> [!Note]  
> I termini seguenti sono definiti nella sezione Glossario di \[ \] MS-SYS:
>
> -   GUID
> -   Little Endian
> -   Named Pipe
> -   Percorso

 

**Binding:** richiesta di includere una determinata colonna in **un** set di **righe restituito.** **L'associazione** specifica una proprietà da includere nei risultati della ricerca.

**Segnalibro:** marcatore che identifica in modo univoco una riga all'interno di un set di righe.

**Catalogo:** unità di livello superiore dell'organizzazione nel servizio di indicizzazione. Rappresenta un set di documenti indicizzati su cui è possibile eseguire query usando content indexing service protocol.

**Category:** raggruppamento gerarchico di righe. Ad esempio, un risultato della query contenente le colonne autore e titolo può essere categorizzato in base all'autore. Ogni gruppo di righe contenente lo stesso valore per author costituisce una categoria.

**Capitolo:** intervallo di righe **all'interno** di un set di **righe** .

**Column:** contenitore per un singolo tipo di informazioni in una **riga** . Le colonne vengono mappate ai nomi delle proprietà e specificano quali proprietà vengono usate per gli elementi dell'albero dei comandi **della** query **di** ricerca.

**Albero dei comandi:** combinazione **di restrizioni,** **categorie** e **ordinamenti** specificati per la query di ricerca.

**Cursor:** entità utilizzata come meccanismo per lavorare  con una riga  o un piccolo blocco di righe alla volta in un set di dati restituito in un set di risultati. Un **cursore** viene posizionato su una singola riga **all'interno** del set di risultati. Dopo aver posizionato il **cursore** su una riga, è possibile eseguire operazioni su tale riga o su un blocco di **righe** a partire da tale posizione. 

**Handle:** token che può essere usato per identificare e accedere a **cursori,** **capitoli** e **segnalibri.**

**Index:** struttura persistente che contiene il contenuto di testo estratto dai file da un **servizio di indicizzazione.** È incluso l'elenco di parole, che vengono archiviate insieme al nome file contenitore, alla posizione della parola e alle **impostazioni locali.**

**Indicizzazione:** processo di estrazione di testo e proprietà dai file e archiviazione dei valori estratti negli indici **(per** il testo) e nella **cache** delle proprietà (per le proprietà).

**Servizio di indicizzazione:** servizio che crea cataloghi **indicizzati per** il contenuto e le proprietà dei file system. Le applicazioni possono cercare nei cataloghi informazioni dai file nel file system.

**Impostazioni** locali: identificatore, come specificato \[ nell'Appendice A MS-GPSI, \] che specifica le preferenze relative alla lingua. Queste preferenze indicano come devono essere formattate le date e le ore, gli elementi devono essere ordinati alfabeticamente, le stringhe devono essere confrontate e così via.

**Query in linguaggio** naturale: query costruita usando il linguaggio umano anziché la sintassi di query.

**Parola non** comune: parola ignorata dal servizio di  indicizzazione quando è presente nelle restrizioni specificate per la query di ricerca perché ha un valore discriminatorio minimo. Gli esempi in inglese includono "a", "and" e "the".

**Cache delle proprietà:** cache delle proprietà dei file estratte da un **servizio di indicizzazione.**

**Indicizzazione delle proprietà:** processo  di  creazione di un indice di proprietà di tipo valore di un documento, tra cui autore, oggetto, tipo, conteggio delle parole, numero di pagine stampate e qualsiasi altra proprietà.

**Restrizione:** set di condizioni che un file deve soddisfare per essere incluso nei risultati della ricerca restituiti dal servizio di indicizzazione **in** risposta a una query di ricerca. Una **restrizione** limita lo stato attivo di una  query di ricerca, limitando i file che il servizio di indicizzazione includerà nei risultati della ricerca solo a quelli che soddisfano le condizioni.

**Riga:** raccolta  di colonne contenente i valori delle proprietà che descrivono un  singolo file del set di file che soddisfano le restrizioni specificate nella query di ricerca inviata al servizio **di indicizzazione** .

**Set di righe:** set di **righe restituito** nei risultati della ricerca.

**Ordinamento:** set di regole in una query di ricerca che definiscono l'ordinamento delle righe nel risultato della ricerca. Ogni regola è costituita da una proprietà (nome, dimensioni e così via) e da una direzione per l'ordinamento (crescente o decrescente). Più regole vengono applicate in sequenza

**Proprietà di tipo testo:** proprietà che descrive il contenuto di un documento e al nome è associato solo testo non formattato.

**Proprietà di tipo valore:** proprietà che descrive un singolo attributo di un intero documento. Una proprietà di tipo valore ha un ID del tipo di dati e un valore di tale tipo di dati associato al nome.

**Virtual Root**(Radice virtuale): percorso alternativo di una cartella. Una cartella fisica può avere zero o più radici virtuali. I percorsi che iniziano con una radice virtuale sono detti percorsi virtuali. Ad esempio, /server/vanityroot potrebbe essere una radice virtuale di C: \\ cartella \\ Web \\ IIS1. Il file C: cartella Web IIS1default.htm il percorso virtuale \\ \\ \\ \\ /server/vanityroot/default.htm.

**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT:** questi termini (in maiuscolo) vengono usati come descritto in \[ RFC2119. \] Tutte le istruzioni di comportamento facoltativo usano MAY, SHOULD, o SHOULD NOT.

### <a name="12-references"></a>1.2 Riferimenti

### <a name="121-normative-references"></a>1.2.1 Riferimenti normativi

\[IEEE754 \] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, ottobre 1985, https://standards.ieee.org/standard/754-1985.html

\[MS-DCOM \] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", giugno 2006.

\[MS-GPSI \] Microsoft Corporation, "Criteri di gruppo Installazione software Extension", giugno 2006.

\[MS-SMB \] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions", maggio 2006.

\[MS-SYS \] Microsoft Corporation, "Panoramica del sistema v4", luglio 2006.

\[SALTON \] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.

\[UNICODE \] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org

### <a name="122-informative-references"></a>1.2.2 Riferimenti informativi

\[MSDN-OLEDB \] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .

\[MSDN-QUERYERR \] Microsoft Corporation, Query-Execution valori, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp

### <a name="13-protocol-overview-synopsis"></a>1.3 Panoramica del protocollo (Synopsis)

Un servizio **di indicizzazione del contenuto** consente di organizzare in modo efficiente le funzionalità estratte di una raccolta di documenti. Il protocollo CISP (Content Indexing Service Protocol) consente a un client di comunicare con un server che ospita un servizio di indicizzazione per eseguire query e consentire a un amministratore di gestire il server di indicizzazione.

Durante l'elaborazione dei file, un servizio di indicizzazione analizza un set di  documenti e riorganizza il contenuto in modo che le proprietà di tali documenti possano essere restituite in modo efficiente in risposta alle query. Una raccolta di documenti su cui è possibile eseguire query include un **catalogo** . Un catalogo può contenere **un indice** (per riferimento rapido al testo) e una **cache** delle proprietà (per il recupero rapido dei valori delle proprietà).

Concettualmente, un catalogo è costituito da una "tabella" logica di proprietà con il testo o il valore e le impostazioni locali corrispondenti archiviate **nelle colonne** della tabella. Ogni "riga" della tabella corrisponde a un documento separato nell'ambito del catalogo e ogni "colonna" della tabella corrisponde a una proprietà.

Le attività specifiche eseguite da CISP sono raggruppate in due aree funzionali:

-   Amministrazione remota dei cataloghi del servizio di indicizzazione,
-   Esecuzione di query remote dei cataloghi del servizio di indicizzazione.

### <a name="131-remote-administration-tasks"></a>1.3.1 Attività di amministrazione remota

CISP abilita le attività di gestione del catalogo del servizio di indicizzazione seguenti da un client:

-   Eseguire una query sullo stato corrente di un catalogo del servizio di indicizzazione nel server.
-   Aggiornare lo stato di un catalogo del servizio di indicizzazione.
-   Avviare il processo di indicizzazione per un particolare set di file.
-   Avviare l'ottimizzazione di un indice per migliorare le prestazioni delle query.

Tutte le attività di amministrazione remota seguono un semplice modello di richiesta/risposta. Nel client non viene mantenuto alcuno stato per qualsiasi chiamata amministrativa e le chiamate amministrative possono essere effettuate in qualsiasi ordine.

### <a name="132-remote-querying"></a>1.3.2 Esecuzione di query remote

CISP consente ai client di eseguire query di ricerca su un server remoto che ospita un servizio di indicizzazione.

L'invio di una query di ricerca è un processo in più passaggi avviato dal client. Attenersi alla procedura seguente:

1.  Il client richiede una connessione a un server che ospita un servizio di indicizzazione.
2.  Il client invia i parametri per la query di ricerca, che includono:
    -   Restrizioni **per specificare** i documenti da includere e/o escludere dai risultati della ricerca.
    -   Ordine in cui devono essere restituiti i risultati della ricerca.
    -   Colonne da restituire nel set di risultati.
    -   Numero massimo di **righe** che devono essere restituite per la query.
    -   Tempo massimo per l'esecuzione della query.

        Dopo che il server ha riconosciuto la richiesta del client di avviare la query, il client può richiedere informazioni sullo stato della query, ma questo non è un passaggio obbligatorio.

3.  Il client specifica quindi le proprietà che il server deve includere nei risultati della ricerca.
4.  Il client richiede un set di risultati dal server e il server risponde inviando al client i valori delle proprietà per i file inclusi nei risultati per la query di ricerca del client. Se il valore di una proprietà è troppo grande per essere contenuto in un singolo buffer di risposta, il server non invierà la proprietà, ma imposterà invece lo stato della proprietà su posticipato. Il client richiede quindi separatamente il valore della proprietà usando una serie di richieste per blocchi successivi del valore e quindi riprende la richiesta di altri valori.
5.  Dopo che il client ha completato la query di ricerca e non richiede più risultati aggiuntivi, il client contatta il server per rilasciare la query.
6.  Dopo che il server ha rilasciato la query, il client può inviare una richiesta di disconnessione dal server. La connessione viene quindi chiusa. In alternativa, il client può eseguire un'altra query e ripetere la sequenza dal passaggio 2.

Windows Comportamento: questo protocollo viene implementato in Windows 2000, Windows XP, Windows Server 2003 e Windows Vista.

### <a name="14-relationship-to-other-protocols"></a>1.4 Relazione con altri protocolli

Il CISP si basa sul protocollo \[ SMB MS-SMB \] per il trasporto dei messaggi. Nessun altro protocollo dipende direttamente dal protocollo del servizio di indicizzazione del contenuto.

*Windows Comportamento: le applicazioni interagiscono in genere con un wrapper di interfaccia OLE DB \[ MSDN-OLEDB (ad esempio, un client di protocollo) e non \] direttamente con il protocollo.*

### <a name="15-prerequisites-and-preconditions"></a>1.5 Prerequisiti e precondizioni

Si presuppone che il client abbia ottenuto il nome del server e un nome di catalogo prima che venga richiamato questo protocollo. Il modo in cui un client esegue questa operazione non rientra nell'ambito di questa specifica.

Si presuppone anche che il client e il server hanno un'associazione di sicurezza utilizzabile con named pipe \[ MS-SMB. \]

### <a name="16-applicability-statement"></a>1.6 Dichiarazione di applicabilità

CISP è progettato per l'esecuzione di query e la gestione dei cataloghi in un server remoto da un client. CISP è deprecato in Windows Vista.

### <a name="17-versioning-and-capability-negotiation"></a>1.7 Controllo delle versioni e negoziazione dalla capacità

Questo protocollo non ha meccanismi di controllo delle versioni o negoziazione delle funzionalità.

### <a name="18-vendor-extensible-fields"></a>1.8 Campi estendibili dal fornitore

Questo protocollo usa HRESULT estendibili dal fornitore. I fornitori possono scegliere i propri valori per questo campo, purché il bit C (0x20000000) sia impostato come specificato nella sezione 4.1.1 di MS-SYS, a indicare che si tratta di un codice \[ \] cliente.

Questo protocollo usa anche i valori NTSTATUS presi dallo spazio dei numeri NTSTATUS definito in \[ MS-SYS \] . I fornitori DEVONO riutilizzare questi valori con il significato indicato. La scelta di qualsiasi altro valore corre il rischio di collisione in futuro.

*Windows Comportamento: Windows usa solo i valori specificati nella Sezione 4.1.3 di \[ \] MS-SYS.*

### <a name="181-property-ids"></a>1.8.1 ID proprietà

Le proprietà sono rappresentate da ID noti come ID proprietà. Ogni proprietà deve avere un identificatore univoco globale. Questo identificatore è costituito da un **GUID** che rappresenta una raccolta di proprietà denominate set di proprietà più una stringa o un intero a 32 bit per identificare la proprietà all'interno del set. Se viene usata la forma integer di ID, i valori 0x00000000, 0xFFFFFFFF e 0xFFFFFFFE vengono considerati non validi.

I fornitori possono garantire che le proprietà siano definite in modo univoco inserendole in un set di proprietà definito dal proprio GUID.

### <a name="19-standards-assignments"></a>1.9 Assegnazioni degli standard

Questo protocollo non ha assegnazioni di standard, ma solo assegnazioni private effettuate da Microsoft usando le procedure di allocazione specificate in altri protocolli.

Microsoft ha allocato questo protocollo named pipe come specificato in \[ MS-SMB. \] L'assegnazione è:



| Parametro | Valore             | Riferimento  |
|-----------|-------------------|------------|
| Nome pipe | \\pipe \\ CI \_ SKADS | \[MS-SMB\] |



 

## <a name="2-messages"></a>2 Messaggi

-   [2.1 Trasporto](#21-transport)
-   [2.2 Sintassi dei messaggi](#22-message-syntax)

### <a name="21-transport"></a>2.1 Trasporto

Tutti i messaggi DEVONO essere trasportati usando un named pipe, come specificato in \[ MS-SMB. \] Viene usato il nome della pipe seguente:

-   \\pipe \\ CI \_ SKADS

Questo protocollo usa il protocollo named pipe SMB sottostante per recuperare l'identità del chiamante che ha effettuato la connessione come specificato nella sezione 2.2.8 di MS-SMB. Il client DEVE impostare SECURITY IDENTIFICATION come \[ ImpersonationLevel nella richiesta di apertura del \] \_ named pipe.

### <a name="22-message-syntax"></a>2.2 Sintassi dei messaggi

Diverse strutture e messaggi nelle sezioni seguenti fanno riferimento agli handle di capitolo o segnalibro. Un handle è una struttura opaca lunga 32 bit che identifica in modo univoco un capitolo o un segnalibro. In genere, le applicazioni client ricevono valori di handle tramite chiamate al metodo . Tuttavia, esistono diversi valori noti che non devono essere ottenuti da un server, il cui significato è specificato nella tabella seguente:



| Valore                         | Significato                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| Db \_ NULL \_ HCHAPTER 0x00000000 | Handle di capitolo per il set di righe nonchaptered, contenente tutti i risultati della query.    |
| DBBMK \_ FIRST 0x00000001       | Handle di segnalibro per un segnalibro che identifica la prima riga del set di righe. |
| DBBMK \_ LAST 0x00000002        | Handle di segnalibro per un segnalibro che identifica l'ultima riga nel set di righe.  |



 

### <a name="221-structures"></a>2.2.1 Strutture

In questa sezione vengono fornite informazioni dettagliate sulle strutture di dati definite e usate da CISP.

Tutti gli interi con segno a 2, 4 e 8 byte e senza segno nelle strutture seguenti DEVONO essere trasferiti in ordine di byte little-endian.

Nella tabella seguente sono riepilogate le strutture di dati definite in questa sezione.



| Struttura                    | Descrizione                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| CBaseStorageVariant          | Contiene il valore su cui eseguire un'operazione di corrispondenza per una proprietà specificata in una struttura CPropertyRestriction. |
| SAFEARRAY, SAFEARRAY2        | Contiene una matrice multidimensionale.                                                                                     |
| SAFEARRAYBOUND               | Rappresenta i limiti per una dimensione di una matrice specificata in una struttura SAFEARRAY.                                  |
| CFullPropSpec                | Contiene una specifica di proprietà.                                                                                     |
| CContentRestriction          | Contiene una stringa di cui trovare la corrispondenza per un valore di proprietà nella cache delle proprietà.                                                 |
| CKey                         | Contiene un valore della proprietà.                                                                                             |
| CInternalPropertyRestriction | Contiene un valore della proprietà da associare a un'operazione.                                                                  |
| CNatLanguageRestriction      | Contiene una corrispondenza di query in linguaggio naturale per una proprietà.                                                                |
| CNodeRestriction             | Contiene una matrice di nodi dell'albero dei comandi che specificano le restrizioni per una query.                                       |
| COccRestriction              | Contiene la posizione di una parola in una frase.                                                                           |
| CPropertyRestriction         | Contiene un valore della proprietà da associare a un'operazione.                                                                  |
| CRangeRestriction            | Contiene una restrizione per un intervallo di valori.                                                                           |
| CScopeRestriction            | Contiene una restrizione sui file in cui eseguire la ricerca.                                                                    |
| CSort                        | Identifica una colonna da ordinare.                                                                                           |
| CSynRestriction              | Contiene una parola o i relativi sinonimi per una frase di query.                                                                    |
| CVectorRestriction           | Contiene un'operazione OR ponderata in un nodo dell'albero dei comandi.                                                               |
| CWordRestriction             | Contiene una parola per una frase di query.                                                                                    |
| CRestriction                 | Contiene un nodo di un albero dei comandi di query.                                                                               |
| CColumnSet                   | Indica il numero di colonne da restituire.                                                                             |
| CCategorizationSet           | Contiene informazioni sul raggruppamento di un set di risultati della query.                                                     |
| CCategorizationSpec          | Contiene una definizione di categorie in cui verranno categorizzati i risultati della query.                                      |
| CDbColId                     | Contiene una colonna.                                                                                                     |
| CDbProp                      | Contiene una proprietà .                                                                                                   |
| CDbPropSet                   | Contiene un set di proprietà.                                                                                          |
| CPidMapper                   | Contiene una matrice di ID proprietà che specificano le proprietà da restituire in un set di righe.                                     |
| CRowSeekAt                   | Contiene l'offset in corrispondenza del quale recuperare le righe in un messaggio CPMGetRowsIn                                                |
| CRowSeekAtRatio              | Identifica il punto in cui iniziare il recupero per un messaggio CPMGetRowsIn.                                           |
| CRowSeekByBookmark           | Identifica i segnalibri da cui recuperare le righe per un messaggio CPMGetRowsIn.                                       |
| CRowSeekNext                 | Contiene il numero di righe da ignorare in un messaggio CPMGetRowsIn.                                                         |
| Proprietà CRowsetProperties            | Contiene le informazioni di configurazione per una query.                                                                    |
| CSortSet                     | Contiene l'ordinamento per una query.                                                                                   |
| CTableColumn                 | Contiene una colonna per il messaggio CPMSetBindings.                                                                      |
| SERIALIZEDPROPERTYVALUE      | Contiene un valore serializzato.                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a>2.2.1.1 CBaseStorageVariant

La struttura CBaseStorageVariant contiene il valore su cui eseguire un'operazione di corrispondenza per una proprietà specificata nella struttura CPropertyRestriction.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

vType

vData1

vData2

vValue (variabile)



 

**vType:** indicatore di tipo che indica il tipo di vValue. DEVE essere uno dei valori VARENUM specificati nella tabella seguente.



| Valore                 | Significato                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ EMPTY (0x0000)    | vValue non è presente.                                                                                                               |
| VT \_ NULL (0x0001)     | vValue non è presente.                                                                                                               |
| VT \_ I1 (0x0010)       | Intero con segno a 1 byte.                                                                                                             |
| VT \_ UI1 (0x0011)      | Intero senza segno a 1 byte.                                                                                                           |
| VT \_ I2 (0x0002)       | Intero con segno a 2 byte.                                                                                                             |
| VT \_ UI2 (0x0012)      | Intero senza segno a 2 byte.                                                                                                           |
| VT \_ BOOL (0x000B)     | Valore booleano; Intero a 2 byte contenente 0x0000 (FALSE) o 0xFFFF (TRUE).                                                        |
| VT \_ I4 (0x0003)       | Intero con segno a 4 byte.                                                                                                             |
| VT \_ UI4 (0x0013)      | Intero senza segno a 4 byte.                                                                                                           |
| VT \_ R4 (0x0004)       | Numero a virgola mobile A 32 bit IEEE, come definito in \[ IEEE754. \]                                                                     |
| VT \_ INT (0x0016)      | Intero con segno a 4 byte.                                                                                                             |
| UINT \_ VT (0x0017)     | Intero senza segno a 4 byte.                                                                                                           |
| ERRORE \_ VT (0x000A)    | Intero senza segno a 4 byte contenente un HRESULT, come specificato in \[ \] MS-SYS.                                                         |
| VT \_ I8 (0x0014)       | Intero con segno a 8 byte.                                                                                                            |
| VT \_ UI8 (0x0015)      | Intero senza segno a 8 byte.                                                                                                          |
| VT \_ R8 (0x0005)       | Numero a virgola mobile IEEE a 64 bit come definito in \[ IEEE754. \]                                                                      |
| VT \_ CY (0x0006)       | Intero complementare a 8 byte a due (ridimensionato di 10.000).                                                                               |
| VT \_ DATE (0x0007)     | Numero a virgola mobile a 64 bit che rappresenta il numero di giorni a partire dalle 00.00.00 del 31 dicembre 1899 (Coordinated Universal Time).     |
| VT \_ FILETIME (0x0040) | Intero a 64 bit che rappresenta il numero di intervalli di 100 nanosecondi dalle 00.00.00 del 1° gennaio 1601 (Coordinated Universal Time). |
| VT \_ DECIMAL (0x000E)  | Struttura DECIMAL come specificato nella sezione 2.2.1.1.1.1.                                                                             |
| \_CLSID VT (0x0048)    | Valore binario a 16 byte contenente un GUID.                                                                                            |
| BLOB VT \_ (0x0041)     | Numero intero senza segno a 4 byte di byte nel BLOB, seguito da tale numero di byte di dati.                                           |
| VT \_ BSTR (0x0008)     | Numero intero senza segno a 4 byte di byte nella stringa, seguito da una stringa, come specificato di seguito in vValue.                       |
| VT \_ LPSTR (0x001E)    | Stringa ANSI con terminazione Null.                                                                                                       |
| VT \_ LPWSTR (0x001F)   | Stringa UNICODE Unicode con \[ \] terminazione Null.                                                                                        |
| VT \_ VARIANT (0x000C)  | CBaseStorageVariant. DEVE essere combinato con un modificatore di tipo VT \_ ARRAY o VT \_ VECTOR.                                               |



 

Nella tabella seguente vengono specificati i modificatori di tipo per vType. I modificatori di tipo possono essere ORed binari con vType, per modificare il significato di vValue per indicare che si tratta di uno dei due tipi di matrice possibili.



| Valore               | Significato                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VETTORE \_ VT (0x1000) | Se l'indicatore di tipo viene combinato con VT VECTOR usando un operatore OR, vValue è una matrice conteggiata di \_ valori del tipo indicato. Per informazioni dettagliate, vedere la sezione 2.2.1.1.1.2. <br/> Questo modificatore di tipo NON DEVE essere combinato con i tipi seguenti: VT \_ INT, VT \_ UINT, VT \_ DECIMAL, VT \_ BLOB, VT \_ BLOB \_ OBJECT.<br/>                                    |
| VT \_ ARRAY (0x2000)  | Se l'indicatore di tipo viene combinato con VT ARRAY da un operatore OR, il valore è safeARRAY (come specificato nella sezione \_ 2.2.1.1.1.3) contenente i valori del tipo indicato. <br/> Questo modificatore di tipo NON DEVE essere combinato con i tipi seguenti: VT \_ I8, VT \_ UI8, VT \_ FILETIME, \_ CLSID VT, BLOB \_ VT, VT \_ BLOB \_ OBJECT, VT \_ LPSTR, VT \_ LPWSTR. <br/> |



 

**vData1:** quando vType è VT DECIMAL, il valore di questo campo viene specificato come campo Scale nella sezione \_ 2.2.1.1.1.1. Per tutti gli altri vType, il valore DEVE essere impostato su 0x00.

**vData2:** quando vType è VT DECIMAL, il valore di questo campo viene specificato come campo Sign nella sezione \_ 2.2.1.1.1.1. Per tutti gli altri vType, il valore DEVE essere impostato su 0x00.

**vValue:** valore per l'operazione di corrispondenza. La sintassi DEVE essere come indicato nel campo vType.

La tabella seguente riepiloga le dimensioni per il campo vValue, a seconda del campo vType per i tipi di dati a lunghezza fissa. La dimensione è espressa in byte.



| vType                                                   | Dimensione |
|---------------------------------------------------------|------|
| VT \_ I1, VT, \_ UI1                                        | 1    |
| VT \_ I2, VT \_ UI2, VT \_ BOOL                               | 2    |
| VT \_ I4, VT \_ UI4, VT \_ R4, VT \_ INT, VT \_ UINT, ERRORE \_ VT   | 4    |
| VT \_ I8, VT \_ UI8, VT \_ R8, VT \_ CY, VT \_ DATE, VT \_ FILETIME | 8    |
| VT \_ DECIMAL, VT \_ CLSID                                  | 16   |



 

Se vType è impostato su VT \_ BLOB, VT BSTR o \_ VT \_ LPSTR, la struttura di vValue viene specificata nel diagramma seguente:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cbSize

blobData (variabile, facoltativo)



 

**cbSize:** intero senza segno a 32 bit, che indica le dimensioni del campo blobData in byte. Se vType è impostato su VT BSTR o \_ VT LPSTR, cbSize DEVE essere impostato su 0x00000000 quando la stringa rappresentata \_ è una stringa vuota.

**blobData:** DEVE essere di lunghezza cbSize in byte.

Per vType impostato su BLOB VT, questo campo è dati BLOB \_ binari opachi.

Per vType impostato su VT BSTR, questo campo è un set di caratteri in un set di caratteri \_ OEM selezionato. Il client e il server DEVONO essere configurati per avere set di caratteri interoperabili (fuori banda del protocollo). Non è necessario che sia con terminazione Null.

Per vType impostato su VT LPSTR, questo campo è una stringa di caratteri con terminazione Null in un set di caratteri \_ OEM selezionato. Il client e il server DEVONO essere configurati per avere set di caratteri interoperabili (fuori banda del protocollo).

Se vType è impostato su VT \_ LPWSTR, la struttura di vValue viene specificata nel diagramma seguente:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

ccLen

string (variabile, facoltativo)



 

**ccLen:** intero senza segno a 32 bit, che indica le dimensioni del campo stringa in caratteri Unicode. DEVE essere impostato su 0x00000000 per una stringa vuota.

**string:** stringa Unicode con terminazione Null.

### <a name="22111-cbasestoragevariant-structures"></a>2.2.1.1.1 Strutture CBaseStorageVariant

Le strutture seguenti vengono usate nella struttura CBaseStorageVariant.

### <a name="221111-decimal"></a>2.2.1.1.1.1 DECIMALE

DECIMAL viene usato per rappresentare un valore numerico esatto con precisione fissa e scala fissa.

Quando vType è impostato su VT DECIMAL (0x0000E), i campi \_ vData1 e vData2 di CBaseStorageVariant DEVONO essere interpretati come segue:

**vData1:** numero di cifre a destra del separatore decimale. DEVE essere compreso nell'intervallo da 0 a 28.

**vData2:** segno del valore numerico. Impostare su 0x00 se positivo, 0x80 se negativo.

Il formato del campo vValue è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Hi32

Lo32

Mid32



 

**Hi32:** i 32 bit più alti dell'intero a 96 bit.

**Lo32:** i 32 bit più bassi dell'intero a 96 bit.

**Mid32:** 32 bit intermedi dell'intero a 96 bit.

### <a name="221112-vt_vector"></a>2.2.1.1.1.2 VETTORE \_ VT

VT \_ Vector viene usato per passare matrici unidimensionali.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

vVectorElements

vVectorData



 

**vVectorElements:** intero senza segno a 32 bit, che indica il numero di elementi nel campo vVectorData.

**vVectorData:** matrice di elementi con un tipo indicato da vType con 0x1000 bit cancellato. Le dimensioni di un singolo elemento a lunghezza fissa possono essere ottenute dalla tabella con tipo di dati a lunghezza fissa, come specificato nella sezione 2.2.1.1. La lunghezza di questo campo, in byte, può essere calcolata moltiplicando vVectorElements per le dimensioni del singolo elemento.

Per i tipi di dati a lunghezza variabile vVectorData contiene una sequenza di tipi semplici con marshalling consecutivo in cui il tipo è indicato da vType con il 0x1000 bit cancellato. Ciò include un caso speciale indicato da vType VT \_ ARRAY \| VT \_ VARIANT (ad esempio, 0x100C).

Gli elementi nel campo vVectorData DEVONO essere separati da 0 a 3 byte di riempimento in modo che ogni elemento inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa matrice. Se sono presenti byte di riempimento, il valore in essi contenuto è arbitrario. Il contenuto dei byte di riempimento DEVE essere ignorato dal ricevitore.

Per un vType impostato su VT ARRAY VT VARIANT, il tipo per gli elementi in questa sequenza \_ \| è \_ CBaseStorageVariant.

### <a name="221113-safearray"></a>2.2.1.1.1.3 SAFEARRAY

SAFEARRAY viene usato per passare matrici multidimensionali. La struttura contiene informazioni sulle dimensioni della matrice, nonché i dati nella matrice.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cDims

fFeatures

cbElements

Rgsabound (variabile)

vData (variabile)



 

**cDims:** intero senza segno a 16 bit, che indica il numero di dimensioni della matrice multidimensionale.

**fFeatures:** campo di bit a 16 bit. I valori rappresentano le funzionalità, definite dalle applicazioni di livello superiore e DEVONO essere ignorate.

**cbElements:** intero senza segno a 32 bit che specifica le dimensioni di ogni elemento della matrice.

**Rgsabound:** matrice che contiene una struttura SAFEARRAYBOUND, come specificato nella sezione 2.2.1.1.1.4, per dimensione in SAFEARRAY. Questa matrice ha prima la dimensione più a sinistra e la dimensione più a destra per ultima.

**vData:** vettore di elementi di cui è stato effettuato il marshalling di un determinato tipo, indicato dal tipo vType dell'oggetto CBaseStorageVariant contenitore, con il bit 0x2000 cancellato.

Il marshalling di vData viene eseguito in modo analogo a VT VECTOR, come specificato nella Sezione 2.2.1.1.1.2, con la differenza che il numero di elementi non viene archiviato davanti al \_ vettore. Il numero di elementi viene invece calcolato moltiplicando il valore cElements con tutti i limiti di matrice sicuri nel campo Rgsabound. Gli elementi vengono archiviati in un vettore in ordine di dimensioni, che iniziano con la dimensione più a destra.

Il diagramma seguente rappresenta visivamente una matrice bidimensionale di esempio. La prima dimensione ha cElements uguale a 4 (rappresentato orizzontalmente) e lLbound uguale a 0 e la seconda dimensione ha cElements uguale a 2 (rappresentato verticalmente) e lLbound uguale a 0.

:::row:::
    :::column:::
        0x00000001
    :::column-end:::
    :::column:::
        0x00000002
    :::column-end:::
    :::column:::
        0x00000003
    :::column-end:::
    :::column:::
        0x00000005
    :::column-end:::
:::row-end:::

::row:::
    :::column:::
        0x00000007
    :::column-end:::
    :::column:::
        0x00000011
    :::column-end:::
    :::column:::
        0x00000013
    :::column-end:::
    :::column:::
        0x00000017
    :::column-end:::
:::row-end:::

Usando il diagramma precedente, vData conterrà la sequenza seguente: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (scorrere prima la dimensione più a destra, quindi incrementare la dimensione successiva). L'oggetto Rgsabound precedente (che registra cElements e Lbound) sarà: 0x00000004, 0x00000000, 0x00000002, 0x00000000.

### <a name="221114-safearraybound"></a>2.2.1.1.1.4 SAFEARRAYBOUND

La struttura SAFEARRAYBOUND rappresenta i limiti di una dimensione di safearray o SAFEARRAY2. Il formato è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cElements

lLbound



 

**cElements:** intero senza segno a 32 bit che specifica il numero di elementi nella dimensione.

**lLbound:** intero senza segno a 32 bit che specifica il limite inferiore della dimensione.

### <a name="221115-safearray2"></a>2.2.1.1.1.5 SAFEARRAY2

SAFEARRAY2 viene usato per passare matrici multidimensionali in SERIALIZEDPROPERTYVALUE. La struttura contiene informazioni sui limiti e i dati.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cDims

Rgsabound (variabile)

vData (variabile)



 

**cDims:** intero senza segno a 32 bit, che indica il numero di dimensioni di SAFEARRAY2.

**Rgsabound:** matrice che contiene una struttura SAFEARRAYBOUND, come specificato nella sezione 2.2.1.1.1.4 per dimensione in SAFEARRAY2. Questa matrice ha prima la dimensione più a sinistra e la dimensione più a destra per ultima.

**vData:** vettore di elementi di cui è stato effettuato il marshalling di un particolare tipo, indicato dal tipo dwType dell'oggetto serializedPROPERTYVALUE contenitore, con i bit 0x2000 cancellati. Il formato di vData corrisponde a quello specificato per il campo vData di SAFEARRAY nella sezione 2.2.1.1.1.3.

### <a name="2212-cfullpropspec"></a>2.2.1.2 CFullPropSpec

La struttura CFullPropSpec contiene un GUID del set di proprietà e un identificatore di proprietà per identificare in modo univoco la proprietà.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_guidPropSet

...

...

...

ulKind

PrSpec

Nome proprietà (variabile)



 

**\_ guidPropSet:** GUID del set di proprietà a cui appartiene la proprietà.

**ulKind:** intero senza segno a 32 bit. Uno dei valori seguenti, che indica il contenuto di PrSpec.



| Valore                                            | Significato                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| PRSPEC \_ LPWSTR<br/> 0x00000000<br/> | Il campo PrSpec specifica il numero di caratteri non NULL nel campo Nome proprietà. |
| PRSPEC \_ PROPID<br/> 0x00000001<br/>  | Il campo PrSpec specifica l'ID proprietà (PROPID).                                     |



 

**PrSpec:** intero senza segno a 32 bit con un significato indicato dal campo ulKind.

**Nome proprietà:** se ulKind è impostato su PRSPEC \_ PROPID, questo campo NON DEVE essere presente. Se ulKind è impostato su PRSPEC LPWSTR, questo campo DEVE contenere una matrice di caratteri Unicode non Null prSpec senza distinzione tra maiuscole e minuscole, contenente il nome della \_ proprietà.

### <a name="2213-ccontentrestriction"></a>2.2.1.3 CContentRestriction

La struttura CContentRestriction contiene una stringa di cui trovare una corrispondenza per una proprietà nella cache delle proprietà.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Proprietà (variabile)

...

Padding1 (variabile)

Cc

\_pwcsPhrase (variabile)

...

Padding2 (variabile)

lcid

\_ulGenerateMethod



 

**\_ Property:** struttura CFullPropSpec, come specificato nella sezione 2.2.1.2. Questo campo indica la proprietà su cui eseguire un'operazione di corrispondenza.

**Padding1:** questo campo DEVE avere una lunghezza da 0 a 3 byte. La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura. Se questo campo è presente(ad esempio lunghezza diversa da zero), il valore in esso contenuto è arbitrario. Il contenuto di questo campo DEVE essere ignorato dal ricevitore.

**Cc:** intero senza segno a 32 bit che specifica il numero di caratteri nel \_ campo pwcsPhrase.

**\_ pwcsPhrase:** stringa Unicode non con terminazione Null che rappresenta la parola o la frase di cui trovare la corrispondenza per la proprietà . Questo campo NON DEVE essere vuoto. Il campo Cc contiene la lunghezza della stringa.

**Padding2:** questo campo DEVE avere una lunghezza da 0 a 3 byte. La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura. Se questo campo è presente(ad esempio lunghezza diversa da zero), il valore in esso contenuto è arbitrario. Il contenuto di questo campo DEVE essere ignorato dal ricevitore.

**Lcid:** intero senza segno a 32 bit che indica le impostazioni locali di \_ pwcsPhrase, come specificato \[ nell'appendice A MS-GPSI. \]

**\_ ulGenerateMethod:** intero senza segno a 32 bit che specifica il metodo da usare per la generazione di forme di parole alternative



| Valore                                                       | Significato                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GENERARE \_ IL METODO \_ ESATTO<br/> 0x00000000<br/>    | Corrispondenza esatta.                                                                                                                                                                                                                                                                                      |
| GENERARE IL \_ PREFISSO DEL \_ METODO<br/> 0x00000001 <br/>  | Corrispondenza del prefisso.                                                                                                                                                                                                                                                                                     |
| GENERATE \_ METHOD \_ INFLECT <br/> 0x00000002<br/> | Corrisponde alle flesshe di una parola. Un'inflezione di una parola è una variante della parola radice nella stessa parte del discorso che è stata modificata in base alle regole linguistiche di una determinata lingua. Ad esempio, le flesszioni del verbo "corsia" in inglese includono "corsia", "corsia", "gonfia" e "swam". |



 

### <a name="2214-ckey"></a>2.2.1.4 CKey

La struttura CKey contiene un valore di proprietà.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

PROPID

Cb

buf (variabile)



 

**PROPID:** intero senza segno a 32 bit che rappresenta l'ID proprietà come descritto nella sezione 1.8.1. I valori noti sono:



| Valore      | Significato                                                 |
|------------|---------------------------------------------------------|
| 0xffffffff | Rappresenta un ID di proprietà non valido e NON DEVE essere utilizzato. |
| 0xFFFFFFFE | Rappresenta un ID di proprietà non valido e NON DEVE essere utilizzato. |
| 0x00000000 | Rappresenta qualsiasi ID proprietà.                             |



 

**Cb:** intero senza segno a 32 bit contenente la lunghezza di buf, in byte.

**buf:** sequenza di byte che rappresenta il valore della proprietà.

### <a name="2215-cinternalpropertyrestriction"></a>2.2.1.5 CInternalPropertyRestriction

La struttura CInternalPropertyRestriction contiene un valore di proprietà da associare a un'operazione.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_lop

\_pid

\_prval (variabile)

restrictionPresent

nextRestriction (variabile)



 

**\_ relop:** intero a 32 bit che specifica la relazione da eseguire sulla proprietà. DEVE essere uno dei valori seguenti:



| Valore                 | Significato                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| Prlt 0x00000000       | Confronto minore di.                                                                                           |
| PRLE 0x00000001       | Confronto minore o uguale a.                                                                               |
| PRGT 0x00000002       | Confronto maggiore di.                                                                                        |
| PrGE 0x00000003       | Confronto maggiore o uguale a.                                                                            |
| PreQ 0x00000004       | Confronto di uguaglianza.                                                                                           |
| PRNE 0x00000005       | Confronto diverso da uguale a .                                                                                           |
| PrRE 0x00000006       | Confronto di espressioni regolari.                                                                                  |
| PrAllBits 0x00000007  | AND bit per bit che restituisce l'operando destro.                                                                     |
| PRSomeBits 0x00000008 | AND bit per bit che restituisce un valore diverso da zero.                                                                       |
| PRTutti 0x00000100      | L'operazione deve essere eseguita su una colonna di un set di righe ed è true solo se l'operazione è true per tutte le righe. |
| PRAny 0x00000200      | L'operazione deve essere eseguita su una colonna di un set di righe ed è true se l'operazione è true per qualsiasi riga.       |



 

**\_ pid:** intero senza segno a 32 bit che rappresenta l'ID proprietà (vedere PROPID nella sezione 2.2.1.4).

**\_ prval:** CBaseStorageVariant contenente il valore da correlare alla proprietà.

**restrictionPresent:** valore byte che indica se è presente il campo nextRestriction. DEVE essere impostato su 0x00 o 0x01. Se impostato su 0x01, restrictionPresent indica che è presente il campo nextRestriction. Se impostato su 0x00, restrictionPresent indica che il campo nextRestriction non è presente.

**nextRestriction:** struttura CRestriction, come specificato nella sezione 2.2.1.16, che specifica un'ulteriore restrizione.

### <a name="2216-cnatlanguagerestriction"></a>2.2.1.6 CNatLanguageRestriction

La struttura CNatLanguageRestriction contiene una corrispondenza di **query in linguaggio** naturale per una proprietà.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Proprietà (variabile)

...

\_padding \_ cc (variabile)

Cc

\_pwcsPhrase (variabile)

...

\_padding \_ lcid (variabile)

LCID



 

**\_ Property:** struttura CFullPropSpec, come specificato nella Sezione 2.2.1.3. Questo campo indica la proprietà in cui eseguire l'operazione di corrispondenza.

**\_ padding \_ cc:** questo campo DEVE avere una lunghezza da 0 a 3 byte. La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset pari a un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura. Se questo campo è presente (ad esempio lunghezza diversa da zero), il valore in esso contenuto è arbitrario. Il contenuto di questo campo DEVE essere ignorato dal ricevitore.

**Cc:** intero senza segno a 32 bit. Numero di caratteri nel \_ campo pwcsPhrase.

**\_ pwcsPhrase:** stringa Unicode non con terminazione Null che rappresenta la parola o la frase di cui trovare la corrispondenza per la proprietà. NON DEVE essere vuoto. Il campo Cc contiene la lunghezza della stringa.

**\_ padding \_ lcid:** questo campo DEVE avere una lunghezza da 0 a 3 byte. La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset pari a un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura. Se questo campo è presente (ad esempio lunghezza diversa da zero), il valore in esso contenuto è arbitrario. Il contenuto di questo campo DEVE essere ignorato dal ricevitore.

**Lcid:** intero senza segno a 32 bit che indica le impostazioni locali \_ di pwcsPhrase, come specificato \[ nell'appendice A di MS-GPSI. \]

### <a name="2217-cnoderestriction"></a>2.2.1.7 CNodeRestriction

La struttura CNodeRestriction contiene una matrice **di** nodi dell'albero dei comandi che specificano le restrizioni per la query.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cNode

\_paNode (variabile)



 

**\_ cNode:** intero senza segno a 32 bit che specifica il numero di strutture CRestriction contenute nel \_ campo paNode.

**\_ paNode:** matrice di strutture CRestriction. Le strutture nella matrice DEVONO essere separate da 0 a 3 byte di spaziatura interna in modo che ogni struttura inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa matrice. Se sono presenti byte di spaziatura interna, il valore che contengono è arbitrario. Il contenuto dei byte di riempimento DEVE essere ignorato dal ricevitore.

### <a name="2218-coccrestriction"></a>2.2.1.8 COccRestriction

La struttura COccRestriction contiene la posizione di una parola in una frase.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Occ

\_cPrevNoiseWords

\_cNextNoiseWords



 

**\_ occ:** intero senza segno a 32 bit che specifica l'offset della parola in una stringa di query, in unità di parole. Una parola, usata in questa specifica, è un'unità di lingua in tutte le impostazioni locali che hanno significato.

**\_ cPrevNoiseWords:** intero senza segno a 32  bit contenente il numero di parole non pronunciate che si verificano tra questa parola e la parola precedente nella frase.

**\_ cNextNoiseWords:** intero senza segno a 32 bit contenente il numero di parole non pronunciate che si verificano tra questa parola e la parola successiva nella frase.

### <a name="2219-cpropertyrestriction"></a>2.2.1.9 CPropertyRestriction

La struttura CPropertyRestriction contiene un valore di proprietà da associare a un'operazione.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_relop

\_Proprietà (variabile)

\_prval (variabile)



 

**\_ relop:** intero senza segno a 32 bit che specifica la relazione da eseguire sulla proprietà . DEVE essere uno dei valori seguenti.



| Valore                 | Significato                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| 0x00000000 PRLT       | Confronto minore di.                                                                                           |
| PRLE 0x00000001       | Confronto minore o uguale a.                                                                               |
| 0x00000002 PRGT       | Confronto maggiore di.                                                                                        |
| Richiesta pull 0x00000003       | Confronto maggiore o uguale a.                                                                            |
| Preq 0x00000004       | Confronto di uguaglianza.                                                                                           |
| PRNE 0x00000005       | Confronto diverso da.                                                                                           |
| Richiesta pull 0x00000006       | Confronto di espressioni regolari.                                                                                  |
| PrAllBits 0x00000007  | AND bit per bit che restituisce l'operando destro.                                                                     |
| PrSomeBits 0x00000008 | AND bit per bit che restituisce un valore diverso da zero.                                                                       |
| PrAll 0x00000100      | L'operazione deve essere eseguita su una colonna di un set di righe ed è true solo se l'operazione è true per tutte le righe. |
| PRAny 0x00000200      | L'operazione deve essere eseguita su una colonna di un set di righe e è true se l'operazione è true per qualsiasi riga.       |



 

**\_ Property:** struttura CFullPropSpec, come specificato nella sezione 2.2.1.2, che indica la proprietà su cui eseguire un'operazione di corrispondenza.

**\_ prval:** struttura CBaseStorageVariant, come specificato nella sezione 2.2.1.1, contenente il valore da correlare alla proprietà.

### <a name="22110-crangerestriction"></a>2.2.1.10 CRangeRestriction

La struttura CRangeRestriction contiene una restrizione su un intervallo di valori.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_keyStart (variabile)

\_keyEnd (variabile)



 

**\_ keyStart:** struttura CKey, come specificato nella sezione 2.2.1.4, contenente l'inizio dell'intervallo.

**\_ keyEnd:** struttura CKey contenente la fine dell'intervallo.

### <a name="22111-cscoperestriction"></a>2.2.1.11 CScopeRestriction

La struttura CScopeRestriction contiene una restrizione sui file in cui eseguire la ricerca



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

CcLowerPath

\_lowerPath (variabile)

...

\_padding (variabile)

\_Lunghezza

\_fRecursive

\_fVirtual



 

**CcLowerPath:** intero senza segno a 32 bit contenente il numero di caratteri Unicode nel \_ campo lowerPath.

**\_ lowerPath:** stringa Unicode non con terminazione Null che rappresenta il **percorso** a cui la query deve essere limitata. Il campo CcLowerPath contiene la lunghezza della stringa.

**\_ padding:** questo campo DEVE avere una lunghezza da 0 a 3 byte. La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura. Se questo campo è presente(ad esempio lunghezza diversa da zero), il valore in esso contenuto è arbitrario. Il contenuto di questo campo DEVE essere ignorato dal ricevitore.

**\_ length:** intero senza segno a 32 bit contenente la lunghezza di \_ lowerPath, in caratteri Unicode. Deve essere lo stesso valore di CcLowerPath.

**\_ fRecursive:** intero senza segno a 32 bit. DEVE essere impostato su 0x00000001 o 0x00000000. Se impostato su 0x00000001, il server deve esaminare in modo ricorsivo tutte le sottodirectory del percorso. Se impostato su 0x00000000, il server non esamina le sottodirectory.

**\_ fVirtual:** intero senza segno a 32 bit. DEVE essere impostato su 0x00000001 o 0x00000000. Se impostato su 0x00000001, lowerPath è un percorso virtuale (l'Uniform Resource Locator (URL) associato a una directory fisica nel file system) per \_ un sito Web. Se impostato su 0x00000000, \_ lowerPath è un file system percorso.

### <a name="22112-csort"></a>2.2.1.12 CSort

La struttura CSort identifica una colonna da ordinare.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

pidColumn

dwOrder

locale



 

**pidColumn:** intero senza segno a 32 bit. Numero della colonna in base alla quale eseguire l'ordinamento.

**dwOrder:** intero senza segno a 32 bit. DEVE essere uno dei valori seguenti, specificando come eseguire l'ordinamento in base alla colonna.



| Valore                        | Significato                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| QUERY \_ SORTASCEND 0x00000000 | Le righe devono essere ordinate in ordine crescente in base ai valori nella colonna specificata.  |
| QUERY \_ DISCENDENTE 0X00000001    | Le righe devono essere ordinate in ordine decrescente in base ai valori nella colonna specificata. |



 

**locale:** intero senza segno a 32 bit che indica le impostazioni locali della colonna, come \[ specificato \] nell'Appendice A MS-GPSI.

### <a name="22113-csynrestriction"></a>2.2.1.13 CSynRestriction

La struttura CSynRestriction contiene una parola o i relativi sinonimi per una frase di query.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Restrizione

...

...

cKey

\_keyArray (variabile)

\_isRange



 

**Restriction:** struttura COccRestriction che specifica la posizione della parola.

**cKey:** intero senza segno a 32 bit che specifica il numero di elementi nella \_ matrice keyArray.

**\_ keyArray:** matrice di strutture CKey che specifica una parola e i relativi sinonimi.

**\_ isRange:** se impostato su 0x01, le chiavi sono prefissi per la corrispondenza. Se impostato su 0x00, le chiavi sono valori esatti di cui trovare una corrispondenza. \_isRange NON DEVE essere impostato su altri valori.

### <a name="22114-cvectorrestriction"></a>2.2.1.14 CVectorRestriction

La struttura CVectorRestriction contiene un'operazione OR ponderata su un nodo della struttura ad albero dei comandi.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_pres (variabile)

...

\_padding (variabile)

\_ulRankMethod



 

**\_ pres:** albero dei comandi CNodeRestriction su cui deve essere eseguita un'operazione OR classificata.

**\_ padding:** questo campo DEVE avere una lunghezza da 0 a 3 byte. La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura. Se questo campo è presente(ad esempio lunghezza diversa da zero), il valore in esso contenuto è arbitrario. Il contenuto di questo campo DEVE essere ignorato dal ricevitore.

**\_ ulRankMethod:** intero senza segno a 32 bit che specifica un algoritmo di classificazione. DEVE essere impostato su uno dei valori seguenti.



| Valore                            | Significato                                       |
|----------------------------------|-----------------------------------------------|
| NUMERO \_ MINIMO DI CLASSIFICAZIONE \_ VETTORE 0X00000000     | Usare l'algoritmo \[ minimo SALTON \] .             |
| DIMENSIONI \_ \_ MASTO DEL VETTORE 0X00000001     | Usare l'algoritmo \[ massimo SALTON \] .             |
| VETTORE \_ RANK \_ INNER 0x00000002   | Usare l'algoritmo del \[ prodotto interno SALTON \] .       |
| VECTOR \_ RANK \_ DICE 0x00000003    | Usare l'algoritmo del \[ coefficiente Dice SALTON \] .    |
| VECTOR \_ RANK \_ RANK 0X00000004 | Usare l'algoritmo del \[ coefficiente Diasimmetrico \] SALTON. |



 

### <a name="22115-cwordrestriction"></a>2.2.1.15 CWordRestriction

La struttura CWordRestriction contiene una parola per una frase di query.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

restrizione

...

...

\_key (variabile)

\_isRange



 

**restriction:** struttura COccRestriction che specifica la posizione della parola.

**\_ key:** struttura CKey che specifica una parola.

**\_ isRange:** se impostato su 0x01, la chiave è un prefisso di cui trovare la corrispondenza. Se impostato su 0x00, la chiave è un valore esatto di cui trovare la corrispondenza. \_isRange NON DEVE essere impostato su qualsiasi altro valore.

### <a name="22116-crestriction"></a>2.2.1.16 CRestriction

La struttura CRestriction contiene un nodo di un albero dei comandi di query.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_ulType

Peso

Restrizione



 

**\_ ulType:** intero senza segno a 32 bit che indica il tipo di restrizione usato per il nodo dell'albero dei comandi. DEVE essere impostato su uno dei valori seguenti.



| Valore                    | Significato                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| RTNone 0x00000000        | Il nodo rappresenta una parola non erta in una query vettoriale.                                         |
| RTAnd 0x00000001         | Il nodo contiene un CNodeRestriction su cui deve essere eseguita un'operazione AND logica. |
| RTOr 0x00000002          | Il nodo contiene un oggetto CNodeRestriction su cui deve essere eseguita un'operazione or logica.  |
| RTNot 0x00000003         | Il nodo contiene un CRestriction su cui deve essere eseguita un'operazione NOT.             |
| RtContent 0x00000004     | Il nodo contiene un CContentRestriction.                                                    |
| Proprietà RTProperty 0x00000005    | Il nodo contiene un oggetto CPropertyRestriction.                                                   |
| RtProximity 0x00000006   | Il nodo contiene un oggetto CNodeRestriction su cui deve essere eseguita una classificazione di prossimità,     |
| RTVector 0x00000007      | Il nodo contiene un CVectorRestriction.                                                     |
| RTNatLanguage 0x00000008 | Il nodo contiene un CNatLanguageRestriction.                                                |
| RtScope 0x00000009       | Il nodo contiene un CScopeRestriction.                                                      |
| PRAny 0xFFFFFFFA         | Il nodo contiene un oggetto CInternalPropertyRestriction.                                           |
| RtRange 0xFFFFFFFC       | Il nodo contiene un oggetto CRangeRestriction.                                                      |
| RtPhrase 0xFFFFFFFD      | Il nodo contiene un oggetto CNodeRestriction su cui deve essere eseguita una corrispondenza di frase.          |
| RTSynonym 0xFFFFFFFE     | Il nodo contiene un CSynRestriction.                                                        |
| RtWord 0xFFFFFFFF        | Il nodo contiene un CWordRestriction.                                                       |



 

**Weight:** intero senza segno a 32 bit che rappresenta il peso del nodo. Weight indica l'importanza del nodo rispetto ad altri nodi nell'albero dei comandi di query. I valori di peso più elevati sono più importanti.

**Restrizione**: tipo di restrizione per il nodo dell'albero dei comandi. La sintassi DEVE essere indicata dal \_ campo ulType.

### <a name="22117-ccolumnset"></a>2.2.1.17 CColumnSet

La struttura CColumnSet specifica i numeri di colonna da restituire. Questa struttura viene sempre usata in riferimento a una struttura CPidMapper specifica (sezione 2.2.1.23).



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

count

indexes (variabile)



 

**count:** intero senza segno a 32 bit che specifica il numero di elementi nella matrice di indici.

**indexes:** matrice di interi senza segno a 4 byte che rappresentano indici in base zero nella matrice aPropSpec nella struttura CPidMapper corrispondente.

### <a name="22118-ccategorizationset"></a>2.2.1.18 CCategorizationSet

La struttura CCategorizationSet contiene informazioni sul raggruppamento di un set di risultati della query.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

count

categories (variabile)



 

**count**: intero senza segno a 32 bit contenente il numero di elementi nella matrice categories.

**categories:** matrice di strutture CCategorizationSpec che specifica il raggruppamento della query.

### <a name="22119-ccategorizationspec"></a>2.2.1.19 CCategorizationSpec

La struttura CCategorizationSpec contiene un raggruppamento per un set di risultati della query.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_csColumns (variabile)

\_ulCategType



 

**\_ csColumns:** struttura CColumnSet che indica le colonne in base alle quali raggruppare la query.

**\_ ulCategType:** intero senza segno a 32 bit. DEVE essere impostato su 0x00000000.

### <a name="22120-cdbcolid"></a>2.2.1.20 CDbColId

La struttura CDbColId contiene una colonna.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

eKind

GUID

...

...

...

ulId

vString (variabile)



 

**eKind:** DEVE essere impostato su uno dei valori seguenti che indica il contenuto di GUID e vValue.



| Valore                            | Significato                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| NOME GUID DBKIND \_ \_ 0x00000000    | vString contiene un nome di proprietà.                                                                               |
| DBKIND \_ GUID \_ PROPID 0x00000001  | ulId contiene un intero a 4 byte che indica l'ID della proprietà.                                                      |
| NOME \_ DBKIND PGUID \_ 0x00000003   | vString contiene un nome di proprietà. Questo valore DEVE essere considerato uguale a DBKIND \_ GUID \_ NAME.                    |
| DBKIND \_ PGUID \_ PROPID 0x00000004 | ulId contiene un intero a 4 byte che indica l'ID della proprietà. Questo valore DEVE corrispondere al \_ \_ PROPID GUID DBKIND. |



 

**GUID: GUID** della proprietà.

**ulId:** se eKind è \_ DBKIND GUID PROPID o DBKIND PGUID PROPID, questo campo contiene un intero senza segno, specificando \_ \_ \_ l'ID della proprietà. Se eKind è DBKIND GUID NAME o DBKIND PGUID NAME, questo campo contiene un intero senza segno che specifica il numero di caratteri Unicode contenuti nel \_ \_ campo \_ \_ vString.

**vString:** stringa Unicode senza terminazione Null che rappresenta il nome della proprietà. Deve essere omesso a meno che il campo eKind non sia impostato su DBKIND \_ GUID \_ NAME o DBKIND \_ PGUID \_ NAME.

### <a name="22121-cdbprop"></a>2.2.1.21 CDbProp

La struttura CDbProp contiene una proprietà .



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

DBPROPID

DBPROPOPTIONS

DBPROPSTATUS

colid (variabile)

vValue (variabile)



 

**DBPROPID:** intero senza segno a 32 bit che indica l'ID della proprietà.

**DBPROPOPTIONS:** deve essere impostato su 0x00000000.

**DBPROPSTATUS:** deve essere impostato su 0x00000000.

**colid:** struttura CDbColId, come specificato nella sezione 2.2.1.20, che indica la colonna a cui si applica la proprietà.

**vValue:** CBaseStorageVariant contenente il valore della proprietà.

### <a name="221211-properties"></a>2.2.1.21.1 Proprietà

Questa sezione contiene informazioni dettagliate sulle proprietà usate da CISP. Queste proprietà sono raggruppate in tre set di proprietà, ident2.2.1.21.1 nel campo guidPropertySet della struttura CDbPropSet (Sezione 2.2.1.22).

Nella tabella seguente sono elencate le proprietà che fanno parte del set di proprietà DBPROPSET \_ FSCIFRMWRK \_ EXT.



| Valore                                  | Significato                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| DBPROP \_ CI CATALOG NAME \_ \_ 0x00000002   | Specifica il nome del catalogo o dei cataloghi su cui eseguire la query. Il valore DEVE essere un \_ LPWSTR VT o VT \_ VECTOR \| VT \_ LPWSTR                                   |
| DBPROP \_ CI \_ INCLUDE \_ SCOPES 0x00000003 | Specifica uno o più percorsi da includere nella query. Il valore DEVE essere un \_ LPWSTR VT o VT \_ VECTOR \| VT \_ LPWSTR.                                 |
| FLAG DI \_ AMBITO CI \_ DBPROP \_ 0x00000004    | Specifica la modalità di gestione dei percorsi specificati dalla proprietà DBPROP \_ CI \_ INCLUDE \_ SCOPES. Il valore DEVE essere VT \_ I4 o VT \_ VECTOR \| VT \_ I4. |
| TIPO DI \_ QUERY DBPROP CI \_ \_ 0x00000007     | Specifica il tipo di query. CDbColId DEVE essere impostato su DB \_ NULLID.                                                                               |



 

Nella tabella seguente sono elencati i flag per la proprietà DBPROP \_ CI \_ SCOPE \_ FLAGS:



| Valore                     | Significato                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| QUERY \_ DEEP 0x01          | Se impostata, indica che i file nella directory dell'ambito e in tutte le sottodirectory vengono inclusi nei risultati. Se deselezionata, nei risultati vengono inclusi solo i file nella directory dell'ambito. NON DEVE essere combinato con QUERY \_ DEEP. |
| ESEGUIRE QUERY \_ \_ SUL PERCORSO VIRTUALE 0x02 | Se impostato, indica che l'ambito è un percorso virtuale. Se è deselezionata, indica che l'ambito è una directory fisica.                                                                                                         |



 

Nella tabella seguente sono elencati i tipi di query per la proprietà DBPROP \_ CI \_ QUERY \_ TYPE:



| Valore                     | Significato                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| CiNormal 0x00000000       | Una query normale.                                                                                                   |
| CiVirtualRoots 0x00000001 | La query richiede un elenco delle radici virtuali del catalogo. Questo valore richiede privilegi amministrativi. |
| Proprietà ci 0x00000003   | La query richiede un elenco di tutte le proprietà supportate dal servizio di indicizzazione.                            |
| CiAdminOp 0x00000004      | La query è un'operazione amministrativa. Questo valore richiede privilegi amministrativi.                           |



 

Nella tabella seguente sono elencate le proprietà che fanno parte del set di proprietà \_ DBPROPSET QUERYEXT.



| Valore                                      | Significato                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DBPROP \_ USECONTENTINDEX 0x00000002         | Specifica il modo in cui il servizio di indicizzazione deve gestire le query lente. Il valore DEVE essere un valore \_ BOOL VT. Se TRUE, al server è consentito l'esito negativo di queste query.                                                                                    |
| DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003 | Indica se il servizio di indicizzazione deve eseguire l'operazione di taglio dei risultati. Se TRUE, il server deve prendere in considerazione l'esecuzione del trimming dei risultati in modo da ottimizzare il tempo di risposta al client. Il valore DEVE essere un valore \_ BOOL VT.             |
| DBPROP \_ USEEXTENDEDDBTYPES 0x00000004      | Indica se il client supporta i tipi di dati \_ VECTOR VT. Se TRUE, il client supporta VT VECTOR; se FALSE, il server deve convertire i tipi di dati \_ \_ VT VECTOR in tipi di dati VT \_ ARRAY.  Il valore DEVE essere un valore \_ BOOL VT. |
| DBPROP \_ FIRSTROWS 0x00000007               | Indica le corrispondenze di riga da restituire. Se TRUE, il server deve restituire il primo set di righe corrispondenti. Se FALSE, devono essere restituite le righe corrispondenti migliori. Il valore DEVE essere un valore \_ BOOL VT.                                             |



 

Nella tabella seguente sono elencate le proprietà che fanno parte del set di proprietà DBPROPSET \_ CIFRMWRKCORE \_ EXT.



| Value/DBPROPID                 | Significato                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| DBPROP \_ MACHINE 0x00000002       | Specifica i nomi dei computer in cui deve essere elaborata una query. Il valore DEVE essere VT \_ BSTR o VT \_ ARRAY \| VT \_ BSTR. |
| DBPROP \_ CLIENT \_ CLSID 0x00000003 | Specifica una costante di connessione per il servizio di indicizzazione. Il valore DEVE essere un CLSID VT \_ contenente 0x2A4880706FD911D0A80800A0C906241A.  |



 

### <a name="22122-cdbpropset"></a>2.2.1.22 CDbPropSet

La struttura CDbPropSet contiene un set di proprietà. Si noti che il primo campo ha dimensioni fisse, ma potrebbe non essere allineato a un offset che rappresenta un multiplo a 4 byte dall'inizio del messaggio contenente questa struttura. Tuttavia, il campo cProperties è allineato come tale e di conseguenza il formato è illustrato come segue:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

guidPropertySet

...

...

...

...

\_padding (variabile)

cProperties

aProps (variabile)



 

**guidPropertySet:** GUID che identifica il set di proprietà. DEVE essere impostato sul formato binario corrispondente a uno dei valori seguenti (visualizzati nel formato di rappresentazione di stringa), identificando il set di proprietà delle proprietà contenute nel campo aProps.



| Valore/GUID                                                                              | Nome                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| DBPROPSET \_ FSCIFRMWRK \_ EXT<br/> {A9BD1526-6A80-11D0-8C9D-0020AF1D740E}<br/>   | Set di proprietà del framework dell'indice del contenuto del file system |
| DBPROPSET \_ QUERYEXT<br/> {A7AC77ED-F8D7-11CE-A798-0020F8008025}<br/>          | Set di proprietà dell'estensione della query                     |
| DBPROPSET \_ CIFRMWRKCORE \_ EXT<br/> {AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}<br/> | Content Index Framework Core Property Set        |



 

**\_ padding:** questo campo DEVE avere una lunghezza da 0 a 3 byte. La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura. Se questo campo è presente(ad esempio, lunghezza diversa da zero), il valore in esso contenuto è arbitrario. Il contenuto di questo campo DEVE essere ignorato dal ricevitore.

**cProperties:** intero senza segno a 32 bit contenente il numero di elementi nella matrice aProps.

**aProps:** matrice di strutture CDbProp, come specificato nella sezione 0, contenente le proprietà. Le strutture nella matrice DEVONO essere separate da 0 a 3 byte di riempimento in modo che ogni struttura inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa matrice. Se sono presenti byte di riempimento, il valore in essi contenuto è arbitrario. Il contenuto dei byte di riempimento DEVE essere ignorato dal ricevitore.

### <a name="22123-cpidmapper"></a>2.2.1.23 CPidMapper

La struttura CPidMapper contiene una matrice di ID proprietà che specificano le proprietà da restituire in un set di righe.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

count

aPropSpec

... (variabile)



 

**count:** intero senza segno a 32 bit contenente il numero di elementi nella matrice aPropSpec.

**aPropSpec:** matrice di strutture CFullPropSpec che indicano le proprietà da restituire. Le strutture nella matrice DEVONO essere separate da 0 a 3 byte di spaziatura interna in modo che ogni struttura abbia un allineamento a 4 byte dall'inizio di un messaggio. Tali byte di spaziatura interna possono essere qualsiasi valore arbitrario e DEVONO essere ignorati alla ricezione.

### <a name="22124-crowseekat"></a>2.2.1.24 CRowSeekAt

La struttura CRowSeekAt contiene l'offset in corrispondenza del quale recuperare le righe in un messaggio CPMGetRowsIn.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hRegion

\_cskip

\_bmkOffset



 

**\_ hRegion:** DEVE essere impostato su 0x00000000 e DEVE essere ignorato.

**\_ cskip:** intero senza segno a 32 bit contenente il numero di righe da ignorare nel set di righe.

**\_ bmkOffset:** valore a 32 bit che  rappresenta l'handle del segnalibro che indica la posizione iniziale da cui ignorare il numero di righe specificato in cskip, prima di iniziare il \_ recupero.

### <a name="22125-crowseekatratio"></a>2.2.1.25 CRowSeekAtRatio

La struttura CRowSeekAtRatio identifica il punto in cui iniziare il recupero per un messaggio CPMGetRowsIn.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

CiTblChapt

\_hRegion

\_ulNumerator

\_ulDenominator



 

**CiTblChapt:** intero senza segno a 32 bit che indica il capitolo del set di righe da cui recuperare le righe.

**\_ hRegion:** DEVE essere impostato su 0x00000000 e DEVE essere ignorato.

**\_ ulNumerator:** intero senza segno a 32 bit che rappresenta il numeratore del rapporto tra le righe del capitolo da cui iniziare il recupero.

**\_ ulDenominator:** intero senza segno a 32 bit che rappresenta il denominatore del rapporto tra le righe del capitolo da cui iniziare il recupero. DEVE essere maggiore di zero.

### <a name="22126-crowseekbybookmark"></a>2.2.1.26 CRowSeekByBookmark

La struttura CRowSeekByBookmark identifica i segnalibri da cui iniziare a recuperare le righe per un messaggio CPMGetRowsIn.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_area hRegion

\_cBookmarks

\_maxRet

\_cValidRet

\_aBookmarks (variabile)

\_ascRet (variabile)



 

**\_ hRegion:** deve essere impostato su 0x00000000 e DEVE essere ignorato.

**\_ cBookmarks:** intero senza segno a 32 bit che rappresenta il numero di elementi in \_ una matriceBookmarks.

**\_ maxRet:** intero senza segno a 32 bit che rappresenta il numero di elementi nella \_ matrice ascRet.

**\_ cValidRet:** intero senza segno a 32 bit che rappresenta il numero di elementi validi nella \_ matrice ascRet. Gli elementi validi sono stati definiti nella matrice, mentre gli elementi non validi non sono definiti.

**\_ aBookmarks:** matrice di handle di segnalibro (ognuno rappresentato da 4 byte), ottenuto da un messaggio CPMGetRowsOut.

**\_ ascRet:** matrice di valori HRESULT. Quando CRowSeekByBookMark viene inviato come parte della richiesta CPMGetRowsIn, il numero di voci nella matrice DEVE essere uguale a \_ cBookMarks. Quando vengono inviati dal client, i valori DEVONO essere impostati su zero e il server DEVE ignorare il contenuto della matrice. Quando vengono inviati dal server (come parte del messaggio CPMGetRowsOut), i valori nella matrice indicano lo stato del risultato per ogni recupero di riga.

### <a name="22127-crowseeknext"></a>2.2.1.27 CRowSeekNext

La struttura CRowSeekNext contiene il numero di righe da ignorare in un messaggio CPMGetRowsIn.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

CiTblChapt

\_area hRegion

\_cskip



 

**CiTblChapt:** intero senza segno a 32 bit che specifica il capitolo del set di righe da cui recuperare le righe.

**\_ hRegion:** deve essere impostato su 0x00000000 e DEVE essere ignorato.

**\_ cskip:** intero senza segno a 32 bit che rappresenta il numero di righe da ignorare nel set di righe.

### <a name="22128-crowsetproperties"></a>2.2.1.28 CRowsetProperties

La struttura CRowsetProperties contiene informazioni di configurazione per una query.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_uBooleanOptions

\_ulMaxOpenRows

\_ulMemoryUsage

\_cMaxResults

\_cCmdTimeout



 

**\_ uBooleanOptions:** i 3 bit meno significativi di questo campo DEVONO contenere uno dei tre valori seguenti:



| Valore                  | Significato                                                             |
|------------------------|---------------------------------------------------------------------|
| eSequential 0x00000001 | Il cursore può essere spostato solo in avanti.                              |
| eLocatable 0x00000003  | Il cursore può essere spostato in qualsiasi posizione.                            |
| eScrollable 0x00000007 | Il cursore può essere spostato in qualsiasi posizione e recuperato in qualsiasi direzione. |



 

I bit rimanenti possono essere chiari o impostati su qualsiasi combinazione dei valori seguenti in modo logico OR'd insieme:



| Valore                     | Significato                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| eAsynchronous 0x00000008  | Il client non attenderà il completamento dell'esecuzione.                                                          |
| eFirstRows 0x00000080     | Restituisce le prime righe incontrate, non le corrispondenze migliori.                                                    |
| eHoldRows 0x00000200      | Il server NON DEVE eliminare le righe fino a quando il client non viene eseguito con una query.                                     |
| eChaptered 0x00000800     | Il set di righe supporta i capitoli.                                                                               |
| eUseCI 0x00001000         | Rispondere solo alla query dall'indice, non dal file system.                                                  |
| eDeferTrimming 0x00002000 | Il servizio di indicizzazione deve prendere in considerazione l'ottimizzazione del tempo di risposta al client durante l'esecuzione della rimozione dei risultati. |



 

**\_ ulMaxOpenRows:** intero senza segno a 32 bit. Deve essere impostato su 0x00000000. Non usato e DEVE essere ignorato.

**\_ ulMemoryUsage:** intero senza segno a 32 bit. Deve essere impostato su 0x00000000. Non usato e DEVE essere ignorato.

**\_ cMaxResults:** intero senza segno a 32 bit che specifica il numero massimo di righe da restituire per la query.

**\_ cCmdTimeout:** intero senza segno a 32 bit che specifica il numero di secondi in cui una query deve timeout e termina automaticamente, contando dal momento in cui la query inizia l'esecuzione nel server. Il valore 0x00000000 indica che la query non deve avere un timeout.

### <a name="22129-crowvariant"></a>2.2.1.29 CRowVariant

La struttura CRowVariant contiene la parte di dimensioni fisse di un tipo di dati a lunghezza variabile archiviata nel messaggio CPMGetRowsOut.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

vType

reserved1

reserved2

Offset (facoltativo)



 

**vType:** indicatore di tipo che indica il tipo di vValue. DEVE essere uno dei valori VARENUM specificati nella sezione 2.2.1.1.

**reserved1:** non usato. Il valore può essere impostato su qualsiasi valore arbitrario e deve essere ignorato alla ricezione.

**reserved2:** non usato. Il valore può essere impostato su qualsiasi valore arbitrario e deve essere ignorato alla ricezione.

**Offset:** offset di dati a lunghezza variabile,ad esempio una stringa.  DEVE essere un valore a 32 bit (lunghezza di 4 byte) se vengono usati offset a 32 bit (in base alle regole della sezione 2.2.3.16) o un valore a 64 byte (lunghezza di 8 byte) se vengono usati offset a 64 bit.

### <a name="22130-csortset"></a>2.2.1.30 CSortSet

La struttura CSortSet contiene l'ordinamento della query.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Conteggio

sortArray (variabile)



 

**count:** intero senza segno a 32 bit che specifica il numero di elementi in sortArray.

**sortArray:** matrice di strutture CSort che descrive l'ordine in cui ordinare i risultati della query. Le strutture nella matrice DEVONO essere separate da 0 a 3 byte di riempimento in modo che ogni struttura abbia un allineamento di 4 byte dall'inizio di un messaggio. Tali byte di riempimento possono essere qualsiasi valore arbitrario e DEVONO essere ignorati alla ricezione.

### <a name="22131-ctablecolumn"></a>2.2.1.31 CTableColumn

La struttura CTableColumn contiene una colonna di un messaggio CPMSetBindingsIn



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

PropSpec

... (variabile)

vType

Valore usato

\_padding1 (facoltativo)

ValueOffset (facoltativo)

ValueSize (facoltativo)

StatusUsed

\_padding2 (facoltativo)

StatusOffset (facoltativo)

LengthUsed

\_padding3 (facoltativo)

LengthOffset (facoltativo)



 

**PropSpec:** struttura CFullPropSpec come specificato nella sezione 2.2.1.3.

**vType**: specifica il tipo di valore di dati contenuto nella colonna. Vedere il campo vType nella sezione 2.2.1.1 per l'elenco dei valori per questo campo.

**ValueUsed:** campo a un byte che DEVE essere impostato su 0x01 o 0x00. Se impostato su 0x01, la colonna viene trasferita all'interno della riga a dimensione fissa. Se impostato su 0x00, il valore della colonna viene trasferito nella sezione a lunghezza variabile alla fine del buffer.

**\_ padding1:** campo di un byte che DEVE essere inserito prima di ValueOffset se, senza di esso, ValueOffset non inizia in corrispondenza di un offset pari dall'inizio del messaggio. Il valore di questo byte è arbitrario e DEVE essere ignorato. Se ValueUsed è impostato su 0x00, questo campo NON DEVE essere presente.

**ValueOffset:** intero senza segno a 2 byte che specifica l'offset del valore della colonna nella riga. Se ValueUsed è impostato su 0x00, questo campo NON DEVE essere presente.

**ValueSize:** intero senza segno a 2 byte che specifica le dimensioni del valore della colonna in byte. Se ValueUsed è impostato su 0x00, questo campo NON DEVE essere presente.

**StatusUsed:** campo di un byte che DEVE essere impostato su 0x01 o 0x00. Se impostato su 0x01, lo stato della colonna viene trasferito all'interno della riga. Se 0x00, lo stato della colonna non viene trasferito all'interno della riga.

**\_ padding2:** campo di un byte che DEVE essere inserito prima di StatusOffset se, senza di esso, il campo StatusOffset non inizia in corrispondenza di un offset pari dall'inizio del messaggio. Il valore di questo byte è arbitrario e DEVE essere ignorato. Se StatusUsed è impostato su 0x00, questo campo NON DEVE essere presente.

**StatusOffset:** intero senza segno a 2 byte che specifica l'offset dello stato della colonna nella riga. Se StatusUsed è impostato su 0x00, questo campo NON DEVE essere presente.

**LengthUsed:** campo a un byte che deve essere impostato su 0x01 o 0x00. Se impostato su 0x01, la lunghezza della colonna viene trasferita all'interno della riga. Se 0x00, la lunghezza della colonna NON DEVE essere trasferita all'interno della riga.

**\_ padding3:** campo a un byte che DEVE essere inserito prima di LengthOffset se, senza di esso, LengthOffset non inizia in corrispondenza di un offset pari dall'inizio di un messaggio. Il valore di questo byte è arbitrario e DEVE essere ignorato. Se LengthUsed è impostato su 0x00, questo campo NON DEVE essere presente.

**LengthOffset:** intero senza segno a 2 byte che specifica l'offset della lunghezza della colonna nella riga. Se LengthUsed è impostato su 0x00, questo campo NON DEVE essere presente.

### <a name="22132-serializedpropertyvalue"></a>2.2.1.32 SERIALIZEDPROPERTYVALUE

La struttura SERIALIZEDPROPERTYVALUE contiene un valore serializzato.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

dwType

rgb (variabile)



 

**dwType:** uno dei tipi variant, definito nella sezione 2.2.1.1, che può essere combinato con modificatori di tipo variant. Per tutti i tipi variant, ad eccezione di quelli combinati con VT ARRAY, SERIALIZEDPROPERTYVALUE ha lo stesso layout di \_ CBaseStorageVariant, come specificato nella sezione 2.2.1.1. Se il tipo variant viene combinato con il modificatore di tipo VT ARRAY, viene usato SAFEARRAY2, specificato nella sezione \_ 2.2.1.2.1.1, anziché SAFEARRAY nel campo vValue di CBaseStorageVariant.

**rgb:** valore serializzato. Vedere i dettagli della serializzazione per vValue nella versione 2.2.1.1.

### <a name="222-message-headers"></a>2.2.2 Intestazioni dei messaggi

Tutti i messaggi content indexing service protocol hanno un'intestazione di 16 byte.

Di seguito è riportato un diagramma che mostra il formato di intestazione del messaggio Content Indexing Service Protocol.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_msg

\_Stato

\_ulChecksum

\_ulReserved2



 

\_**msg:** intero a 32 bit che identifica il tipo di messaggio dopo l'intestazione. Nella tabella seguente sono elencati i messaggi del protocollo del servizio di indicizzazione del contenuto e i valori interi specificati per ogni messaggio. Come illustrato nella tabella, alcuni valori identificano 2 messaggi nella tabella. In questi casi il messaggio che segue l'intestazione può essere identificato dalla direzione del flusso del messaggio. Se la direzione è da client a server, viene indicato il messaggio con "In" aggiunto al nome del messaggio. Se la direzione è da server a client, viene indicato il messaggio con "Out" aggiunto al nome del messaggio.



| Valore      | Significato                                                     |
|------------|-------------------------------------------------------------|
| 0x000000C8 | CPMConnectIn o CPMConnectOut                               |
| 0x000000C9 | CPMDisconnect                                               |
| 0x000000CA | CPMCreateQueryIn o CPMCreateQueryOut                       |
| 0x000000CB | CPMFreeCursorIn o CPMFreeCursorOut                         |
| 0x000000CC | CPMGetRowsIn o CPMGetRowsOut                               |
| 0x000000CD | CPMRatioFinishedIn o CPMRatioFinishedOut                   |
| 0x000000CE | CPMCompareBmkIn o CPMCompareBmkOut                         |
| 0x000000CF | CPMGetApproximatePositionIn o CPMGetApproximatePositionOut |
| 0x000000D0 | CPMSetBindingsIn                                            |
| 0x000000D1 | CPMGetNotify                                                |
| 0x000000D2 | CPMSendNotifyOut                                            |
| 0x000000D7 | CPMGetQueryStatusIn o CPMGetQueryStatusOut                 |
| 0x000000D9 | CPMCiStateInOut                                             |
| 0x000000E1 | CPMForceMergeIn                                             |
| 0x000000E4 | CPMFetchValueIn o CPMFetchValueOut                         |
| 0x000000E6 | CPMUpdateDocumentsIn                                        |
| 0x000000E7 | CPMGetQueryStatusExIn o PMGetQueryStatusExOut              |
| 0x000000E8 | CPMRestartPositionIn                                        |
| 0x000000E9 | CPMStopAsynchIn                                             |
| 0x000000EC | CPMSetCatStateIn o CPMSetCatStateOut                       |



 

\_**status**: HRESULT \[ MS-SYS \] che indica lo stato dell'operazione richiesta.

\* *

*Windows Comportamento: il client imposta sempre il \_ campo di stato su 0x00000000.*

**\_ ulChecksum:** \_ ulChecksum MUST deve essere calcolato come specificato nella Sezione 3.2.4 per i messaggi seguenti:

-   CPMConnectIn
-   CPMCreateQueryIn
-   CPMSetBindingsIn
-   CPMGetRowsIn
-   CPMFetchValueIn

Per tutti gli altri messaggi, \_ ulChecksum DEVE essere impostato su 0x00000000. Un client DEVE ignorare il \_ campo ulChecksum.

**\_ ulReserved2:** DEVE essere impostato su 0 e ignorato dal ricevitore.

### <a name="223-messages"></a>2.2.3 Messaggi

### <a name="2231-cpmcistateinout"></a>2.2.3.1 CPMCiStateInOut

Il messaggio CPMCiStateInOut contiene informazioni sullo stato del servizio di indicizzazione. Il formato del messaggio CPMCiStateInOut che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cbStruct

cWordList

cPersistentIndex

cQueries

cDocuments

cFreshTest

dwMergeProgress

Tenuta

cFilteredDocuments

cTotalDocuments

cPendingScans

dwIndexSize

cUniqueKeys

cSecQDocuments

dwPropCacheSize



 

**cbStruct:** intero senza segno a 32 bit. Dimensione in byte di questo messaggio (esclusa l'intestazione comune). DEVE essere impostato su 0x0000003C.

**cWordList:** intero senza segno a 32 bit che indica il conteggio degli indici iniziali creati per i documenti indicizzati di recente.

**cPersistentIndex:** intero senza segno a 32 bit che indica il conteggio degli indici persistenti.

**cQueries:** intero senza segno a 32 bit che indica un numero di query in esecuzione attiva.

**cDocuments:** intero senza segno a 32 bit che indica il numero totale di documenti in attesa di indicizzazione.

**cFreshTest:** intero senza segno a 32 bit che indica il numero di documenti univoci con informazioni negli indici non completamente ottimizzate per le prestazioni.

**dwMergeProgress:** intero senza segno a 32 bit che specifica la percentuale di completamento dell'ottimizzazione completa corrente degli indici, se l'ottimizzazione è in corso. DEVE essere minore o uguale a 100.

**eState:** stato dell'indicizzazione del contenuto fornito da una o più costanti CI \_ \_ \* STATE, definite nella tabella seguente.



| Valore                                         | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CI \_ STATE SHADOW MERGE \_ \_ 0x00000001           | Il servizio di indicizzazione sta ottimizzando alcuni indici per ridurre l'utilizzo della memoria e migliorare le prestazioni delle query.                                                                                                                                                                                                                                                                                                                                                                |
| CI \_ STATE MASTER MERGE \_ \_ 0x00000002           | Il servizio di indicizzazione è in corso di ottimizzazione completa per tutti gli indici.                                                                                                                                                                                                                                                                                                                                                                                                                  |
| CI \_ STATE CONTENT SCAN REQUIRED \_ \_ \_ 0x00000004 | Alcuni documenti nell'indice sono stati modificati e il servizio di indicizzazione deve determinare quali sono stati aggiunti, modificati o eliminati.                                                                                                                                                                                                                                                                                                                                                              |
| CI \_ STATE \_ ANNEALING \_ MERGE 0x00000008        | Il servizio di indicizzazione sta ottimizzando gli indici per ridurre l'utilizzo della memoria e migliorare le prestazioni delle query. Questo processo è più completo di quello identificato dal valore CI STATE SHADOW MERGE, ma non è così completo come specificato dal \_ valore CI STATE MASTER \_ \_ \_ \_ \_ MERGE. Queste ottimizzazioni sono specifiche dell'implementazione perché dipendono dal modo in cui i dati vengono archiviati internamente; Le ottimizzazioni non influiscono sul protocollo in alcun modo diverso dal tempo di risposta. |
| ANALISI \_ DELLO STATO CI \_ 0x00000010                | Il servizio di indicizzazione sta esaminando una directory o un set di directory per verificare se sono stati aggiunti, eliminati o aggiornati file dall'ultima indicizzazione della directory.                                                                                                                                                                                                                                                                                                                 |
| CI \_ STATE \_ RECOVERING 0x00000020              | Il servizio viene avviato dall'ultimo stato salvato ed è in corso il ripristino.                                                                                                                                                                                                                                                                                                                                                                                                        |
| STATO CI \_ \_ MEMORIA INSUFFICIENTE \_ 0x00000080             | La maggior parte della memoria virtuale del server è in uso.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| CI \_ STATE HIGH IO \_ \_ 0x00000100                | Il livello di attività di input/output (I/O) nel server è relativamente elevato.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CI \_ STATE MASTER MERGE \_ \_ \_ PAUSED 0x00000200   | Il processo di ottimizzazione completa per tutti gli indici in corso è stato sospeso. Questo viene fornito solo a scopo informativo e non influisce sul CISP.                                                                                                                                                                                                                                                                                                                                  |
| CI \_ STATE READ ONLY \_ \_ 0x00000400              | La parte del servizio di indicizzazione che preleva nuovi documenti da indicizzare è stata sospesa. Questo viene fornito solo a scopo informativo e non influisce sul CISP.                                                                                                                                                                                                                                                                                                                               |
| CI \_ STATE BATTERY POWER \_ \_ 0x00000800          | La parte del servizio di indicizzazione che preleva nuovi documenti da indicizzare è stata sospesa per risparmiare la durata della batteria, ma risponde comunque alle query. Questo viene fornito solo a scopo informativo e non influisce sul CISP.                                                                                                                                                                                                                                                                 |
| CI \_ STATE USER ACTIVE \_ \_ 0x00001000            | La parte del servizio di indicizzazione che preleva nuovi documenti da indicizzare è stata sospesa a causa dell'elevata attività dell'utente (tastiera o mouse), ma risponde comunque alle query. Questo viene fornito solo a scopo informativo e non influisce sul CISP.                                                                                                                                                                                                                                         |
| CI \_ STATE \_ STARTING 0x00002000                | Il servizio è in fase di avvio. Le query possono essere eseguite, ma l'analisi e la notifica non sono ancora state abilitate. Questo viene fornito solo a scopo informativo e non influisce sul CISP.                                                                                                                                                                                                                                                                                                                   |
| CI \_ STATE \_ READING \_ USNS 0x00004000           | Il servizio non ha letto il log mantenuto dal file system per tenere traccia delle modifiche apportate a file o directory in un volume, pertanto l'indice potrebbe non essere aggiornato.                                                                                                                                                                                                                                                                                                                                  |



 

**cFilteredDocuments:** intero senza segno a 32 bit che indica il numero di documenti indicizzati dall'inizio dell'indicizzazione del contenuto.

**cTotalDocuments:** intero senza segno a 32 bit che indica il numero totale di documenti nel sistema.

**cPendingScans:** intero senza segno a 32 bit che indica il numero di operazioni di indicizzazione di alto livello in sospeso. Il significato di questo valore è specifico del provider, ma si prevede che numeri più grandi indichi che rimane un'indicizzazione maggiore.

*Windows: questo valore* è in genere zero, tranne immediatamente dopo l'avvio dell'indicizzazione o dopo l'overflow di una coda di notifica.

**dwIndexSize:** intero senza segno a 32 bit che indica le dimensioni, in megabyte, dell'indice (esclusa la cache delle proprietà).

**cUniqueKeys:** intero senza segno a 32 bit che indica il numero approssimativo di chiavi univoche nel catalogo.

**cSecQDocuments:** intero senza segno a 32 bit che indica il numero di documenti che il servizio di indicizzazione tenterà nuovamente di indicizzare a causa di un errore durante il tentativo di indicizzazione iniziale.

**dwPropCacheSize:** intero senza segno a 32 bit che indica le dimensioni, in megabyte, della cache delle proprietà.

### <a name="2232-cpmsetcatstatein"></a>2.2.3.2 CPMSetCatStateIn

Il messaggio CPMSetCatStateIn imposta lo stato di un catalogo. Il formato del messaggio CPMSetCatStateIn che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_partID

\_dwNewState

\_CatName (variabile, facoltativo)



 

**\_ partID:** DEVE essere impostato su 0x00000001.

**\_ dwNewState:** DEVE essere impostato su uno dei valori seguenti, che indica il nuovo stato del catalogo.



| Valore                         | Significato                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CICAT \_ ARRESTATO 0x00000001     | Il catalogo è stato arrestato. Questo stato indica che non devono essere indicizzati nuovi file e non devono essere elaborate query di ricerca.                                                     |
| CICAT \_ READONLY 0x00000002    | Il catalogo è di sola lettura. Non è necessario indicizzare nuovi file.                                                                                                               |
| CICAT \_ WRITABLE 0x00000004    | Il catalogo è scrivibile. È possibile indicizzare nuovi file e elaborare query di ricerca.                                                                              |
| CICAT \_ NO \_ QUERY 0x00000008   | Il catalogo non è disponibile per l'esecuzione di query.                                                                                                                              |
| CICAT \_ GET \_ STATE 0x00000010  | Lo stato del catalogo non deve essere modificato, ma solo recuperato.                                                                                                          |
| CICAT \_ ALL \_ OPENED 0x00000020 | Controllo per verificare se tutti i cataloghi sono stati avviati. In tal caso, il campo \_ dwOldState inviato nella risposta CPMSetCatStateOut a questo messaggio verrà segnalato come diverso da zero. |



 

**\_ CatName:** nome del catalogo che deve avere lo stato modificato. Il nome DEVE essere una stringa Unicode con terminazione Null. Questo campo DEVE essere omesso se \_ dwNewState è impostato su CICAT \_ ALL \_ OPENED.

### <a name="2233-cpmsetcatstateout"></a>2.2.3.3 CPMSetCatStateOut

Il messaggio CPMSetCatStateOut è una risposta a un messaggio CPMSetCatStateIn con lo stato precedente del catalogo. Il formato del messaggio CPMSetCatStateOut che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_dwOldState



 

**\_ dwOldState:** uno dei valori seguenti, che indica lo stato precedente del catalogo.



| Valore                       | Significato                                    |
|-----------------------------|--------------------------------------------|
| CICAT \_ ARRESTATO 0x00000001   | Il catalogo è stato arrestato.                    |
| CICAT \_ READONLY 0x00000002  | Il catalogo è di sola lettura.                  |
| CICAT \_ WRITABLE 0x00000004  | Il catalogo è scrivibile.                   |
| CICAT \_ NO \_ QUERY 0x00000008 | Il catalogo non è disponibile per l'esecuzione di query. |



 

### <a name="2234-cpmupdatedocumentsin"></a>2.2.3.4 CPMUpdateDocumentsIn

Il messaggio CPMUpdateDocumentsIn indica al server di indicizzare il percorso specificato.

Il server risponderà con l'intestazione del messaggio CPMUpdateDocumentsOut, con i risultati della richiesta contenuti nel campo dello stato \_ dell'intestazione del messaggio.

Il formato del messaggio CPMUpdateDocumentsIn che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_flag (facoltativo)

\_fRootPath (facoltativo)

RootPath (variabile, facoltativo)



 

**\_ flag**: tipo di aggiornamento da eseguire. Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server. Questo campo DEVE essere impostato su uno dei valori seguenti:



| Valore                  | Significato                                   |
|------------------------|-------------------------------------------|
| UPD \_ INCREM 0x00000000 | È necessario eseguire un aggiornamento incrementale. |
| UPD \_ FULL 0x00000001   | È necessario eseguire un aggiornamento completo.         |
| UPD \_ INIT 0x00000002   | Deve essere eseguita una nuova inizializzazione.  |



 

**\_ fRootPath:** valore booleano che indica se il campo RootPath specifica un percorso in cui eseguire l'aggiornamento. Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server. Questo campo DEVE essere impostato su 0x00000001 o 0x00000000. Se impostato su 0x00000001, un percorso in cui eseguire l'aggiornamento viene incluso in RootPath. Se impostato su 0x00000000, l'aggiornamento deve essere eseguito in tutti i percorsi indicizzati.

**RootPath:** nome del percorso da aggiornare. Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server. Il nome DEVE essere una stringa Unicode con terminazione Null. Questo campo DEVE essere omesso se \_ fRootPath è impostato su 0x00000000.

### <a name="2235-cpmforcemergein"></a>2.2.3.5 CPMForceMergeIn

Il messaggio CPMForceMergeIn richiede a un server di eseguire qualsiasi manutenzione necessaria per migliorare le prestazioni delle query. Il server risponderà con l'intestazione del messaggio CPMForceMergeIn, con i risultati della richiesta contenuti nel \_ campo dello stato.

Il formato del messaggio CPMForceMergeIn che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_partID (facoltativo)



 

**\_ partID:** questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server. Quando questo campo è presente, deve essere impostato su 0x00000001.

### <a name="2236-cpmconnectin"></a>2.2.3.6 CPMConnectIn

Il messaggio CPMConnectIn avvia una sessione tra il client e il server.

Il formato del messaggio CPMConnectIn che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_iClientVersion

\_fClientIsRemote

\_cbBlob1

\_cbBlob2

\_Imbottitura

...

...

MachineName

... (variabile)

Nome utente

... (variabile)

\_paddingcPropSets (facoltativo, variabile)

cPropSets

PropertySet1 (variabile)

PropertySet2 (variabile)

\_paddingExtPropset (facoltativo, variabile)

cExtPropSet

aPropertySets (variabile)



 

**\_ iClientVersion:** intero a 32 bit che indica se il server deve convalidare il valore di checksum specificato nel campo ulChecksum delle intestazioni dei messaggi inviati \_ dal client. Se il campo iClientVersion è impostato su 0x00000008 o superiore, il server DEVE convalidare il valore del campo \_ \_ ulChecksum per i messaggi seguenti:

-   CPMConnectIn
-   CPMCreateQueryIn
-   CPMFetchValueIn
-   CPMGetRowsIn
-   CPMSetBindingsIn

Per informazioni dettagliate sul modo in cui il server convalida il valore specificato dal client nel campo ulChecksum per i messaggi elencati in precedenza, vedere la sezione 3.2.5.

Se il valore è maggiore 0x00000008, si presuppone che il client sia in grado di gestire gli offset a 64 bit nei messaggi CPMGetRowsOut. Per informazioni dettagliate, vedere la sezione 2.2.3.16.

*Windows comportamento: nei Windows client, iClientVersion viene impostato come segue:*



| Valore      | Significato                                                              |
|------------|----------------------------------------------------------------------|
| 0x00000005 | Il sistema operativo client Windows 2000.                                           |
| 0x00000008 | Il sistema operativo client è a 32 bit Windows XP o a 32 bit Windows Server 2003. |
| 0x00010008 | Il sistema operativo client è a 64 bit Windows XP o a 64 bit Windows Server 2003. |



 

\_**fClientIsRemote:** valore booleano che indica se il client è in esecuzione in un computer diverso dal server. DEVE essere impostato su 0x00000001.

\_**cbBlob1:** intero senza segno a 32 bit che indica le dimensioni in byte dei campi cPropSet, PropertySet1 e PropertySet2 combinati.

\_**cbBlob2:** intero senza segno a 32 bit che indica le dimensioni in byte dei campi cExPropSet e aPropertySet, combinati.

\_**padding:** 12 byte di spaziatura interna che può contenere valori arbitrari e DEVE essere ignorato.

**MachineName:** nome del computer del client. La stringa del nome DEVE essere una matrice con terminazione Null di meno di 512 caratteri Unicode, incluso il carattere di terminazione NULL.

**UserName:** stringa che rappresenta il nome utente della persona che esegue l'applicazione che ha richiamato questo protocollo. La stringa del nome DEVE essere una matrice con terminazione Null di meno di 512 caratteri Unicode se concatenata con MachineName.

**\_ paddingcPropSets:** questo campo DEVE avere una lunghezza da 0 a 7 byte. Il numero di byte DEVE essere il numero necessario per fare in modo che l'offset dei byte del campo cPropSets dall'inizio del messaggio che contiene questa struttura sia un multiplo di 8. Il valore dei byte può essere qualsiasi valore arbitrario e DEVE essere ignorato dal ricevitore.

**cPropSets:** intero senza segno a 32 bit che indica il numero di strutture CDbPropSet che segue questo campo. Questo valore DEVE essere impostato su 0x0000002.

**PropertySet1:** struttura CDbPropSet con guidPropertySet contenente DBPROPSET \_ FSCIFRMWRK EXT (vedere la sezione \_ 2.2.1.22).

**PropertySet2:** struttura CDbPropSet con guidPropertySet contenente DBPROPSET \_ CIFRMWRKCORE EXT (vedere la sezione \_ 2.2.1.22).

\_**PaddingExtPropset:** questo campo DEVE avere una lunghezza da 0 a 7 byte. Il numero di byte DEVE essere il numero necessario per fare in modo che l'offset dei byte del campo cExtPropSets dall'inizio del messaggio che contiene questa struttura sia un multiplo di 8. Il valore dei byte può essere qualsiasi valore arbitrario e DEVE essere ignorato dal ricevitore.

**cExtPropSet:** intero senza segno a 32 bit che indica il numero di strutture CDbPropSet che segue questo campo.

**aPropertySets:** matrice di strutture CDbPropSet che specificano altre proprietà. Il numero di elementi in questa matrice DEVE essere uguale a cExtPropSet.

### <a name="2237-cpmconnectout"></a>2.2.3.7 CPMConnectOut

Il messaggio CPMConnectOut contiene una risposta a un messaggio CPMConnectIn.

Il formato del messaggio CPMConnectOut che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Serverversion

\_reserved (variabile)



 

**\_ serverVersion:**

Intero a 32 bit che indica se il server può supportare offset a 64 *bit.* Per informazioni dettagliate, vedere la sezione 2.2.3.16.



| Valore      | Significato                                 |
|------------|-----------------------------------------|
| 0x00000007 | Il server può inviare solo offset a 32 bit. |
| 0x00010007 | Il server può inviare offset a 32 o 64 bit.   |



 

**\_ reserved:** riservato. Il server PUÒ inviare un numero arbitrario di valori arbitrari e il client DEVE ignorare questi valori, se presenti.

### <a name="2238-cpmcreatequeryin"></a>2.2.3.8 CPMCreateQueryIn

Il messaggio CPMCreateQueryIn crea una nuova query. Il formato del messaggio CPMCreateQueryIn che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Dimensione

CColumnSetPresent

ColumnSet (facoltativo)

... (variabile)

CRestrictionPresent.

Restrizione (facoltativa)

... (variabile)

CSortSetPresent

SortSet (facoltativo)

... (variabile)

CCategorizationSetPresent

CategorizationSet (facoltativo)

... (variabile)

Proprietà RowSetProperties

...

...

...

...

PidMapper (variabile)



 

**Size:** intero senza segno a 32 bit che indica il numero di byte dall'inizio di questo campo alla fine del messaggio.

**CColumnSetPresent:** campo byte che indica se il campo ColumnSet è presente. Questo campo DEVE essere impostato su 0x01 o 0x00. Se impostato su 0x01 il campo CColumnSet DEVE essere presente. Se impostato su 0x00, DEVE essere assente.

**ColumnSet:** struttura CColumnSet contenente i numeri di colonna in cui devono essere restituite le proprietà di CPidMapper.

**CRestrictionPresent:** campo byte che indica se il campo Restriction è presente. Se impostato su un valore diverso da zero, il campo Restrizione DEVE essere presente. Se impostato su 0x00, Restriction MUST essere assente.

**Restrizione:** struttura CRestriction contenente l'albero dei comandi della query.

**CSortSetPresent:** campo byte che indica se il campo SortSet è presente. Se impostato su un valore diverso da zero, il campo SortSet DEVE essere presente. Se impostato su 0x00, SortSet DEVE essere assente.

**SortSet:** struttura CSortSet che indica l'ordinamento della query.

**CCategorizationSetPresent:** campo byte che indica se il campo CCategorizationSet è presente. Se impostato su un valore diverso da zero, il campo CCategorizationSet DEVE essere presente. Se impostato su 0x00, CCategorizationSet DEVE essere assente.

**CCategorizationSet:** struttura CCategorizationSet che contiene i gruppi per la query.

**RowSetProperties:** struttura CRowsetProperties che fornisce informazioni di configurazione per la query.

**PidMapper:** struttura CPidMapper contenente le proprietà da restituire in un set di righe.

### <a name="2239-cpmcreatequeryout"></a>2.2.3.9 CPMCreateQueryOut

Il messaggio CPMCreateQueryOut contiene una risposta a un messaggio CPMCreateQueryIn.

Il formato del messaggio CPMCreateQueryOut che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_fTrueSequential

\_fWorkIdUnique

aCursors



 

**\_ fTrueSequential:** valore booleano informativo che indica se è possibile che la query fornisca risultati più velocemente. Se impostato su 0x00000001 per la query fornita in CPMCreateQueryIn, il server può usare l'indice in modo che i risultati della query possano essere recapitati più velocemente. Se impostato su 0x00000000, la distribuzione dei risultati delle query comporta una latenza maggiore. NON DEVE essere impostato su nessun altro valore.

**\_ fWorkIdUnique:** valore booleano che indica se gli identificatori di documento a cui puntano i cursori sono univoci nei risultati della query. Se impostato su 0x00000001, gli identificatori sono univoci. Se impostato su 0x00000000, sono univoci solo in tutto il set di righe.

**aCursors:** matrice di interi senza segno a 32 bit che rappresentano gli handle per i cursori, con il numero di elementi uguale al numero di categorie nel campo CategorizationSet del messaggio CPMCreateQueryIn.

### <a name="22310-cpmgetquerystatusin"></a>2.2.3.10 CPMGetQueryStatusIn

Il messaggio CPMGetQueryStatusIn richiede lo stato di una query. Il formato del messaggio CPMGetQueryStatusIn che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor



 

**\_ hCursor:** intero senza segno a 32 bit che rappresenta l'handle dal messaggio CPMCreateQueryOut che identifica la query per cui recuperare le informazioni sullo stato.

### <a name="22311-cpmgetquerystatusout"></a>2.2.3.11 CPMGetQueryStatusOut

Il messaggio CPMGetQueryStatusOut risponde a un messaggio CPMGetQueryStatusIn con lo stato della query. Il formato del messaggio CPMGetQueryStatusOut che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Stato



 

**\_ Stato:** maschera di bit dei valori definiti nelle tabelle seguenti che descrive la query.

Nella tabella seguente sono elencati i valori STAT \_ \* ottenuti eseguendo un'operazione AND bit per bit \_ su Status con 0x00000007. Il risultato DEVE essere uno dei seguenti:



| Costante                 | Significato                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| STAT \_ BUSY 0x00000000    | La query asincrona è ancora in esecuzione.                                          |
| Errore STAT \_ 0x00000001   | La query è in uno stato di errore.                                                   |
| STAT \_ DONE 0x00000002    | La query è stata completata.                                                            |
| Aggiornamento STAT \_ 0x00000003 | La query è stata completata, ma gli aggiornamenti hanno come risultato un calcolo aggiuntivo delle query. |



 

Nella tabella seguente sono elencati i bit STAT aggiuntivi \_ \* che possono essere impostati in modo indipendente.



| Costante                                    | Significato                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| STAT \_ NOISE \_ WORDS 0x00000010               | Le parole non erre sono state sostituite da caratteri jolly nella query sul contenuto.                                                              |
| CONTENUTO \_ STAT \_ \_ NON AGGIORNATO \_ 0X00000020     | I risultati della query potrebbero non essere corretti perché la query ha modificato, ma non indicizzato, i file.                             |
| AGGIORNAMENTO STAT \_ \_ INCOMPLETO 0x00000040        | I risultati della query potrebbero non essere corretti perché la query ha modificato e indicizzato nuovamente i file il cui contenuto non è stato incluso. |
| QUERY \_ SUL CONTENUTO \_ \_ STAT INCOMPLETE 0x00000080 | La query sul contenuto era troppo complessa per essere completata o richiedeva l'enumerazione anziché usare l'indice di contenuto.                          |
| LIMITE DI \_ TEMPO \_ STAT \_ SUPERATO 0X00000100      | I risultati della query potrebbero non essere corretti perché il tempo di esecuzione della query ha raggiunto il tempo massimo consentito.                    |



 

### <a name="22312-cpmgetquerystatusexin"></a>2.2.3.12 CPMGetQueryStatusExIn

Il messaggio CPMGetQueryStatusExIn richiede lo stato di una query e informazioni aggiuntive, ad esempio il numero di documenti indicizzati, il numero di documenti rimanenti da indicizzare e così via. Il formato del messaggio CPMGetQueryStatusExIn che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_Bmk



 

**\_ hCursor:** valore a 32 bit che rappresenta l'handle dal messaggio CPMCreateQueryOut che identifica la query per cui recuperare le informazioni sullo stato.

**\_ bmk:** valore a 32 bit che indica l'handle di un segnalibro la cui posizione deve essere recuperata.

### <a name="22313-cpmgetquerystatusexout"></a>2.2.3.13 CPMGetQueryStatusExOut

Il messaggio CPMGetQueryStatusExOut risponde a un messaggio CPMGetQueryStatusExIn con lo stato della query e altre informazioni sullo stato, come descritto nel diagramma seguente. Il formato del messaggio CPMGetQueryStatusExOut che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Stato

\_cFilteredDocuments

\_cDocumentsToFilter

\_dwRatioFinishedDenominator

\_dwRatioFinishedNumerator

\_iRowBmk

\_cRowsTotal



 

**\_ Stato:** uno dei dati STAT \_ \* i valori specificati nella Sezione 2.2.3.11.

**\_ cFilteredDocuments:** intero senza segno a 32 bit che indica il numero di documenti indicizzati

**\_ cDocumentsToFilter:** intero senza segno a 32 bit che indica il numero di documenti ancora da indicizzare.

**\_ dwRatioFinishedDenominator:** intero senza segno a 32 bit che indica il denominatore del rapporto tra i documenti che la query ha terminato l'elaborazione.

**\_ dwRatioFinishedNumerator:** intero senza segno a 32 bit che indica il numeratore del rapporto tra i documenti che la query ha terminato l'elaborazione.

**\_ iRowBmk:** intero senza segno a 32 bit che indica la posizione approssimativa del segnalibro nel set di righe in termini di righe.

**\_ cRowsTotal:** intero senza segno a 32 bit che specifica il numero totale di righe nel set di righe.

### <a name="22314-cpmsetbindingsin"></a>2.2.3.14 CPMSetBindingsIn

Il messaggio CPMSetBindingsIn richiede l'associazione di colonne a un set di righe. Il server risponderà al messaggio di richiesta CPMSetBindingsIn usando la sezione di intestazione del messaggio CPMBindingsIn con i risultati della richiesta contenuta nel campo \_ dello stato. Il formato del messaggio CPMSetBindingsIn che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor (facoltativo)

\_cbRow (facoltativo)

\_cbBindingDesc (facoltativo)

\_fittizio (facoltativo)

cColumns (facoltativo)

aColumns (variabile, facoltativo)



 

**\_ hCursor:** valore a 32 bit che rappresenta l'handle del messaggio CPMCreateQueryOut che identifica la riga per cui impostare le associazioni. Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.

**\_ cbRow:** intero senza segno a 32 bit che indica le dimensioni, in byte, di una riga. Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.

**\_ cbBindingDesc:** intero senza segno a 32 bit che indica la lunghezza, in byte, dei campi che segue \_ il campo fittizio. Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.

**\_ fittizio:** questo campo non è usato e deve essere ignorato. Può essere impostato su qualsiasi valore arbitrario. Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.

**cColumns:** intero senza segno a 32 bit che indica il numero di elementi nella matrice aColumns. Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.

**aColumns:** matrice delle strutture CTableColumn che descrivono le colonne di una riga nel set di righe. Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server. Le strutture nella matrice DEVONO essere separate da 0 a 3 byte di riempimento in modo che ogni struttura abbia un allineamento di 4 byte dall'inizio di un messaggio. Tali byte di riempimento possono essere qualsiasi valore arbitrario e DEVONO essere ignorati alla ricezione.

### <a name="22315-cpmgetrowsin"></a>2.2.3.15 CPMGetRowsIn

Il messaggio CPMGetRowsIn richiede righe da una query. Il formato del messaggio CPMGetRowsIn che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_cRowsToTransfer

\_cbRowWidth

\_cbSeek

\_cbReserved

\_cbReadBuffer

\_ulClientBase

\_fBwdFetch

eType

\_chapt

SeekDescription

...

... (variabile)



 

**\_ hCursor:** valore a 32 bit che rappresenta l'handle del messaggio CPMCreateQueryOut che identifica la query per cui recuperare le righe.

**\_ cRowsToTransfer:** intero senza segno a 32 bit che indica il numero massimo di righe che il client vuole ricevere in risposta a questo messaggio.

**\_ cbRowWidth:** intero senza segno a 32 bit che indica la lunghezza di una riga, in byte.

**\_ cbSeek:** intero senza segno a 32 bit che indica la dimensione del messaggio che inizia con eType.

**\_ cbReserved:** intero senza segno a 32 bit che indica le dimensioni, in byte, di un messaggio CPMGetRowsOut (senza i campi Rows e SeekDescriptions). Questo valore in questo campo viene aggiunto al valore del campo cbSeek e quindi deve essere usato per calcolare l'offset del campo Rows nel messaggio \_ CPMGetRowsOut.

**\_ cbReadBuffer:** intero senza segno a 32 bit che DEVE essere impostato sul valore massimo di cbRowWidth o 1000 volte il valore di \_ cRowsToTransfer, arrotondato al multiplo di \_ 512 byte più vicino. Il valore NON DEVE superare 0x00004000.

**\_ ulClientBase:** intero senza segno a 32 bit che indica il valore di base da usare per i calcoli del puntatore nel buffer di riga. Se vengono usati offset a 64 bit, il campo reserved2 dell'intestazione del messaggio viene usato come 32 bit superiori e ulClientBase come 32 bit inferiori di un valore \_ a 64 bit. Per informazioni dettagliate, vedere la sezione 2.2.3.16.

**\_ fBwdFetch:** intero senza segno a 32 bit che indica l'ordine in cui recuperare le righe. Se impostato su 0x00000001, le righe devono essere recuperate in ordine inverso. Se impostato su 0x00000000, le righe devono essere recuperate in avanti. NON DEVE essere impostato su altri valori.

**eType:** intero senza segno a 32 bit contenente uno dei valori seguenti per indicare il tipo di operazione da eseguire.



| Valore                         | Significato                                                  |
|-------------------------------|----------------------------------------------------------|
| eRowSeekNext 0x00000001       | SeekDescription contiene una struttura CRowSeekNext.       |
| eRowSeekAt 0x00000002         | SeekDescription contiene una struttura CRowSeekAt.         |
| eRowSeekAtRatio 0x00000003    | SeekDescription contiene una struttura CRowSeekAtRatio.    |
| eRowSeekByBookmark 0x00000004 | SeekDescription contiene una struttura CRowSeekByBookmark. |



 

**\_ chapt:** valore a 32 bit che rappresenta l'handle del capitolo del set di righe.

**SeekDescription:** questo campo DEVE contenere una struttura del tipo indicato dal valore eType.

### <a name="22316-cpmgetrowsout"></a>2.2.3.16 CPMGetRowsOut

Il messaggio CPMGetRowsOut risponde a un messaggio CPMGetRowsIn con le righe di una query. I server DEVONO formattare gli offset per i tipi di dati a lunghezza variabile nel campo Righe come indicato di seguito:

-   Il client ha indicato che si tratta di un sistema a 32 bit (0x00000008 o inferiore nel campo iClientVersion di CPMConnectIn): gli offset sono numeri interi a 32 bit.
-   Il client ha indicato che si tratta di un sistema a 64 bit ( iClientVersion > 0x00000008 in CPMConnectIn) e Il server ha indicato che si tratta di un sistema a 32 bit ( serverVersion impostato su \_ 0x00000007 in CPMConnectOut): gli offset sono interi a \_ 32 bit
-   Il client ha indicato che si tratta di un sistema a 64 bit ( iClientVersion > 0x00000008 in CPMConnectIn) e il server ha indicato che si tratta di un sistema a 64 bit ( serverVersion impostato su \_ 0x00010007 in CPMConnectOut): gli offset sono interi a \_ 64 bit

Il formato del messaggio CPMGetRowsOut che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cRowsReturned

eType

\_chapt

SeekDescription (facoltativo, variabile)

...

...

paddingRows (facoltativo, variabile)

Righe



 

**\_ cRowsReturned:** intero senza segno a 32 bit che indica il numero di righe restituite in Rows.

**eType:** intero senza segno a 32 bit contenente uno dei valori seguenti per indicare il tipo di operazione rowseek da eseguire



| Valore                         | Significato                                                  |
|-------------------------------|----------------------------------------------------------|
| eRowsSeekNone 0x00000000      | Nessun seekdescription, ignorare il campo SeekDescription.        |
| eRowSeekNext 0x00000001       | SeekDescription contiene una struttura CRowSeekNext.       |
| eRowSeekAt 0x00000002         | SeekDescription contiene una struttura CRowSeekAt.         |
| eRowSeekAtRatio 0x00000003    | SeekDescription contiene una struttura CRowSeekAtRatio.    |
| eRowSeekByBookmark 0x00000004 | SeekDescription contiene una struttura CRowSeekByBookmark. |



 

**\_ chapt:** valore a 32 bit che rappresenta l'handle del capitolo del set di righe.

**SeekDescription:** questo campo DEVE contenere una struttura del tipo indicato dal campo eType.

**paddingRows:** questo campo DEVE essere di lunghezza sufficiente (da 0 a cbReserved-1 byte) per riempire il campo Rows per l'offset cbReserved dall'inizio di un messaggio, dove cbReserved è il valore nel messaggio \_ \_ \_ CPMGetRowsIn. I byte di riempimento usati in questo campo possono essere qualsiasi valore arbitrario. Questo campo DEVE essere ignorato dal ricevitore.

**Righe:** i dati delle righe vengono formattati in base alle informazioni sulla colonna nel messaggio CPMSetBindingsIn più recente. Le righe DEVONO essere archiviate in avanti (ad esempio, la riga 1 prima della riga 2).

Le colonne a dimensione fissa DEVONO essere archiviate in corrispondenza degli offset specificati dal messaggio CPMSetBindingsIn più recente.

Le colonne a dimensione variabile (ad esempio, stringhe) DEVONO essere archiviate come segue:

-   I dati della variabile stessa (ad esempio, la stringa) vengono archiviati vicino alla fine del buffer in ordine decrescente(ad esempio, la raccolta di tutti i dati delle variabili per la riga 1 si trova alla fine, la riga 2 più vicina e così via).
-   L'area a dimensione fissa (all'inizio del buffer di riga) DEVE contenere un CRowVariant per ogni colonna, archiviato in corrispondenza dell'offset specificato nel messaggio CPMSetBindingsIn più recente. vType DEVE contenere il tipo di dati ,ad esempio VT \_ LPWSTR. Se, come determinato dalle regole all'inizio di questa sezione, vengono usati offset a 32 bit, il campo Offset in CRowVariant DEVE contenere un valore a 32 bit che rappresenta l'offset dei dati della variabile dall'inizio del messaggio CPMGetRowsOut, più il valore di ulClientBase specificato nel messaggio \_ CPMGetRowsIn più recente. Se vengono usati offset a 64 bit, il campo Offset in CRowVariant DEVE contenere un valore a 64 bit che rappresenta l'offset dall'inizio del messaggio CPMGetRowsOut, aggiunto a un valore a 64 bit composto usando ulClientBase come minimo \_ a 32 bit e \_ ulReserved2 come 32 bit alti.

Ad esempio, se nel messaggio CPMSetBindingsIn sono specificate due colonne: Size (VT \_ I4) e Title (VT \_ LPWSTR) e ulClientBase da CPMGetRowsIn 0x10000 verranno visualizzate due righe come indicato di \_ seguito. La sezione contrassegnata in grigio è la parte a lunghezza fissa del buffer.

![Esempio di messaggio cpmsetbindingsin](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a>2.2.3.17 CPMRatioFinishedIn

Il messaggio CPMRatioFinishedIn richiede la percentuale di completamento di una query. Il formato del messaggio CPMRatioFinishedIn che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_fQuick



 

**\_ hCursor:** handle del messaggio CPMCreateQueryOut che identifica la query per cui richiedere informazioni di completamento.

**\_ fQuick:** DEVE essere impostato su 0x00000001. Non usato e DEVE essere ignorato dal server.

### <a name="22318-cpmratiofinishedout"></a>2.2.3.18 CPMRatioFinishedOut

Il messaggio CPMRatioFinishedOut risponde a un messaggio CPMRatioFinishedIn con il rapporto di completamento di una query. Il formato del messaggio CPMRatioFinishedOut che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_ ulNumerator

\_ulDenominator

\_Corvi

\_fNewRows



 

**\_ ulNumerator:** intero senza segno a 32 bit che indica il numeratore del rapporto di completamento in termini di righe.

**\_ ulDenominator:** intero senza segno a 32 bit che indica il denominatore del rapporto di completamento in termini di righe. DEVE essere maggiore di zero.

**\_ cRows:** intero senza segno a 32 bit che indica il numero totale di righe per la query.

**\_ fNewRows:** valore booleano che indica se sono disponibili nuove righe. Il valore 0x00000001 indica che nel set di righe sono disponibili nuove righe. Il valore 0x00000000 indica che il set di righe non contiene nuove righe. Questo campo NON DEVE essere impostato su altri valori.

### <a name="22319-cpmfetchvaluein"></a>2.2.3.19 CPMFetchValueIn

Il messaggio CPMFetchValueIn richiede un valore di proprietà troppo grande per essere restituito in un set di righe. Come specificato nella sezione 3.2.4.2.5, questo messaggio viene inviato ripetutamente per recuperare tutti i byte della proprietà, aggiornando cbSoFar per ognuno, fino a quando il campo fMoreExists del messaggio \_ \_ CPMFetchValueOut non è impostato su **FALSE.**

Il formato del messaggio CPMFetchValueIn che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Wid

\_cbSoFar

\_cbPropSpec

\_cbChunk

PropSpec (variabile)

...

\_padding (variabile)



 

**\_ wid:** intero senza segno a 32 bit contenente informazioni sull'ID documento che identifica il documento per cui deve essere recuperata una proprietà.

**\_ cbSoFar:** intero senza segno a 32 bit contenente il numero di byte trasferiti in precedenza per questa proprietà. DEVE essere impostato su 0x00000000 nel primo messaggio.

**\_ cbPropSpec:** intero senza segno a 32 bit contenente le dimensioni del campo PropSpec, in byte.

**\_ cbChunk:** intero senza segno a 32 bit contenente il numero massimo di byte che il mittente può accettare in un messaggio CPMFetchValueOut.

*Windows Comportamento: questo campo è impostato su 0x00004000 per tutte le versioni di Windows.*

**PropSpec:** struttura CFullPropSpec che specifica la proprietà da recuperare.

**\_ padding:** questo campo DEVE essere della lunghezza necessaria (da 0 a 3 byte) per riempire il messaggio su un multiplo di 4 byte di lunghezza. Il valore dei byte di spaziatura interna può essere qualsiasi valore arbitrario. Questo campo DEVE essere ignorato dal ricevitore.

### <a name="22320-cpmfetchvalueout"></a>2.2.3.20 CPMFetchValueOut

Il messaggio CPMFetchValueOut risponde a un messaggio CPMFetchValueIn con un valore di proprietà di una query precedente. Come specificato nella sezione 3.1.5.2.8, questo messaggio viene inviato dopo ogni messaggio CPMFetchValueIn fino al trasferimento di tutti i byte della proprietà.

Il formato del messaggio CPMFetchValueOut che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cbValue

\_fMoreExists

\_fValueExists

vType

vValue (variabile)



 

**\_ cbValue:** intero senza segno a 32 bit contenente le dimensioni totali, in byte in vValue.

**\_ fMoreExists:** valore booleano che indica se sono disponibili messaggi CPMFetchValueOut aggiuntivi. Se impostato su 0x00000001, sono presenti altri messaggi CPMFetchValueOut. Se impostato su 0x00000000, non sono disponibili altri messaggi CPMFetchValueOut.

**\_ fValueExists:** valore booleano che indica se è presente un valore per la proprietà. Se impostato su 0x00000001, esiste un valore per la proprietà . Se impostato su 0x00000000, un valore per la proprietà non esiste.

**vType:** valore dell'enumerazione VARENUM, vedere la sezione 2.2.1.1 per informazioni dettagliate, che descrivono il tipo della proprietà.

**vValue:** parte di una matrice di byte contenente una struttura SERIALIZEDPROPERTYVALUE come specificato nella sezione 2.2.1.32, dove l'offset dell'inizio della parte è il valore \_ di cbSoFar in CPMFetchValueIn. La lunghezza della parte, indicata dal campo cbValue, DEVE essere uguale al valore di \_ \_ cbChunk in CPMFetchValueIn se fMoreExists è impostato su 0x00000001 e DEVE essere minore o uguale al valore di \_ cbChunk in caso \_ contrario.

### <a name="22321-cpmgetnotify"></a>2.2.3.21 CPMGetNotify

Il messaggio CPMGetNotify richiede al client di ricevere una notifica delle modifiche al set di righe.

Il messaggio NON DEVE includere un corpo. solo l'intestazione del messaggio, come specificato nella Sezione 2.2.2, deve essere inviata.

### <a name="22322-cpmsendnotifyout"></a>2.2.3.22 CPMSendNotifyOut

Il messaggio CPMSendNotifyOut notifica al client una modifica ai risultati di una query.

Questo messaggio viene inviato solo quando si verifica una modifica. Il formato del messaggio CPMSendNotifyOut che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_watchNotify



 

**\_ watchNotify:** modifica alla query. DEVE essere uno dei valori seguenti:



| Valore                                     | Significato                                             |
|-------------------------------------------|-----------------------------------------------------|
| DBWATCHNOTIFY \_ ROWSCHANGED 0x00000001     | Il numero di righe nel set di righe della query è stato modificato. |
| DBWATCHNOTIFY \_ QUERYDONE 0x00000002       | La query è stata completata.                            |
| DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003 | La query è stata rieseguiti.                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a>2.2.3.23 CPMGetApproximatePositionIn

Il messaggio CPMGetApproximatePositionIn richiede la posizione approssimativa di un segnalibro in un capitolo. Il formato del messaggio CPMGetApproximatePositionIn che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_chapt

\_Bmk



 

**\_ hCursor:** valore a 32 bit che rappresenta il cursore di query ottenuto da CPMCreateQueryOut per il set di righe contenente il segnalibro.

**\_ chapt:** valore a 32 bit che rappresenta l'handle del capitolo contenente il segnalibro.

**\_ bmk:** valore a 32 bit che rappresenta l'handle del segnalibro per il quale recuperare la posizione approssimativa.

### <a name="22324-cpmgetapproximatepositionout"></a>2.2.3.24 CPMGetApproximatePositionOut

Il messaggio CPMGetApproximatePositionOut risponde a un messaggio CPMGetApproximatePositionIn che descrive la posizione approssimativa del segnalibro nel capitolo. Il formato del messaggio CPMGetApproximatePositionOut che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_numerator

\_denominator



 

**\_ numerator:** intero senza segno a 32 bit contenente il numero di riga del segnalibro nel set di righe. Se non sono presenti righe, questo campo DEVE essere impostato su 0x00000000.

**\_ denominator:** intero senza segno a 32 bit contenente il numero di righe nel set di righe.

### <a name="22325-cpmcomparebmkin"></a>2.2.3.25 CPMCompareBmkIn

Il messaggio CPMCompareBmkIn richiede un confronto tra due segnalibri in un capitolo.

Il formato del messaggio CPMCompareBmkIn che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_chapt

\_bmkFirst

\_bmkSecond



 

\_**hCursor:** valore a 32 bit che rappresenta l'handle del messaggio CPMCreateQueryOut per il set di righe contenente i segnalibri.

\_**chapt:** valore a 32 bit che rappresenta l'handle del capitolo contenente i segnalibri da confrontare.

\_**bmkFirst:** valore a 32 bit che rappresenta l'handle del primo segnalibro da confrontare.

\_**bmkSecond:** valore a 32 bit che rappresenta l'handle al secondo segnalibro da confrontare.

### <a name="22326-cpmcomparebmkout"></a>2.2.3.26 CPMCompareBmkOut

Il messaggio CPMCompareBmkOut risponde a un messaggio CPMCompareBmkIn con il confronto dei due segnalibri nel capitolo. Il formato del messaggio CPMCompareBmkOut che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_dwComparison



 

\_**dwComparison:** uno dei valori seguenti, che indica le posizioni relative dei due segnalibri nel capitolo.



| Valore                               | Significato                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| DBCOMPARE \_ LT 0x00000000            | Il primo segnalibro viene posizionato prima del secondo.               |
| DBCOMPARE \_ EQ 0x00000001            | Il primo segnalibro ha la stessa posizione del secondo.           |
| DBCOMPARE \_ GT 0x00000002            | Il primo segnalibro viene posizionato dopo il secondo.                |
| DBCOMPARE \_ NE 0x00000003            | Il primo segnalibro non ha la stessa posizione del secondo. |
| DBCOMPARE \_ NOTCOMPARABLE 0x00000004 | Il primo segnalibro non è confrontabile con il secondo.               |



 

### <a name="22327-cpmrestartpositionin"></a>2.2.3.27 CPMRestartPositionIn

Il messaggio CPMRestartPositionIn sposta la posizione di recupero di un cursore all'inizio del capitolo. Come specificato nella sezione 3.1.5.2.12, il server risponderà usando lo stesso messaggio, con i risultati della richiesta contenuti nel campo \_ stato dell'intestazione CISP.

Il formato del messaggio CPMRestartPositionIn che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor (facoltativo)

\_chapt (facoltativo)



 

**\_ hCursor:** valore a 32 bit che rappresenta l'handle, ottenuto da un messaggio CPMCreateQueryOut, che identifica la query per cui riavviare la posizione. Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.

**\_ chapt:** valore a 32 bit che rappresenta l'handle di un capitolo da cui recuperare le righe. Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.

### <a name="22328-cpmfreecursorin"></a>2.2.3.28 CPMFreeCursorIn

Il messaggio CPMFreeCursorIn richiede il rilascio di un cursore. Il formato del messaggio CPMFreeCursorIn che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor



 

**\_ hCursor:** valore a 32 bit che rappresenta l'handle del cursore dal messaggio CPMCreateQueryOut da rilasciare.

### <a name="22329-cpmfreecursorout"></a>2.2.3.29 CPMFreeCursorOut

Il messaggio CPMFreeCursorOut risponde a un messaggio CPMFreeCursorIn con i risultati del salvataggio di un cursore. Il formato del messaggio CPMFreeCursorOut che segue l'intestazione è:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cCursorsRemaining



 

**\_ cCursorsRemaining:** intero senza segno a 32 bit che indica il numero di cursori ancora in uso per la query.

### <a name="22330-cpmdisconnect"></a>2.2.3.30 CPMDisconnect

Il messaggio CPMDisconnect termina la connessione con il server

Il messaggio NON DEVE includere un corpo. deve essere inviata solo l'intestazione del messaggio, come specificato nella sezione 2.2.2.

### <a name="224-errors"></a>2.2.4 Errori

Tutti i messaggi del protocollo del servizio di indicizzazione del contenuto DEVONO 0x00000000 se l'operazione ha esito positivo; In caso contrario, restituiscono un codice di errore diverso da zero a 32 bit che può essere un valore HRESULT o NTSTATUS (vedere la sezione 1.8). Se un buffer è troppo piccolo per adattarsi a un risultato, deve essere restituito un codice di stato STATUS \_ INSUFFICIENT RESOURCES (0xC0000009A) e l'operazione non riuscita deve essere ritentata con un buffer più \_ grande.

Tutti gli altri valori di errore DEVONO essere considerati uguali.

Si noti che attualmente gli spazi di numerazione HRESULT e NTSTATUS non si sovrappongono se non con valori di significato identico, ma anche se dovevano essere conflitti in futuro, non causerebbe problemi di protocollo purché il valore per STATUS \_ RISORSE \_ INSUFFICIENTI rimane univoca, poiché tutti gli altri valori di errore vengono considerati uguali.

## <a name="3-protocol-details"></a>3 Dettagli del protocollo

-   [3.1 Dettagli server](#31-server-details)
-   [3.2 Dettagli client](#32-client-details)

Le richieste di messaggi CISP per l'esecuzione di query in remoto nei cataloghi del servizio di indicizzazione non richiedono alcuna sequenza specifica. È tuttavia consigliabile che il livello superiore rispetti una sequenza di messaggi significativa, ad esempio per i messaggi ricevuti da questa sequenza o con dati non validi, il server risponderà con un errore. Alcuni messaggi dipendono anche dal livello superiore che fornisce dati validi ricevuti nei messaggi in precedenza nella sequenza.

Una sequenza di messaggi tipica per una query semplice da un client a un computer remoto è illustrata nel diagramma seguente.

![sequenza di messaggi per query semplice](images/protocoldetails.jpg)

I messaggi rappresentati nel diagramma precedente rappresentano un subset di tutti i messaggi CISP usati per l'esecuzione di query su un catalogo del servizio di indicizzazione remoto.

### <a name="31-server-details"></a>3.1 Dettagli server

### <a name="311-abstract-data-model"></a>3.1.1 Modello di dati astratto

La sezione seguente specifica i dati e lo stato gestiti dal server CISP. I dati forniti qui sono per facilitare la spiegazione del comportamento del protocollo. Questa sezione non impone che le implementazioni siano conformi a questo modello, purché il comportamento esterno sia coerente con quello descritto in questo documento.

Un servizio di indicizzazione che implementa CISP DEVE mantenere gli elementi di dati astratti seguenti:

-   Elenco dei client connessi al server
-   Informazioni su ogni client, tra cui:
-   -   Versione del client (come indicato nel messaggio CPMConnectIn specificato nella sezione 2.2.3.6)
    -   Catalogo associato al client (tramite un messaggio CPMConnectIn)
    -   Proprietà client aggiuntive come specificato nella sezione 2.2.1.21.1.
    -   Query di ricerca del client
    -   Elenco di handle di cursore per la query e posizione nel set di risultati per ogni handle.
    -   Set corrente di associazioni
    -   Stato corrente della query che include (per ogni cursore):
    -   -   Numero di righe nel risultato della query
        -   Numeratore e denominatore del completamento delle query
        -   Ultimo numero di righe, segnalato dal messaggio CPMRatioFinishedOut più recente per questo cursore
        -   Se la query viene monitorata dal server per le modifiche nei risultati della query e se viene monitorata, cosa è cambiato nei risultati della query dall'ultima volta che è stata segnalata al client da CPMSendNotifyOut
        -   Elenco di handle di capitolo, serviti da questa query a un client.
        -   Elenco di handle di segnalibro per ogni cursore, servito da questa query a un client.

-   Stato corrente del servizio di indicizzazione, che può essere "non inizializzato", "in esecuzione" o "in fase di arresto". Si noti che la maggior parte del server di ora è in stato "in esecuzione". Di seguito è riportato il diagramma della macchina a stati per il server:

    ![diagramma della macchina a stati del server del servizio di indicizzazione](images/abstractdatamodel.jpg)

-   Informazioni per catalogo: numero di documenti indicizzati, dimensioni dell'indice, numero di chiavi univoche e così via (vedere la sezione 2.2.3.1 per l'elenco completo), stato (che corrisponde ai valori di dwNewState nella sezione 2.2.3.2).
-   Per ogni lingua supportata, un database di variazioni delle parole come descritto nella sezione 2.2.1.3.

### <a name="312-timers"></a>3.1.2 Timer

Non sono necessari timer di protocollo.

### <a name="313-initialization"></a>3.1.3 Inizializzazione

Al momento dell'inizializzazione, il server DEVE impostare lo stato su "non inizializzato" e avviare l'ascolto dei messaggi sul named pipe specificato nella sezione 1.9. Dopo aver eseguito qualsiasi altra inizializzazione interna, deve passare allo stato "in esecuzione".

### <a name="314-higher-layer-triggered-events"></a>3.1.4 Eventi attivati di livello più alto

Nessuno.

### <a name="315-message-processing-and-sequencing-rules"></a>3.1.5 Regole di elaborazione e sequenziazione dei messaggi

Ogni volta che si verifica un errore durante l'elaborazione di un messaggio inviato da un client, il server DEVE segnalare un errore al client come segue:

-   Arrestare l'elaborazione del messaggio inviato dal client
-   Rispondere con l'intestazione del messaggio (solo) del messaggio inviato dal client, mantenendo intatto \_ il campo msg.
-   Impostare il \_ campo dello stato sul valore del codice di errore.

Quando arriva un messaggio, il server DEVE controllare il valore del campo msg per verificare se è un tipo noto (vedere la sezione \_ 2.2.2). Se il tipo non è noto, deve segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).

Il server DEVE quindi convalidare il \_ valore del campo ulChecksum se il tipo di messaggio è uno dei seguenti:

-   CPMConnectIn (0x000000C8)
-   CPMCreateQueryIn (0x000000CA)
-   CPMSetBindingsIn (0x000000D0)
-   CPMGetRowsIn (0x000000CC)
-   CPMFetchValueIn (0x000000E4)

Per convalidare il valore del campo ulChecksum, il server DEVE controllare il valore specificato dal client nel campo \_ \_ iClientVersion del messaggio CPMConnectIn.

Se il campo iClientVersion non è impostato su 0x00000008 e il campo ulChecksum non è impostato su 0x00000000, il server DEVE segnalare un errore \_ \_ STATUS INVALID PARAMETER \_ \_ (0xC000000D). Il server NON DEVE convalidare il campo ulChecksum per i client. Impostare il campo iClientVersion su un valore minore \_ \_ di 0x00000008.

Se il valore del campo iClientVersionfield è 0x00000008 o superiore, il server DEVE convalidare che il campo ulChecksum sia stato calcolato come specificato nella sezione \_ \_ 3.2.4. Se il \_ valore ulChecksum non è valido, il server DEVE segnalare un errore STATUS \_ INVALID PARAMETER \_ (0xC000000D).

Successivamente, il server controlla in quale stato si trova. Se lo stato è "non inizializzato", il server DEVE segnalare un errore CI \_ E \_ NOT \_ INITIALIZED (0x8004180B). Se lo stato è "arresto in corso" il server DEVE segnalare un errore CI \_ E \_ SHUTDOWN (0x80041812).

Dopo che un'intestazione è stata determinata come valida e il server è in stato "in esecuzione", è necessario eseguire un'ulteriore elaborazione specifica del messaggio come specificato nelle sottosezioni seguenti.

### <a name="3151-remote-indexing-service-catalog-management"></a>3.1.5.1 Gestione del catalogo del servizio di indicizzazione remota

### <a name="31511-receiving-a-cpmcistateinout-request"></a>3.1.5.1.1 Ricezione di una richiesta CPMCiStateInOut

Quando il server riceve una richiesta di messaggio CPMCIStateInOut dal client, il server DEVE prima verificare se il client è in un elenco di client connessi. Se il client non è presente nell'elenco, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D). In caso contrario, deve rispondere al client con un messaggio CPMCIStateInOut, inserendo le informazioni sul catalogo associato del client come specificato nella sezione 2.2.3.1.

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a>3.1.5.1.2 Ricezione di una richiesta CPMSetCatStateIn

Quando il server riceve una richiesta di messaggio CPMSetCatStateIn dal client, il server DEVE eseguire le operazioni seguenti:

-   Verificare che il client abbia accesso amministrativo. Se il client non dispone di accesso amministrativo, il server DEVE segnalare un errore STATUS \_ ACCESS \_ DENIED (0xC0000022).
-   Se dwNewState non è uguale a CICAT ALL OPENED, modificare lo stato del catalogo specificato nel campo CatName come specificato dal \_ \_ campo \_ \_ dwNewState. Per altri dettagli, vedere la sezione 2.2.3.2. Se il server non individua un catalogo con il nome specificato nel campo CatName, il server DEVE restituire un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Rispondere al client con un messaggio CPMSetCatStateOut, in cui \_ dwOldState DEVE essere impostato sullo stato precedente del catalogo. Se dwNewState è uguale a CICAT ALL OPENED, il server DEVE controllare lo stato di tutti i cataloghi e, se tutti sono avviati, DEVE impostare dwOldState su 0x00000001 e in caso contrario impostare \_ \_ \_ \_ \_ dwOldState su 0x00000000.

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a>3.1.5.1.3 Ricezione di una richiesta CPMUpdateDocumentsIn

Quando il server riceve una richiesta di messaggio CPMUpdateDocumentsIn, il server DEVE eseguire le operazioni seguenti:

-   Controllare se il client è in un elenco di client connessi (a cui è associato un catalogo). Se il client non è presente nell'elenco, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Verificare che il client abbia accesso amministrativo. Se il client non dispone dell'accesso amministrativo al server, il server DEVE segnalare un errore DI ACCESSO NEGATO \_ \_ (0xC0000022).
-   Avviare il processo di indicizzazione del percorso specificato dal client, eseguendo un'analisi completa o incrementale, a seconda del valore del campo \_ flag nel messaggio CPMUpdateDocumentsIn. Se il percorso non è stato indicizzato in precedenza, deve essere aggiunto alla raccolta di percorsi indicizzati e viene eseguita un'analisi completa. Se viene specificato un valore non valido del campo flag, il server DEVE agire come se il flag fosse impostato su \_ \_ UPD \_ INIT ed eseguire un'analisi completa. Questa operazione DEVE essere eseguita nel catalogo associato al client.
-   Rispondere al client con l'intestazione del messaggio per CPMUpdateDocumentsIn e impostare il campo dello stato \_ sui risultati della richiesta.

### <a name="31514-receiving-a-cpmforcemergein-request"></a>3.1.5.1.4 Ricezione di una richiesta CPMForceMergeIn

Quando il server riceve una richiesta di messaggio CPMForceMergeIn, il server DEVE eseguire le operazioni seguenti:

-   Controllare se il client è in un elenco di client connessi (a cui è associato un catalogo). Se il client non è presente nell'elenco, il server deve segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Verificare che il client abbia accesso amministrativo. Se il client non dispone di accesso amministrativo, il server DEVE segnalare un errore STATUS \_ ACCESS \_ DENIED (0xC0000022).
-   Avviare qualsiasi processo di manutenzione necessario per migliorare le prestazioni delle query in un catalogo, associato al client.
-   Rispondere al client con un'intestazione del messaggio per CPMForceMergeIn e impostare il campo dello stato sui \_ risultati della richiesta.

Si noti che il processo di manutenzione è asincrono e può continuare dopo che il client riceve il messaggio di risposta. Questo processo non influisce direttamente sul protocollo in alcun modo (ad esempio, il tempo di risposta).

### <a name="3152-remote-indexing-service-querying"></a>3.1.5.2 Query del Servizio di indicizzazione remota

### <a name="31521-receiving-a-cpmconnectin-request"></a>3.1.5.2.1 Ricezione di una richiesta CPMConnectIn

Quando il server riceve una richiesta CPMConnectIn da un client, il server DEVE eseguire le operazioni seguenti:

-   Controllare se il client è presente nell'elenco dei client connessi. In questo caso, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Verifica se il catalogo specificato esiste e non si trova nello stato arrestato. Se non è questo il caso, il server deve segnalare un errore CI \_ E \_ NO CATALOG \_ (0x8004181D).
-   Aggiungere il client all'elenco dei client connessi.
-   Associare il catalogo al client.
-   Archiviare le informazioni passate nel messaggio CPMConnectIn ,ad esempio il nome del catalogo, la versione del client e così via, nello stato client.
-   Rispondere al client con un messaggio CPMConnectOut.

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a>3.1.5.2.2 Ricezione di una richiesta CPMCreateQueryIn

Quando il server riceve una richiesta di messaggio CPMCreateQueryIn da un client, il server DEVE eseguire le operazioni seguenti:

-   Controllare se il client è presente nell'elenco dei client connessi. In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Controllare se al client è già associata una query. In questo caso, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Controllare se il catalogo associato al client è nello stato che consente l'elaborazione della query (CICAT \_ READONLY o CICAT \_ WRITABLE). In caso contrario, il server DEVE segnalare un errore QUERY \_ S \_ NO QUERY \_ (0x8004160C).
-   Analizzare il set di restrizioni, i criteri di ordinamento e i raggruppamenti specificati nella query. Se il server rileva un errore, deve segnalare un errore appropriato. Se questo passaggio ha esito negativo per qualsiasi altro motivo, il server DEVE segnalare l'errore rilevato. Per informazioni sugli errori di query del servizio di indicizzazione, \[ vedere MSDN-QUERYERR. \]
-   Salvare la query di ricerca nello stato per il client.
-   Eseguire le operazioni di preparazione necessarie per rendere disponibili le righe a un client e associare la query agli handle di cursore appropriati, a seconda delle informazioni passate nel messaggio CPMCreateQueryIn.
-   Aggiungere tali handle all'elenco di handle di cursore del client e inizializzare elenchi di handle di capitolo e segnalibri.
-   Inizializzare l'elenco di handle di capitolo per ogni cursore nella query al database \_ NULL \_ HCHAPTER
-   Inizializzare l'elenco di handle di segnalibro per ogni cursore nella query su un set di DBBMK \_ FIRST e DBBMK \_ LAST.
-   Contrassegnare la query come non monitorata per le modifiche.
-   Inizializzare il numero di righe sul numero di righe attualmente calcolato (che può essere 0 se l'esecuzione della query non è stata avviata o un numero se la query è in un processo di esecuzione) e inizializzare il numeratore e il denominatore del completamento della query.
-   Rispondere al client con un messaggio CPMCreateQueryOut.

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a>3.1.5.2.3 Ricezione di una richiesta CPMGetQueryStatusIn

Quando il server riceve una richiesta di messaggio CPMGetQueryStatusIn da un client, il server DEVE eseguire le operazioni seguenti:

-   Controllare se al client è associata una query. In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Controllare se l'handle del cursore si trova in un elenco di handle di cursore del client. In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).
-   Preparare un messaggio CPMGetQueryStatusOut. Il server DEVE recuperare lo stato della query corrente e impostarlo nel campo \_ QStatus (vedere 2.2.3.11 per i valori possibili). Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare un errore.
-   Rispondere al client con il messaggio CPMGetQueryStatusOut.

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a>3.1.5.2.4 Ricezione di una richiesta CPMGetQueryStatusExIn

Quando il server riceve una richiesta di messaggio CPMGetQueryStatusExIn da un client, il server DEVE eseguire le operazioni seguenti:

-   Controllare se al client è associata una query. In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Controllare se l'handle di cursore passato è in un elenco di handle di cursore del client. In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).
-   Preparare un messaggio CPMGetQueryStatusExOut. Il server DEVE recuperare lo stato corrente della query e lo stato della query e impostare QStatus (vedere 2.2.3.11 per i valori \_ possibili), dwRatioFinishedDenominator e \_ dwRatioFinishedNumerator rispettivamente. Deve quindi impostare il numero di righe nei risultati della query su \_ cRowsTotal. Se questo passaggio ha esito negativo per qualsiasi motivo, il server DEVE segnalare che si è verificato un errore.
-   Recuperare informazioni sul catalogo del client e \_ compilare cFilteredDocuments e \_ cDocumentsToFilter. Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare che si è verificato un errore.
-   Recuperare la posizione del segnalibro indicato dall'handle nel campo bmk e compilare il campo iRowBmk rimanente nel messaggio \_ \_ CPMGetQueryStatusExOut. Se questo passaggio ha esito negativo per qualsiasi motivo, il server DEVE segnalare che si è verificato un errore.
-   Rispondere al client con il messaggio CPMGetQueryStatusExOut.

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a>3.1.5.2.5 Ricezione di una richiesta CPMRatioFinishedIn

Quando il server riceve una richiesta di messaggio CPMRatioFinishedIn da un client, il server DEVE eseguire le operazioni seguenti:

-   Controllare se al client è associata una query. In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Controllare se l'handle di cursore passato è presente nell'elenco degli handle di cursore del client. In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).
-   Preparare un messaggio CPMRatioFinishedOut. Il server DEVE recuperare lo stato della query del client e compilare i campi \_ ulNumerator, \_ ulDenominator \_ e cRows. Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare che si è verificato un errore.
-   Se cRows è uguale all'ultimo numero segnalato di righe per questa query, impostare \_ fNewRows su 0x00000000, in caso contrario impostarlo su \_ 0x00000001.
-   Aggiornare l'ultimo numero segnalato di righe per questa query al valore \_ di cRows.
-   Rispondere al client con il messaggio CPMRatioFinishedOut.

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a>3.1.5.2.6 Ricezione di una richiesta CPMSetBindingsIn

Quando il server riceve una richiesta di messaggio CPMSetBindingsIn da un client, il server DEVE eseguire le operazioni seguenti:

-   Controllare se al client è associata una query. In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Controllare se l'handle di cursore passato è presente nell'elenco degli handle di cursore del client. In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).
-   Verificare che le informazioni sulle associazioni siano valide(ad esempio, la colonna specifica almeno il valore, la lunghezza o lo stato da restituire; nessuna sovrapposizione nelle associazioni per valore, lunghezza o stato; e valore, lunghezza e stato si adattano alle dimensioni della riga specificate) e se non segnala un errore \_ DB E \_ BADBINDINFO (0x80040E08).
-   Salvare le informazioni di associazione associate alle colonne specificate nel campo aColumns. Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare che si è verificato un errore.
-   Rispondere al client con un'intestazione del messaggio (solo) con msg impostato su CPMSetBindingsIn e stato impostato sui risultati \_ \_ dell'associazione specificata.

### <a name="31527-receiving-a-cpmgetrowsin-request"></a>3.1.5.2.7 Ricezione di una richiesta CPMGetRowsIn

Quando il server riceve una richiesta di messaggio CPMGetRowsIn da un client, il server DEVE eseguire le operazioni seguenti:

-   Controllare se al client è associata una query. In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Controllare se l'handle di cursore passato è in athelist degli handle di cursore del client. In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).
-   Controllare se il client ha un set corrente di associazioni. In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).
-   Preparare un messaggio CPMGetRowsOut. Il server DEVE posizionare il cursore nei risultati della query come indicato dalla descrizione della ricerca. Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare che si è verificato un errore.
-   Recuperare tutte le righe che si adattano a un buffer, le cui dimensioni sono indicate da cbReadBuffer, ma non più di quanto indicato \_ da \_ cRowsToTransfer. Quando si recuperano righe, il server DEVE confrontare il tipo di valore della proprietà di ogni colonna selezionata con il tipo specificato nel set corrente di associazioni del client (sezione 3.1.1). Se il tipo nell'associazione non è VT VARIANT, il server DEVE tentare di convertire il valore della proprietà della colonna \_ in tale tipo. In caso contrario, se il flag DBPROP USEEXTENDEDDBTYPES è impostato nel set di proprietà DBPROPSET QUERYEXT del client o se il valore della proprietà della colonna non è un \_ tipo VT VECTOR, il valore della proprietà DEVE essere restituito nel \_ \_ tipo normale. In caso contrario, il server deve tentare di convertirlo in un tipo VT ARRAY come \_ \_ \_ segue: VT \_ I8, VT \_ UI8, VT FILETIME e gli elementi di matrice \_ CLSID VT \_ non possono essere convertiti e hanno invece esito negativo. Gli elementi della matrice \_ VT LPSTR e VT LPWSTR DEVONO essere convertiti in VT BSTR. Gli elementi di matrice di tutti gli altri tipi \_ \_ DEVONO rimanere invariati. Infine, se le colonne di riga contengono handle di capitolo o segnalibri, il server DEVE aggiornare gli elenchi corrispondenti. Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare che si è verificato un errore.
-   Archiviare il numero effettivo di righe recuperate in \_ cRowsReturned.
-   Copiare il campo della descrizione della ricerca e del capitolo da CPMGetRowsIn in un messaggio CPMGetRowsOut da inviare.
-   Archiviare le righe recuperate nel campo Righe (vedere la nota sul byte di stato sotto e la sezione 2.2.3.16 nella struttura del campo Righe).
-   Rispondere al client con il messaggio CPMGetRowsOut.

Nota sul campo byte di stato:

Se StatusUsed è impostato su 0x01 nella colonna CTableColumn del messaggio CPMSetBindingIn per la colonna, il server DEVE impostare il byte di stato (che si trova in StatusOffset dall'inizio della riga) per questa colonna su uno dei valori seguenti:



| Valore | Significato        |
|-------|----------------|
| 0x00  | StatusOK       |
| 0x01  | StatusDeferred |
| 0x02  | StatusNull     |



 

Se il valore della proprietà è assente per questa riga, il server DEVE impostare il byte di stato su StatusNull. Se il valore è troppo grande per essere trasferito nel messaggio CPMGetRowsOut, il server DEVE impostare il byte di stato su StatusDeferred. In caso contrario, il server DEVE impostare il byte di stato su StatusOK.

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a>3.1.5.2.8 Ricezione di una richiesta CPMFetchValueIn

Quando il server riceve una richiesta di messaggio CPMFetchValueIn da un client, il server DEVE eseguire le operazioni seguenti:

-   Controllare se al client è associata una query. In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Preparare un messaggio CPMFetchValueOut. Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare un errore.
-   Trovare il documento indicato dal campo wid e verificare se l'ID proprietà per questo documento (in seguito indicato come "valore della proprietà") indicato dalla struttura PropSpec è disponibile per \_ questo client. Se questo valore non è disponibile, il server DEVE impostare fValueExists su 0x00000000 e in caso contrario impostare \_ \_ fValueExists su 0x00000001. Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare un errore.
-   Se \_ fValueExists è uguale a 0x00000001 il server DEVE eseguire le operazioni seguenti:
-   -   Serializzare il valore della proprietà in una struttura SERIALIZEDPROPERTYVALUE e copiare, a partire \_ dall'offset cbSoFar, al massimo byte cbChunk (ma non oltre la fine della proprietà serializzata) nel campo \_ vValue. Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare un errore.
    -   Impostare \_ cbValue sul numero di byte copiati nel passaggio precedente.
    -   Impostare vType sul tipo di proprietà del valore della proprietà.
    -   Se la lunghezza della proprietà serializzata è maggiore di \_ cbSoFar aggiunta a \_ cbValue, impostare fMoreExists su 0x00000001, in caso contrario impostarla su \_ 0x00000000.

-   Rispondere al client con il messaggio CPMFetchValueOut

### <a name="31529-receiving-a-cpmgetnotify-request"></a>3.1.5.2.9 Ricezione di una richiesta CPMGetNotify

Quando il server riceve un messaggio CPMGetNotify da un client, il server DEVE eseguire le operazioni seguenti:

-   Controllare se al client è associata una query. In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Se non sono state apportate modifiche al set di risultati della query dopo l'ultimo messaggio CPMSendNotifyOut per questo client o se la query non è attualmente monitorata per le modifiche nel set di risultati, il server DEVE rispondere con il messaggio CPMGetNotify e iniziare a monitorare la query per le modifiche nel set di risultati. Se in un secondo momento si verifica una modifica nel set di risultati della query, il server DEVE inviare esattamente un messaggio CPMSendNotifyOut al client e DEVE specificare la modifica nel campo \_ watchNotify.
-   Se sono state apportate modifiche al set di risultati della query dall'ultimo messaggio CPMSendNotifyOut, il server DEVE rispondere con CPMSendNotifyOut e DEVE specificare la modifica nel campo \_ watchNotify. Si noti che, nel caso di molte modifiche ai risultati della query, DBWATCHNOTIFY ROWSCHANGED ha la priorità,ad esempio, se la query è stata eseguita di nuovo e quindi il numero di righe modificate e la query è stata eseguita di nuovo, l'evento segnalato sarà \_ DBWATCHNOTIFY \_ ROWSCHANGED.

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a>3.1.5.2.10 Ricezione di una richiesta CPMGetApproximatePositionIn

Quando il server riceve una richiesta di messaggio CPMGetApproximatePositionIn dal client, il server DEVE eseguire le operazioni seguenti:

-   Controllare se al client è associata una query. In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Controllare se l'handle del cursore, l'handle del capitolo e l'handle del segnalibro passati si trova negli elenchi corrispondenti. In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).
-   Trovare una riga associata all'handle del segnalibro nei risultati della query e approssimare la posizione della riga nel set di righe, a cui fa riferimento l'handle del capitolo, e determinare il numeratore e il denominatore per la posizione. Si noti che quando l'handle del capitolo è DB \_ NULL HCHAPTER, il capitolo corrispondente \_ è il set di righe principale della query. Se per qualsiasi motivo questo passaggio non riesce, il server DEVE segnalare un errore.
-   Rispondere al client con un messaggio CPMFetchValueOut.

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a>3.1.5.2.11 Ricezione di una richiesta CPMCompareBmkIn

Quando il server riceve una richiesta di messaggio CPMCompareBmkIn dal client, il server DEVE eseguire le operazioni seguenti:

-   Controllare se al client è associata una query. In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Controllare se l'handle del cursore, l'handle del capitolo e gli handle di segnalibro passati si trova negli elenchi corrispondenti. In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).
-   Preparare un messaggio CPMCompareBmkOut.
-   Se gli handle dei segnalibri sono uguali, \_ dwComparison MUST è impostato su DBCOMPARE \_ EQ.
-   In caso contrario, se uno degli handle di segnalibro è DBBMK FIRST o \_ DBBMK \_ LAST, \_ dwComparison DEVE essere impostato su DBCOMPARE \_ NE.
-   In caso contrario, il server DEVE eseguire le operazioni seguenti:
-   -   Trovare le righe a cui fa riferimento ogni handle di segnalibro nei risultati della query
    -   Se una delle righe non è presente nel capitolo indicato dall'handle del capitolo in CPMCompareBmkIn, \_ dwComparison DEVE essere impostato su DBCOMPARE \_ NOTCOMPARABLE.
    -   In caso contrario, quando entrambe le righe sono nello stesso capitolo, il server DEVE approssimare una posizione approssimativa di tali righe nel set di righe a cui fa riferimento l'handle del capitolo. DEVE quindi confrontare i valori di posizione e impostare dwComparison su DBCOMPARE LT se la posizione della prima riga è inferiore alla posizione della seconda riga; in caso \_ \_ \_ contrario, dwComparison DEVE essere impostato su DBCOMPARE \_ GT.

-   Rispondere al client con il messaggio CPMCompareBmkOut compilato.

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a>3.1.5.2.12 Ricezione di una richiesta CPMRestartPositionIn

Quando il server riceve la richiesta di messaggio CPMRestartPositionIn dal client, il server DEVE eseguire le operazioni seguenti:

-   Controllare se al client è associata una query. In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Controllare se l'handle del cursore e l'handle del capitolo passati si trova negli elenchi corrispondenti. In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).
-   Spostare il cursore all'inizio del capitolo, identificato dall'handle del capitolo. Si noti che quando l'handle del capitolo è DB \_ NULL HCHAPTER, il capitolo corrispondente \_ è il set di righe principale della query. Se per qualsiasi motivo questo passaggio non riesce, il server DEVE segnalare un errore.
-   Rispondere al client con un messaggio CPMRestartPositionIn.

### <a name="315213-receiving-a-cpmfreecursorin-request"></a>3.1.5.2.13 Ricezione di una richiesta CPMFreeCursorIn

Quando il server riceve una richiesta di messaggio CPMFreeCursorIn dal client, il server DEVE eseguire le operazioni seguenti:

-   Controllare se al client è associata una query. In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Controllare se l'handle di cursore passato è presente nell'elenco degli handle di cursore del client. In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).
-   Rilasciare il cursore e le risorse associate (vedere la sezione 3.1.1 per l'elenco completo) per questo handle di cursore.
-   Rimuovere il cursore dall'elenco di cursori per il client.
-   Rispondere con un messaggio CPMFreeCursorOut, impostando il campo \_ cCursorsRemaining con il numero di cursori rimanenti. nell'elenco di questo client.
-   Se non sono presenti altri cursori per questo client, il server DEVE rilasciare la query e le risorse associate (vedere la sezione 3.1.1).

### <a name="315214-receiving-a-cpmdisconnect-request"></a>3.1.5.2.14 Ricezione di una richiesta CPMDisconnect

Quando il server riceve una richiesta di messaggio CPMDisconnect dal client, il server DEVE rimuovere il client dall'elenco dei client connessi e rilasciare tutte le risorse associate al client.

### <a name="316-timer-events"></a>3.1.6 Eventi timer

Nessuno.

### <a name="317-other-local-events"></a>3.1.7 Altri eventi locali

Quando il server viene arrestato, deve prima passare allo stato "arresto in corso". Deve quindi arrestare l'ascolto della pipe, eseguire qualsiasi altra attività di arresto specifica dell'implementazione e quindi passare allo stato "arrestato".

### <a name="32-client-details"></a>3.2 Dettagli client

### <a name="321-abstract-data-model"></a>3.2.1 Modello di dati astratto

Nella sezione seguente vengono specificati i dati e lo stato gestiti dal client Content Indexing Service Protocol. I dati forniti sono per facilitare la spiegazione del comportamento del protocollo. Questa sezione non impone che le implementazioni siano conformi a questo modello, purché il comportamento esterno sia coerente con quello descritto in questo documento.

Un client ha lo stato astratto seguente:

-   **Last Message Sent**: copia dell'ultimo messaggio inviato al server.
-   **Valore della proprietà** corrente: valore parziale di una proprietà "posticipata", in corso di recupero.
-   **Byte correnti ricevuti:** numero di byte ricevuti finora per il valore della proprietà corrente.
-   **Stato della connessione named pipe:** connessione al server

### <a name="322-timers"></a>3.2.2 Timer

Non sono necessari timer di protocollo.

### <a name="323-initialization"></a>3.2.3 Inizializzazione

Non viene eseguita alcuna azione fino a quando non viene ricevuta una richiesta di livello superiore.

### <a name="324-higher-layer-triggered-events"></a>3.2.4 Higher-Layer eventi attivati

Quando una richiesta viene ricevuta da un livello superiore, il client DEVE creare una connessione named pipe al server, usando i dettagli specificati nella sezione 2.1. Se non è possibile eseguire questa operazione, la richiesta di livello superiore DEVE non essere riuscita. Ciò significa che, in caso di errore di connessione, è responsabilità del livello superiore riprovare, se necessario.

Un'intestazione DEVE essere precompilata con i campi impostati come specificato nella sezione 2.2.2.

Per i messaggi specificati come che richiedono un checksum diverso da zero, il \_ valore ulChecksum DEVE essere calcolato come segue:

1.  Il contenuto del messaggio dopo il campo ulReserved2 nell'intestazione del messaggio DEVE essere interpretato come una sequenza di interi \_ a 32 bit. Il client DEVE calcolare la somma dei valori numerici specificati da questi numeri interi.
2.  Calcolare l'XOR bit per bit di questo valore con 0x59533959.
3.  Sottrae il valore specificato \_ da msg dal valore restituito dall'operatore XOR bit per bit.

### <a name="3241-remote-indexing-service-catalog-management"></a>3.2.4.1 Gestione del catalogo del servizio di indicizzazione remota

Ogni messaggio viene attivato da una richiesta dal livello superiore. Non esiste alcuna sequenza di messaggi applicata dal client per le richieste di messaggi CISP per la gestione remota dei cataloghi, ma (ad eccezione di un messaggio CPMSetCatStateIn) il server risponderà con esito positivo solo se il client si connetteva in precedenza tramite un messaggio CPMConnectIn.

### <a name="32411-sending-a-cpmcistateinout-request"></a>3.2.4.1.1 Invio di una richiesta CPMCiStateInOut

In genere, il livello superiore chiede al client del protocollo di inviare un messaggio CPMCiStateInOut quando sono necessarie informazioni sui servizi di indicizzazione nel server.

Quando viene richiesto di inviare questo messaggio, il client DEVE eseguire le operazioni seguenti:

-   Inviare un messaggio CPMCiStateInOut come specificato nella sezione 2.2.3.1 al server.
-   Attendere la ricezione del messaggio CPMCiStateInOut dal server, rimuovendo automaticamente tutti gli altri messaggi.
-   Segnalare il valore del campo dello stato della risposta e, se l'operazione ha avuto esito positivo, la struttura informativo \_ torna al livello superiore.

### <a name="32412-sending-a-cpmsetcatstatein-request"></a>3.2.4.1.2 Invio di una richiesta CPMSetCatStateIn

In genere, il livello superiore chiede al client del protocollo di inviare un messaggio CPMSetCatStateIn quando sono necessarie informazioni su un catalogo o su tutti i cataloghi. Per questo messaggio, il livello superiore deve fornire al client del protocollo un valore \_ per dwNewState e, se necessario, il nome del catalogo.

Quando viene richiesto di inviare questo messaggio, il client DEVE eseguire le operazioni seguenti:

-   Inviare un messaggio CPMSetCatStateIn come specificato nella versione 2.2.3.2 al server.
-   Attendere di ricevere un messaggio CPMSetCatStateOut dal server, rimuovendo automaticamente tutti gli altri messaggi.
-   Segnalare il valore del campo status della risposta e, se l'operazione ha avuto esito \_ positivo, \_ dwOldState di nuovo al livello superiore.

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a>3.2.4.1.3 Invio di una richiesta CPMUpdateDocumentsIn

Il livello superiore richiede in genere di inviare questo messaggio quando è necessario aggiornare i documenti nel percorso esistente o aggiungere un nuovo percorso di file all'indice. Il livello superiore è quindi quello di fornire il percorso e il tipo di un'analisi, specificata come nella sezione 2.2.3.4, in cui un aggiornamento incrementale o completo è destinato ai percorsi esistenti e la nuova inizializzazione è destinata a nuovi percorsi.

Per soddisfare la richiesta di livello superiore, il client DEVE eseguire le operazioni seguenti:

-   Inviare un messaggio CPMUpdateDocumentsIn come specificato nella sezione 2.2.3.4 al server.
-   Attendere la ricezione del messaggio CPMUpdateDocumentsIn dal server, rimuovendo automaticamente tutti gli altri messaggi.
-   Segnalare il valore del \_ campo di stato della risposta al livello superiore.

### <a name="32414-sending-a-cpmforcemergein-request"></a>3.2.4.1.4 Invio di una richiesta CPMForceMergeIn

In genere, il livello superiore richiede di inviare questo messaggio quando è necessario migliorare le prestazioni delle query o fa parte della manutenzione pianificata del servizio di indicizzazione.

Per gestire il livello superiore, il client DEVE eseguire le operazioni seguenti:

-   Inviare il messaggio CPMForceMergeIn come specificato dalla sezione 2.2.3.5 al server.
-   Attendere la ricezione di un messaggio CPMUpdateDocumentsIn dal server, rimuovendo automaticamente tutti gli altri messaggi.
-   Segnalare il valore del \_ campo di stato della risposta al livello superiore.

### <a name="3242-remote-indexing-service-catalog-query-messages"></a>3.2.4.2 Messaggi di query del catalogo del servizio di indicizzazione remota

Ad eccezione di CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, esiste una relazione uno-a-uno tra i messaggi CISP e le richieste di livello superiore. Per le due eccezioni indicate in precedenza, possono essere generati più messaggi dal client per soddisfare i requisiti di dimensione o per recuperare una proprietà completa. Il livello superiore tiene in genere traccia di tutte le informazioni specifiche della query (ad esempio gli handle di cursore aperti, i valori validi per gli handle di segnalibro e capitolo, i valori wid per i valori delle proprietà posticipate e così via) e tiene traccia anche se il client si trova in uno stato connesso, ma questo non viene applicato in alcun modo dal client.

A scopo illustrativo, la parte client del diagramma nella sezione 3 illustra questa sequenza per una semplice query del servizio di indicizzazione.

### <a name="32421-sending-a-cpmconnectin-request"></a>3.2.4.2.1 Invio di una richiesta CPMConnectIn

Questo messaggio è in genere la prima richiesta dal livello superiore (come se il client non fosse connesso, il server avrà esito negativo per la maggior parte dei messaggi ad eccezione di CPMSetCatStateIn). Il livello superiore fornisce al client del protocollo le informazioni necessarie per la connessione.

Per soddisfare il livello superiore, il client DEVE eseguire le operazioni seguenti:

-   Compilare il messaggio usando le informazioni fornite dal client di livello superiore (vedere la sezione 2.2.3.6) in \_ iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 e aPropertySet.
-   Impostare \_ fClientIsRemote, \_ cbBlob, \_ cbBlob2, cPropSet e cExtPropSet come specificato nella versione 2.2.3.6.
-   Impostare il checksum nel \_ campo ulChecksum.
-   Inviare il messaggio CPMConnectIn al server.
-   Attendere la ricezione di un messaggio CPMConnectOut dal server, rimuovendo automaticamente tutti gli altri messaggi.
-   Segnalare il valore del campo status della risposta e, se ha avuto esito \_ positivo, \_ serverVersion torna al livello superiore.

Per scopi informativi, è previsto che i livelli superiori eseereranno in genere le azioni seguenti al completamento della connessione, ma queste non vengono applicate dal client CISP:

-   Usare i messaggi di gestione del catalogo del servizio di indicizzazione remota per le attività amministrative
-   Usare una richiesta CPMCreateQueryIn per creare una query di ricerca allo scopo di recuperare i risultati dal catalogo.

### <a name="32422-sending-a-cpmcreatequeryin-request"></a>3.2.4.2.2 Invio di una richiesta CPMCreateQueryIn

Il livello superiore in genere fornirà informazioni per la creazione della query dopo la connessione del client del protocollo. Il livello superiore fornisce al client un set di restrizioni, un set di colonne, regole di ordinamento e set di categorizzazione (ognuna delle quali può essere omessa), proprietà del set di righe e struttura del mapper di ID proprietà.

Quando questa richiesta viene ricevuta da un livello superiore, il client DEVE eseguire le operazioni seguenti:

-   Preparare un oggetto CPMCreateQueryOut come indicato di seguito.
-   -   Se è presente un set di colonne, impostare CColumnsSetPreset su 0x01 e compilare il campo ColumnsSet.
    -   Se sono presenti restrizioni, impostare CRestrictionPresent su 0x01 e compilare il campo Restrizione.
    -   Se è presente un set di ordinamento, compilare il campo SortSet.
    -   Se è presente un set di categorizzazione, impostare CSortSetPresent su 0x01 e compilare il campo CategorizationSet.
    -   Impostare il resto dei campi come specificato nella versione 2.2.3.8

-   Calcolare \_ il campo ulCheckSum nell'intestazione.
-   Inviare il messaggio CPMCreateQueryIn al server.
-   Attendere la ricezione del messaggio CPMCreateQueryOut (vedere i dettagli nella sezione 3.2.5.1.1), rimuovendo automaticamente tutti gli altri messaggi.
-   Segnalare il valore del campo di stato della risposta e, se ha avuto esito positivo, la matrice di handle di cursore e i valori booleani informativi (come specificato \_ nella 2.2.3.9) di nuovo al livello superiore.

### <a name="32423-sending-a-cpmsetbindingsin-request"></a>3.2.4.2.3 Invio di una richiesta CPMSetBindingsIn

In genere, il livello superiore imposta le associazioni per ogni colonna da restituire nelle righe quando ha già un handle di cursore valido (dopo aver ricevuto correttamente CPMCreateQueryOut, vedere la sezione 3.2.5.1.1). Maggiore è il valore previsto per fornire una matrice di strutture CTableColumn, come specificato nella Sezione 2.2.4.31, per il campo aColumns e un handle di cursore valido.

Quando questa richiesta viene ricevuta dal livello superiore, il client DEVE eseguire le operazioni seguenti:

-   Calcolare il numero di strutture CTableColumn nella matrice aColumns e impostare il campo cColumns su questo valore.
-   Calcolare le dimensioni totali in byte dei campi cColumns e aColumns e impostare il campo \_ cbBindingDesc su questo valore.
-   Impostare i campi specificati nel messaggio CPMSetBindingsIn ai valori forniti dal livello applicazione superiore. Impostare il \_ campo ulChecksum sul valore calcolato come specificato nella Sezione 3.2.5.
-   Inviare il messaggio CPMSetBindignsIn completato al server.
-   Attendere la ricezione di un messaggio CPMSetBindingsIn dal server, rimuovendo altri messaggi.
-   Indicare lo stato \_ dal campo di stato della risposta al livello superiore.

Per scopi informativi, è previsto che i livelli superiori in genere richiedono a un client di inviare un messaggio CPMGetRowsIn, ma questo non viene applicato dal protocollo del servizio di indicizzazione del contenuto.

### <a name="32424-sending-a-cpmgetrowsin-request"></a>3.2.4.2.4 Invio di una richiesta CPMGetRowsIn

Quando il livello superiore sta per ricevere informazioni sulle righe, fornirà al client del protocollo un cursore e un handle di capitolo validi e fornirà una descrizione di ricerca appropriata. In genere, è previsto che un livello superiore esegui questa operazione quando ha un cursore e/o un handle di capitolo validi e le associazioni sono state impostate con il messaggio CPMSetBindingsIn. Per accedere al set di righe in un capitolo, il livello superiore è usare l'handle di capitolo ricevuto dal server in un messaggio CPMGetRowsOut precedente.

Quando questa richiesta viene ricevuta dal livello superiore, il client DEVE eseguire le operazioni seguenti:

-   Determinare il valore intero senza segno da specificare per il \_ campo cbReadBuffer. Per determinare questo valore, il client DEVE prendere il valore massimo dagli elementi seguenti:
-   -   Mille volte il valore del campo \_ c RowsToTransfer.
    -   Valore di \_ cbRowWidth, arrotondato al multiplo di 512 byte più vicino.
    -   Prendere il valore più alto di questi due valori, fino al limite di 16.000.
    -   Nei casi in cui una singola riga è maggiore di 16.000, il server non può restituire risultati a questa query.

Specificare una base client per i dati di riga di dimensioni variabili nello spazio indirizzi del client nel \_ campo ulClientBase.

*Windows Comportamento: per un client a 32 bit che parla con un server a 32 bit o un client a 64 bit che parla con un server a 64 bit, questo valore è impostato su un indirizzo di memoria del buffer ricevente nel processo dell'applicazione. Ciò consente ai puntatori ricevuti nel campo Rows di CPMGetRowsOut di essere puntatori di memoria corretti in un processo dell'applicazione client. In caso contrario, è impostato su 0x00000000.*

-   Calcolare le dimensioni della descrizione della ricerca e impostarla nel \_ campo cbSeek.
-   Impostare il valore di cbReserved (che fungerebbe da offset per l'inizio delle righe) sul valore \_ cbSeek più 0x14.
-   Inviare un messaggio CPMConnectIn come specificato nella versione 2.2.3.15 al server.

### <a name="32425-sending-a-cpmfetchvaluein-request"></a>3.2.4.2.5 Invio di una richiesta CPMFetchValueIn

Se il client riceve una risposta CPMGetRowsOut dal server con il campo Status della colonna impostato su StatusDeferred (0x01), significa che il valore della proprietà non è stato incluso nel campo Rows del messaggio CPMGetRowsOut. In questo caso il livello superiore richiede in genere al client del protocollo di recuperare il valore tramite il messaggio CPMFetchValueIn e fornisce il valore PropSpec e wid per una proprietà posticipata, che il client del protocollo DEVE usare nel primo messaggio \_ CPMFetchValueIn.

Se si tratta del primo messaggio CPMFetchValueIn inviato dal client per richiedere la proprietà specificata, il client DEVE eseguire le operazioni seguenti:

-   Impostare tutti i campi in un messaggio come specificato nella sezione 2.2.3.19.
-   Impostare \_ cbSoFar su 0x00000000.
-   Impostare Byte correnti ricevuti su 0.
-   Inviare il messaggio CPMFetchValueIn al server.

### <a name="32426-sending-a-cpmfreecursorin-request"></a>3.2.4.2.6 Invio di una richiesta CPMFreeCursorIn

Quando il livello superiore non usa più la query di ricerca, può rilasciare le risorse nel server richiedendo al client di inviare un messaggio CPMFreeCursorIn.

Quando questa richiesta viene ricevuta, il client DEVE inviare un messaggio CPMFreeCursorIn come specificato in 2.2.3.28 al server, contenente l'handle specificato dal livello superiore.

### <a name="32427-sending-a-cpmdisconnect-message"></a>3.2.4.2.7 Invio di un messaggio CPMDisconnect

Se il livello superiore non dispone di altre query per il servizio di indicizzazione, per liberare più risorse del server, l'applicazione può richiedere che il client invii un messaggio CPMDisconnect al server. Quando questa query viene ricevuta, il client DEVE inviare semplicemente il messaggio come richiesto. Non è disponibile alcuna risposta a questo messaggio dal server.

### <a name="325-message-processing-and-sequencing-rules"></a>3.2.5 Regole di elaborazione e sequenziazione dei messaggi

Quando il client riceve una risposta di messaggio dal server, il client DEVE usare l'ultimo messaggio inviato per determinare se il messaggio ricevuto dal server è quello previsto dal client. Tutti i messaggi con \_ il campo msg diverso da quello in Last Send Message MUST devono essere ignorati.

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a>3.2.5.1 Ricezione di una risposta CPMCreateQueryOut

Quando il client riceve una risposta di messaggio CPMCreateQueryOut dal server, il client DEVE restituire lo stato e(se lo stato ha esito positivo) i valori di handle del cursore tornano \_ al livello superiore. Eventuali altre azioni sono fino al livello superiore.

Poiché il livello superiore è a conoscenza della struttura delle query, nel messaggio CPMCreateOueryOut verrà sempre restituito il numero corretto di handle di cursore. Gli handle di cursore vengono restituiti nell'ordine seguente: il primo handle è per il set di righe nonchaptered, il secondo per il primo set di righe in capitoli (ovvero il raggruppamento dei risultati in base alla prima categoria specificata nel campo CategorizationSet del messaggio CPMCreateQueryIn).

Per scopi informativi, è previsto che i livelli superiori possano eseguire le azioni seguenti, ma non vengono applicate dal client CISP:

-   Usare CPMSetBindingsIn per impostare associazioni per singole colonne ed eseguire eventuali azioni successive sul percorso della query
-   Usare CPMGetQueryStatusIn per controllare lo stato di esecuzione di una query.
-   Usare CPMRatioFinishedIn per richiedere la percentuale di completamento della query.

### <a name="3252-receiving-a-cpmgetrowsout-response"></a>3.2.5.2 Ricezione di una risposta CPMGetRowsOut

Quando il client riceve una risposta di messaggio CPMGetRowsOut dal server, il client DEVE eseguire le operazioni seguenti:

-   Controllare se il \_ campo dello stato nell'intestazione indica esito positivo o negativo.
-   Se il \_ valore di stato è STATUS BUFFER TOO SMALL \_ (0xC0000023), il client DEVE controllare lo stato Ultimo messaggio \_ \_ inviato. Se non contiene un messaggio CPMGetRowsIn, il messaggio ricevuto DEVE essere ignorato automaticamente. In caso contrario, il client DEVE inviare al server un nuovo messaggio CPMGetRowsIn con tutti i campi identici a quello archiviato, ad eccezione del fatto che cbReadBuffer DEVE essere aumentato di 512 (ma non maggiore di \_ 0x4000). Se lo stato è STATUS BUFFER TOO SMALL (0xC0000023) e Last Message Sent ha già \_ \_ \_ \_ \_ cbReadBuffer uguale 0x4000 client DEVE segnalare l'errore fino al livello superiore.
-   Se il \_ valore di stato è qualsiasi altro valore di errore, il client DEVE indicare l'errore fino al livello superiore.
-   Se il valore di stato indica l'esito positivo, i risultati DEVONO essere indicati fino al livello superiore che richiede le informazioni e altre azioni sono fino \_ al livello superiore.

Per scopi informativi, è previsto che i livelli superiori eseereranno in genere le azioni seguenti, ma non vengono applicate dal client Content Indexing Service Protocol:

-   Se i valori nelle righe rappresentano gli ID documento, gli handle di capitolo o segnalibro del livello superiore li archivierà in genere per l'uso nelle operazioni successive che coinvolgono ID documento validi, handle di capitolo o segnalibro validi.
-   Il livello superiore in genere archivia o visualizza o usa in altro modo i dati dei valori di riga.
-   Per i valori contrassegnati come livello superiore posticipato, il valore verrà recuperato usando i messaggi CPMFetchValueIn.
-   La descrizione della ricerca viene restituita anche al livello superiore e può essere riutilizzata o esaminata dal livello superiore.

A scopo informativo, se il livello superiore ha richiesto handle per i capitoli e i segnalibri ricevuti nelle righe, è possibile eseguire le operazioni seguenti:

-   Usare CPMGetQueryStatusExIn per controllare lo stato di esecuzione di una query, nonché informazioni aggiuntive sullo stato, ad esempio il numero di documenti filtrati, i documenti rimanenti da filtrare, il rapporto tra i documenti elaborati dalla query, il numero totale di righe nella query e la posizione del segnalibro nel set di righe.
-   Usare CPMGetNotify per richiedere che il server invii una notifica al client delle modifiche al set di righe.
-   Usare CPMGetApproximatePositionIn per richiedere la posizione approssimativa di un segnalibro in un capitolo.
-   Usare CPMCompareBmkIn per richiedere un confronto tra due segnalibri in un capitolo.
-   Usare CPMRestartPositionIn nel server per modificare la posizione del cursore all'inizio del set di righe.

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a>3.2.5.3 Ricezione di una risposta CPMFetchValueOut

Quando il client riceve una risposta di messaggio CPMGetRowsOut dal server, il client DEVE eseguire le operazioni seguenti:

-   Controllare se il \_ campo dello stato nell'intestazione indica esito positivo o negativo. In caso di errore, inviare una notifica al livello superiore. In caso contrario, continuare di seguito.
-   Selezionare fValueExist e, se impostato su 0x00000000 notificare al livello \_ superiore che il valore non è stato trovato.
-   In caso contrario, \_ aggiungere i byte cbValue da vValue al valore della proprietà corrente.
-   Se fMoreExists è impostato su 0x00000001, incrementare i byte correnti ricevuti da cbValue e inviare un messaggio \_ \_ \_ \_ CPMFetchValueIn al server, impostando \_ cbSoFar sul valore di Current Bytes Received, \_ cbPropSpec su zero e \_ cbChunk alle dimensioni del buffer desiderate dal livello superiore.
-   Se fMoreExists è impostato su 0x00000000 il valore della proprietà da \_ Valore proprietà corrente al livello superiore.

### <a name="3254-receiving-a-cpmfreecursorout-response"></a>3.2.5.4 Ricezione di una risposta CPMFreeCursorOut

Quando il client riceve una risposta di messaggio CPMFreeCursorOut dal server, il client DEVE restituire il valore \_ cCursorsRemaining al livello superiore.

Le informazioni seguenti vengono fornite solo a scopo informativo e non vengono applicate dal client CISP. È previsto che il livello superiore tenga traccia degli handle del cursore e non usi quelli già liberati. Quando il numero di cCursorsRemaining è uguale a 0x00000000, il livello superiore può usare la connessione per specificare un'altra query (usando un \_ messaggio CPMCreateQueryIn).

### <a name="326-timer-events"></a>3.2.6 Eventi timer

Nessuno.

### <a name="327-other-local-events"></a>3.2.7 Altri eventi locali

Nessuno.

## <a name="4-protocol-examples"></a>4 Esempi di protocollo

-   [4.1 Esempio 1](#41-example-1)
-   [4.2 Esempio 2](#42-example-2)

### <a name="41-example-1"></a>4.1 Esempio 1

Nell'esempio seguente si considera uno scenario in cui l'utente JOHN nel computer A vuole ottenere le dimensioni dei file che contengono la parola "Microsoft" dal set di documenti archiviati nel server X nel catalogo SYSTEM. Si supponga che il computer A eserciti un sistema operativo Windows XP a 32 bit e che il computer X eserciti un sistema operativo Windows Server 2003 a 32 bit.

1.  L'utente avvia un'applicazione di ricerca e immette la query di ricerca. L'applicazione passa a sua volta la query di ricerca al client del protocollo.
2.  Il client del protocollo stabilisce una connessione con il server di indicizzazione X. Il client del protocollo usa named pipe \\ \\ pipe CI \_ SKADS per connettersi al server X tramite SMB.
3.  Il client del protocollo prepara quindi un messaggio CPMConnectIn con i valori seguenti:

    L'intestazione del messaggio viene popolata come segue:

    -   **\_ msg** è impostato su 0x000000C8, a indicare che si tratta di un messaggio CPMConnectIn.
    -   **\_ status** è impostato su 0x00000000.
    -   **\_ ulChecksum** contiene il checksum, calcolato come specificato nella Sezione 3.2.4.
    -   **\_ ulReserved2** è impostato su 0x00000000.

    Il corpo del messaggio viene popolato come segue:

    -   **\_ iClientVersion è** impostato su 0x00000008, che indica che il server deve convalidare il campo checksum.
    -   **\_ fClientIsRemote** è impostato su 0x00000001, a indicare che il server è un server remoto.
    -   **\_ cbBlob1** è impostato sulla dimensione, in byte, dei campi cPropSet, PropertySet1 e PropertySet2 combinati.
    -   **\_ cbBlob2 è** impostato su 0x00000004 (ovvero nessun set di proprietà aggiuntivo).
    -   **MachineName** è impostato su A.
    -   **UserName** è impostato su JOHN.
    -   **cPropSets** è impostato su 0x00000002.
    -   **Il campo PropertySet1** è di tipo CDbPropSet. La struttura CDbPropSet che comprende il campo PropertySet1 viene popolata come segue:
        -   Il campo **GuidPropSet** è impostato su A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ EXT).
        -   **Il campo cProperties** è impostato su 0x00000004.
        -   **un campo aProps** è una matrice di strutture CDbProp.

            Per **l'elemento aProps \[ 0: \]**

            -   **PropId** è impostato su 0x00000002 (DBPROP \_ CI \_ CATALOG \_ NAME).
            -   **DBPROPOPTIONS è** impostato su 0x0000000.
            -   **DBPROPSTATUS è** impostato su 0x00000000.
            -   Per **l'elemento ColId:**
                -   **eKind** è impostato su 0x00000001 (DBKIND \_ GUID \_ PROPID)
                -   **GUID** è Null (tutti zeri), ovvero il valore si applica alla query, non solo a una singola colonna.
                -   **ulID** è impostato su 0x00000000.
            -   Per **l'elemento vValue:**
                -   **vType** è impostato su 0x001F (VT \_ LPWSTR).
                -   **vValue** è impostato su "SYSTEM", il nome del catalogo desiderato.

            Per **l'elemento aProps \[ 1: \]**

            -   **PropId** è impostato su 0x00000007 (DBPROP \_ CI \_ QUERY \_ TYPE)
            -   **DBPROPOPTIONS è** impostato su 0x0000000.
            -   **DBPROPSTATUS è** impostato su0x00000000.
            -   Per **l'elemento ColId:**
                -   **eKind** è impostato su 0x00000001 (DBKIND \_ GUID \_ PROPID).
                -   **GUID** è Null (tutti zeri), ovvero il valore si applica alla query, non solo a una singola colonna.
                -   **ulID** è impostato su 0x00000000.
            -   Per **l'elemento vValue:**
                -   **vType** è impostato su 0x0003 (VT \_ I4).
                -   **vValue** è impostato su 0x00000000 (CiNormal), ovvero si tratta di una query normale.

            Per **l'elemento aProps \[ 2: \]**

            -   **PropId** è impostato su 0x00000004 (DBPROP \_ CI \_ SCOPE \_ FLAGS).
            -   **DBPROPOPTIONS è** impostato su 0x0000000.
            -   **DBPROPSTATUS è** impostato su 0x00000000.
            -   Per **l'elemento ColId:**
                -   **eKind** è impostato su 0x00000001 (DBKIND \_ GUID \_ PROPID).
                -   **GUID** è Null (tutti zeri), ovvero il valore si applica alla query, non solo a una singola colonna.
                -   **ulID** è impostato su 0x00000000.
            -   Per **l'elemento vValue:**
                -   **vType:** 0x1003 (VT \_ VECTOR \| VT \_ I4)
                -   **vValue:** 0x00000001/0x00000001 (un elemento con valore 1), ovvero le sottocartelle di ricerca

            Per **l'elemento aProps \[ 3: \]**

            -   **PropId:** 0x00000003 (AMBITI DI \_ INCLUSIONE DBPROP \_ \_ CI)
            -   **DBPROPOPTIONS**: 0x0000000
            -   **DBPROPSTATUS:** 0x00000000
            -   Per **l'elemento ColId:**
                -   **eKind** è impostato su 0x00000001 \_ \_ (DBKIND GUID PROPID).
                -   **IL GUID** è Null (tutti zeri), vale a dire che il valore si applica alla query, non solo a una singola colonna.
                -   **ulID** è impostato su 0x00000000
            -   Per **l'elemento vValue:**
                -   **vType** è impostato su 0x101F (VT \_ VECTOR \| VT \_ LPWSTR).
                -   **vValue** è impostato su 0x00000001/0x00000002 / " " (un elemento con una stringa con terminazione \\ Null a 2 caratteri), ovvero l'ambito radice.

    -   Il **campo PropertySet2** è di tipo CDbPropSet.

        La struttura CDbPropSet che comprende il campo PropertySet1 viene popolata come segue:

        -   **GuidPropSet** è impostato su AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ EXT).
        -   **Il campo cProperties** è impostato su 0x00000001.
        -   Il **campo aProps** è una matrice di strutture CDbProp.

            Per **l'elemento aProps \[ 0: \]**

            -   **PropId** è impostato su 0x00000002 (DBPROP \_ MACHINE).
            -   **DBPROPOPTIONS è** impostato su 0x0000000.
            -   **DBPROPSTATUS è** impostato su 0x00000000.
            -   Per **l'elemento ColId:**
                -   **eKind** è impostato su 0x00000001 \_ \_ (DBKIND GUID PROPID),
                -   **IL GUID** è Null (tutti zeri), vale a dire che il valore si applica alla query, non solo a una singola colonna.
                -   **ulID** è impostato su 0x00000000.
            -   Per **l'elemento vValue:**
                -   **vType:** 0x0008 (VT \_ BSTR)
                -   **vValue**: 0x04 /"X" (4 byte/stringa Unicode con terminazione Null), ovvero "X" -name di un server.

    -   **Il campo cExtPropSet** è impostato su 0x00000000.
    -   **La matrice aPropertySets** non esiste.
    -   I vari campi di riempimento vengono compilati in base alle esigenze. Il messaggio viene inviato al server.

4.  Il server verifica che **\_ ulChecksum** sia corretto, verifica che l'utente sia autorizzato a effettuare questa richiesta e risponde con un messaggio CPMConnectOut.

    L'intestazione del messaggio viene popolata come segue:

    -   **\_ msg** è impostato su 0x000000C8, a indicare che si tratta di un messaggio CPMConnectOut.
    -   **\_ status** è impostato su 0x0000000 che indica SUCCESS.
    -   **\_ ulChecksum** è impostato su 0.
    -   **\_ ulReserved2 è** impostato su 0x00000000.

    Il corpo del messaggio viene popolato come segue:

    -   **\_ il campo serverVersion** è impostato 0x00000007 (32 bit Windows XP o 32 bit Windows Server 2003).
    -   **\_ I** campi riservati vengono compilati con dati arbitrari.

5.  Il client prepara un messaggio CPMCreateQueryIn.

    L'intestazione del messaggio viene popolata come segue:

    -   **\_ msg** è impostato su 0x000000CA, a indicare che si tratta di un messaggio CPMCreateQueryIn.
    -   **\_ status** è impostato su 0x00000000.
    -   **\_ ulChecksum** contiene il checksum, calcolato in base alla versione 3.2.5.
    -   **\_ ulReserved2 è** impostato su 0x00000000.

    Il corpo del messaggio viene popolato come segue:

    -   **Il** campo Dimensioni è impostato sulla dimensione del resto del messaggio.
    -   **Il campo CColumnSetPresent** è impostato su 0x01.
    -   **Il campo ColumnSet** è di tipo CColumnSet. La struttura CColumnSet che comprende questo campo viene impostata come segue:
        -   **\_ Il** campo count è impostato su 0x00000001 che indica che viene restituita una colonna.
        -   **La matrice indexes** 0x00000000 che indica la prima voce in \_ un oggettoPropSpec.
    -   **Il campo CRestrictionPresent** è impostato su 0x01 che indica che il **campo Restriction** è presente.
    -   **Il** campo Restriction è di tipo CRestriction ed è impostato su:
        -   **\_ ulType** è impostato su 0x00000004 (RTContent).
        -   **\_ weight** è impostato su 0x00000000.
    -   Il resto del campo contiene una struttura CContentRestriction:
        -   **\_ La** proprietà è impostata sul GUID B725F130-47EF-101A-A5F1-02608c9eebac/0x00000001 (per PRSPEC PROPID) /0x13 che rappresenta il corpo \_ del documento.
        -   **\_ Cc** è impostato su 0x00000009.
        -   **\_ pwcsphrase** è impostato sulla stringa "Microsoft".
        -   **\_ lcid** è impostato su 0x409 (per l'inglese).
        -   **\_ ulGenerateMethod** è impostato su 0x00000000 (corrispondenza esatta).
    -   **CSortPresent è** impostato su 0x00.
    -   **CCategorizationSetPresent** è impostato su 0x00.
    -   **RowSetProperties viene** impostato come segue:
        -   **\_ uBooleanOptions** è impostato su 0x00000001 (sequenziale).
        -   **\_ ulMaxOpenRows** è impostato su 0x00000000.
        -   **\_ ulMemoryUsage** è impostato su 0x00000000.
        -   \_**cMaxResults è** impostato su 0x00000100 (restituisce al massimo 256 righe).
        -   **\_ cCmdTimeOut** è impostato su 0x00000000 (mai timeout).
    -   **PidMapper** è impostato su:
        -   **\_ count** è impostato su 0x00000001.
        -   **\_ aPropSpec** è impostato sul GUID B725F130-47EF-101A-A5-F1-02608C9EEBATT/0x00000001 (per PRSPEC PROPID) /0x0000000c che rappresenta la proprietà delle dimensioni del \_ file Windows.

6.  Il server lo elabora e risponde con un messaggio CPMCreateQueryOut.

    L'intestazione del messaggio viene popolata come segue:

    -   **\_ msg** è impostato su 0x000000CA, a indicare che si tratta di un messaggio CPMCreateQueryOut.
    -   **\_ status** è impostato su SUCCESS.
    -   **\_ ulChecksum** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).
    -   **\_ ulReserved2 è** impostato su 0x00000000 (o qualsiasi altro valore arbitrario).

    Il corpo del messaggio viene popolato come segue:

    -   **\_ fTrueSeqeuntial** è impostato su 0x00000000, a indicare che la query può usare un indice.
    -   **\_ fWorkIdUnique** è impostato su 0x00000001.
    -   La **matrice aCursors** contiene un solo elemento, che rappresenta un handle di cursore per questa query. Il valore dipende dallo stato del server. Si supponga che il valore restituito sia 0xAAAAAAAA.

7.  Il client esegui un messaggio di richiesta CPMSetBindingsIn per definire il formato di una riga.

    L'intestazione del messaggio viene popolata come segue:

    -   **\_ msg** è impostato su 0x000000D0, a indicare che si tratta di un messaggio CPMSetBindingsIn.
    -   **\_ status** è impostato su SUCCESS.
    -   **\_ ulChecksum** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).
    -   **\_ ulReserved2 è** impostato su 0x00000000 (o qualsiasi altro valore arbitrario).

    Il corpo del messaggio viene popolato come segue:

    -   **\_ hCursor** è impostato su 0xAAAAAAAA.
    -   **\_ cbRow è** impostato su 0x10 (sufficientemente grande da adattarsi alle colonne).
    -   **\_ cbBindingDesc** è impostato sulla dimensione dei campi **\_ cColumns** **\_ e aColumns** combinati.
    -   **\_ cColumns** è impostato su 0x00000001.
    -   **\_ La matrice aColumns** è impostata in modo da contenere una struttura CTableColumn contenente:
    -   -   **\_ PropSpec** è impostato su GUID b725f130-47ef-101a-a5-f1-02608c9eebatt / 0x00000001 (per PRSPEC PROPID) / 0x0000000c che rappresenta la proprietà delle dimensioni \_ del file Windows.
        -   **\_ vType** è impostato su 0x0015 (VT \_ UI8).
        -   **\_ ValueUsed** è impostato su 0x01 (colonna trasferita nella riga).
        -   **\_ ValueOffset** è impostato su 0x0002 (all'inizio della riga).
        -   **\_ ValueSize è** impostato su 0x08 (dimensioni di un'interfaccia utente VT8). \_
        -   **\_ StatusUsed** è impostato su 0x01.
        -   **\_ StatusOffset** è impostato su 0x0A.
        -   **\_ LengthUsed** è impostato su 0x00.

8.  Il server lo elabora e risponde con un messaggio CPMSetBindingsIn.

    L'intestazione del messaggio viene popolata come segue:

    -   **\_ msg** è impostato su 0x000000D0.
    -   **\_ status** è impostato su SUCCESS.
    -   **\_ ulChecksum** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).
    -   **\_ ulReserved2 è** impostato su 0x00000000 (o qualsiasi altro valore arbitrario).

9.  Il client genera un messaggio di richiesta CPMGetRowsIn. Si supponga che il client sia pronto ad accettare 100 righe a questo punto e le voglia in ordine crescente.

    L'intestazione del messaggio viene popolata come segue:

    -   **\_ msg** è impostato su 0x000000CC, a indicare che si tratta di un messaggio CPMGetRowsIn.
    -   **\_ status** è impostato su 0x00000000
    -   **\_ ulChecksum** contiene il checksum, calcolato in base alla sezione 0.
    -   **\_ ulReserved2 è** impostato su 0x00000000.

    Il corpo del messaggio viene popolato come segue:

    -   **\_ hCursor** è impostato su 0xAAAAAAAA.
    -   **\_ cRowsToTransfer** è impostato su 0x00000064.
    -   **\_ cRowWidth** è impostato su 0x00000010 (da associazioni).
    -   **\_ cbSeek** è impostato 0x14 che è la dimensione dei campi eType, chapt e \_ CRowSeekNext combinati.
    -   **\_ cbReserved è** impostato su 0x18 (0x14 \_ più cbSeek).
    -   **\_ cbReadBuffer** è impostato su 0x800 (0x64 0x10 arrotondato al multiplo \* successivo di 0x200).
    -   **\_ ulClientBase è** impostato su 0x00000000.
    -   **\_ fBwdfetch** è impostato su 0x00000000 che indica che le righe devono essere recuperate in avanti.
    -   **eType** è impostato su 0x0000001 che indica che il client desidera righe successive.
    -   **\_ chapt** è impostato su 0 (non su un risultato in capitolo).
    -   **SeekDescription** è impostato su CRowSeekNext. La struttura CRowSeekNext contiene i valori seguenti:
        -   **CiTblChapt è** impostato su 0x00000000.
        -   **\_ hRegion** è impostato su 0x00000000.
        -   **\_ cSkip** è impostato su 0, a indicare che il client non vuole ignorare le righe.

10. Il server lo elabora e risponde con un messaggio CPMGetRowsOut. Si supponga che il server ha trovato 100 documenti contenenti la parola "Microsoft".

    L'intestazione del messaggio viene popolata come segue:

    -   **\_ msg** è impostato su 0x000000CC, a indicare che si tratta di un messaggio CPMGetRowsOut.
    -   **\_ status** è impostato su SUCCESS.
    -   **\_ ulChecksum** è impostato su 0x00000000.
    -   **\_ ulReserved2 è** impostato su 0x00000000.

    Il corpo del messaggio viene popolato come segue:

    -   **\_ CRowsReturned è** impostato su 0x00000064.
    -   **eType** è impostato su 0x00000001.
    -   **\_ Chapt** è impostato su 0x00000000 (non un risultato capitolo).
    -   **SeekDescription** contiene una struttura CRowSeekNext, popolata come segue:
        -   **CiTblChapt è** impostato su 0x00000000.
        -   **\_ hRegion** è impostato su 0x00000000.
        -   **\_ cSkip** è impostato su 0, a indicare che il client non vuole ignorare le righe.
    -   **Rows** contiene le dimensioni dei 100 documenti che contengono la parola "Microsoft". Poiché si tratta di dati a dimensione fissa, sono semplicemente strutturati come un elenco di interi senza segno a 100, 8 byte.

11. Il client invia un messaggio CPMDisconnect per terminare la connessione.

    L'intestazione del messaggio viene popolata come segue:

    -   **\_ msg** è impostato su 0x000000C9, a indicare che si tratta di un messaggio CPMDisconnect.
    -   **\_ status** è impostato su 0x00000000.
    -   **\_ ulChecksum** è impostato su 0x00000000.

12. Il server elabora il messaggio e rimuove tutti gli stati client.

### <a name="42-example-2"></a>4.2 Esempio 2

Nell'esempio precedente la query era piuttosto semplice. Si consideri ora una query leggermente più complessa. Si supponga che l'utente voglia recuperare le dimensioni dei documenti che contengono entrambe le parole seguenti: "Microsoft" e "Office". Questo valore viene specificato modificando il campo Restriction contenuto nel messaggio CPMCreateQueryIn inviato nel passaggio 5 come indicato di seguito:

Il **campo Restriction** è di tipo CRestriction ed è impostato su:

-   -   **\_ ulType** è impostato su 0x00000004 (RTAnd).
    -   **\_ weight** è impostato su 0x00000000.

Il resto del campo contiene una struttura CNodeRestriction:

-   -   **\_ cNode** è impostato su 0x00000002, a indicare che sono presenti due nodi nella matrice paNode.
    -   Il **\_ campo paNode** è una matrice di due strutture CRestriction.

        **\_ paNode \[ \] 0** contiene:

        -   -   **\_ ulType** è impostato su 0x00000004 (RTContent).
            -   **\_ weight** è impostato su 0x00000000.
            -   Il resto del campo contiene una struttura CContentRestriction:
                -   **\_ La** proprietà è impostata sul GUID b725f130-47ef-101a-a5f1-02608c9eebac/0x00000001 (per \_ PRSPEC PROPID) / 0x13.
                -   **\_ Cc** è impostato su 0x00000009.
                -   **\_ pwcsphrase** è impostato sulla stringa "Microsoft".
                -   **\_ lcid** è impostato su 0x409 (per l'inglese).
                -   **\_ ulGenerateMethod** è impostato su 0x00000000 (corrispondenza esatta).

        **\_ paNode \[ \] 1** contiene:

        -   -   **\_ ulType** è impostato su 0x00000004 (RTContent).
            -   **\_ weight** è impostato su 0x00000000.
            -   Il resto del campo contiene una struttura CContentRestriction:
                -   **\_ La** proprietà è impostata sul GUID b725f130-47ef-101a-a5f1-02608c9eebac/0x00000001 (per \_ PRSPEC PROPID) / 0x13.
                -   **\_ Cc** è impostato su 0x00000006.
                -   **\_ pwcsphrase** è impostato sulla stringa "Office".
                -   **\_ lcid** è impostato su 0x409 (per l'inglese).
                -   **\_ ulGenerateMethod** è impostato su 0x00000000 (corrispondenza esatta).

## <a name="5-security"></a>5 Sicurezza

### <a name="51-security-considerations-for-implementers"></a>5.1 Considerazioni sulla sicurezza per i responsabili dell'implementazione

Le implementazioni di indicizzazione che indicizzano contenuto protetto devono prendere in considerazione l'uso del contesto utente fornito da SMB MS-SMB per tagliare i risultati della ricerca e restituire solo quelli accessibili \[ \] al chiamante.

### <a name="52-index-of-security-parameters"></a>5.2 Indice dei parametri di sicurezza



| Parametro di sicurezza  | Sezione |
|---------------------|---------|
| Livello di rappresentazione | 2.1     |



 

## <a name="6-index-of-version-specific-behavior"></a>6 Indice del comportamento specifico della versione



| Comportamento specifico della versione                                                                         | Sezione   | Windows 2000 | Windows XP | Windows Server 2003 |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| Questo protocollo viene implementato in Windows 2000, Windows XP, Windows Server 2003 e Windows Vista. | 1.3.2     | X            | X          | X                   |
| Le applicazioni interagiscono in genere con un wrapper OLE DB interfaccia utente                                  | 1.4       | X            | X          | X                   |
| Valori NTSTATUS                                                                                   | 1.8       | X            | X          | X                   |
| Il client imposta il \_ campo dello stato in ogni intestazione del messaggio.                                        | 2.2.2     | X            | X          | X                   |
| Il valore di cPendingScans è in genere zero                                                               | 2.2.3.1   | X            | X          | X                   |
| Valore iClientVersion                                                                              | 2.2.3.6   | X            | X          | X                   |
| \_Valore cbChunk                                                                                   | 2.2.3.19  | X            | X          | X                   |
| Indirizzi di memoria a 32 bit e a 64 bit                                                                | 3.2.4.2.4 | X            | X          | X                   |



 

 

 





