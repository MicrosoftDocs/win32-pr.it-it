---
title: Protocollo di servizi di indicizzazione del contenuto
description: Questo documento è una specifica del protocollo del servizio di indicizzazione del contenuto.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c22bbda912333368e50d3e4a8ace2cd98856ea
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "103724226"
---
# <a name="content-indexing-services-protocol"></a>Protocollo di servizi di indicizzazione del contenuto

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .

Specifica del protocollo, versione 0,12

-   [1 Introduzione](#1-introduction)
    -   [1.1 Glossario](#11-glossary)
    -   [1.2 Riferimenti](#12-references)
    -   [Panoramica sul protocollo 1,3 (sinossia)](#13-protocol-overview-synopsis)
    -   [1.4 Relazione con altri protocolli](#14-relationship-to-other-protocols)
    -   [1,5 prerequisiti e precondizioni](#15-prerequisites-and-preconditions)
    -   [1.6 Dichiarazione di applicabilità](#16-applicability-statement)
    -   [1.7 Controllo delle versioni e negoziazione dalla capacità](#17-versioning-and-capability-negotiation)
    -   [1.8 Campi estendibili dal fornitore](#18-vendor-extensible-fields)
    -   [1.9 Assegnazioni degli standard](#19-standards-assignments)
-   [2 Messaggi](#2-messages)
    -   [2.1 Trasporto](#21-transport)
    -   [2.2 Sintassi dei messaggi](#22-message-syntax)
-   [3 Dettagli del protocollo](#3-protocol-details)
    -   [3,1 Dettagli server](#31-server-details)
    -   [3,2 Dettagli client](#32-client-details)
-   [4 Esempi di protocollo](#4-protocol-examples)
    -   [4,1 esempio 1](#41-example-1)
    -   [4,2 esempio 2](#42-example-2)
-   [5 Sicurezza](#5-security)
    -   [5.1 Considerazioni sulla sicurezza per i responsabili dell'implementazione](#51-security-considerations-for-implementers)
    -   [5.2 Indice dei parametri di sicurezza](#52-index-of-security-parameters)
-   [6 Indice del comportamento specifico della versione](#6-index-of-version-specific-behavior)

Questo documento è una specifica del protocollo del servizio di indicizzazione del contenuto.

La documentazione di WSPP (Workgroup Server Protocol Program) è destinata all'utilizzo in combinazione con la documentazione degli standard pubblici, la programmazione di rete e i concetti relativi ai sistemi distribuiti del gruppo di lavoro e presuppone che il lettore abbia familiarità con il materiale menzionato in questo caso o abbia accesso immediato.

Una specifica del protocollo WSPP non richiede l'uso di strumenti di programmazione Microsoft o ambienti di programmazione per consentire a una licenza di sviluppare un'implementazione. Le licenze che hanno accesso agli strumenti e agli ambienti di programmazione Microsoft sono gratuite per sfruttarle.

## <a name="1-introduction"></a>1 Introduzione

-   [1.1 Glossario](#11-glossary)
-   [1.2 Riferimenti](#12-references)
-   [Panoramica sul protocollo 1,3 (sinossia)](#13-protocol-overview-synopsis)
-   [1.4 Relazione con altri protocolli](#14-relationship-to-other-protocols)
-   [1,5 prerequisiti e precondizioni](#15-prerequisites-and-preconditions)
-   [1.6 Dichiarazione di applicabilità](#16-applicability-statement)
-   [1.7 Controllo delle versioni e negoziazione dalla capacità](#17-versioning-and-capability-negotiation)
-   [1.8 Campi estendibili dal fornitore](#18-vendor-extensible-fields)
-   [1.9 Assegnazioni degli standard](#19-standards-assignments)

### <a name="11-glossary"></a>1.1 Glossario

> [!Note]  
> I termini seguenti sono definiti nella sezione Glossario di \[ ms-sys \] :
>
> -   GUID
> -   Little Endian
> -   Named pipe
> -   Percorso

 

**Binding**: richiesta di inclusione di una determinata **colonna** in un **set di righe** restituito. L' **associazione** specifica una proprietà da includere nei risultati della ricerca.

**Segnalibro**: marcatore che identifica in modo univoco una riga all'interno di un set di righe.

**Catalog**: unità di livello superiore dell'organizzazione nel servizio di indicizzazione. Rappresenta un set di documenti indicizzati su cui è possibile eseguire query utilizzando il protocollo del servizio di indicizzazione del contenuto.

**Category**: raggruppamento gerarchico di righe. Ad esempio, il risultato di una query contenente le colonne autore e titolo può essere categorizzato in base all'autore. Ogni gruppo di righe contenente lo stesso valore per autore costituisce una categoria.

**Capitolo** : un intervallo di **righe** all'interno di un set di **righe** .

**Column**: contenitore per un singolo tipo di informazioni in una **riga** . Le colonne eseguono il mapping ai nomi di proprietà e specificano quali proprietà vengono usate per gli elementi della **struttura ad albero** dei **comandi** della query di ricerca.

**Albero dei comandi**: una combinazione di **restrizioni** , **categorie** e **ordinamenti specificati per** la query di ricerca.

**Cursor**: entità utilizzata come meccanismo per lavorare con una **riga** o un piccolo blocco di **righe** alla volta in un set di dati restituito in un set di risultati. Un **cursore** viene posizionato in corrispondenza di una singola **riga** all'interno del set di risultati. Dopo aver posizionato il **cursore** su una riga, è possibile eseguire le operazioni su tale **riga** o su un blocco di **righe** a partire da quella posizione.

**Handle**: token che può essere utilizzato per identificare e accedere a **cursori** , **capitoli** e **segnalibri** .

**Index**: struttura permanente che contiene il contenuto di testo estratto dai file da un **servizio di indicizzazione** . Include l'elenco di parole, che vengono archiviate insieme al nome file, alla posizione e alle **impostazioni locali** .

**Indicizzazione**: processo di estrazione di testo e proprietà da file e archiviazione dei valori estratti negli **indici** (per il testo) e nella **cache delle proprietà** (per le proprietà).

**Servizio di indicizzazione**: un servizio che crea **cataloghi** indicizzati per il contenuto e le proprietà dei file System. Le applicazioni possono eseguire ricerche nei cataloghi per ottenere informazioni dai file nella file system indicizzata.

**Impostazioni locali**: un identificatore, come specificato nell' \[ appendice MS-GPSI \] , che specifica le preferenze relative alla lingua. Queste preferenze indicano il modo in cui le date e le ore devono essere formattate, gli elementi devono essere ordinati alfabeticamente, le stringhe devono essere confrontate e così via.

**Query in linguaggio naturale**: una query costruita usando il linguaggio umano invece della sintassi di query.

**Parole non significative**: una parola che viene ignorata dal servizio di indicizzazione quando è presente nelle **restrizioni** specificate per la query di ricerca perché presenta un valore discriminatorio minimo. Gli esempi in inglese includono "a", "and" e "The".

**Cache delle proprietà**: una cache delle proprietà dei file estratte da un **servizio di indicizzazione** .

**Indicizzazione delle proprietà**: processo di creazione di un **Indice** di proprietà del **tipo di valore** di un documento, tra cui autore, oggetto, tipo, conteggio delle parole, conteggio delle pagine stampate e qualsiasi altra proprietà.

**Restrizione**: set di condizioni che un file deve soddisfare per essere incluso nei risultati della ricerca restituiti dal **servizio di indicizzazione** in risposta a una query di ricerca. Una **restrizione** restringe l'attenzione di una query di ricerca, limitando i file che il **servizio di indicizzazione** include nei risultati della ricerca solo a quelli che soddisfano le condizioni.

**Row**: raccolta di **colonne** contenente i valori delle proprietà che descrivono un singolo file del set di file che corrisponde alle **restrizioni** specificate nella query di ricerca inviata al **servizio di indicizzazione** .

**Rowset**: set di **righe** restituito nei risultati della ricerca.

**Ordinamento**: set di regole in una query di ricerca che definiscono l'ordinamento delle righe nei risultati della ricerca. Ogni regola è costituita da una proprietà (nome, dimensioni e così via) e da una direzione per l'ordinamento (crescente o decrescente). Più regole vengono applicate in sequenza

**Proprietà di tipo text**: proprietà che descrive il contenuto di un documento e ha solo testo non formattato associato al nome.

**Proprietà di tipo valore**: proprietà che descrive un singolo attributo di un intero documento. Una proprietà di tipo valore ha un ID del tipo di dati e un valore di tale tipo di dati associato al nome.

**Radice virtuale**: un percorso alternativo a una cartella. Una cartella fisica può avere zero o più radici virtuali. I percorsi che iniziano con una radice virtuale sono denominati percorsi virtuali. Ad esempio,/server/vanityroot potrebbe essere una radice virtuale di C: \\ \\ folder1 Web IIS \\ . Il file C: \\ IIS \\ web \\ folder1 \\default.htm avrà quindi un percorso virtuale/Server/vanityroot/default.htm.

**May, should, Most, should not, must not**: questi termini (in tutti i limiti) vengono usati come descritto in \[ RFC2119 \] . Tutte le istruzioni di comportamento facoltativo usano MAY, SHOULD, o SHOULD NOT.

### <a name="12-references"></a>1.2 Riferimenti

### <a name="121-normative-references"></a>1.2.1 Riferimenti normativi

\[IEEE754 \] Institute of Electrical and Electronics Engineers, "standard for Binary Floating-Point aritmetico", IEEE 754-1985, ottobre 1985, https://standards.ieee.org/standard/754-1985.html

\[MS-DCOM \] Microsoft Corporation, "distributed Component Object Model Remote Protocols", giugno 2006.

\[MS-GPSI \] Microsoft Corporation, "criteri di gruppo Installazione software Extension", 2006 giugno.

\[MS-SMB \] Microsoft Corporation, protocollo "Microsoft Server Message Block (SMB) ed estensioni", 2006 maggio.

\[MS-SYS \] Microsoft Corporation, "System Overview V4", luglio 2006.

\[Salton \] Salton, G., "elaborazione automatica del testo: analisi della trasformazione e recupero di informazioni per computer", 1988, ISBN 0-201-2227-8.

\[UNICODE \] il Consorzio Unicode, "lo standard Unicode, versione 2,0", 1996, https://www.unicode.org

### <a name="122-informative-references"></a>1.2.2 Riferimenti informativi

\[MSDN-OLEDB \] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .

\[MSDN-QUERYERR \] Microsoft Corporation, valori Query-Execution, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp

### <a name="13-protocol-overview-synopsis"></a>Panoramica sul protocollo 1,3 (sinossia)

Un **servizio di indicizzazione** del contenuto consente di organizzare in modo efficiente le funzionalità estratte di una raccolta di documenti. Il protocollo CISP (Content Indexing Service) consente a un client di comunicare con un server che ospita un servizio di indicizzazione per eseguire query e consentire a un amministratore di gestire il server di indicizzazione.

Quando si elaborano i file, un servizio di indicizzazione analizza un set di documenti e ne riorganizza il contenuto in modo che le **Proprietà** di tali documenti possano essere restituite in modo efficiente in risposta alle query. Una raccolta di documenti su cui è possibile eseguire query è costituita da un **Catalogo** . Un catalogo può contenere un **Indice** (per riferimento rapido al testo) e una **cache delle proprietà** (per il recupero rapido dei valori delle proprietà).

Concettualmente, un catalogo è costituito da una "tabella" logica di proprietà con il testo o il valore e le impostazioni locali corrispondenti archiviate nelle **colonne** della tabella. Ogni "riga" della tabella corrisponde a un documento separato nell'ambito del catalogo e ogni "colonna" della tabella corrisponde a una proprietà.

Le attività specifiche eseguite da CISP vengono raggruppate in due aree funzionali:

-   Amministrazione remota dei cataloghi di servizi di indicizzazione,
-   Esecuzione di query remote sui cataloghi dei servizi di indicizzazione.

### <a name="131-remote-administration-tasks"></a>1.3.1 attività di amministrazione remota

CISP Abilita le seguenti attività di gestione del catalogo dei servizi di indicizzazione da un client:

-   Eseguire una query sullo stato corrente di un catalogo di servizi di indicizzazione nel server.
-   Aggiornare lo stato di un catalogo di servizi di indicizzazione.
-   Avviare il processo di indicizzazione per un determinato set di file.
-   Avviare l'ottimizzazione di un indice per migliorare le prestazioni di esecuzione delle query.

Tutte le attività di amministrazione remota seguono un semplice modello di richiesta/risposta. Non viene mantenuto alcuno stato sul client per nessuna chiamata di amministrazione e le chiamate amministrative possono essere eseguite in qualsiasi ordine.

### <a name="132-remote-querying"></a>1.3.2 query remote

CISP consente ai client di eseguire query di ricerca su un server remoto che ospita un servizio di indicizzazione.

L'invio di una query di ricerca è un processo in più passaggi avviato dal client. Attenersi alla procedura seguente:

1.  Il client richiede una connessione a un server che ospita un servizio di indicizzazione.
2.  Il client invia i parametri per la query di ricerca, che includono:
    -   **Limitazioni** per specificare quali documenti devono essere inclusi e/o esclusi dai risultati della ricerca.
    -   Ordine in cui devono essere restituiti i risultati della ricerca.
    -   Colonne da restituire nel set di risultati.
    -   Numero massimo di **righe** che devono essere restituite per la query.
    -   Tempo massimo per l'esecuzione delle query.

        Una volta che il server ha riconosciuto la richiesta di avvio della query da parte del client, il client può richiedere informazioni sullo stato della query, ma non si tratta di un passaggio obbligatorio.

3.  Il client specifica quindi le proprietà che il server deve includere nei risultati della ricerca.
4.  Il client richiede un set di risultati dal server e il server risponde inviando al client i valori della proprietà per i file inclusi nei risultati per la query di ricerca del client. Se il valore di una proprietà è troppo grande per essere inserito in un singolo buffer di risposta, il server non invierà la proprietà, ma lo stato della proprietà verrà impostato su rinviato. Il client richiede quindi il valore della proprietà separatamente usando una serie di richieste per i blocchi successivi del valore, quindi riprende la richiesta di altri valori.
5.  Una volta terminata la query di ricerca e non sono più necessari risultati aggiuntivi, il client contatta il server per rilasciare la query.
6.  Una volta che il server ha rilasciato la query, il client può inviare una richiesta di disconnessione dal server. La connessione viene quindi chiusa. In alternativa, il client può eseguire un'altra query e ripetere la sequenza dal passaggio 2.

Comportamento di Windows: questo protocollo viene implementato in Windows 2000, Windows XP, Windows Server 2003 e Windows Vista.

### <a name="14-relationship-to-other-protocols"></a>1.4 Relazione con altri protocolli

Il CISP si basa sul protocollo SMB \[ MS-SMB \] per il trasporto dei messaggi. Nessun altro protocollo dipende direttamente dal protocollo del servizio di indicizzazione del contenuto.

*Comportamento di Windows: le applicazioni in genere interagiscono con un wrapper di interfaccia OLE DB \[ MSDN-OLEDB \] (ad esempio, un client di protocollo) e non direttamente con il protocollo.*

### <a name="15-prerequisites-and-preconditions"></a>1,5 prerequisiti e precondizioni

Si presuppone che il client abbia ottenuto il nome del server e un nome di catalogo prima che questo protocollo venga richiamato. Il modo in cui un client esegue questa operazione esula dall'ambito di questa specifica.

Si presuppone inoltre che il client e il server dispongano di un'associazione di sicurezza utilizzabile con named pipe \[ MS-SMB \] .

### <a name="16-applicability-statement"></a>1.6 Dichiarazione di applicabilità

CISP è progettato per l'esecuzione di query e la gestione di cataloghi in un server remoto da un client. CISP è deprecato in Windows Vista.

### <a name="17-versioning-and-capability-negotiation"></a>1.7 Controllo delle versioni e negoziazione dalla capacità

Questo protocollo non dispone di meccanismi di negoziazione delle versioni o di funzionalità.

### <a name="18-vendor-extensible-fields"></a>1.8 Campi estendibili dal fornitore

Questo protocollo utilizza HRESULT che sono estendibili dal fornitore. I fornitori possono scegliere i propri valori per questo campo, purché il bit C (0x20000000) sia impostato come specificato nella sezione 4.1.1 di \[ ms-sys \] , a indicare che si tratta di un codice cliente.

Questo protocollo usa anche valori NTSTATUS tratti dallo spazio dei numeri NTSTATUS definito in \[ ms-sys \] . I fornitori devono riutilizzare questi valori con il significato indicato. La scelta di qualsiasi altro valore può comportare il rischio di un conflitto in futuro.

*Comportamento di Windows: Windows utilizza solo i valori specificati nella sezione 4.1.3 di \[ ms-sys \] .*

### <a name="181-property-ids"></a>ID proprietà 1.8.1

Le proprietà sono rappresentate da ID noti come ID di proprietà. Ogni proprietà deve avere un identificatore univoco globale. Questo identificatore è costituito da un **GUID** che rappresenta una raccolta di proprietà denominate set di proprietà più una stringa o un integer a 32 bit per identificare la proprietà all'interno del set. Se viene usato il formato integer di ID, i valori 0x00000000, 0xFFFFFFFF e 0xFFFFFFFE vengono considerati non validi.

I fornitori possono garantire che le proprie proprietà siano definite in modo univoco inserendole in un set di proprietà definito dal rispettivo GUID.

### <a name="19-standards-assignments"></a>1.9 Assegnazioni degli standard

Questo protocollo non prevede assegnazioni di standard, ma solo le assegnazioni private effettuate da Microsoft utilizzando le procedure di allocazione specificate in altri protocolli.

Questo protocollo è stato allocato da Microsoft named pipe come specificato in \[ MS-SMB \] . L'assegnazione è:



| Parametro | Valore             | Riferimento  |
|-----------|-------------------|------------|
| Nome pipe | \\\\SKADS ci \_ pipe | \[MS-SMB\] |



 

## <a name="2-messages"></a>2 Messaggi

-   [2.1 Trasporto](#21-transport)
-   [2.2 Sintassi dei messaggi](#22-message-syntax)

### <a name="21-transport"></a>2.1 Trasporto

Tutti i messaggi devono essere trasportati utilizzando un named pipe, come specificato in \[ MS-SMB \] . Viene utilizzato il seguente nome pipe:

-   \\\\SKADS ci \_ pipe

Questo protocollo usa il protocollo di named pipe SMB sottostante per recuperare l'identità del chiamante che ha effettuato la connessione come specificato nella sezione 2.2.8 di \[ MS-SMB \] . il client deve impostare l'identificazione di sicurezza \_ come ImpersonationLevel nella richiesta per aprire il named pipe.

### <a name="22-message-syntax"></a>2.2 Sintassi dei messaggi

Diverse strutture e messaggi nelle sezioni seguenti si riferiscono agli handle del capitolo o dei segnalibri. Un handle è una struttura opaca lunga a 32 bit che identifica in modo univoco un capitolo o un segnalibro. In genere, le applicazioni client ricevono valori di handle tramite chiamate al metodo; Tuttavia, esistono diversi valori noti che non devono essere ottenuti da un server, il cui significato è specificato nella tabella seguente:



| Valore                         | Significato                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| DB \_ null \_ hChapter 0x00000000 | Handle del capitolo per il set di righe non sottocapito, che contiene tutti i risultati della query.    |
| DBBMK \_ primo 0x00000001       | Handle di segnalibro per un segnalibro che identifica la prima riga nel set di righe. |
| DBBMK \_ ultimo 0x00000002        | Handle di segnalibro per un segnalibro che identifica l'ultima riga nel set di righe.  |



 

### <a name="221-structures"></a>2.2.1 strutture

In questa sezione vengono illustrate in dettaglio le strutture di dati definite e utilizzate da CISP.

Tutti gli Integer a 2, 4 e 8 byte con segno e senza segno nelle seguenti strutture devono essere trasferiti nell'ordine dei byte little-endian.

Nella tabella seguente sono riepilogate le strutture di dati definite in questa sezione.



| Struttura                    | Descrizione                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| CBaseStorageVariant          | Contiene il valore su cui eseguire un'operazione di corrispondenza per una proprietà specificata in una struttura CPropertyRestriction. |
| SAFEARRAY, SAFEARRAY2        | Contiene una matrice multidimensionale.                                                                                     |
| SAFEARRAYBOUND               | Rappresenta i limiti per una dimensione di una matrice specificata in una struttura SAFEARRAY.                                  |
| CFullPropSpec                | Contiene una specifica della proprietà.                                                                                     |
| CContentRestriction          | Contiene una stringa di cui trovare una corrispondenza per un valore di proprietà nella cache delle proprietà.                                                 |
| CKey                         | Contiene un valore della proprietà.                                                                                             |
| CInternalPropertyRestriction | Contiene un valore della proprietà da confrontare con un'operazione.                                                                  |
| CNatLanguageRestriction      | Contiene una corrispondenza di query in linguaggio naturale per una proprietà.                                                                |
| CNodeRestriction             | Contiene una matrice di nodi della struttura ad albero dei comandi che specificano le restrizioni per una query.                                       |
| COccRestriction              | Contiene la posizione di una parola in una frase.                                                                           |
| CPropertyRestriction         | Contiene un valore della proprietà da confrontare con un'operazione.                                                                  |
| CRangeRestriction            | Contiene una restrizione per un intervallo di valori.                                                                           |
| CScopeRestriction            | Contiene una restrizione sui file in cui eseguire la ricerca.                                                                    |
| CSort                        | Identifica una colonna da ordinare.                                                                                           |
| CSynRestriction              | Contiene una parola o i sinonimi per una frase di query.                                                                    |
| CVectorRestriction           | Contiene un'operazione ponderata o su un nodo della struttura ad albero del comando.                                                               |
| CWordRestriction             | Contiene una parola per una frase di query.                                                                                    |
| CRestriction                 | Contiene un nodo di un albero dei comandi di query.                                                                               |
| CColumnSet                   | Indica il numero di colonne da restituire.                                                                             |
| CCategorizationSet           | Contiene informazioni sul raggruppamento di un set di risultati della query.                                                     |
| CCategorizationSpec          | Contiene una definizione di categorie in cui verranno categorizzati i risultati della query.                                      |
| CDbColId                     | Contiene una colonna.                                                                                                     |
| CDbProp                      | Contiene una proprietà.                                                                                                   |
| CDbPropSet                   | Contiene un set di proprietà.                                                                                          |
| CPidMapper                   | Contiene una matrice di ID di proprietà che specificano le proprietà da restituire in un set di righe.                                     |
| CRowSeekAt                   | Contiene l'offset in corrispondenza del quale recuperare le righe in un messaggio CPMGetRowsIn                                                |
| CRowSeekAtRatio              | Identifica il punto in corrispondenza del quale iniziare il recupero per un messaggio CPMGetRowsIn.                                           |
| CRowSeekByBookmark           | Identifica i segnalibri da cui recuperare le righe per un messaggio CPMGetRowsIn.                                       |
| CRowSeekNext                 | Contiene il numero di righe da ignorare in un messaggio CPMGetRowsIn.                                                         |
| CRowsetProperties            | Contiene le informazioni di configurazione per una query.                                                                    |
| CSortSet                     | Contiene l'ordinamento di una query.                                                                                   |
| CTableColumn                 | Contiene una colonna per il messaggio CPMSetBindings.                                                                      |
| SERIALIZEDPROPERTYVALUE      | Contiene un valore serializzato.                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a>CBaseStorageVariant 2.2.1.1

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



 

**vType**: indicatore di tipo, che indica il tipo di vValue. DEVE essere uno dei valori di VARENUM specificati nella tabella seguente.



| Valore                 | Significato                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ vuoto (0x0000)    | vValue non è presente.                                                                                                               |
| VT \_ null (0x0001)     | vValue non è presente.                                                                                                               |
| VT \_ I1 (0x0010)       | Intero con segno a 1 byte.                                                                                                             |
| VT \_ Ui1 (0x0011)      | Intero senza segno a 1 byte.                                                                                                           |
| VT \_ I2 (0x0002)       | Intero con segno a 2 byte.                                                                                                             |
| VT \_ UI2 (0x0012)      | Intero senza segno a 2 byte.                                                                                                           |
| VT \_ bool (0x000B)     | Valore booleano; intero a 2 byte contenente 0x0000 (FALSE) o 0xFFFF (TRUE).                                                        |
| VT \_ I4 (0x0003)       | Intero con segno a 4 byte.                                                                                                             |
| VT \_ UI4 (0x0013)      | Intero senza segno a 4 byte.                                                                                                           |
| VT \_ R4 (0x0004)       | Numero a virgola mobile IEEE a 32 bit, come definito in \[ IEEE754 \] .                                                                     |
| VT \_ int (0x0016)      | Intero con segno a 4 byte.                                                                                                             |
| VT \_ uint (0x0017)     | Intero senza segno a 4 byte.                                                                                                           |
| \_Errore VT (0x000a)    | Unsigned Integer a 4 byte contenente un HRESULT, come specificato in \[ ms-sys \] .                                                         |
| VT \_ i8 (0x0014)       | Intero con segno a 8 byte.                                                                                                            |
| VT \_ UI8 (0x0015)      | Intero senza segno a 8 byte.                                                                                                          |
| VT \_ R8 (0x0005)       | Numero a virgola mobile IEEE a 64 bit come definito in \[ IEEE754 \] .                                                                      |
| \_CY VT (0x0006)       | Intero di complemento a due byte a 8 byte (ridimensionato di 10.000).                                                                               |
| \_Data VT (0x0007)     | Numero a virgola mobile a 64 bit che rappresenta il numero di giorni a partire da 00:00:00 il 31 dicembre 1899 (Coordinated Universal Time).     |
| FILETIME VT \_ (0x0040) | Intero a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi a partire dal 00:00:00 il 1 ° gennaio 1601 (Coordinated Universal Time). |
| \_Decimale VT (0x000E)  | Struttura decimale come specificato nella sezione 2.2.1.1.1.1.                                                                             |
| \_CLSID VT (0x0048)    | Valore binario a 16 byte contenente un GUID.                                                                                            |
| \_BLOB VT (0x0041)     | Un numero Unsigned Integer di byte di 4 byte nel BLOB, seguito da tale numero di byte di dati.                                           |
| \_BSTR VT (0x0008)     | Un numero Unsigned Integer di byte di 4 byte nella stringa, seguito da una stringa, come specificato di seguito in vValue.                       |
| VT \_ LPSTR (0x001E)    | Stringa ANSI con terminazione null.                                                                                                       |
| VT \_ LPWSTR (0x001F)   | Stringa Unicode Unicode con terminazione null \[ \] .                                                                                        |
| \_Variante VT (0x000C)  | CBaseStorageVariant. DEVE essere combinato con un modificatore di tipo di \_ matrice VT o \_ vettore VT.                                               |



 

Nella tabella seguente vengono specificati i modificatori di tipo per vType. I modificatori di tipo possono essere ORed binari con vType per modificare il significato di vValue per indicare che si tratta di uno dei due tipi di matrice possibili.



| Valore               | Significato                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Vettore VT (0x1000) | Se l'indicatore di tipo è combinato con \_ un vettore VT usando un operatore OR, vValue è una matrice conteggiata di valori del tipo indicato. Per informazioni dettagliate, vedere la sezione 2.2.1.1.1.2. <br/> Questo modificatore di tipo non deve essere combinato con i tipi seguenti: VT \_ int, VT \_ uint, VT \_ Decimal, VT \_ BLOB, VT \_ BLOB \_ Object.<br/>                                    |
| \_Array VT (0x2000)  | Se l'indicatore di tipo è combinato con \_ una matrice VT da un operatore OR, il valore è un SAFEARRAY (come specificato nella sezione 2.2.1.1.1.3) che contiene i valori del tipo indicato. <br/> Questo modificatore di tipo non deve essere combinato con i tipi seguenti: VT \_ i8, VT \_ UI8, VT \_ FILETIME, VT \_ CLSID, VT \_ BLOB, VT \_ BLOB \_ Object, VT \_ LPSTR, VT \_ LPWSTR. <br/> |



 

**vData1**: quando vType è un \_ numero decimale VT, il valore di questo campo viene specificato come campo di scala nella sezione 2.2.1.1.1.1. Per tutti gli altri vTypes, il valore deve essere impostato su 0x00.

**vData2**: quando vType è un \_ numero decimale VT, il valore di questo campo viene specificato come campo di segno nella sezione 2.2.1.1.1.1. Per tutti gli altri vTypes, il valore deve essere impostato su 0x00.

**vValue**: valore per l'operazione di corrispondenza. La sintassi deve essere come indicato nel campo vType.

Nella tabella seguente sono riepilogate le dimensioni per il campo vValue, a seconda del campo vType per i tipi di dati a lunghezza fissa. La dimensione è in byte.



| vType                                                   | Dimensione |
|---------------------------------------------------------|------|
| VT \_ i1, VT, \_ UI1                                        | 1    |
| VT \_ I2, VT \_ UI2, VT \_ bool                               | 2    |
| VT \_ I4, VT \_ UI4, VT \_ R4, VT \_ int, VT \_ uint, VT \_ Error   | 4    |
| VT \_ i8, VT \_ UI8, VT \_ R8, VT \_ CY, \_ Data VT, \_ FILETIME VT | 8    |
| \_decimale VT, \_ CLSID VT                                  | 16   |



 

Se vType è impostato su VT \_ BLOB, VT \_ BSTR o VT \_ LPSTR, la struttura di vValue viene specificata nel diagramma seguente:



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



 

**cbSize**: intero senza segno a 32 bit, che indica le dimensioni in byte del campo BlobData. Se vType è impostato su VT \_ BSTR o VT \_ LPSTR, cbSize deve essere impostato su 0x00000000 quando la stringa rappresentata è una stringa vuota.

**blobData**: deve essere di lunghezza cbSize in byte.

Per vType impostato su VT \_ BLOB, questo campo è dati BLOB binari opachi.

Per vType impostato su VT \_ BSTR, questo campo è un set di caratteri in un set di caratteri selezionato OEM. Il client e il server devono essere configurati in modo che dispongano di set di caratteri interoperativi (fuori banda del protocollo). Non è necessario che sia con terminazione null.

Per vType impostato su VT \_ LPSTR questo campo è una stringa di caratteri con terminazione null in un set di caratteri selezionato OEM. Il client e il server devono essere configurati in modo che dispongano di set di caratteri interoperativi (fuori banda del protocollo).

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

String (variabile, facoltativo)



 

**ccLen**: intero senza segno a 32 bit, che indica le dimensioni del campo stringa nei caratteri Unicode. DEVE essere impostato su 0x00000000 per una stringa vuota.

**stringa**: stringa Unicode con terminazione null.

### <a name="22111-cbasestoragevariant-structures"></a>Strutture CBaseStorageVariant di 2.2.1.1.1

Nella struttura CBaseStorageVariant vengono utilizzate le strutture seguenti.

### <a name="221111-decimal"></a>2.2.1.1.1.1 DECIMAL

DECIMAL viene usato per rappresentare un valore numerico esatto con una precisione fissa e una scala fissa.

Quando vType è impostato su VT \_ Decimal (0x0000E), i campi vData1 e vData2 di CBASESTORAGEVARIANT devono essere interpretati nel modo seguente:

**vData1**: numero di cifre a destra della virgola decimale. DEVE essere compreso tra 0 e 28.

**vData2**: il segno del valore numerico. Impostare su 0x00 se positivo, 0x80 se negativo.

Il formato del Campo vValue è:



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



 

**Hi32**: i 32 bit più alti dell'integer a 96 bit.

**Lo32**: 32 bit più bassi dell'integer a 96 bit.

**Mid32**: bit 32 intermedi dell'integer a 96 bit.

### <a name="221112-vt_vector"></a>vettore 2.2.1.1.1.2 VT \_

Il \_ vettore VT viene usato per passare matrici unidimensionali.



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



 

**vVectorElements**: intero senza segno a 32 bit, che indica il numero di elementi nel campo vVectorData.

**vVectorData**: matrice di elementi il cui tipo è indicato da vType con il bit 0x1000 cancellato. Le dimensioni di un singolo elemento a lunghezza fissa possono essere ottenute dalla tabella con tipo di dati a lunghezza fissa, come specificato nella sezione 2.2.1.1. La lunghezza di questo campo, in byte, può essere calcolata moltiplicando vVectorElements per la dimensione del singolo elemento.

Per i tipi di dati a lunghezza variabile vVectorData contiene una sequenza di tipi semplici con marshalling consecutivo in cui il tipo è indicato da vType con il bit 0x1000 cancellato. Questo include un caso speciale indicato da vType VT \_ array \| VT \_ Variant (ad esempio, 0x100C).

Gli elementi nel campo vVectorData devono essere separati da un byte di riempimento compreso tra 0 e 3 in modo che ogni elemento inizi in corrispondenza di un offset costituito da un multiplo di 4 byte a partire dall'inizio del messaggio che contiene la matrice. Se sono presenti byte di riempimento, il valore che contengono è arbitrario. Il contenuto dei byte di riempimento deve essere ignorato dal ricevitore.

Per una vType impostata su VT \_ array \| VT \_ Variant, il tipo per gli elementi in questa sequenza è CBaseStorageVariant.

### <a name="221113-safearray"></a>SAFEARRAY 2.2.1.1.1.3

SAFEARRAY viene utilizzato per passare matrici multidimensionali. La struttura contiene informazioni sulle dimensioni della matrice, oltre ai dati nella matrice.



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



 

**cDims**: intero senza segno a 16 bit, che indica il numero di dimensioni della matrice multidimensionale.

**fFeatures**: bit A 16 bit. I valori rappresentano le funzionalità, definite dalle applicazioni di livello superiore, e devono essere ignorate.

**cbElements**: un Unsigned Integer a 32 bit che specifica la dimensione di ogni elemento della matrice.

**Rgsabound**: matrice che contiene una struttura SAFEARRAYBOUND, come specificato nella sezione 2.2.1.1.1.4, per dimensione in SafeArray. Questa matrice contiene prima la dimensione più a sinistra e la dimensione più a destra.

**vdata**: vettore di elementi di cui è stato eseguito il marshalling di un determinato tipo, indicato da vType dell'oggetto che lo contiene CBaseStorageVariant, con il bit 0x2000 cancellato.

viene eseguito il marshalling di vData in modo analogo al \_ vettore VT, come specificato nella sezione 2.2.1.1.1.2, con la differenza che il numero di elementi non è archiviato davanti al vettore. Invece il numero di elementi viene calcolato moltiplicando il valore cElements con tutti i limiti di matrice sicuri specificati nel campo rgsabound. Gli elementi vengono archiviati in un vettore in ordine di dimensioni, scorrendo a partire dalla dimensione più a destra.

Il diagramma seguente rappresenta visivamente una matrice bidimensionale di esempio. La prima dimensione ha cElements uguale a 4 (rappresentato orizzontalmente) e lLbound è uguale a 0, mentre la seconda dimensione ha cElements uguale a 2 (rappresentata verticalmente) e lLbound uguale a 0.



|            |            |            |            |
|------------|------------|------------|------------|
| 0x00000001 | 0x00000002 | 0x00000003 | 0x00000005 |
| 0x00000007 | 0x00000011 | 0x00000013 | 0x00000017 |



 

Utilizzando il diagramma precedente, vData conterrà la sequenza seguente: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (per prima cosa scorrendo la dimensione più a destra e quindi incrementando la dimensione successiva). Il rgsabound precedente (che registra cElements e LBound) sarà: 0x00000004, 0x00000000, 0x00000002, 0x00000000.

### <a name="221114-safearraybound"></a>SAFEARRAYBOUND 2.2.1.1.1.4

La struttura SAFEARRAYBOUND rappresenta i limiti di una dimensione di SAFEARRAY o SAFEARRAY2. Il formato è:



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



 

**cElements**: Unsigned Integer a 32 bit, che specifica il numero di elementi nella dimensione.

**lLbound**: Unsigned Integer A 32 bit, che specifica il limite inferiore della dimensione.

### <a name="221115-safearray2"></a>2.2.1.1.1.5 SAFEARRAY2

SAFEARRAY2 viene utilizzato per passare matrici multidimensionali in SERIALIZEDPROPERTYVALUE. La struttura contiene informazioni sui limiti e sui dati.



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



 

**cDims**: intero senza segno a 32 bit, che indica il numero di dimensioni di SAFEARRAY2.

**Rgsabound**: matrice che contiene una struttura SAFEARRAYBOUND, come specificato nella sezione 2.2.1.1.1.4 per dimensione in SAFEARRAY2. Questa matrice contiene prima la dimensione più a sinistra e la dimensione più a destra.

**vdata**: vettore di elementi di cui è stato eseguito il marshalling di un determinato tipo, indicato da dwType dell'oggetto che lo contiene SERIALIZEDPROPERTYVALUE, con bit 0x2000 cancellato. Il formato di vData è uguale a quello specificato per il campo vData di SAFEARRAY nella sezione 2.2.1.1.1.3.

### <a name="2212-cfullpropspec"></a>CFullPropSpec 2.2.1.2

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



 

**\_ GUIDPROPSET**: GUID del set di proprietà a cui appartiene la proprietà.

**ulKind**: Unsigned Integer A 32 bit. Uno dei valori seguenti, che indica il contenuto di PrSpec.



| Valore                                            | Significato                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| \_LPWSTR PRSPEC<br/> 0x00000000<br/> | Il campo PrSpec specifica il numero di caratteri non NULL nel campo del nome della proprietà. |
| \_propid PRSPEC<br/> 0x00000001<br/>  | Il campo PrSpec specifica l'ID della proprietà (PROPID).                                     |



 

**PrSpec**: un Unsigned Integer a 32 bit con un significato come indicato dal Campo ulKind.

**Nome proprietà**: se ulKind è impostato su PRSPEC \_ propid, questo campo non deve essere presente. Se ulKind è impostato su PRSPEC \_ LPWSTR, questo campo deve contenere una matrice senza distinzione tra maiuscole e minuscole di PRSPEC caratteri Unicode non null, che contiene il nome della proprietà.

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



 

**\_ Property**: struttura CFullPropSpec, come specificato nella sezione 2.2.1.2. Questo campo indica la proprietà su cui eseguire un'operazione di corrispondenza.

**Padding1**: questo campo deve avere una lunghezza compresa tra 0 e 3 byte. La lunghezza di questo campo deve essere tale che il campo seguente inizia con un offset costituito da un multiplo di 4 byte a partire dall'inizio del messaggio che contiene la struttura. Se questo campo è presente, ad esempio length diverso da zero, il valore in esso contenuto è arbitrario. Il contenuto di questo campo deve essere ignorato dal ricevitore.

**CC**: Unsigned Integer a 32 bit, che specifica il numero di caratteri nel \_ campo pwcsPhrase.

**\_ pwcsPhrase**: stringa Unicode senza terminazione null che rappresenta la parola o la frase da confrontare per la proprietà. Questo campo non deve essere vuoto. Il campo CC contiene la lunghezza della stringa.

**Padding2**: questo campo deve avere una lunghezza compresa tra 0 e 3 byte. La lunghezza di questo campo deve essere tale che il campo seguente inizia con un offset costituito da un multiplo di 4 byte a partire dall'inizio del messaggio che contiene la struttura. Se questo campo è presente, ad esempio length diverso da zero, il valore in esso contenuto è arbitrario. Il contenuto di questo campo deve essere ignorato dal ricevitore.

**LCID**: Unsigned Integer a 32 bit, che indica le impostazioni locali di \_ pwcsPhrase, come specificato in \[ MS-GPSI \] appendice a.

**\_ ulGenerateMethod**: Unsigned Integer a 32 bit, che specifica il metodo da usare per la generazione di moduli Word alternativi



| Valore                                                       | Significato                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GENERA il \_ metodo \_ esatto<br/> 0x00000000<br/>    | Corrispondenza esatta.                                                                                                                                                                                                                                                                                      |
| \_prefisso del metodo generate \_<br/> 0x00000001 <br/>  | Corrispondenza prefisso.                                                                                                                                                                                                                                                                                     |
| GENERA il \_ metodo \_ flettere <br/> 0x00000002<br/> | Corrisponde a flessioni di una parola. Una flessione di una parola è una variante della parola radice nella stessa parte del discorso che è stata modificata in base alle regole linguistiche di una determinata lingua. Ad esempio, le flessioni del verbo "swim" in inglese includono "swim", "swims", "swimming" e "nuotate". |



 

### <a name="2214-ckey"></a>CKey 2.2.1.4

La struttura CKey contiene un valore della proprietà.



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

CB

BUF (variabile)



 

**Propid**: Unsigned Integer a 32 bit, che rappresenta l'ID della proprietà, come illustrato nella sezione 1.8.1. I valori noti sono:



| Valore      | Significato                                                 |
|------------|---------------------------------------------------------|
| 0xFFFFFFFF | Rappresenta un ID di proprietà non valido e non deve essere utilizzato. |
| 0xFFFFFFFE | Rappresenta un ID di proprietà non valido e non deve essere utilizzato. |
| 0x00000000 | Rappresenta qualsiasi ID di proprietà.                             |



 

**CB**: Unsigned Integer a 32 bit contenente la lunghezza di BUF, in byte.

**BUF**: sequenza di byte che rappresenta il valore della proprietà.

### <a name="2215-cinternalpropertyrestriction"></a>2.2.1.5 CInternalPropertyRestriction

La struttura CInternalPropertyRestriction contiene un valore della proprietà da confrontare con un'operazione.



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

\_RelOp

\_pid

\_prval (variabile)

restrictionPresent

nextRestriction (variabile)



 

**\_ RelOp**: intero a 32 bit che specifica la relazione da eseguire sulla proprietà. DEVE essere uno dei valori seguenti:



| Valore                 | Significato                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| 0x00000000 PRLT       | Confronto di minore di.                                                                                           |
| 0x00000001 PRLE       | Confronto di minore o uguale a.                                                                               |
| 0x00000002 PRGT       | Confronto maggiore di.                                                                                        |
| 0x00000003 PRGE       | Confronto maggiore di o uguale a.                                                                            |
| 0x00000004 PREQ       | Confronto di uguaglianza.                                                                                           |
| 0x00000005 PRNE       | Confronto non uguale.                                                                                           |
| PRRE 0x00000006       | Confronto di espressioni regolari.                                                                                  |
| PRAllBits 0x00000007  | Operatore AND bit per bit che restituisce l'operando destro.                                                                     |
| 0x00000008 PRSomeBits | Operatore AND bit per bit che restituisce un valore diverso da zero.                                                                       |
| 0x00000100 PRAll      | L'operazione deve essere eseguita su una colonna di un set di righe ed è true solo se l'operazione è true per tutte le righe. |
| PRAny 0x00000200      | L'operazione deve essere eseguita su una colonna di un set di righe e è true se l'operazione è true per qualsiasi riga.       |



 

**\_ pid**: Unsigned Integer a 32 bit, che rappresenta l'ID della proprietà (vedere propid nella sezione 2.2.1.4).

**\_ Prval**: CBaseStorageVariant che contiene il valore da correlare alla proprietà.

**restrictionPresent**: valore di byte che indica se il campo nextRestriction è presente. DEVE essere impostato su 0x00 o 0x01. Se impostato su 0x01, restrictionPresent indica che è presente il campo nextRestriction. Se impostato su 0x00, restrictionPresent indica che il campo nextRestriction non è presente.

**nextRestriction**: struttura CRestriction, come specificato nella sezione 2.2.1.16, che specifica un'ulteriore restrizione.

### <a name="2216-cnatlanguagerestriction"></a>2.2.1.6 CNatLanguageRestriction

La struttura CNatLanguageRestriction contiene una corrispondenza di **query in linguaggio naturale** per una proprietà.



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

\_riempimento di \_ CC (variabile)

Cc

\_pwcsPhrase (variabile)

...

\_riempimento \_ LCID (variabile)

LCID



 

**\_ Property**: struttura CFullPropSpec, come specificato nella sezione 2.2.1.3. Questo campo indica la proprietà sulla quale eseguire l'operazione di corrispondenza.

**\_ riempimento \_ CC**: questo campo deve avere una lunghezza compresa tra 0 e 3 byte. La lunghezza di questo campo deve essere tale che il campo seguente inizia con un offset costituito da un multiplo di 4 byte a partire dall'inizio del messaggio che contiene la struttura. Se questo campo è presente, ad esempio length diverso da zero, il valore in esso contenuto è arbitrario. Il contenuto di questo campo deve essere ignorato dal ricevitore.

**CC**: A 32 bit unsigned integer. Numero di caratteri nel \_ campo pwcsPhrase.

**\_ pwcsPhrase**: stringa Unicode senza terminazione null che rappresenta la parola o la frase da confrontare per la proprietà. NON deve essere vuoto. Il campo CC contiene la lunghezza della stringa.

**\_ riempimento \_ LCID**: questo campo deve avere una lunghezza compresa tra 0 e 3 byte. La lunghezza di questo campo deve essere tale che il campo seguente inizia con un offset costituito da un multiplo di 4 byte a partire dall'inizio del messaggio che contiene la struttura. Se questo campo è presente, ad esempio length diverso da zero, il valore in esso contenuto è arbitrario. Il contenuto di questo campo deve essere ignorato dal ricevitore.

**LCID**: Unsigned Integer a 32 bit che indica le impostazioni locali di \_ pwcsPhrase, come specificato in \[ MS-GPSI \] appendice a.

### <a name="2217-cnoderestriction"></a>2.2.1.7 CNodeRestriction

La struttura CNodeRestriction contiene una matrice di nodi della **struttura ad albero dei comandi** che specificano le restrizioni per la query.



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



 

**\_ CNode**: un Unsigned Integer a 32 bit che specifica il numero di strutture CRestriction contenute nel \_ campo paNode.

**\_ paNode**: matrice di strutture CRestriction. Le strutture nella matrice devono essere separate da un byte di riempimento compreso tra 0 e 3 in modo che ogni struttura inizi in corrispondenza di un offset costituito da un multiplo di 4 byte a partire dall'inizio del messaggio che contiene la matrice. Se sono presenti byte di riempimento, il valore che contengono è arbitrario. Il contenuto dei byte di riempimento deve essere ignorato dal ricevitore.

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

\_ETag

\_cPrevNoiseWords

\_cNextNoiseWords



 

**\_ OCC**: un Unsigned Integer a 32 bit che specifica l'offset della parola in una stringa di query, in unità di parole. Una parola, come usato in questa specifica, è un'unità di linguaggio in tutte le impostazioni locali che portano il significato.

**\_ cPrevNoiseWords**: un Unsigned Integer a 32 bit contenente il numero di **parole non significative** che si verificano tra la parola e la parola precedente nella frase.

**\_ cNextNoiseWords**: un Unsigned Integer a 32 bit contenente il numero di parole non significative che si verificano tra la parola e la parola successiva nella frase.

### <a name="2219-cpropertyrestriction"></a>2.2.1.9 CPropertyRestriction

La struttura CPropertyRestriction contiene un valore della proprietà da confrontare con un'operazione.



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

\_RelOp

\_Proprietà (variabile)

\_prval (variabile)



 

**\_ RelOp**: una Unsigned Integer a 32 bit che specifica la relazione da eseguire sulla proprietà. DEVE essere uno dei valori seguenti.



| Valore                 | Significato                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| 0x00000000 PRLT       | Confronto di minore di.                                                                                           |
| 0x00000001 PRLE       | Confronto di minore o uguale a.                                                                               |
| 0x00000002 PRGT       | Confronto maggiore di.                                                                                        |
| 0x00000003 PRGE       | Confronto maggiore di o uguale a.                                                                            |
| 0x00000004 PREQ       | Confronto di uguaglianza.                                                                                           |
| 0x00000005 PRNE       | Confronto non uguale.                                                                                           |
| PRRE 0x00000006       | Confronto di espressioni regolari.                                                                                  |
| PRAllBits 0x00000007  | Operatore AND bit per bit che restituisce l'operando destro.                                                                     |
| 0x00000008 PRSomeBits | Operatore AND bit per bit che restituisce un valore diverso da zero.                                                                       |
| 0x00000100 PRAll      | L'operazione deve essere eseguita su una colonna di un set di righe ed è true solo se l'operazione è true per tutte le righe. |
| PRAny 0x00000200      | L'operazione deve essere eseguita su una colonna di un set di righe e è true se l'operazione è true per qualsiasi riga.       |



 

**\_ Property**: una struttura CFullPropSpec, come specificato nella sezione 2.2.1.2, che indica la proprietà su cui eseguire un'operazione di corrispondenza.

**\_ prval**: struttura CBaseStorageVariant, come specificato nella sezione 2.2.1.1, che contiene il valore da correlare alla proprietà.

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

\_Avvio della pagina (variabile)

\_keyEnd (variabile)



 

**\_ Start di avvio**: una struttura CKey, come specificato nella sezione 2.2.1.4, che contiene l'inizio dell'intervallo.

**\_ keyEnd**: struttura CKey che contiene la fine dell'intervallo.

### <a name="22111-cscoperestriction"></a>2.2.1.11 CScopeRestriction

La struttura CScopeRestriction contiene una restrizione sui file da cercare



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

\_spaziatura interna (variabile)

\_lunghezza

\_fRecursive

\_fVirtual



 

**CcLowerPath**: Unsigned Integer a 32 bit contenente il numero di caratteri Unicode nel \_ campo lowerPath.

**\_ lowerPath**: stringa Unicode senza terminazione null che rappresenta il **percorso** in cui la query deve essere limitata. Il campo CcLowerPath contiene la lunghezza della stringa.

**\_ spaziatura interna**: questo campo deve avere una lunghezza compresa tra 0 e 3 byte. La lunghezza di questo campo deve essere tale che il campo seguente inizia con un offset costituito da un multiplo di 4 byte a partire dall'inizio del messaggio che contiene la struttura. Se questo campo è presente, ad esempio length diverso da zero, il valore in esso contenuto è arbitrario. Il contenuto di questo campo deve essere ignorato dal ricevitore.

**\_ length**: Unsigned Integer a 32 bit contenente la lunghezza di \_ LowerPath, in caratteri Unicode. DEVE corrispondere al valore di CcLowerPath.

**\_ fRecursive**: Unsigned Integer A 32 bit. DEVE essere impostato su 0x00000001 o 0x00000000. Se impostato su 0x00000001, il server deve esaminare in modo ricorsivo tutte le sottodirectory del percorso. Se impostato su 0x00000000, il server non deve esaminare le sottodirectory.

**\_ fVirtual**: Unsigned Integer A 32 bit. DEVE essere impostato su 0x00000001 o 0x00000000. Se è impostato su 0x00000001, \_ lowerPath è un percorso virtuale, ovvero il Uniform Resource Locator (URL) associato a una directory fisica nel file System) per un sito Web. Se impostato su 0x00000000, \_ lowerPath è un percorso file System.

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



 

**pidColumn**: Unsigned Integer A 32 bit. Numero della colonna in base alla quale eseguire l'ordinamento.

**dworder**: Unsigned Integer A 32 bit. DEVE essere uno dei valori seguenti, che specifica la modalità di ordinamento in base alla colonna.



| Valore                        | Significato                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| QUERY \_ SORTASCEND 0x00000000 | Le righe devono essere ordinate in ordine crescente in base ai valori nella colonna specificata.  |
| QUERY \_ discendente 0x00000001    | Le righe devono essere ordinate in ordine decrescente in base ai valori nella colonna specificata. |



 

**impostazioni locali**: un Unsigned Integer a 32 bit che indica le impostazioni locali, come specificato nell' \[ appendice MS-GPSI \] , della colonna.

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

\_Matrice di matrici (variabile)

\_isRange



 

**Restrizione**: struttura COccRestriction che specifica la posizione della parola.

**CKEY**: un Unsigned Integer a 32 bit che specifica il numero di elementi nella \_ matrice di matrici di matrici.

**\_ dataArray**: matrice di strutture CKey che specifica una parola e i relativi sinonimi.

IsMatch **\_ : se** è impostato su 0x01, le chiavi sono prefissi per la corrispondenza. Se impostato su 0x00, le chiavi corrispondono ai valori esatti corrispondenti. \_l'intervallo di valori non deve essere impostato su nessun altro valore.

### <a name="22114-cvectorrestriction"></a>2.2.1.14 CVectorRestriction

La struttura CVectorRestriction contiene un'operazione ponderata o su un nodo della struttura ad albero dei comandi.



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

\_Pres (variabile)

...

\_spaziatura interna (variabile)

\_ulRankMethod



 

**\_ pres**: albero dei comandi CNodeRestriction su cui deve essere eseguita un'operazione di classificazione o.

**\_ spaziatura interna**: questo campo deve avere una lunghezza compresa tra 0 e 3 byte. La lunghezza di questo campo deve essere tale che il campo seguente inizia con un offset costituito da un multiplo di 4 byte a partire dall'inizio del messaggio che contiene la struttura. Se questo campo è presente, ad esempio length diverso da zero, il valore in esso contenuto è arbitrario. Il contenuto di questo campo deve essere ignorato dal ricevitore.

**\_ ulRankMethod**: un Unsigned Integer a 32 bit che specifica un algoritmo di classificazione. DEVE essere impostato su uno dei valori seguenti.



| Valore                            | Significato                                       |
|----------------------------------|-----------------------------------------------|
| \_Dimensioni \_ minime vettore 0x00000000     | Usare l'algoritmo minimo \[ Salton \] .             |
| \_ \_ Numero massimo di 0x00000001 di rango vettoriale     | Usare l'algoritmo Max \[ Salton \] .             |
| \_ \_ 0x00000002 Inner Rank vettore   | Usare l'algoritmo prodotto interno \[ Salton \] .       |
| VECTOR \_ Rank \_ dadi 0x00000003    | Usare l'algoritmo del coefficiente dadi \[ \] .    |
| VECTOR \_ Rank \_ JACCARD 0x00000004 | Usare l'algoritmo coefficiente Jaccard di \[ Salton \] . |



 

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

\_chiave (variabile)

\_isRange



 

**restrizione**: struttura COccRestriction che specifica la posizione della parola.

**\_ Key**: struttura CKey che specifica una parola.

IsMatch **\_ : se** è impostato su 0x01, la chiave corrisponde a un prefisso. Se impostato su 0x00, la chiave è un valore esatto per la corrispondenza. \_l'intervallo di valori non deve essere impostato su un altro valore.

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



 

**\_ ulType**: Unsigned Integer a 32 bit che indica il tipo di restrizione utilizzato per il nodo della struttura ad albero dei comandi. DEVE essere impostato su uno dei valori seguenti.



| Valore                    | Significato                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| 0x00000000 RTNone        | Il nodo rappresenta una parola non significativa in una query vettoriale.                                         |
| 0x00000001 RTAnd         | Il nodo contiene un CNodeRestriction su cui eseguire un'operazione AND logica. |
| 0x00000002 RTOr          | Il nodo contiene un CNodeRestriction su cui deve essere eseguita un'operazione OR logica.  |
| 0x00000003 RTNot         | Il nodo contiene un CRestriction su cui deve essere eseguita un'operazione NOT.             |
| 0x00000004 RTContent     | Il nodo contiene un CContentRestriction.                                                    |
| 0x00000005 RTProperty    | Il nodo contiene un CPropertyRestriction.                                                   |
| RTProximity 0x00000006   | Il nodo contiene un CNodeRestriction su cui deve essere eseguita una classificazione di prossimità.     |
| RTVector 0x00000007      | Il nodo contiene un CVectorRestriction.                                                     |
| 0x00000008 RTNatLanguage | Il nodo contiene un CNatLanguageRestriction.                                                |
| RTScope 0x00000009       | Il nodo contiene un CScopeRestriction.                                                      |
| PRAny 0xFFFFFFFA         | Il nodo contiene un CInternalPropertyRestriction.                                           |
| RTRange 0xFFFFFFFC       | Il nodo contiene un CRangeRestriction.                                                      |
| RTPhrase 0xFFFFFFFD      | Il nodo contiene un CNodeRestriction su cui deve essere eseguita una frase corrispondente.          |
| 0xFFFFFFFE RTSynonym     | Il nodo contiene un CSynRestriction.                                                        |
| RTWord 0xFFFFFFFF        | Il nodo contiene un CWordRestriction.                                                       |



 

**Weight**: Unsigned Integer A 32 bit che rappresenta il peso del nodo. Weight indica l'importanza del nodo rispetto ad altri nodi nell'albero dei comandi di query. I valori di peso più elevati sono più importanti.

**Restrizione**: tipo di restrizione per il nodo della struttura ad albero dei comandi. La sintassi deve essere indicata dal \_ campo ulType.

### <a name="22117-ccolumnset"></a>CColumnSet 2.2.1.17

La struttura CColumnSet specifica i numeri di colonna da restituire. Questa struttura viene sempre utilizzata in riferimento a una struttura CPidMapper specifica (Section 2.2.1.23).



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

indici (variabile)



 

**count**: un Unsigned Integer a 32 bit che specifica il numero di elementi nella matrice di indici.

**indici**: matrice di interi senza segno a 4 byte che rappresenta gli indici in base zero nella matrice aPropSpec nella struttura CPidMapper corrispondente.

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

Categorie (variabile)



 

**count**: Unsigned Integer a 32 bit contenente il numero di elementi nella matrice di categorie.

**categorie**: matrice di strutture CCategorizationSpec che specificano il raggruppamento della query.

### <a name="22119-ccategorizationspec"></a>CCategorizationSpec 2.2.1.19

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



 

**\_ csColumns**: struttura CColumnSet che indica le colonne in base alle quali raggruppare la query.

**\_ ulCategType**: Unsigned Integer A 32 bit. DEVE essere impostato su 0x00000000.

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



 

**eKind**: deve essere impostato su uno dei valori riportati di seguito che indica il contenuto di GUID e vValue.



| Valore                            | Significato                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| \_Nome GUID dbkind \_ 0x00000000    | vString contiene un nome di proprietà.                                                                               |
| \_GUID dbkind \_ propid 0x00000001  | ulId contiene un intero a 4 byte che indica l'ID della proprietà.                                                      |
| DBKIND \_ PGUID \_ nome 0x00000003   | vString contiene un nome di proprietà. Questo valore deve essere considerato uguale al \_ nome GUID di dbkind \_ .                    |
| DBKIND \_ PGUID \_ propid 0x00000004 | ulId contiene un intero a 4 byte che indica l'ID della proprietà. Questo valore deve corrispondere al \_ GUID dbkind \_ propid. |



 

**GUID**: GUID della proprietà.

**ulId**: se EKIND è dbkind \_ GUID \_ propid o dbkind PGUID propid \_ \_ , questo campo contiene un Unsigned Integer, specificando l'ID della proprietà. Se eKind è DBKIND \_ GUID \_ Name o dbkind \_ PGUID \_ Name, questo campo contiene un Unsigned Integer specificando il numero di caratteri Unicode contenuti nel campo VString.

**VString**: stringa Unicode senza terminazione null che rappresenta il nome della proprietà. È necessario ometterlo, a meno che il campo eKind non sia impostato su DBKIND \_ GUID \_ Name o dbkind \_ PGUID \_ .

### <a name="22121-cdbprop"></a>2.2.1.21 CDbProp

La struttura CDbProp contiene una proprietà.



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



 

**DBPROPID**: Unsigned Integer A 32 bit, che indica l'ID della proprietà.

**DBPROPOPTIONS** : deve essere impostato su 0x00000000.

**DBPROPSTATUS**: deve essere impostato su 0x00000000.

**colid**: struttura CDbColId, come specificato nella sezione 2.2.1.20, che indica la colonna a cui viene applicata la proprietà.

**vValue**: CBaseStorageVariant che contiene il valore della proprietà.

### <a name="221211-properties"></a>Proprietà di 2.2.1.21.1

In questa sezione vengono illustrate in dettaglio le proprietà utilizzate da CISP. Queste proprietà sono raggruppate in tre set di proprietà, ident 2.2.1.21.1 in Unified nel campo guidPropertySet della struttura CDbPropSet (Section 2.2.1.22).

La tabella seguente elenca le proprietà che fanno parte del set di \_ proprietà DBPROPSET FSCIFRMWRK \_ ext.



| Valore                                  | Significato                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| DBPROP \_ \_ nome catalogo ci \_ 0x00000002   | Specifica il nome del catalogo o dei cataloghi su cui eseguire una query. Il valore deve essere un VT \_ LPWSTR o un \_ vettore \| VT \_ LPWSTR                                   |
| DBPROP \_ ci \_ include \_ ambiti 0x00000003 | Specifica uno o più percorsi da includere nella query. Il valore deve essere un \_ LPWSTR VT o un \_ LPWSTR VT Vector VT \| \_ .                                 |
| DBPROP \_ \_ flag di ambito ci \_ 0x00000004    | Specifica il modo in cui devono essere gestiti i percorsi specificati dalla \_ \_ proprietà degli ambiti di inclusione DBPROP ci \_ . Il valore deve essere un VT \_ I4 o un \_ vettore \| VT \_ i4. |
| \_Tipo di \_ query ci DBPROP \_ 0x00000007     | Specifica il tipo di query. CDbColId deve essere impostato su DB \_ NULLID.                                                                               |



 

La tabella seguente elenca i flag per la \_ proprietà dei \_ flag di ambito ci DBPROP \_ :



| Valore                     | Significato                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eseguire QUERY \_ 0x01 approfondite          | Se impostato, indica che i file nella directory scope e in tutte le sottodirectory sono inclusi nei risultati. Se è chiaro, nei risultati vengono inclusi solo i file nella directory dell'ambito. NON devono essere combinati con una QUERY \_ approfondita. |
| QUERY \_ \_ percorso virtuale 0x02 | Se impostato, indica che l'ambito è un percorso virtuale. Se chiaro, indica che l'ambito è una directory fisica.                                                                                                         |



 

Nella tabella seguente sono elencati i tipi di query per \_ la \_ Proprietà tipo di query ci DBPROP \_ :



| Valore                     | Significato                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| 0x00000000 CiNormal       | Query normale.                                                                                                   |
| 0x00000001 CiVirtualRoots | La query richiede un elenco delle radici virtuali del catalogo. Questo valore richiede privilegi amministrativi. |
| 0x00000003 CiProperties   | La query richiede un elenco di tutte le proprietà supportate dal servizio di indicizzazione.                            |
| 0x00000004 CiAdminOp      | La query è un'operazione amministrativa. Questo valore richiede privilegi amministrativi.                           |



 

La tabella seguente elenca le proprietà che fanno parte del set di \_ Proprietà QUERYEXT di DBPROPSET.



| Valore                                      | Significato                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DBPROP \_ USECONTENTINDEX 0x00000002         | Specifica il modo in cui il servizio di indicizzazione è in grado di gestire query lente. Il valore deve essere un \_ bool VT. Se TRUE, il server è autorizzato a eseguire l'errore di queste query.                                                                                    |
| DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003 | Indica se il servizio di indicizzazione deve eseguire la rimozione dei risultati. Se TRUE, il server deve prendere in considerazione l'esecuzione del taglio dei risultati in modo da ottimizzare il tempo di risposta per il client. Il valore deve essere un \_ bool VT.             |
| DBPROP \_ USEEXTENDEDDBTYPES 0x00000004      | Indica se il client supporta i \_ tipi di dati vettoriali VT. Se TRUE, il client supporta il \_ vettore VT; se è false, il server deve convertire i \_ tipi di dati vettoriali VT in tipi di \_ dati matrice VT.  Il valore deve essere un \_ bool VT. |
| DBPROP \_ FIRSTROWS 0x00000007               | Indica le corrispondenze di riga da restituire. Se TRUE, il server deve restituire il primo set di righe corrispondenti. Se FALSE, verranno restituite le righe corrispondenti migliori. Il valore deve essere un \_ bool VT.                                             |



 

La tabella seguente elenca le proprietà che fanno parte del set di \_ proprietà DBPROPSET CIFRMWRKCORE \_ ext.



| Valore/DBPROPID                 | Significato                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| \_0x00000002 del computer DBPROP       | Specifica i nomi dei computer in cui deve essere elaborata una query. Il valore deve essere VT \_ BSTR o VT \_ Array VT \| \_ BSTR. |
| \_ \_ 0x00000003 CLSID client DBPROP | Specifica una costante di connessione per il servizio di indicizzazione. Il valore deve essere un \_ CLSID VT contenente 0x2A4880706FD911D0A80800A0C906241A.  |



 

### <a name="22122-cdbpropset"></a>CDbPropSet 2.2.1.22

La struttura CDbPropSet contiene un set di proprietà. Si noti che il primo campo è a dimensione fissa, ma potrebbe non essere allineato a un offset che corrisponde a un multiplo di 4 byte dall'inizio del messaggio che contiene la struttura. Tuttavia, il campo cProperties è allineato come tale, quindi il formato viene illustrato nel modo seguente:



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

\_spaziatura interna (variabile)

cProperties

aProps (variabile)



 

**guidPropertySet**: GUID che identifica il set di proprietà. DEVE essere impostato sul form binario corrispondente a uno dei valori seguenti (visualizzato nel formato di rappresentazione di stringa), che identifica il set di proprietà delle proprietà contenute nel campo aProps.



| Valore/GUID                                                                              | Nome                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| DBPROPSET \_ FSCIFRMWRK \_ ext<br/> {A9BD1526-6A80-11D0-8C9D-0020AF1D740E}<br/>   | Set di proprietà del Framework dell'indice di contenuto del file System |
| \_QUERYEXT DBPROPSET<br/> {A7AC77ED-F8D7-11CE-A798-0020F8008025}<br/>          | Set di proprietà dell'estensione di query                     |
| DBPROPSET \_ CIFRMWRKCORE \_ ext<br/> {AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}<br/> | Set di proprietà di base dell'indice di contenuto        |



 

**\_ spaziatura interna**: questo campo deve avere una lunghezza compresa tra 0 e 3 byte. La lunghezza di questo campo deve essere tale che il campo seguente inizia con un offset costituito da un multiplo di 4 byte a partire dall'inizio del messaggio che contiene la struttura. Se questo campo è presente (ovvero, lunghezza diversa da zero), il valore in esso contenuto è arbitrario. Il contenuto di questo campo deve essere ignorato dal ricevitore.

**cProperties**: Unsigned Integer a 32 bit contenente il numero di elementi nella matrice aProps.

**aProps**: matrice di strutture CDbProp, come specificato nella sezione 0, che contiene le proprietà. Le strutture nella matrice devono essere separate da un byte di riempimento compreso tra 0 e 3 in modo che ogni struttura inizi in corrispondenza di un offset costituito da un multiplo di 4 byte a partire dall'inizio del messaggio che contiene la matrice. Se sono presenti byte di riempimento, il valore che contengono è arbitrario. Il contenuto dei byte di riempimento deve essere ignorato dal ricevitore.

### <a name="22123-cpidmapper"></a>2.2.1.23 CPidMapper

La struttura CPidMapper contiene una matrice di ID di proprietà che specificano le proprietà da restituire in un set di righe.



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

... variabile



 

**count**: Unsigned Integer a 32 bit contenente il numero di elementi nella matrice aPropSpec.

**aPropSpec**: matrice di strutture CFullPropSpec che indica le proprietà da restituire. Le strutture nella matrice devono essere separate da un byte di riempimento compreso tra 0 e 3 in modo che ogni struttura disponga di un allineamento a 4 byte dall'inizio di un messaggio. Tali byte di riempimento possono essere qualsiasi valore arbitrario e devono essere ignorati alla ricezione.

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



 

**\_ hRegion**: deve essere impostato su 0x00000000 e deve essere ignorato.

**\_ cskip**: Unsigned Integer a 32 bit contenente il numero di righe da ignorare nel set di righe.

**\_ bmkOffset**: valore a 32 bit che rappresenta l'handle del **segnalibro** che indica la posizione iniziale dalla quale ignorare il numero di righe specificato in \_ cskip, prima di iniziare il recupero.

### <a name="22125-crowseekatratio"></a>2.2.1.25 CRowSeekAtRatio

La struttura CRowSeekAtRatio identifica il punto in corrispondenza del quale iniziare il recupero per un messaggio CPMGetRowsIn.



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



 

**CiTblChapt**: Unsigned Integer a 32 bit che indica il capitolo del set di righe da cui recuperare le righe.

**\_ hRegion**: deve essere impostato su 0x00000000 e deve essere ignorato.

**\_ ulNumerator**: intero senza segno a 32 bit che rappresenta il numeratore del rapporto di righe nel capitolo da cui iniziare il recupero.

**\_ ulDenominator**: intero senza segno a 32 bit che rappresenta il denominatore del rapporto di righe nel capitolo da cui iniziare il recupero. DEVE essere maggiore di zero.

### <a name="22126-crowseekbybookmark"></a>2.2.1.26 CRowSeekByBookmark

La struttura CRowSeekByBookmark identifica i segnalibri da cui iniziare il recupero delle righe per un messaggio CPMGetRowsIn.



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

\_cBookmarks

\_maxRet

\_cValidRet

\_aBookmarks (variabile)

\_ascRet (variabile)



 

**\_ hRegion**: deve essere impostato su 0x00000000 e deve essere ignorato.

**\_ cBookmarks**: intero senza segno a 32 bit che rappresenta il numero di elementi nella \_ matrice aBookmarks.

**\_ maxRet**: intero senza segno a 32 bit che rappresenta il numero di elementi nella \_ matrice ascRet.

**\_ cValidRet**: intero senza segno a 32 bit che rappresenta il numero di elementi nella \_ matrice ascRet che sono validi. Nella matrice sono stati definiti elementi validi, mentre gli elementi non validi sono indefiniti.

**\_ aBookmarks**: matrice di handle di segnalibro, rappresentati da 4 byte, ottenuti da un messaggio CPMGetRowsOut.

**\_ ascRet**: matrice di valori HRESULT. Quando CRowSeekByBookMark viene inviato come parte della richiesta CPMGetRowsIn, il numero di voci nella matrice deve essere uguale a \_ cBookMarks. Quando vengono inviati dal client, i valori devono essere impostati su zero e il server deve ignorare il contenuto della matrice. Quando viene inviato dal server (come parte del messaggio CPMGetRowsOut), i valori nella matrice indicano lo stato dei risultati per ogni recupero di riga.

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

\_hRegion

\_cskip



 

**CiTblChapt**: intero senza segno a 32 bit che specifica il capitolo del set di righe da cui recuperare le righe.

**\_ hRegion**: deve essere impostato su 0x00000000 e deve essere ignorato.

**\_ cskip**: intero senza segno a 32 bit che rappresenta il numero di righe da ignorare nel set di righe.

### <a name="22128-crowsetproperties"></a>2.2.1.28 CRowsetProperties

La struttura CRowsetProperties contiene le informazioni di configurazione per una query.



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



 

**\_ uBooleanOptions**: i 3 bit meno significativi di questo campo devono contenere uno dei tre valori seguenti:



| Valore                  | Significato                                                             |
|------------------------|---------------------------------------------------------------------|
| 0x00000001 eSequential | Il cursore può essere spostato solo in un altro passaggio.                              |
| 0x00000003 eLocatable  | È possibile spostare il cursore in qualsiasi posizione.                            |
| eScrollable 0x00000007 | È possibile spostare il cursore in qualsiasi posizione e recuperarlo in qualsiasi direzione. |



 

I bit rimanenti possono essere cancellati o essere impostati in modo logico o combinato tra i valori seguenti:



| Valore                     | Significato                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| 0x00000008 eAsynchronous  | Il client non attende il completamento dell'esecuzione.                                                          |
| eFirstRows 0x00000080     | Restituisce le prime righe rilevate, non le corrispondenze migliori.                                                    |
| eHoldRows 0x00000200      | Il server non deve eliminare righe finché il client non viene eseguito con una query.                                     |
| eChaptered 0x00000800     | Il set di righe supporta i capitoli.                                                                               |
| 0x00001000 eUseCI         | Rispondere solo alla query dall'indice, non al file system.                                                  |
| 0x00002000 eDeferTrimming | Il servizio di indicizzazione consiste nel considerare l'ottimizzazione del tempo di risposta al client quando si esegue la rimozione dei risultati. |



 

**\_ ulMaxOpenRows**: intero senza segno a 32 bit. Deve essere impostato su 0x00000000. Non usato e deve essere ignorato.

**\_ ulMemoryUsage**: intero senza segno a 32 bit. Deve essere impostato su 0x00000000. Non usato e deve essere ignorato.

**\_ cMaxResults**: un Unsigned Integer a 32 bit che specifica il numero massimo di righe da restituire per la query.

**\_ cCmdTimeout**: Unsigned Integer a 32 bit, che specifica il numero di secondi di timeout di una query e di interruzione automatica, dal momento che la query inizia l'esecuzione nel server. Il valore 0x00000000 indica che non è previsto il timeout della query.

### <a name="22129-crowvariant"></a>2.2.1.29 CRowVariant

La struttura CRowVariant contiene la parte a dimensione fissa di un tipo di dati a lunghezza variabile archiviato nel messaggio CPMGetRowsOut.



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

Reserved1

reserved2

Offset (facoltativo)



 

**vType**: indicatore di tipo, che indica il tipo di vValue. DEVE essere uno dei valori VARENUM specificati nella sezione 2.2.1.1.

**Reserved1**: non utilizzato. Il valore può essere impostato su qualsiasi valore arbitrario ed è necessario ignorarlo alla ricezione.

**Reserved2**: non utilizzato. Il valore può essere impostato su qualsiasi valore arbitrario ed è necessario ignorarlo alla ricezione.

**Offset**: offset ai dati a lunghezza variabile (ad esempio, una stringa).  DEVE essere un valore a 32 bit (lungo 4 byte) se vengono usati offset a 32 bit (in base alle regole nella sezione 2.2.3.16) o un valore di 64 byte (lungo 8 byte) se vengono usati offset a 64 bit.

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



 

**count**: un Unsigned Integer a 32 bit che specifica il numero di elementi in SortArray.

**SortArray**: matrice di strutture CSort che descrive l'ordine in cui ordinare i risultati della query. Le strutture nella matrice devono essere separate da un byte di riempimento compreso tra 0 e 3 in modo che ogni struttura disponga di un allineamento a 4 byte dall'inizio di un messaggio. Tali byte di riempimento possono essere qualsiasi valore arbitrario e devono essere ignorati alla ricezione.

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

Campo PROPSPEC

... variabile

vType

ValueUsed

\_padding1 (facoltativo)

ValueOffset (facoltativo)

ValueSize (facoltativo)

StatusUsed

\_padding2 (facoltativo)

StatusOffset (facoltativo)

LengthUsed

\_padding3 (facoltativo)

LengthOffset (facoltativo)



 

**Campo PROPSPEC**: struttura CFullPropSpec come specificato nella sezione 2.2.1.3.

**vType**: specifica il tipo di valore di dati contenuto nella colonna. Vedere il campo vType nella sezione 2.2.1.1 per l'elenco dei valori per questo campo.

**ValueUsed**: campo a un byte che deve essere impostato su 0x01 o 0x00. Se impostato su 0x01, la colonna viene trasferita all'interno della riga a dimensione fissa. Se impostato su 0x00, il valore della colonna viene trasferito nella sezione a lunghezza variabile alla fine del buffer.

**\_ padding1**: campo a un byte che deve essere inserito prima di ValueOffset se, senza di esso, ValueOffset non inizierà con un offset pari dall'inizio del messaggio. Il valore di questo byte è arbitrario e deve essere ignorato. Se ValueUsed è impostato su 0x00, questo campo non deve essere presente.

**ValueOffset**: intero senza segno a 2 byte che specifica l'offset del valore della colonna nella riga. Se ValueUsed è impostato su 0x00, questo campo non deve essere presente.

**ValueSize**: intero senza segno a 2 byte che specifica le dimensioni in byte del valore della colonna. Se ValueUsed è impostato su 0x00, questo campo non deve essere presente.

**StatusUsed**: campo a un byte che deve essere impostato su 0x01 o 0x00. Se impostato su 0x01, lo stato della colonna viene trasferito all'interno della riga. Se 0x00, lo stato della colonna non viene trasferito all'interno della riga.

**\_ padding2**: campo a un byte che deve essere inserito prima di StatusOffset se, senza di esso, il campo StatusOffset non inizia con un offset pari dall'inizio del messaggio. Il valore di questo byte è arbitrario e deve essere ignorato. Se StatusUsed è impostato su 0x00, questo campo non deve essere presente.

**StatusOffset**: intero senza segno a 2 byte che specifica l'offset dello stato della colonna nella riga. Se StatusUsed è impostato su 0x00, questo campo non deve essere presente.

**LengthUsed**: campo a un byte che deve essere impostato su 0x01 o 0x00. Se impostato su 0x01, la lunghezza della colonna viene trasferita all'interno della riga. Se 0x00, la lunghezza della colonna non deve essere trasferita all'interno della riga.

**\_ padding3**: campo a un byte che deve essere inserito prima di LengthOffset se, senza di esso, LengthOffset non inizierà con un offset pari dall'inizio di un messaggio. Il valore di questo byte è arbitrario e deve essere ignorato. Se LengthUsed è impostato su 0x00, questo campo non deve essere presente.

**LengthOffset**: intero senza segno a 2 byte che specifica l'offset della lunghezza della colonna nella riga. Se LengthUsed è impostato su 0x00, questo campo non deve essere presente.

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

RGB (variabile)



 

**dwType**: uno dei tipi Variant, definito nella sezione 2.2.1.1, che può essere combinato con modificatori di tipo Variant. Per tutti i tipi Variant, ad eccezione di quelli combinati con \_ la matrice VT, SERIALIZEDPROPERTYVALUE ha lo stesso layout di CBaseStorageVariant, come specificato nella sezione 2.2.1.1. Se il tipo Variant è combinato con il \_ modificatore di tipo matrice VT, viene usato SAFEARRAY2, specificato nella sezione 2.2.1.2.1.1, anziché SAFEARRAY nel campo vValue di CBaseStorageVariant.

**RGB**: valore serializzato. Vedere i dettagli della serializzazione per vValue in 2.2.1.1.

### <a name="222-message-headers"></a>2.2.2 intestazioni di messaggio

Tutti i messaggi del protocollo del servizio di indicizzazione del contenuto hanno un'intestazione di 16 byte.

Di seguito è riportato un diagramma che mostra il formato dell'intestazione del messaggio protocollo del servizio di indicizzazione contenuto.



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

\_messaggio

\_stato

\_ulChecksum

\_ulReserved2



 

\_**msg**: intero A 32 bit che identifica il tipo di messaggio dopo l'intestazione. Nella tabella seguente sono elencati i messaggi del protocollo del servizio di indicizzazione del contenuto e i valori integer specificati per ogni messaggio. Come illustrato nella tabella, alcuni valori identificano 2 messaggi nella tabella. In tali istanze il messaggio che segue l'intestazione può essere identificato dalla direzione del flusso di messaggi. Se la direzione è da client a server, viene indicato il messaggio con "in" aggiunto al nome del messaggio. Se la direzione è da server a client, viene indicato il messaggio con "out" aggiunto al nome del messaggio.



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



 

\_**stato**: HRESULT \[ ms-sys \] , che indica lo stato dell'operazione richiesta.

\* *

*Comportamento di Windows: il client imposta sempre il \_ campo stato su 0x00000000.*

**\_ ulChecksum**: \_ ulChecksum deve essere calcolato come specificato nella sezione 3.2.4 per i messaggi seguenti:

-   CPMConnectIn
-   CPMCreateQueryIn
-   CPMSetBindingsIn
-   CPMGetRowsIn
-   CPMFetchValueIn

Per tutti gli altri messaggi, \_ ULCHECKSUM deve essere impostato su 0x00000000. Un client deve ignorare il \_ campo ulChecksum.

**\_ ulReserved2**: deve essere impostato su 0 e ignorato dal ricevitore.

### <a name="223-messages"></a>2.2.3 messaggi

### <a name="2231-cpmcistateinout"></a>CPMCiStateInOut 2.2.3.1

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

Area

cFilteredDocuments

cTotalDocuments

cPendingScans

dwIndexSize

cUniqueKeys

cSecQDocuments

dwPropCacheSize



 

**cbStruct**: Unsigned Integer A 32 bit. Dimensioni in byte di questo messaggio (esclusa l'intestazione comune). DEVE essere impostato su 0x0000003C.

**cWordList**: Unsigned Integer A 32 bit che indica il numero di indici iniziali creati per i documenti indicizzati di recente.

**cPersistentIndex**: Unsigned Integer A 32 bit che indica il numero di indici permanenti.

**cQueries**: un Unsigned Integer a 32 bit che indica una serie di query attivamente in esecuzione.

**CDocuments**: Unsigned Integer a 32 bit che indica il numero totale di documenti in attesa di essere indicizzati.

**cFreshTest**: un Unsigned Integer a 32 bit che indica il numero di documenti univoci con informazioni negli indici che non sono completamente ottimizzati per le prestazioni.

**dwMergeProgress**: intero senza segno a 32 bit che specifica la percentuale di completamento dell'ottimizzazione completa corrente degli indici, se è attualmente in corso l'ottimizzazione. DEVE essere minore o uguale a 100.

**estate**: stato dell'indicizzazione del contenuto fornito da una o più costanti di \_ stato ci \_ \* , definite nella tabella seguente.



| Valore                                         | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ 0x00000001 Unione Shadow dello stato ci \_           | Il servizio di indicizzazione è in corso di ottimizzazione di alcuni indici per ridurre l'utilizzo della memoria e migliorare le prestazioni delle query.                                                                                                                                                                                                                                                                                                                                                                |
| \_ \_ Unione 0x00000002 Master stati ci \_           | Il servizio di indicizzazione è nel processo di ottimizzazione completa per tutti gli indici.                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \_Analisi del contenuto dello stato ci \_ \_ \_ obbligatoria 0x00000004 | Alcuni documenti nell'indice sono stati modificati e il servizio di indicizzazione deve determinare quali sono stati aggiunti, modificati o eliminati.                                                                                                                                                                                                                                                                                                                                                              |
| \_Stati \_ Uniti che annealing \_ merge 0x00000008        | Il servizio di indicizzazione è in corso di ottimizzazione degli indici per ridurre l'utilizzo della memoria e migliorare le prestazioni delle query. Questo processo è più completo rispetto a quello identificato dal valore di \_ merge Shadow dello stato ci \_ \_ , ma non è completo come specificato dal \_ valore di unione master dello stato ci \_ \_ . Queste ottimizzazioni sono specifiche dell'implementazione perché dipendono dal modo in cui i dati vengono archiviati internamente; le ottimizzazioni non influiscono sul protocollo in alcun modo diverso dal tempo di risposta. |
| \_0x00000010 di analisi dello stato ci \_                | Il servizio di indicizzazione sta esaminando una directory o un set di directory per verificare se i file sono stati aggiunti, eliminati o aggiornati dall'ultima volta che la directory è stata indicizzata.                                                                                                                                                                                                                                                                                                                 |
| \_Ripristino dello stato ci \_ 0x00000020              | Il servizio è stato avviato dall'ultimo stato salvato ed è in corso di ripristino.                                                                                                                                                                                                                                                                                                                                                                                                        |
| Stato CI- \_ \_ memoria insufficiente \_ 0x00000080             | La maggior parte della memoria virtuale del server è in uso.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| I/o \_ elevato stato ci \_ \_ 0x00000100                | Il livello di attività di I/O (input/output) sul server è relativamente elevato.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \_ \_ Unione principale stato \_ ci \_ sospeso 0x00000200   | Il processo di ottimizzazione completa per tutti gli indici in corso è stato sospeso. Questa operazione viene fornita solo a scopo informativo e non influisce su CISP.                                                                                                                                                                                                                                                                                                                                  |
| Stato CI di \_ \_ sola lettura \_ 0x00000400              | La parte del servizio di indicizzazione che preleva nuovi documenti da indicizzare è stata sospesa. Questa operazione viene fornita solo a scopo informativo e non influisce su CISP.                                                                                                                                                                                                                                                                                                                               |
| \_0x00000800 di \_ alimentazione della batteria a stati ci \_          | La parte del servizio di indicizzazione che preleva nuovi documenti da indicizzare è stata sospesa per conservare la durata della batteria, ma comunque risponde alle query. Questa operazione viene fornita solo a scopo informativo e non influisce su CISP.                                                                                                                                                                                                                                                                 |
| \_Utente stato \_ ci \_ attivo 0x00001000            | La parte del servizio di indicizzazione che preleva nuovi documenti da indicizzare è stata sospesa a causa di un'attività elevata da parte dell'utente (tastiera o mouse) ma risponde comunque alle query. Questa operazione viene fornita solo a scopo informativo e non influisce su CISP.                                                                                                                                                                                                                                         |
| \_Stato ci \_ iniziale 0x00002000                | Il servizio è in fase di avvio. È possibile eseguire le query, ma l'analisi e la notifica non sono ancora state abilitate. Questa operazione viene fornita solo a scopo informativo e non influisce su CISP.                                                                                                                                                                                                                                                                                                                   |
| Stato CI che \_ \_ legge \_ USNS 0x00004000           | Il servizio non ha letto il log mantenuto dal file system per tenere traccia delle modifiche apportate ai file o alle directory in un volume, pertanto l'indice potrebbe non essere aggiornato.                                                                                                                                                                                                                                                                                                                                  |



 

**cFilteredDocuments**: Unsigned Integer A 32 bit che indica il numero di documenti indicizzati dall'inizio dell'indicizzazione del contenuto.

**cTotalDocuments**: Unsigned Integer a 32 bit che indica il numero totale di documenti presenti nel sistema.

**cPendingScans**: Unsigned Integer A 32 bit che indica il numero di operazioni di indicizzazione di alto livello in sospeso. Il significato di questo valore è specifico del provider, ma sono previsti numeri maggiori per indicare che l'indicizzazione rimane maggiore.

*Comportamento di Windows*: questo valore è in genere zero, tranne che subito dopo l'avvio dell'indicizzazione o dopo l'overflow di una coda di notifica.

**dwIndexSize**: un Unsigned Integer a 32 bit che indica le dimensioni, in megabyte, dell'indice (esclusa la cache delle proprietà).

**cUniqueKeys**: Unsigned Integer a 32 bit che indica il numero approssimativo di chiavi univoche nel catalogo.

**cSecQDocuments**: un Unsigned Integer a 32 bit che indica il numero di documenti che il servizio di indicizzazione tenterà di eseguire di nuovo l'indicizzazione a causa di un errore durante il tentativo di indicizzazione iniziale.

**dwPropCacheSize**: un Unsigned Integer a 32 bit che indica le dimensioni, in megabyte, della cache delle proprietà.

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



 

**\_ partID**: deve essere impostato su 0x00000001.

**\_ dwNewState**: deve essere impostato su uno dei valori seguenti, che indica il nuovo stato del catalogo.



| Valore                         | Significato                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CICAT \_ arrestato 0x00000001     | Il catalogo è stato arrestato. Questo stato indica che non è necessario indicizzare nuovi file e che non devono essere elaborate query di ricerca.                                                     |
| CICAT \_ ReadOnly 0x00000002    | Il catalogo è di sola lettura. Non è necessario indicizzare nuovi file.                                                                                                               |
| \_0x00000004 scrivibile CICAT    | Il catalogo è scrivibile. I nuovi file possono essere indicizzati e le query di ricerca devono essere elaborate.                                                                              |
| CICAT \_ senza \_ 0x00000008 di query   | Il catalogo non è disponibile per le query.                                                                                                                              |
| CICAT \_ ottenere \_ lo stato 0x00000010  | Lo stato del catalogo non deve essere modificato, ma solo recuperato.                                                                                                          |
| CICAT \_ tutti \_ 0x00000020 aperti | Un controllo per verificare se tutti i cataloghi sono stati avviati. In tal caso, il \_ campo dwOldState inviato nella risposta CPMSetCatStateOut a questo messaggio verrà segnalato come diverso da zero. |



 

**\_ CatName**: nome del catalogo per cui viene modificato lo stato. Il nome deve essere una stringa Unicode con terminazione null. Se \_ dwNewState è impostato su CICAT \_ tutti aperti, questo campo deve essere omesso \_ .

### <a name="2233-cpmsetcatstateout"></a>CPMSetCatStateOut 2.2.3.3

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



 

**\_ dwOldState**: uno dei valori seguenti, che indica lo stato precedente del catalogo.



| Valore                       | Significato                                    |
|-----------------------------|--------------------------------------------|
| CICAT \_ arrestato 0x00000001   | Il catalogo è stato arrestato.                    |
| CICAT \_ ReadOnly 0x00000002  | Il catalogo è di sola lettura.                  |
| \_0x00000004 scrivibile CICAT  | Il catalogo è scrivibile.                   |
| CICAT \_ senza \_ 0x00000008 di query | Il catalogo non è disponibile per le query. |



 

### <a name="2234-cpmupdatedocumentsin"></a>2.2.3.4 CPMUpdateDocumentsIn

Il messaggio CPMUpdateDocumentsIn indica al server di indicizzare il percorso specificato.

Il server risponderà con l'intestazione del messaggio del messaggio CPMUpdateDocumentsOut, con i risultati della richiesta contenuti nel \_ campo stato dell'intestazione del messaggio.

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



 

**\_ flag**: tipo di aggiornamento da eseguire. Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server. Questo campo deve essere impostato su uno dei valori seguenti:



| Valore                  | Significato                                   |
|------------------------|-------------------------------------------|
| UPD \_ INCREM 0x00000000 | È necessario eseguire un aggiornamento incrementale. |
| \_0x00000001 completo UPD   | È necessario eseguire un aggiornamento completo.         |
| UPD \_ init 0x00000002   | È necessario eseguire una nuova inizializzazione.  |



 

**\_ fRootPath**: valore booleano che indica se il campo RootPath specifica un percorso in cui eseguire l'aggiornamento. Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server. Questo campo deve essere impostato su 0x00000001 o 0x00000000. Se impostato su 0x00000001, un percorso in cui eseguire l'aggiornamento è incluso in RootPath. Se impostato su 0x00000000, l'aggiornamento deve essere eseguito su tutti i percorsi indicizzati.

**RootPath**: nome del percorso da aggiornare. Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server. Il nome deve essere una stringa Unicode con terminazione null. Questo campo deve essere omesso se \_ fRootPath è impostato su 0x00000000.

### <a name="2235-cpmforcemergein"></a>2.2.3.5 CPMForceMergeIn

Il messaggio CPMForceMergeIn richiede a un server di eseguire qualsiasi manutenzione necessaria per migliorare le prestazioni di esecuzione delle query. Il server risponderà con l'intestazione del messaggio del messaggio CPMForceMergeIn, con i risultati della richiesta contenuti nel \_ campo stato.

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

\_partId (facoltativo)



 

**\_ partID**: questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server. Quando questo campo è presente, deve essere impostato su 0x00000001.

### <a name="2236-cpmconnectin"></a>2.2.3.6 CPMConnectIn

Il messaggio CPMConnectIn inizia una sessione tra il client e il server.

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

\_imbottitura

...

...

MachineName

... variabile

UserName

... variabile

\_paddingcPropSets (facoltativo, variabile)

cPropSets

PropertySet1 (variabile)

PropertySet2 (variabile)

\_paddingExtPropset (facoltativo, variabile)

cExtPropSet

aPropertySets (variabile)



 

**\_ iClientVersion**: intero a 32 bit che indica se il server deve convalidare il valore di checksum specificato nel \_ campo ulChecksum delle intestazioni del messaggio per i messaggi inviati dal client. Se il \_ campo iClientVersion è impostato su 0x00000008 o su un valore superiore, il server deve convalidare il \_ valore del campo ulChecksum per i messaggi seguenti:

-   CPMConnectIn
-   CPMCreateQueryIn
-   CPMFetchValueIn
-   CPMGetRowsIn
-   CPMSetBindingsIn

Per informazioni dettagliate sul modo in cui il server convalida il valore specificato dal client nel campo ulChecksum per i messaggi sopra elencati, vedere la sezione 3.2.5.

Se il valore è maggiore di 0x00000008, si presuppone che il client sia in grado di gestire gli offset a 64 bit nei messaggi CPMGetRowsOut. Per informazioni dettagliate, vedere la sezione 2.2.3.16.

*Comportamento di Windows: nei client Windows, iClientVersion è impostato come segue*:



| Valore      | Significato                                                              |
|------------|----------------------------------------------------------------------|
| 0x00000005 | Il sistema operativo client è Windows 2000.                                           |
| 0x00000008 | Il sistema operativo client è Windows XP a 32 bit o Windows Server 2003 a 32 bit. |
| 0x00010008 | Il sistema operativo client è Windows XP a 64 bit o Windows Server 2003 a 64 bit. |



 

\_**fClientIsRemote**: valore booleano che indica se il client è in esecuzione in un computer diverso da quello del server. DEVE essere impostato su 0x00000001.

\_**cbBlob1**: un Unsigned Integer a 32 bit che indica le dimensioni in byte dei campi CPropSet, PropertySet1 e PropertySet2, combinati.

\_**cbBlob2**: un Unsigned Integer a 32 bit che indica le dimensioni in byte dei campi CExPropSet e aPropertySet, combinati.

\_**spaziatura interna**: 12 byte di riempimento che possono contenere valori arbitrari e devono essere ignorati.

**MachineName**: nome del computer del client. La stringa del nome deve essere una matrice con terminazione null di meno di 512 caratteri Unicode, incluso il terminatore NULL.

**Username**: stringa che rappresenta il nome utente della persona che esegue l'applicazione che ha richiamato questo protocollo. La stringa del nome deve essere una matrice con terminazione null con un numero di caratteri Unicode inferiore a 512, se concatenata a MachineName.

**\_ paddingcPropSets**: questo campo deve avere una lunghezza compresa tra 0 e 7 byte. Il numero di byte deve essere il numero necessario per fare in modo che l'offset di byte del campo cPropSets dall'inizio del messaggio che contiene la struttura sia un multiplo di 8. Il valore dei byte può essere qualsiasi valore arbitrario e deve essere ignorato dal ricevitore.

**cPropSets**: Unsigned Integer A 32 bit che indica il numero di strutture CDbPropSet che seguono questo campo. Questo valore deve essere impostato su 0x0000002.

**PropertySet1**: struttura CDbPropSet con guidPropertySet che contiene DBPROPSET \_ FSCIFRMWRK \_ ext (vedere la sezione 2.2.1.22).

**PropertySet2**: struttura CDbPropSet con guidPropertySet che contiene DBPROPSET \_ CIFRMWRKCORE \_ ext (vedere la sezione 2.2.1.22).

\_**PaddingExtPropset**: questo campo deve avere una lunghezza compresa tra 0 e 7 byte. Il numero di byte deve essere il numero necessario per fare in modo che l'offset di byte del campo cExtPropSets dall'inizio del messaggio che contiene la struttura sia un multiplo di 8. Il valore dei byte può essere qualsiasi valore arbitrario e deve essere ignorato dal ricevitore.

**cExtPropSet**: Unsigned Integer A 32 bit che indica il numero di strutture CDbPropSet che seguono questo campo.

**aPropertySets**: matrice di strutture CDbPropSet che specifica altre proprietà. Il numero di elementi nella matrice deve essere uguale a cExtPropSet.

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

\_serverVersion

\_riservato (variabile)



 

**\_ ServerVersion**:

Intero A 32 bit che indica se il server può supportare gli offset a 64 bit *.* Per informazioni dettagliate, vedere la sezione 2.2.3.16.



| Valore      | Significato                                 |
|------------|-----------------------------------------|
| 0x00000007 | Il server è in grado di inviare solo offset a 32 bit. |
| 0x00010007 | Il server può inviare offset 32 o 64 bit.   |



 

**\_ riservato**: riservato. Il server può inviare un numero arbitrario di valori arbitrari e il client deve ignorare questi valori, se presenti.

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

ColumnStore (facoltativo)

... variabile

CRestrictionPresent.

Restrizione (facoltativa)

... variabile

CSortSetPresent

Sortt (facoltativo)

... variabile

CCategorizationSetPresent

CategorizationSet (facoltativo)

... variabile

RowSetProperties

...

...

...

...

PidMapper (variabile)



 

**Size**: Unsigned Integer a 32 bit che indica il numero di byte dall'inizio di questo campo alla fine del messaggio.

**CColumnSetPresent**: campo byte che indica se il campo di un oggetto columnstore è presente. Questo campo deve essere impostato su 0x01 o 0x00. Se impostato su 0x01, il campo CColumnSet deve essere presente. Se impostato su 0x00, deve essere assente.

**Columnstore**: struttura CColumnSet contenente i numeri di colonna in cui devono essere restituite le proprietà di CPidMapper.

**CRestrictionPresent**: campo di byte che indica se il campo di restrizione è presente. Se è impostato su un valore diverso da zero, il campo di restrizione deve essere presente. Se impostato su 0x00, la restrizione deve essere assente.

**Restrizione**: struttura CRestriction contenente l'albero dei comandi della query.

**CSortSetPresent**: campo di byte che indica se il campo di ordinamento è presente. Se è impostato su un valore diverso da zero, il campo del set di ordinamenti deve essere presente. Se impostato su 0x00, il set di ordinamenti deve essere assente.

**Sortt**: struttura CSortSet che indica l'ordinamento della query.

**CCategorizationSetPresent**: campo byte che indica se il campo CCategorizationSet è presente. Se è impostato su un valore diverso da zero, è necessario che il campo CCategorizationSet sia presente. Se impostato su 0x00, CCategorizationSet deve essere assente.

**CCategorizationSet**: struttura CCategorizationSet che contiene i gruppi per la query.

**RowSetProperties**: struttura CRowsetProperties che fornisce le informazioni di configurazione per la query.

**PidMapper**: struttura CPidMapper che contiene le proprietà da restituire in un set di righe.

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



 

**\_ fTrueSequential**: valore booleano informativo che indica se la query può fornire risultati più velocemente. Quando è impostato su 0x00000001 per la query fornita in CPMCreateQueryIn, il server può utilizzare l'indice in modo che i risultati della query vengano recapitati più velocemente. Quando è impostato su 0x00000000, si verificherà una latenza maggiore nel recapito dei risultati della query. Non deve essere impostato su un altro valore.

**\_ fWorkIdUnique**: valore booleano che indica se gli identificatori di documento a cui puntano i cursori sono univoci per tutti i risultati della query. Se impostato su 0x00000001, gli identificatori sono univoci. Se impostata su 0x00000000, sono univoche solo in tutto il set di righe.

**aCursors**: matrice di interi senza segno a 32 bit che rappresenta gli handle per i cursori, con il numero di elementi uguale al numero di categorie nel campo CategorizationSet del messaggio CPMCreateQueryIn.

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



 

**\_ hCursor**: un Unsigned Integer a 32 bit che rappresenta l'handle del messaggio CPMCreateQueryOut che identifica la query per la quale recuperare le informazioni sullo stato.

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



 

**\_ Stato**: maschera di maschera dei valori definiti nelle tabelle seguenti, che descrive la query.

La tabella seguente elenca \_ \* i valori stat ottenuti eseguendo un'operazione and bit per bit sullo \_ stato con 0x00000007. Il risultato deve essere uno dei seguenti:



| Costante                 | Significato                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| STAT \_ occupato 0x00000000    | La query asincrona è ancora in esecuzione.                                          |
| \_Errore stat 0x00000001   | La query è in stato di errore.                                                   |
| STAT \_ completato 0x00000002    | La query è stata completata.                                                            |
| STAT \_ Refresh 0x00000003 | La query è stata completata, ma gli aggiornamenti hanno come risultato un calcolo aggiuntivo delle query. |



 

Nella tabella seguente sono elencati i bit STAT aggiuntivi \_ \* che è possibile impostare in modo indipendente.



| Costante                                    | Significato                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| \_Parole non significative \_ 0x00000010               | Parole non significative sostituite da caratteri jolly nella query sul contenuto.                                                              |
| \_Contenuto stat \_ non \_ \_ aggiornato 0x00000020     | I risultati della query potrebbero non essere corretti perché la query ha richiesto file modificati ma non indicizzati.                             |
| \_0x00000040 di aggiornamento stat \_ incompleto        | I risultati della query potrebbero non essere corretti perché la query ha richiesto la modifica e la reindicizzazione dei file il cui contenuto non è incluso. |
| \_Query sul contenuto stat \_ \_ incompleta 0x00000080 | La query sul contenuto è troppo complessa per completare l'enumerazione o obbligatoria anziché utilizzare l'indice di contenuto.                          |
| \_Limite di tempo stat \_ \_ superato 0x00000100      | I risultati della query potrebbero non essere corretti perché il tempo di esecuzione della query ha raggiunto il tempo massimo consentito.                    |



 

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

\_BMK



 

**\_ hCursor**: valore a 32 bit che rappresenta l'handle del messaggio CPMCreateQueryOut che identifica la query per la quale recuperare le informazioni sullo stato.

**\_ BMK**: valore a 32 bit che indica l'handle di un segnalibro la cui posizione deve essere recuperata.

### <a name="22313-cpmgetquerystatusexout"></a>2.2.3.13 CPMGetQueryStatusExOut

Il messaggio CPMGetQueryStatusExOut risponde a un messaggio CPMGetQueryStatusExIn con lo stato della query e altre informazioni sullo stato, come illustrato nel diagramma riportato di seguito. Il formato del messaggio CPMGetQueryStatusExOut che segue l'intestazione è:



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



 

**\_ Stato**: una delle stat \_ \* valori specificati nella sezione 2.2.3.11.

**\_ cFilteredDocuments**: Unsigned Integer A 32 bit che indica il numero di documenti indicizzati

**\_ cDocumentsToFilter**: Unsigned Integer a 32 bit che indica il numero di documenti rimanenti da indicizzare.

**\_ dwRatioFinishedDenominator**: un Unsigned Integer a 32 bit che indica il denominatore del rapporto dei documenti completati dall'elaborazione della query.

**\_ dwRatioFinishedNumerator**: un Unsigned Integer a 32 bit che indica il numeratore del rapporto dei documenti completati dall'elaborazione della query.

**\_ iRowBmk**: Unsigned Integer a 32 bit che indica la posizione approssimativa del segnalibro nel set di righe in termini di righe.

**\_ cRowsTotal**: un Unsigned Integer a 32 bit che specifica il numero totale di righe nel set di righe.

### <a name="22314-cpmsetbindingsin"></a>2.2.3.14 CPMSetBindingsIn

Il messaggio CPMSetBindingsIn richiede l'associazione di colonne a un set di righe. Il server risponderà al messaggio di richiesta CPMSetBindingsIn usando la sezione di intestazione del messaggio CPMBindingsIn con i risultati della richiesta contenuta nel \_ campo stato. Il formato del messaggio CPMSetBindingsIn che segue l'intestazione è:



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



 

**\_ hCursor**: valore a 32 bit che rappresenta l'handle del messaggio CPMCreateQueryOut che identifica la riga per cui impostare le associazioni. Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server.

**\_ cbRow**: un Unsigned Integer a 32 bit che indica le dimensioni, in byte, di una riga. Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server.

**\_ cbBindingDesc**: Unsigned Integer a 32 bit che indica la lunghezza, in byte, dei campi che seguono il \_ campo fittizio. Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server.

**\_ fittizio**: questo campo non è usato e deve essere ignorato. Può essere impostata su qualsiasi valore arbitrario. Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server.

**CColumns**: Unsigned Integer a 32 bit che indica il numero di elementi nella matrice aColumns. Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server.

**aColumns**: matrice di strutture CTableColumn che descrive le colonne di una riga nel set di righe. Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server. Le strutture nella matrice devono essere separate da un byte di riempimento compreso tra 0 e 3 in modo che ogni struttura disponga di un allineamento a 4 byte dall'inizio di un messaggio. Tali byte di riempimento possono essere qualsiasi valore arbitrario e devono essere ignorati alla ricezione.

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

\_Cap

SeekDescription

...

... variabile



 

**\_ hCursor**: valore a 32 bit che rappresenta l'handle del messaggio CPMCreateQueryOut che identifica la query per la quale recuperare le righe.

**\_ cRowsToTransfer**: Unsigned Integer a 32 bit che indica il numero massimo di righe che il client desidera ricevere in risposta a questo messaggio.

**\_ cbRowWidth**: Unsigned Integer a 32 bit che indica la lunghezza di una riga, in byte.

**\_ cbSeek**: Unsigned Integer A 32 bit che indica la dimensione del messaggio che inizia con etype.

**\_ cbReserved**: un Unsigned Integer a 32 bit che indica le dimensioni, in byte, di un messaggio CPMGetRowsOut (senza i campi Rows e SeekDescriptions). Questo valore in questo campo viene aggiunto al valore del \_ campo cbSeek e quindi deve essere utilizzato per calcolare il campo offset di righe nel messaggio CPMGetRowsOut.

**\_ cbReadBuffer**: un Unsigned Integer a 32 bit che deve essere impostato sul valore massimo di \_ cbRowWidth o 1000 volte il valore di \_ cRowsToTransfer, arrotondato per eccesso al più vicino 512 byte multiplo. Il valore non deve superare 0x00004000.

**\_ ulClientBase**: Unsigned Integer a 32 bit che indica il valore di base da utilizzare per i calcoli dei puntatori nel buffer di riga. Se vengono usati offset a 64 bit, il campo Reserved2 dell'intestazione del messaggio viene usato come 32 bit superiore e \_ ulClientBase come 32 bit inferiori di un valore a 64 bit. Per informazioni dettagliate, vedere la sezione 2.2.3.16.

**\_ fBwdFetch**: Unsigned Integer a 32 bit che indica l'ordine in cui recuperare le righe. Se impostato su 0x00000001, le righe devono essere recuperate in ordine inverso. Se impostato su 0x00000000, le righe devono essere recuperate in ordine di avanzamento. NON deve essere impostato su nessun altro valore.

**etype**: Unsigned Integer a 32 bit contenente uno dei valori seguenti per indicare il tipo di operazione da eseguire.



| Valore                         | Significato                                                  |
|-------------------------------|----------------------------------------------------------|
| 0x00000001 eRowSeekNext       | SeekDescription contiene una struttura CRowSeekNext.       |
| 0x00000002 eRowSeekAt         | SeekDescription contiene una struttura CRowSeekAt.         |
| 0x00000003 eRowSeekAtRatio    | SeekDescription contiene una struttura CRowSeekAtRatio.    |
| 0x00000004 eRowSeekByBookmark | SeekDescription contiene una struttura CRowSeekByBookmark. |



 

**\_ Chapt**: valore a 32 bit che rappresenta l'handle del capitolo del set di righe.

**SeekDescription**: questo campo deve contenere una struttura del tipo indicato dal valore di etype.

### <a name="22316-cpmgetrowsout"></a>2.2.3.16 CPMGetRowsOut

Il messaggio CPMGetRowsOut risponde a un messaggio CPMGetRowsIn con le righe di una query. I server devono formattare gli offset in tipi di dati a lunghezza variabile nel campo righe come indicato di seguito:

-   Il client ha indicato che si tratta di un sistema a 32 bit (0x00000008 o less nel campo iClientVersion di CPMConnectIn): gli offset sono Integer a 32 bit.
-   Il client indica che si tratta di un sistema a 64 bit ( \_ iClientVersion > 0x00000008 in CPMConnectIn) e che il server ha indicato che si tratta di un sistema a 32 bit ( \_ ServerVersion impostato su 0X00000007 in CPMConnectOut): gli offset sono integer a 32 bit
-   Il client indica che si tratta di un sistema a 64 bit ( \_ iClientVersion > 0x00000008 in CPMConnectIn) e che il server ha indicato che si tratta di un sistema a 64 bit ( \_ ServerVersion impostato su 0X00010007 in CPMConnectOut): gli offset sono integer a 64 bit

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

\_Cap

SeekDescription (facoltativo, variabile)

...

...

paddingRows (facoltativo, variabile)

Righe



 

**\_ cRowsReturned**: Unsigned Integer a 32 bit che indica il numero di righe restituite nelle righe.

**etype**: Unsigned Integer a 32 bit contenente uno dei valori seguenti per indicare il tipo di operazione rowseek da eseguire



| Valore                         | Significato                                                  |
|-------------------------------|----------------------------------------------------------|
| 0x00000000 eRowsSeekNone      | Nessun SeekDescription, ignora il campo SeekDescription.        |
| 0x00000001 eRowSeekNext       | SeekDescription contiene una struttura CRowSeekNext.       |
| 0x00000002 eRowSeekAt         | SeekDescription contiene una struttura CRowSeekAt.         |
| 0x00000003 eRowSeekAtRatio    | SeekDescription contiene una struttura CRowSeekAtRatio.    |
| 0x00000004 eRowSeekByBookmark | SeekDescription contiene una struttura CRowSeekByBookmark. |



 

**\_ Chapt**: valore a 32 bit che rappresenta l'handle del capitolo del set di righe.

**SeekDescription**: questo campo deve contenere una struttura del tipo indicato dal campo etype.

**paddingRows**: questo campo deve avere una lunghezza sufficiente (da 0 a \_ cbReserved-1 byte) per riempire il campo righe in \_ offset cbReserved dall'inizio di un messaggio, dove \_ cbReserved è il valore nel messaggio CPMGetRowsIn. I byte di riempimento utilizzati in questo campo possono essere qualsiasi valore arbitrario. Questo campo deve essere ignorato dal ricevitore.

**Rows**: i dati delle righe sono formattati come previsto dalle informazioni sulle colonne nel messaggio CPMSetBindingsIn più recente. Le righe devono essere archiviate in ordine di avanzamento (ad esempio, la riga 1 prima della riga 2).

Le colonne a dimensione fissa devono essere archiviate in corrispondenza degli offset specificati dal messaggio CPMSetBindingsIn più recente.

Le colonne di dimensioni variabili, ad esempio le stringhe, devono essere archiviate come segue:

-   I dati della variabile (ad esempio, la stringa) vengono archiviati in ordine decrescente verso la fine del buffer, ad esempio la raccolta di tutti i dati delle variabili per la riga 1 si trova alla fine, riga 2 successiva più vicina e così via.
-   L'area a dimensione fissa (all'inizio del buffer di riga) deve contenere un CRowVariant per ogni colonna, archiviato in corrispondenza dell'offset specificato nel messaggio CPMSetBindingsIn più recente. vType deve contenere il tipo di dati (ad esempio, VT \_ LPWSTR). Se, come determinato dalle regole all'inizio della sezione in questa sezione vengono utilizzati offset 32 bit, il campo offset in CRowVariant deve contenere un valore a 32 bit che rappresenta l'offset dei dati della variabile dall'inizio del messaggio CPMGetRowsOut, più il valore di \_ ulClientBase specificato nel messaggio CPMGetRowsIn più recente. Se vengono utilizzati offset a 64 bit, il campo offset in CRowVariant deve contenere un valore a 64 bit che rappresenta l'offset dall'inizio del messaggio CPMGetRowsOut, aggiunto a un valore a 64 bit composto utilizzando \_ ulClientBase come minimo 32 bit e \_ ulReserved2 come bit 32.

Se, ad esempio, il messaggio CPMSetBindingsIn ha specificato due colonne (VT \_ I4) e title (VT \_ LPWSTR) e \_ ulClientBase da CPMGetRowsIn è 0x10000, verranno visualizzate due righe, come indicato di seguito. La sezione contrassegnata in grigio è la parte a lunghezza fissa del buffer.

![esempio di messaggio cpmsetbindingsin](images/cpmgetrowsout.gif)

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



 

**\_ hCursor**: handle del messaggio CPMCreateQueryOut che identifica la query per la quale richiedere informazioni di completamento.

**\_ fQuick**: deve essere impostato su 0x00000001. Non usato e deve essere ignorato dal server.

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



 

**\_ ulNumerator**: Unsigned Integer a 32 bit che indica il numeratore del rapporto di completamento in termini di righe.

**\_ ulDenominator**: un Unsigned Integer a 32 bit che indica il denominatore del rapporto di completamento in termini di righe. DEVE essere maggiore di zero.

**\_ Crows**: Unsigned Integer a 32 bit che indica il numero totale di righe per la query.

**\_ fNewRows**: valore booleano che indica se sono disponibili nuove righe. Il valore 0x00000001 indica che nel set di righe sono disponibili nuove righe. Il valore 0x00000000 indica che il set di righe non contiene nuove righe. Questo campo non deve essere impostato su nessun altro valore.

### <a name="22319-cpmfetchvaluein"></a>2.2.3.19 CPMFetchValueIn

Il messaggio CPMFetchValueIn richiede un valore della proprietà troppo grande per essere restituito in un set di righe. Come specificato nella sezione 3.2.4.2.5, questo messaggio viene inviato ripetutamente per recuperare tutti i byte della proprietà, aggiornando \_ cbSoFar per ogni, finché il \_ campo fMoreExists del messaggio CPMFetchValueOut non è impostato su **false**.

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

\_wid

\_cbSoFar

\_cbPropSpec

\_cbChunk

Campo PROPSPEC (variabile)

...

\_spaziatura interna (variabile)



 

**\_ wid**: un Unsigned Integer a 32 bit che rappresenta l'ID documento che identifica il documento per cui deve essere recuperata una proprietà.

**\_ cbSoFar**: Unsigned Integer a 32 bit contenente il numero di byte trasferiti in precedenza per questa proprietà. DEVE essere impostato su 0x00000000 nel primo messaggio.

**\_ cbPropSpec**: Unsigned Integer a 32 bit contenente le dimensioni del campo Campo PROPSPEC, in byte.

**\_ cbChunk**: un Unsigned Integer a 32 bit contenente il numero massimo di byte che il mittente può accettare in un messaggio CPMFetchValueOut.

*Comportamento di Windows: questo campo è impostato su 0x00004000 per tutte le versioni di Windows.*

**Campo PROPSPEC**: struttura CFullPropSpec che specifica la proprietà da recuperare.

**\_ spaziatura interna**: questo campo deve essere della lunghezza necessaria (da 0 a 3 byte) per riempire il messaggio a un multiplo di 4 byte di lunghezza. Il valore dei byte di riempimento può essere qualsiasi valore arbitrario. Questo campo deve essere ignorato dal ricevitore.

### <a name="22320-cpmfetchvalueout"></a>2.2.3.20 CPMFetchValueOut

Il messaggio CPMFetchValueOut risponde a un messaggio CPMFetchValueIn con un valore della proprietà di una query precedente. Come specificato nella sezione 3.1.5.2.8, questo messaggio viene inviato dopo ogni messaggio CPMFetchValueIn fino a quando non vengono trasferiti tutti i byte della proprietà.

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



 

**\_ cbValue**: Unsigned Integer a 32 bit contenente le dimensioni totali, in byte in vValue.

**\_ fMoreExists**: valore booleano che indica se sono presenti altri messaggi CPMFetchValueOut disponibili. Se impostato su 0x00000001, sono presenti altri messaggi CPMFetchValueOut. Se impostato su 0x00000000, non sono disponibili altri messaggi di CPMFetchValueOut.

**\_ fValueExists**: valore booleano che indica se è presente un valore per la proprietà. Se impostato su 0x00000001, esiste un valore per la proprietà. Se impostato su 0x00000000, non esiste un valore per la proprietà.

**vType**: valore dell'enumerazione VarEnum. per informazioni dettagliate, vedere la sezione 2.2.1.1, che descrive il tipo della proprietà.

**vValue**: parte di una matrice di byte contenente una struttura SERIALIZEDPROPERTYVALUE come specificato nella sezione 2.2.1.32, in cui l'offset dell'inizio della parte è il valore di \_ cbSoFar in CPMFetchValueIn. La lunghezza della parte, indicata dal \_ campo cbValue, deve essere uguale al valore di \_ CbChunk in CPMFetchValueIn se \_ fMoreExists è impostata su 0x00000001 e deve essere minore o uguale al valore di \_ cbChunk in caso contrario.

### <a name="22321-cpmgetnotify"></a>2.2.3.21 CPMGetNotify

Il messaggio CPMGetNotify richiede che il client desideri ricevere una notifica delle modifiche apportate al set di righe.

Il messaggio non deve includere un corpo; è necessario inviare solo l'intestazione del messaggio, come specificato nella sezione 2.2.2.

### <a name="22322-cpmsendnotifyout"></a>2.2.3.22 CPMSendNotifyOut

Il messaggio CPMSendNotifyOut invia una notifica al client di una modifica ai risultati di una query.

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



 

**\_ watchNotify**: modifica apportata alla query. DEVE essere uno dei valori seguenti:



| Valore                                     | Significato                                             |
|-------------------------------------------|-----------------------------------------------------|
| DBWATCHNOTIFY \_ ROWSCHANGED 0x00000001     | Il numero di righe nel set di righe della query è stato modificato. |
| DBWATCHNOTIFY \_ QUERYDONE 0x00000002       | La query è stata completata.                            |
| DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003 | La query è stata eseguita di nuovo.                     |



 

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

\_Cap

\_BMK



 

**\_ hCursor**: valore a 32 bit che rappresenta il cursore di query ottenuto da CPMCreateQueryOut per il set di righe che contiene il segnalibro.

**\_ Chapt**: valore a 32 bit che rappresenta l'handle per il capitolo contenente il segnalibro.

**\_ BMK**: valore a 32 bit che rappresenta l'handle per il segnalibro per il quale recuperare la posizione approssimativa.

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



 

**\_ numerator**: un Unsigned Integer a 32 bit contenente il numero di riga del segnalibro nel set di righe. Se non sono presenti righe, questo campo deve essere impostato su 0x00000000.

**\_ denominatore**: Unsigned Integer a 32 bit contenente il numero di righe nel set di righe.

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

\_Cap

\_bmkFirst

\_bmkSecond



 

\_**hCursor**: valore a 32 bit che rappresenta l'handle del messaggio CPMCreateQueryOut per il set di righe contenente i segnalibri.

\_**Chapt**: valore a 32 bit che rappresenta l'handle del capitolo contenente i segnalibri da confrontare.

\_**bmkFirst**: valore a 32 bit che rappresenta l'handle del primo segnalibro da confrontare.

\_**bmkSecond**: valore a 32 bit che rappresenta l'handle per il secondo segnalibro da confrontare.

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



 

\_**dwComparison**: uno dei valori seguenti, che indica le posizioni relative dei due segnalibri nel capitolo.



| Valore                               | Significato                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| DBCOMPARE \_ lt 0x00000000            | Il primo segnalibro viene posizionato prima del secondo.               |
| \_0x00000001 DBCOMPARE EQ            | Il primo segnalibro ha la stessa posizione del secondo.           |
| DBCOMPARE \_ gt 0x00000002            | Il primo segnalibro viene posizionato dopo il secondo.                |
| DBCOMPARE \_ ne 0x00000003            | Il primo segnalibro non ha la stessa posizione del secondo. |
| DBCOMPARE \_ NOTCOMPARABLE 0x00000004 | Il primo segnalibro non è confrontabile con il secondo.               |



 

### <a name="22327-cpmrestartpositionin"></a>2.2.3.27 CPMRestartPositionIn

Il messaggio CPMRestartPositionIn sposta la posizione di recupero di un cursore all'inizio del capitolo. Come specificato nella sezione 3.1.5.2.12, il server risponderà usando lo stesso messaggio, con i risultati della richiesta contenuti nel \_ campo status dell'intestazione CISP.

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

\_Chapt (facoltativo)



 

**\_ hCursor**: valore a 32 bit che rappresenta l'handle, ottenuto da un messaggio CPMCreateQueryOut che identifica la query per la quale riavviare la posizione. Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server.

**\_ Chapt**: valore a 32 bit che rappresenta l'handle di un capitolo dal quale recuperare le righe. Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server.

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



 

**\_ hCursor**: valore a 32 bit che rappresenta l'handle del cursore dal messaggio CPMCreateQueryOut da rilasciare.

### <a name="22329-cpmfreecursorout"></a>2.2.3.29 CPMFreeCursorOut

Il messaggio CPMFreeCursorOut risponde a un messaggio CPMFreeCursorIn con i risultati della liberazione di un cursore. Il formato del messaggio CPMFreeCursorOut che segue l'intestazione è:



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



 

**\_ cCursorsRemaining**: Unsigned Integer a 32 bit che indica il numero di cursori ancora in uso per la query.

### <a name="22330-cpmdisconnect"></a>2.2.3.30 CPMDisconnect

Il messaggio CPMDisconnect termina la connessione con il server

Il messaggio non deve includere un corpo; è necessario inviare solo l'intestazione del messaggio, come specificato nella sezione 2.2.2.

### <a name="224-errors"></a>2.2.4 errori

Tutti i messaggi del protocollo del servizio di indicizzazione del contenuto devono restituire 0x00000000 in caso di successo; in caso contrario, restituiscono un codice di errore diverso da zero a 32 bit che può essere un valore HRESULT o un valore NTSTATUS (vedere la sezione 1,8). Se un buffer è troppo piccolo per adattarsi a un risultato, è \_ necessario che venga restituito un codice di stato risorse insufficienti \_ (0XC0000009A) e che l'operazione non riuscita venga ritentata con un buffer più grande.

Tutti gli altri valori di errore devono essere considerati uguali.

Si noti che attualmente gli spazi di numerazione HRESULT e NTSTATUS non si sovrappongono, tranne che con valori di significato identico, ma anche se sono in conflitto in futuro, non si verificheranno problemi di protocollo purché il valore per lo stato \_ Le \_ risorse insufficienti rimangono univoche, in quanto tutti gli altri valori di errore vengono considerati uguali.

## <a name="3-protocol-details"></a>3 Dettagli del protocollo

-   [3,1 Dettagli server](#31-server-details)
-   [3,2 Dettagli client](#32-client-details)

Le richieste di messaggi CISP per l'esecuzione di query remote sui cataloghi dei servizi di indicizzazione non richiedono una sequenza specifica. È consigliabile che il livello più alto rispetti una sequenza di messaggi significativa, tuttavia, come per i messaggi ricevuti da questa sequenza o con dati non validi, il server risponderà con un errore. Alcuni messaggi dipendono anche dal livello superiore che fornisce dati validi ricevuti nei messaggi precedenti nella sequenza.

Nel diagramma seguente viene illustrata una tipica sequenza di messaggi per una query semplice da un client a un computer remoto.

![sequenza di messaggi per query semplice](images/protocoldetails.jpg)

I messaggi rappresentati nel diagramma precedente rappresentano un subset di tutti i messaggi CISP usati per eseguire query su un catalogo di servizi di indicizzazione remota.

### <a name="31-server-details"></a>3,1 Dettagli server

### <a name="311-abstract-data-model"></a>3.1.1 Modello di dati astratto

Nella sezione seguente vengono specificati i dati e lo stato gestiti dal server CISP. I dati forniti sono per semplificare la spiegazione del comportamento del protocollo. Questa sezione non impone che le implementazioni siano conformi a questo modello, purché il loro comportamento esterno sia coerente con quello descritto in questo documento.

Un servizio di indicizzazione che implementa CISP deve mantenere gli elementi dati astratti seguenti:

-   Elenco dei client connessi al server
-   Informazioni su ogni client, che include:
-   -   Versione del client (come indicato nel messaggio CPMConnectIn specificato nella sezione 2.2.3.6)
    -   Catalogo associato al client (tramite un messaggio CPMConnectIn)
    -   Proprietà client aggiuntive come specificato nella sezione 2.2.1.21.1.
    -   Query di ricerca del client
    -   Elenco di handle del cursore per la query e la posizione nel set di risultati per ogni handle.
    -   Set corrente di associazioni
    -   Stato corrente della query che include (per ogni cursore):
    -   -   Numero di righe nel risultato della query
        -   Numeratore e denominatore del completamento delle query
        -   Ultimo numero di righe, segnalato dal messaggio CPMRatioFinishedOut più recente per questo cursore
        -   Indica se la query viene monitorata dal server per le modifiche nei risultati della query e se viene monitorata, cosa è cambiato nei risultati della query dall'ultima segnalazione al client da parte di CPMSendNotifyOut
        -   Elenco di handle dei capitoli, serviti da questa query a un client.
        -   Elenco di handle di segnalibro per ogni cursore, servito da questa query a un client.

-   Stato corrente del servizio di indicizzazione, che può essere "non inizializzato", "in esecuzione" o "arresto". Si noti che la maggior parte del tempo del server si trova nello stato "in esecuzione". Di seguito è riportato il diagramma della macchina a stati per il server:

    ![diagramma della macchina a Stati del server del servizio di indicizzazione](images/abstractdatamodel.jpg)

-   Informazioni per catalogo: numero di documenti indicizzati, dimensioni dell'indice, numero di chiavi univoche e così via (vedere la sezione 2.2.3.1 per l'elenco completo), stato (che corrisponde ai valori di dwNewState nella sezione 2.2.3.2).
-   Per ogni lingua supportata, un database di varianti di parole, come illustrato nella sezione 2.2.1.3.

### <a name="312-timers"></a>3.1.2 Timer

Non sono richiesti timer del protocollo.

### <a name="313-initialization"></a>3.1.3 Inizializzazione

Al momento dell'inizializzazione, il server deve impostare lo stato su "non inizializzato" e iniziare l'ascolto dei messaggi nell'named pipe specificato nella sezione 1,9. Dopo l'esecuzione di qualsiasi altra inizializzazione interna, deve passare allo stato "Running".

### <a name="314-higher-layer-triggered-events"></a>3.1.4 Eventi attivati di livello più alto

Nessuna.

### <a name="315-message-processing-and-sequencing-rules"></a>Regole di sequenziazione e elaborazione dei messaggi 3.1.5

Ogni volta che si verifica un errore durante l'elaborazione di un messaggio inviato da un client, il server deve segnalare un errore al client nel modo seguente:

-   Interrompi elaborazione del messaggio inviato dal client
-   Rispondere con l'intestazione del messaggio (solo) del messaggio inviato dal client, mantenendo \_ intatto il campo msg.
-   Impostare il \_ campo stato sul valore del codice di errore.

Quando arriva un messaggio, il server deve controllare il \_ valore del campo msg per verificare se è un tipo noto (vedere la sezione 2.2.2). Se il tipo non è noto, deve segnalare un errore di \_ parametro di stato non valido \_ (0xc000000d).

Il server deve quindi convalidare il \_ valore del campo ulChecksum se il tipo di messaggio è uno dei seguenti:

-   CPMConnectIn (0x000000C8)
-   CPMCreateQueryIn (0x000000CA)
-   CPMSetBindingsIn (0x000000D0)
-   CPMGetRowsIn (0x000000CC)
-   CPMFetchValueIn (0x000000E4)

Per convalidare il \_ valore del campo ulChecksum, il server deve controllare il valore specificato dal client nel \_ campo iClientVersion del messaggio CPMConnectIn.

Se il \_ campo iClientVersion non è impostato su 0x00000008 e il \_ campo ulChecksum non è impostato su 0x00000000, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d). Il server non deve convalidare il \_ campo ulChecksum per i client impostando il \_ campo iClientVersion su un valore minore di 0x00000008.

Se il \_ valore del campo iClientVersionfield è 0x00000008 o superiore, il server deve verificare che il \_ campo ulChecksum sia stato calcolato come specificato nella sezione 3.2.4. Se il \_ valore ulChecksum non è valido, è necessario che il server segnali un errore di parametro di stato \_ non valido \_ (0xc000000d).

Successivamente, il server verifica lo stato in cui si trova. Se lo stato è "non inizializzato", il server deve segnalare \_ un \_ errore ci E non \_ inizializzato (0x8004180B). Se lo stato è "chiusura in corso", il server deve segnalare un \_ errore ci E \_ Shutdown (0x80041812).

Quando un'intestazione è stata determinata come valida e lo stato del server è "in esecuzione", è necessario eseguire un'ulteriore elaborazione specifica del messaggio come specificato nelle sottosezioni riportate di seguito.

### <a name="3151-remote-indexing-service-catalog-management"></a>Gestione del catalogo di servizi di indicizzazione remota di 3.1.5.1

### <a name="31511-receiving-a-cpmcistateinout-request"></a>3.1.5.1.1 che riceve una richiesta CPMCiStateInOut

Quando il server riceve una richiesta di messaggio CPMCIStateInOut dal client, il server deve prima verificare se il client si trova in un elenco di client connessi. Se il client non è presente nell'elenco, il server deve segnalare un \_ errore di parametro di stato non valido \_ (0xc000000d). In caso contrario, deve rispondere al client con un messaggio CPMCIStateInOut, inserendolo con informazioni sul catalogo associato del client come specificato nella sezione 2.2.3.1.

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a>3.1.5.1.2 che riceve una richiesta CPMSetCatStateIn

Quando il server riceve una richiesta di messaggio CPMSetCatStateIn dal client, il server deve eseguire le operazioni seguenti:

-   Verificare che il client disponga dell'accesso amministrativo. Se il client non dispone di accesso amministrativo, il server deve segnalare un errore di stato \_ accesso \_ negato (0xc0000022).
-   Se \_ dwNewState è diverso da CICAT \_ tutti \_ aperti, modificare lo stato del catalogo specificato nel campo CatName come specificato dal \_ campo dwNewState. Per ulteriori informazioni, vedere la sezione 2.2.3.2. Se il server non individua un catalogo con il nome specificato nel campo CatName, il server deve restituire un errore di parametro di stato \_ non valido \_ (0xc000000d).
-   Rispondere al client con un messaggio CPMSetCatStateOut, in cui \_ DWOLDSTATE deve essere impostato sullo stato precedente del catalogo. Se \_ dwNewState è uguale a CICAT \_ tutti \_ aperti, il server deve controllare lo stato di tutti i cataloghi e, se tutti gli elementi vengono avviati \_ , deve impostare dwOldState su 0x00000001 e in caso contrario impostare \_ dwOldState su 0x00000000.

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a>3.1.5.1.3 che riceve una richiesta CPMUpdateDocumentsIn

Quando il server riceve una richiesta di messaggio CPMUpdateDocumentsIn, il server deve eseguire le operazioni seguenti:

-   Controllare se il client si trova in un elenco di client connessi (a cui è associato un catalogo). Se il client non è presente nell'elenco, il server deve segnalare un \_ errore di parametro di stato non valido \_ (0xc000000d).
-   Verificare che il client disponga dell'accesso amministrativo. Se il client non dispone di accesso amministrativo al server, il server deve segnalare un errore di stato \_ accesso \_ negato (0xc0000022).
-   Avviare il processo di indicizzazione del percorso specificato dal client, eseguendo un'analisi completa o incrementale, a seconda del valore del \_ campo del flag nel messaggio CPMUpdateDocumentsIn. Se il percorso non è stato indicizzato in precedenza, deve essere aggiunto alla raccolta di percorsi indicizzati ed è stata eseguita un'analisi completa. Se viene specificato un valore non valido \_ per il campo del flag, il server deve agire come se \_ flag fosse stato impostato su UPD \_ init ed eseguire un'analisi completa. Questa operazione deve essere eseguita nel catalogo associato al client.
-   Rispondere al client con l'intestazione del messaggio per il CPMUpdateDocumentsIn e impostare il \_ campo stato sui risultati della richiesta.

### <a name="31514-receiving-a-cpmforcemergein-request"></a>3.1.5.1.4 che riceve una richiesta CPMForceMergeIn

Quando il server riceve una richiesta di messaggio CPMForceMergeIn, il server deve eseguire le operazioni seguenti:

-   Controllare se il client si trova in un elenco di client connessi (a cui è associato un catalogo). Se il client non è presente nell'elenco, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).
-   Verificare che il client disponga dell'accesso amministrativo. Se il client non dispone di accesso amministrativo, il server deve segnalare un errore di stato \_ accesso \_ negato (0xc0000022).
-   Avviare qualsiasi processo di manutenzione necessario per migliorare le prestazioni di esecuzione delle query in un catalogo, associato al client.
-   Rispondere al client con un'intestazione del messaggio per il CPMForceMergeIn e impostare il \_ campo stato sui risultati della richiesta.

Si noti che il processo di manutenzione è asincrono e può continuare dopo la ricezione del messaggio di risposta da parte del client. Questo processo non influisca direttamente sul protocollo in alcun modo, ad eccezione del tempo di risposta.

### <a name="3152-remote-indexing-service-querying"></a>Esecuzione di query sul servizio di indicizzazione remota 3.1.5.2

### <a name="31521-receiving-a-cpmconnectin-request"></a>3.1.5.2.1 che riceve una richiesta CPMConnectIn

Quando il server riceve una richiesta CPMConnectIn da un client, il server deve eseguire le operazioni seguenti:

-   Controllare se il client è nell'elenco dei client connessi. In tal caso, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).
-   Verifica se il catalogo specificato esiste e non è nello stato interrotto. In caso contrario, il server deve essere un \_ \_ errore di 0X8004181D (ci E \_ No Catalog) del report.
-   Aggiungere il client all'elenco dei client connessi.
-   Associare il catalogo al client.
-   Archiviare le informazioni passate nel messaggio CPMConnectIn, ad esempio il nome del catalogo, la versione del client e così via, nello stato del client.
-   Rispondere al client con un messaggio CPMConnectOut.

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a>3.1.5.2.2 che riceve una richiesta CPMCreateQueryIn

Quando il server riceve una richiesta di messaggio CPMCreateQueryIn da un client, il server deve eseguire le operazioni seguenti:

-   Controllare se il client è nell'elenco dei client connessi. In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).
-   Controllare se il client dispone già di una query associata. In tal caso, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).
-   Controllare se il catalogo associato al client si trova nello stato che consente l'elaborazione della query (CICAT \_ ReadOnly o CICAT \_ scrivibile). In caso contrario, il server deve segnalare un errore di query \_ S \_ senza \_ query (0x8004160C).
-   Analizza il set di restrizioni, gli ordinamenti e i raggruppamenti specificati nella query. Se il server rileva un errore, deve segnalare un errore appropriato. Se questo passaggio ha esito negativo per qualsiasi altro motivo, il server deve segnalare l'errore rilevato. Per informazioni sugli errori di query del servizio di indicizzazione, vedere \[ MSDN-QUERYERR \] .
-   Salvare la query di ricerca nello stato del client.
-   Apportare le preparazioni necessarie per gestire le righe a un client e associare la query ai cursori appropriati (a seconda delle informazioni passate nel messaggio CPMCreateQueryIn).
-   Aggiungere gli handle all'elenco di handle del cursore del client e inizializzare gli elenchi di punti di manipolazione e segnalibri del capitolo.
-   Inizializza l'elenco di handle del capitolo per ogni cursore in questa query su DB \_ null \_ hChapter
-   Inizializza l'elenco di handle di segnalibro per ogni cursore in questa query su un set di DBBMK \_ First e DBBMK \_ Last.
-   Contrassegnare la query come non monitorata per le modifiche.
-   Inizializza il numero di righe sul numero di righe attualmente calcolato, che può essere 0 se la query non è stata avviata o un numero se la query è in un processo di esecuzione, e inizializza il numeratore e il denominatore del completamento della query.
-   Rispondere al client con un messaggio CPMCreateQueryOut.

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a>3.1.5.2.3 che riceve una richiesta CPMGetQueryStatusIn

Quando il server riceve una richiesta di messaggio CPMGetQueryStatusIn da un client, il server deve eseguire le operazioni seguenti:

-   Controllare se al client è associata una query. In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).
-   Controllare se l'handle del cursore si trova in un elenco di handle del cursore del client. In caso contrario, il server deve segnalare un errore di E \_ (0x80004005).
-   Preparare un messaggio CPMGetQueryStatusOut. Il server deve recuperare lo stato corrente della query e impostarlo nel \_ campo QStatus. per i valori possibili, vedere 2.2.3.11. Se questo passaggio ha esito negativo per qualsiasi motivo, è necessario che il server segnali un errore.
-   Rispondere al client con il messaggio CPMGetQueryStatusOut.

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a>3.1.5.2.4 che riceve una richiesta CPMGetQueryStatusExIn

Quando il server riceve una richiesta di messaggio CPMGetQueryStatusExIn da un client, il server deve eseguire le operazioni seguenti:

-   Controllare se il client dispone di una query associata. In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).
-   Controllare se l'handle del cursore passato si trova in un elenco di handle del cursore del client. In caso contrario, il server deve segnalare un errore di E \_ (0x80004005).
-   Preparare un messaggio CPMGetQueryStatusExOut. Il server deve recuperare lo stato della query corrente e lo stato di avanzamento della query e impostare QStatus (vedere 2.2.3.11 per i valori possibili), \_ rispettivamente dwRatioFinishedDenominator e \_ dwRatioFinishedNumerator. DEVE quindi impostare il numero di righe nei risultati della query su \_ cRowsTotal. Se questo passaggio ha esito negativo per qualsiasi motivo, il server deve segnalare che si è verificato un errore.
-   Recuperare informazioni sul catalogo del client e compilare \_ cFilteredDocuments e \_ cDocumentsToFilter. Se questo passaggio ha esito negativo per qualsiasi motivo, il server deve segnalare che si è verificato un errore.
-   Recuperare la posizione del segnalibro indicato dall'handle nel \_ campo BMK e riempire il campo iRowBmk rimanente \_ nel messaggio CPMGetQueryStatusExOut. Se questo passaggio ha esito negativo per qualsiasi motivo, il server deve segnalare che si è verificato un errore.
-   Rispondere al client con il messaggio CPMGetQueryStatusExOut.

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a>3.1.5.2.5 che riceve una richiesta CPMRatioFinishedIn

Quando il server riceve una richiesta di messaggio CPMRatioFinishedIn da un client, il server deve eseguire le operazioni seguenti:

-   Controllare se al client è associata una query. In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).
-   Controllare se l'handle del cursore passato è nell'elenco degli handle del cursore del client. In caso contrario, il server deve segnalare un errore di E \_ (0x80004005).
-   Preparare un messaggio CPMRatioFinishedOut. Il server deve recuperare lo stato della query del client e compilare i \_ campi ulNumerator, \_ ulDenominator e \_ Crows. Se questo passaggio ha esito negativo per qualsiasi motivo, il server deve segnalare che si è verificato un errore.
-   Se \_ Crow è uguale all'ultimo numero di righe segnalato per la query, impostare \_ fNewRows su 0x00000000. in caso contrario, impostarlo su 0x00000001.
-   Aggiornare l'ultimo numero di righe segnalato per la query al valore di \_ Crows.
-   Rispondere al client con il messaggio CPMRatioFinishedOut.

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a>3.1.5.2.6 che riceve una richiesta CPMSetBindingsIn

Quando il server riceve una richiesta di messaggio CPMSetBindingsIn da un client, il server deve eseguire le operazioni seguenti:

-   Controllare se il client dispone di una query associata. In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).
-   Controllare se l'handle del cursore passato è nell'elenco degli handle del cursore del client. In caso contrario, il server deve segnalare un errore di E \_ (0x80004005).
-   Verificare che le informazioni sulle associazioni siano valide (ad esempio, la colonna almeno specifica il valore, la lunghezza o lo stato da restituire; nessuna sovrapposizione nei binding per valore, lunghezza o stato; e valore, lunghezza e stato rientrano nelle dimensioni della riga specificate) e se non segnala un \_ errore DB e \_ BADBINDINFO (0x80040E08).
-   Salvare le informazioni di binding associate alle colonne specificate nel campo aColumns. Se questo passaggio ha esito negativo per qualsiasi motivo, il server deve segnalare che si è verificato un errore.
-   Rispondere al client con un'intestazione del messaggio (solo) con \_ msg impostato su CPMSetBindingsIn e \_ lo stato impostato sui risultati dell'associazione specificata.

### <a name="31527-receiving-a-cpmgetrowsin-request"></a>3.1.5.2.7 che riceve una richiesta CPMGetRowsIn

Quando il server riceve una richiesta di messaggio CPMGetRowsIn da un client, il server deve eseguire le operazioni seguenti:

-   Controllare se al client è associata una query. In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).
-   Controllare se l'handle del cursore passato è in athelist degli handle del cursore del client. In caso contrario, il server deve segnalare un errore di E \_ (0x80004005).
-   Controllare se il client dispone di un set di associazioni corrente. In caso contrario, il server deve segnalare un errore di E \_ (0x80004005).
-   Preparare un messaggio CPMGetRowsOut. Il server deve posizionare il cursore nei risultati della query come indicato dalla descrizione della ricerca. Se questo passaggio ha esito negativo per qualsiasi motivo, il server deve segnalare che si è verificato un errore.
-   Recuperare il numero di righe che corrisponde a un buffer, le cui dimensioni sono indicate da \_ cbReadBuffer, ma non più di quelle indicate da \_ cRowsToTransfer. Durante il recupero delle righe, il server deve confrontare il tipo di valore della proprietà di ogni colonna selezionata con il tipo specificato nel set di associazioni corrente del client (sezione 3.1.1). Se il tipo nell'associazione non è una \_ variante VT, il server deve tentare di convertire il valore della proprietà della colonna in quel tipo. In caso contrario, se il \_ flag DBPROP USEEXTENDEDDBTYPES è impostato nel set di \_ proprietà DBPROPSET QUERYEXT del client o se il valore della proprietà della colonna non è un tipo di vettore VT \_ , il valore della proprietà deve essere restituito nel tipo normale. Se nessuno di questi casi (ad esempio, il server ha un \_ tipo di vettore VT e il client non supporta il \_ vettore VT), il server deve tentare di convertirlo in un tipo di matrice VT \_ come segue: VT \_ i8, VT \_ UI8, VT \_ FILETIME e \_ gli elementi della matrice CLSID VT non possono essere convertiti e non hanno esito negativo; \_ \_ Gli elementi della matrice VT LPSTR e VT LPWSTR devono essere convertiti in un \_ BSTR di tipo VT; gli elementi di matrice di tutti gli altri tipi devono rimanere invariati. Infine, se le colonne di riga contengono handle di capitolo o di segnalibri, il server deve aggiornare gli elenchi corrispondenti. Se questo passaggio ha esito negativo per qualsiasi motivo, il server deve segnalare che si è verificato un errore.
-   Archiviare il numero effettivo di righe recuperate in \_ cRowsReturned.
-   Copiare la descrizione della ricerca e il campo del capitolo da CPMGetRowsIn a un messaggio CPMGetRowsOut da inviare.
-   Archiviare le righe recuperate nel campo Rows (vedere la nota sul byte di stato sotto e la sezione 2.2.3.16 sulla struttura del campo Rows).
-   Rispondere al client con il messaggio CPMGetRowsOut.

Nota sul campo byte di stato:

Se StatusUsed è impostato su 0x01 in CTableColumn del messaggio CPMSetBindingIn per la colonna, il server deve impostare il byte di stato (che si trova in StatusOffset dall'inizio della riga) per la colonna su uno dei valori seguenti:



| Valore | Significato        |
|-------|----------------|
| 0x00  | StatusOK       |
| 0x01  | StatusDeferred |
| 0x02  | StatusNull     |



 

Se per questa riga il valore della proprietà è assente, il server deve impostare il byte di stato su StatusNull. Se il valore è troppo grande per essere trasferito nel messaggio CPMGetRowsOut, il server deve impostare il byte di stato su StatusDeferred. In caso contrario, il server deve impostare il byte di stato su StatusOK.

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a>3.1.5.2.8 che riceve una richiesta CPMFetchValueIn

Quando il server riceve una richiesta di messaggio CPMFetchValueIn da un client, il server deve eseguire le operazioni seguenti:

-   Controllare se al client è associata una query. In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).
-   Preparare un messaggio CPMFetchValueOut. Se questo passaggio ha esito negativo per qualsiasi motivo, è necessario che il server segnali un errore.
-   Trovare il documento indicato dal \_ campo wid e verificare se l'ID di proprietà del documento (in seguito definito "valore della proprietà") indicato dalla struttura Campo PROPSPEC è disponibile per questo client. Se questo valore non è disponibile, il server deve impostare \_ fValueExists su 0x00000000 e in caso contrario impostare \_ fValueExists su 0x00000001. Se questo passaggio ha esito negativo per qualsiasi motivo, è necessario che il server segnali un errore.
-   Se \_ fValueExists è uguale a 0x00000001, il server deve eseguire le operazioni seguenti:
-   -   Serializzare il valore della proprietà in una struttura SERIALIZEDPROPERTYVALUE e copiare, a partire dall' \_ offset cbSoFar, al massimo \_ cbChunk byte, ma non oltre la fine della proprietà serializzata, nel campo vValue. Se questo passaggio ha esito negativo per qualsiasi motivo, il server deve segnalare un errore.
    -   Impostare \_ cbValue sul numero di byte copiati nel passaggio precedente.
    -   Impostare vType sul tipo di proprietà del valore della proprietà.
    -   Se la lunghezza della proprietà serializzata è maggiore di \_ cbSoFar aggiunta a \_ cbValue, impostare \_ fMoreExists su 0x00000001. in caso contrario, impostarla su 0x00000000.

-   Rispondere al client con il messaggio CPMFetchValueOut

### <a name="31529-receiving-a-cpmgetnotify-request"></a>3.1.5.2.9 che riceve una richiesta CPMGetNotify

Quando il server riceve un messaggio CPMGetNotify da un client, il server deve eseguire le operazioni seguenti:

-   Controllare se al client è associata una query. In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).
-   Se non sono state apportate modifiche al set di risultati della query dopo l'ultimo messaggio CPMSendNotifyOut per questo client o se la query non è attualmente monitorata per le modifiche nel set di risultati, il server deve rispondere con un messaggio CPMGetNotify e iniziare a monitorare la query per le modifiche nel set di risultati. Se in un secondo momento viene apportata una modifica al set di risultati della query, il server deve inviare esattamente un messaggio CPMSendNotifyOut al client e deve specificare la modifica nel \_ campo watchNotify.
-   Se sono state apportate modifiche al set di risultati della query dall'ultimo messaggio CPMSendNotifyOut, il server deve rispondere con CPMSendNotifyOut e deve specificare la modifica nel \_ campo watchNotify. Si noti che, nel caso di molte modifiche ai risultati della query, DBWATCHNOTIFY \_ ROWSCHANGED ha priorità (ad esempio, se la query è stata eseguita, rieseguita e quindi il numero di righe è stato modificato e la query è stata eseguita di nuovo, l'evento segnalato sarebbe DBWATCHNOTIFY \_ ROWSCHANGED).

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a>3.1.5.2.10 che riceve una richiesta CPMGetApproximatePositionIn

Quando il server riceve una richiesta di messaggio CPMGetApproximatePositionIn dal client, il server deve eseguire le operazioni seguenti:

-   Controllare se il client dispone di una query associata. In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).
-   Verificare che l'handle del cursore, l'handle del capitolo e l'handle di segnalibro passati si trovino negli elenchi corrispondenti. In caso contrario, il server deve segnalare un errore di E \_ (0x80004005).
-   Trovare una riga associata all'handle dei segnalibri nei risultati della query e approssimare la posizione della riga nel set di righe, a cui fa riferimento l'handle del capitolo e determinare il numeratore e il denominatore per la posizione. Si noti che quando l'handle del capitolo è DB \_ null \_ hChapter, il capitolo corrispondente è il set di righe principale della query. Se questo passaggio ha esito negativo per qualsiasi motivo, è necessario che il server segnali un errore.
-   Rispondere al client con un messaggio CPMFetchValueOut.

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a>3.1.5.2.11 che riceve una richiesta CPMCompareBmkIn

Quando il server riceve una richiesta di messaggio CPMCompareBmkIn dal client, il server deve eseguire le operazioni seguenti:

-   Controllare se il client dispone di una query associata. In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).
-   Verificare che l'handle del cursore, l'handle del capitolo e gli handle dei segnalibri passati si trovino negli elenchi corrispondenti. In caso contrario, il server deve segnalare un errore di E \_ (0x80004005).
-   Preparare un messaggio CPMCompareBmkOut.
-   Se gli handle di segnalibro sono uguali, \_ DWCOMPARISON deve essere impostato su DBCOMPARE \_ EQ.
-   In caso contrario, se uno dei segnalibri gestisce è DBBMK \_ First o DBBMK \_ Last, \_ dwComparison deve essere impostato su DBCOMPARE \_ ne.
-   In caso contrario, il server deve eseguire le operazioni seguenti:
-   -   Trova le righe a cui fa riferimento ogni handle di segnalibro nei risultati della query
    -   Se una delle righe non è presente nel capitolo indicato dall'handle del capitolo in CPMCompareBmkIn, \_ DWCOMPARISON deve essere impostato su DBCOMPARE \_ NOTCOMPARABLE.
    -   In caso contrario, quando entrambe le righe si trovano nello stesso capitolo, il server deve approssimare una posizione di tali righe nel set di righe a cui fa riferimento l'handle di questo capitolo. DEVE quindi confrontare i valori di posizione e impostare \_ dwComparison su DBCOMPARE \_ lt se la posizione della prima riga è minore della posizione della seconda riga; in caso contrario, \_ dwComparison deve essere impostato su DBCOMPARE \_ gt.

-   Rispondere al client con un messaggio CPMCompareBmkOut compilato.

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a>3.1.5.2.12 che riceve una richiesta CPMRestartPositionIn

Quando il server riceve la richiesta del messaggio CPMRestartPositionIn dal client, il server deve eseguire le operazioni seguenti:

-   Controllare se il client dispone di una query associata. In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).
-   Controllare se l'handle del cursore e l'handle del capitolo sono stati passati negli elenchi corrispondenti. In caso contrario, il server deve segnalare un errore di E \_ (0x80004005).
-   Spostare il cursore all'inizio del capitolo, identificato dall'handle del capitolo. Si noti che quando l'handle del capitolo è DB \_ null \_ hChapter, il capitolo corrispondente è il set di righe principale della query. Se questo passaggio ha esito negativo per qualsiasi motivo, è necessario che il server segnali un errore.
-   Rispondere al client con un messaggio CPMRestartPositionIn.

### <a name="315213-receiving-a-cpmfreecursorin-request"></a>3.1.5.2.13 che riceve una richiesta CPMFreeCursorIn

Quando il server riceve una richiesta di messaggio CPMFreeCursorIn dal client, il server deve eseguire le operazioni seguenti:

-   Controllare se il client dispone di una query associata. In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).
-   Controllare se l'handle del cursore passato è nell'elenco degli handle del cursore del client. In caso contrario, il server deve segnalare un errore di E \_ (0x80004005).
-   Rilasciare il cursore e le risorse associate (vedere la sezione 3.1.1 per l'elenco completo) per questo handle del cursore.
-   Rimuovere il cursore dall'elenco dei cursori per il client.
-   Rispondere con un messaggio CPMFreeCursorOut, impostando il \_ campo cCursorsRemaining con il numero di cursori rimanenti. nell'elenco di questo client.
-   Se non sono presenti altri cursori per questo client, il server deve rilasciare la query e le risorse associate (vedere la sezione 3.1.1).

### <a name="315214-receiving-a-cpmdisconnect-request"></a>3.1.5.2.14 che riceve una richiesta CPMDisconnect

Quando il server riceve una richiesta di messaggio CPMDisconnect dal client, il server deve rimuovere il client dall'elenco dei client connessi e rilasciare tutte le risorse associate al client.

### <a name="316-timer-events"></a>Eventi del timer 3.1.6

Nessuna.

### <a name="317-other-local-events"></a>3.1.7 altri eventi locali

Quando il server viene arrestato, è necessario innanzitutto eseguire la transizione allo stato "chiusura in corso". DEVE quindi interrompere l'ascolto della pipe, eseguire altre attività di arresto specifiche dell'implementazione e quindi passare allo stato "arrestato".

### <a name="32-client-details"></a>3,2 Dettagli client

### <a name="321-abstract-data-model"></a>3.2.1 modello di dati astratto

La sezione seguente specifica i dati e lo stato gestiti dal client del protocollo del servizio di indicizzazione del contenuto. I dati forniti consentono di semplificare la spiegazione del comportamento del protocollo. Questa sezione non impone che le implementazioni siano conformi a questo modello, purché il loro comportamento esterno sia coerente con quello descritto in questo documento.

Un client ha lo stato astratto seguente:

-   **Ultimo messaggio inviato**: copia dell'ultimo messaggio inviato al server.
-   **Valore della proprietà corrente**: valore parziale di una proprietà "rinviata", che è in fase di recupero.
-   **Byte correnti ricevuti**: finora il numero di byte ricevuti per il valore corrente della proprietà.
-   **Stato connessione named pipe**: una connessione al server

### <a name="322-timers"></a>3.2.2 timer

Non sono richiesti timer del protocollo.

### <a name="323-initialization"></a>3.2.3 inizializzazione

Non viene eseguita alcuna azione fino a quando non viene ricevuta una richiesta di livello superiore.

### <a name="324-higher-layer-triggered-events"></a>3.2.4 Higher-Layer eventi attivati

Quando una richiesta viene ricevuta da un livello superiore, il client deve creare una connessione named pipe al server, usando i dettagli specificati nella sezione 2,1. Se non è possibile eseguire questa operazione, la richiesta di livello superiore deve essere non riuscita. Ovvero, in caso di errore di connessione, è responsabilità del livello superiore ritentare, se lo si desidera.

Un'intestazione deve essere pre-sospesa con i campi impostati come specificato nella sezione 2.2.2.

Per i messaggi specificati in modo da richiedere un checksum diverso da zero, il \_ valore di ULCHECKSUM deve essere calcolato come segue:

1.  Il contenuto del messaggio dopo il \_ campo ulReserved2 nell'intestazione del messaggio deve essere interpretato come una sequenza di interi a 32 bit. Il client deve calcolare la somma dei valori numerici forniti da questi numeri interi.
2.  Calcola l'XOR bit per bit di questo valore con 0x59533959.
3.  Sottrae il valore specificato da \_ msg dal valore risultante dall'operazione XOR bit per bit.

### <a name="3241-remote-indexing-service-catalog-management"></a>Gestione del catalogo di servizi di indicizzazione remota di 3.2.4.1

Ogni messaggio viene attivato da una richiesta dal livello superiore. Non esiste alcuna sequenza di messaggi applicata dal client per le richieste di messaggi CISP per la gestione remota dei cataloghi, ma (ad eccezione di un messaggio CPMSetCatStateIn) il server risponderà con esito positivo solo se il client si è connesso in precedenza tramite un messaggio CPMConnectIn.

### <a name="32411-sending-a-cpmcistateinout-request"></a>3.2.4.1.1 invio di una richiesta CPMCiStateInOut

In genere, il livello superiore chiede al client del protocollo di inviare un messaggio CPMCiStateInOut quando richiede informazioni sull'indicizzazione dei servizi nel server.

Quando viene richiesto di inviare questo messaggio, il client deve eseguire le operazioni seguenti:

-   Inviare un messaggio CPMCiStateInOut come specificato nella sezione 2.2.3.1 al server.
-   Attendere la ricezione del messaggio CPMCiStateInOut dal server, ignorando automaticamente tutti gli altri messaggi.
-   Segnalare il valore del \_ campo status della risposta e, in caso di esito positivo, la struttura informativa torna al livello superiore.

### <a name="32412-sending-a-cpmsetcatstatein-request"></a>3.2.4.1.2 invio di una richiesta CPMSetCatStateIn

In genere, il livello superiore chiede al client del protocollo di inviare un messaggio CPMSetCatStateIn quando richiede informazioni su un catalogo o su tutto il catalogo. Per questo messaggio, il livello superiore deve fornire al client del protocollo un valore per \_ dwNewState e, se necessario, il nome del catalogo.

Quando viene richiesto di inviare questo messaggio, il client deve eseguire le operazioni seguenti:

-   Inviare un messaggio CPMSetCatStateIn come specificato in 2.2.3.2 al server.
-   Attendere la ricezione di un messaggio CPMSetCatStateOut dal server, ignorando automaticamente tutti gli altri messaggi.
-   Segnalare il valore del \_ campo status della risposta e, in caso di esito positivo, \_ dwOldState di nuovo al livello superiore.

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a>3.2.4.1.3 invio di una richiesta CPMUpdateDocumentsIn

Il livello superiore richiede in genere di inviare questo messaggio quando è necessario aggiornare i documenti in un percorso esistente o aggiungere un nuovo percorso di file all'indice. Quindi, il livello superiore consiste nel fornire il percorso e il tipo di un'analisi, specificata come nella sezione 2.2.3.4, in cui un aggiornamento incrementale o completo è destinato ai percorsi esistenti e la nuova inizializzazione è destinata a nuovi percorsi.

Per soddisfare la richiesta di livello superiore, il client deve eseguire le operazioni seguenti:

-   Inviare un messaggio CPMUpdateDocumentsIn come specificato nella sezione 2.2.3.4 al server.
-   Attendere la ricezione del messaggio CPMUpdateDocumentsIn dal server, ignorando automaticamente tutti gli altri messaggi.
-   Segnalare il valore del \_ campo stato della risposta al livello superiore.

### <a name="32414-sending-a-cpmforcemergein-request"></a>3.2.4.1.4 invio di una richiesta CPMForceMergeIn

In genere, il livello superiore richiede di inviare questo messaggio quando è necessario migliorare le prestazioni di esecuzione delle query oppure fa parte della manutenzione pianificata del servizio di indicizzazione.

Per gestire il livello superiore, il client deve eseguire le operazioni seguenti:

-   Inviare il messaggio CPMForceMergeIn come specificato dalla sezione 2.2.3.5 al server.
-   Attendere la ricezione di un messaggio CPMUpdateDocumentsIn dal server, ignorando automaticamente tutti gli altri messaggi.
-   Segnalare il valore del \_ campo stato della risposta al livello superiore.

### <a name="3242-remote-indexing-service-catalog-query-messages"></a>Messaggi di query del catalogo di servizi di indicizzazione remota 3.2.4.2

Ad eccezione di CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, esiste una relazione uno-a-uno tra i messaggi di CISP e le richieste di livello superiore. Per le due eccezioni indicate in precedenza, possono essere presenti più messaggi generati dal client per soddisfare i requisiti di dimensione o per recuperare una proprietà completa. Il livello superiore tiene in genere traccia di tutte le informazioni specifiche della query (ad esempio, gli handle del cursore aperti, i valori validi per gli handle di segnalibro e di capitolo, i valori wid per i valori delle proprietà posticipate e così via) e tiene traccia anche se il client si trova in uno stato connesso, ma ciò non viene applicato in alcun modo dal client.

A scopo illustrativo, la parte client del diagramma nella sezione 3 illustra questa sequenza per una semplice query del servizio di indicizzazione.

### <a name="32421-sending-a-cpmconnectin-request"></a>3.2.4.2.1 invio di una richiesta CPMConnectIn

Questo messaggio è in genere la prima richiesta del livello superiore (come se il client non fosse connesso, il server avrà esito negativo nella maggior parte dei messaggi ad eccezione di CPMSetCatStateIn). Il livello superiore fornisce al client del protocollo le informazioni necessarie per la connessione.

Per gestire il livello superiore, il client deve eseguire le operazioni seguenti:

-   Compilare il messaggio, usando le informazioni fornite dal client di livello superiore (vedere la sezione 2.2.3.6) in \_ iClientVersion, MachineName, username, PropertySet1, PropertySet2 e aPropertySet.
-   Impostare \_ fClientIsRemote, \_ cbBlob, \_ cbBlob2, cPropSet e cExtPropSet come specificato in 2.2.3.6.
-   Impostare il checksum nel \_ campo ulChecksum.
-   Inviare il messaggio CPMConnectIn al server.
-   Attendere la ricezione di un messaggio CPMConnectOut dal server, ignorando automaticamente tutti gli altri messaggi.
-   Segnalare il valore del \_ campo status della risposta e, in caso di esito positivo, \_ ServerVersion di nuovo al livello superiore.

A scopo informativo, si prevede che i livelli più elevati eseguano in genere le azioni seguenti al completamento della connessione, ma non vengono applicati dal client CISP:

-   Usare i messaggi di gestione del catalogo di servizi di indicizzazione remota per le attività amministrative
-   Usare una richiesta CPMCreateQueryIn per creare una query di ricerca con lo scopo di recuperare i risultati dal catalogo.

### <a name="32422-sending-a-cpmcreatequeryin-request"></a>3.2.4.2.2 invio di una richiesta CPMCreateQueryIn

Il livello superiore fornirà in genere informazioni per la creazione della query dopo la connessione del client del protocollo. Il livello superiore fornisce al client un set di restrizioni, un set di colonne, le regole di ordinamento e il set di categorizzazione (ognuno di essi può essere omesso), le proprietà del set di righe e la struttura di mapping degli ID di proprietà.

Quando questa richiesta viene ricevuta da un livello superiore, il client deve eseguire le operazioni seguenti:

-   Preparare un CPMCreateQueryOut come indicato di seguito.
-   -   Se è presente un set di colonne, impostare CColumnsSetPreset su 0x01 e compilare il campo ColumnsSet.
    -   Se sono presenti restrizioni, impostare CRestrictionPresent su 0x01 e compilare il campo restrizione.
    -   Se è presente un set di ordinamento, compilare il campo Fascicola.
    -   Se è presente un set di categorizzazione, impostare CSortSetPresent su 0x01 e compilare il campo CategorizationSet.
    -   Imposta il resto dei campi come specificato in 2.2.3.8

-   Calcolare \_ il campo ulCheckSum nell'intestazione.
-   Inviare il messaggio CPMCreateQueryIn al server.
-   Attendere la ricezione del messaggio CPMCreateQueryOut (vedere i dettagli nella sezione 3.2.5.1.1), ignorando automaticamente tutti gli altri messaggi.
-   Segnalare il valore del \_ campo status della risposta e, in caso di esito positivo, la matrice di handle del cursore e i valori booleani informativi, come specificato in 2.2.3.9, al livello superiore.

### <a name="32423-sending-a-cpmsetbindingsin-request"></a>3.2.4.2.3 invio di una richiesta CPMSetBindingsIn

In genere, il livello superiore imposta le associazioni per ogni colonna da restituire nelle righe quando dispone già di un handle di cursore valido (dopo la ricezione corretta di CPMCreateQueryOut, vedere la sezione 3.2.5.1.1). Maggiore è il previsto che fornisca una matrice di strutture CTableColumn, come specificato nella sezione 2.2.4.31, per il campo aColumns e un handle di cursore valido.

Quando questa richiesta viene ricevuta dal livello superiore, il client deve eseguire le operazioni seguenti:

-   Calcolare il numero di strutture CTableColumn nella matrice aColumns e impostare il campo cColumns su questo valore.
-   Calcolare la dimensione totale in byte dei campi cColumns e aColumns e impostare il \_ campo cbBindingDesc su questo valore.
-   Impostare i campi specificati nel messaggio CPMSetBindingsIn sui valori forniti dal livello dell'applicazione superiore. Impostare il \_ campo ulChecksum sul valore calcolato come specificato nella sezione 3.2.5.
-   Inviare il messaggio CPMSetBindignsIn completato al server.
-   Attendere la ricezione di un messaggio CPMSetBindingsIn dal server, ignorando gli altri messaggi.
-   Indicare lo stato dal \_ campo stato della risposta al livello superiore.

A scopo informativo, è previsto che i livelli più elevati in genere chiedano a un client di inviare un messaggio CPMGetRowsIn, ma questo non viene applicato dal protocollo del servizio di indicizzazione del contenuto.

### <a name="32424-sending-a-cpmgetrowsin-request"></a>3.2.4.2.4 invio di una richiesta CPMGetRowsIn

Quando il livello superiore sta per ricevere le informazioni sulle righe, fornirà il client del protocollo con handle di cursore e capitolo validi e fornirà la descrizione di ricerca appropriata. In genere, è previsto un livello superiore quando dispone di un handle di cursore e/o di un capitolo valido e i binding sono stati impostati con un messaggio CPMSetBindingsIn. Per accedere al set di righe in un capitolo, il livello superiore prevede l'uso dell'handle del capitolo ricevuto dal server in un messaggio CPMGetRowsOut precedente.

Quando questa richiesta viene ricevuta dal livello superiore, il client deve eseguire le operazioni seguenti:

-   Determinare il valore Unsigned Integer da specificare per il \_ campo cbReadBuffer. Per determinare questo valore, il client deve assumere il valore massimo da quanto segue:
-   -   1000 volte il valore del campo c \_ RowsToTransfer.
    -   Valore di \_ cbRowWidth, arrotondato per eccesso al più vicino 512 byte più vicino.
    -   Prendere il valore superiore di questi due valori, fino al limite di 16K.
    -   Nei casi in cui una singola riga è maggiore di 16K, il server non può restituire risultati a questa query.

Specificare una base client per i dati di riga a dimensione variabile nello spazio degli indirizzi del client nel \_ campo ulClientBase.

*Comportamento di Windows: per un client a 32 bit che comunica con un server a 32 bit o un client a 64 bit che comunica con un server a 64 bit, questo valore è impostato su un indirizzo di memoria del buffer di ricezione nel processo dell'applicazione. In questo modo, i puntatori, ricevuti nel campo Rows di CPMGetRowsOut, sono corretti per i puntatori di memoria in un processo dell'applicazione client. In caso contrario, viene impostato su 0x00000000.*

-   Calcolare la dimensione della descrizione della ricerca e impostarla nel \_ campo cbSeek.
-   Impostare il valore di cbReserved (che fungerebbe da offset per l'avvio delle righe) al valore di \_ cbSeek più 0x14.
-   Inviare un messaggio CPMConnectIn come specificato in 2.2.3.15 al server.

### <a name="32425-sending-a-cpmfetchvaluein-request"></a>3.2.4.2.5 invio di una richiesta CPMFetchValueIn

Se il client riceve una risposta CPMGetRowsOut dal server con il campo di stato della colonna impostato su StatusDeferred (0x01), significa che il valore della proprietà non è stato incluso nel campo Rows del messaggio CPMGetRowsOut. In questo caso, il livello superiore richiede in genere al client del protocollo di recuperare il valore per mezzo del messaggio CPMFetchValueIn e fornisce il \_ valore Campo PROPSPEC e wid per una proprietà posticipata, che il client del protocollo deve usare nel primo messaggio CPMFetchValueIn.

Se questo è il primo messaggio CPMFetchValueIn inviato dal client per richiedere la proprietà specificata, il client deve eseguire le operazioni seguenti:

-   Impostare tutti i campi in un messaggio come specificato nella sezione 2.2.3.19.
-   Impostare \_ cbSoFar su 0x00000000.
-   Imposta i byte correnti ricevuti su 0.
-   Inviare il messaggio CPMFetchValueIn al server.

### <a name="32426-sending-a-cpmfreecursorin-request"></a>3.2.4.2.6 invio di una richiesta CPMFreeCursorIn

Quando il livello superiore non utilizza più la query di ricerca, può rilasciare le risorse sul server chiedendo al client di inviare un messaggio CPMFreeCursorIn.

Quando viene ricevuta questa richiesta, il client deve inviare un messaggio CPMFreeCursorIn come specificato in 2.2.3.28 al server, contenente l'handle specificato dal livello superiore.

### <a name="32427-sending-a-cpmdisconnect-message"></a>3.2.4.2.7 invio di un messaggio CPMDisconnect

Se il livello superiore non ha altre query per il servizio di indicizzazione, per liberare più risorse server, l'applicazione può richiedere che il client invii un messaggio CPMDisconnect al server. Quando la query viene ricevuta, il client deve semplicemente inviare il messaggio come richiesto. Non esiste alcuna risposta a questo messaggio dal server.

### <a name="325-message-processing-and-sequencing-rules"></a>Regole di sequenziazione e elaborazione dei messaggi 3.2.5

Quando il client riceve una risposta del messaggio dal server, il client deve utilizzare l'ultimo messaggio inviato per determinare se il messaggio ricevuto dal server è quello previsto dal client. Tutti i messaggi con \_ un campo msg diverso da quello nell'ultimo messaggio di invio devono essere ignorati.

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a>3.2.5.1 ricezione di una risposta CPMCreateQueryOut

Quando il client riceve una risposta del messaggio CPMCreateQueryOut dal server, il client deve restituire \_ lo stato e (se lo stato ha esito positivo) i valori di handle del cursore al livello superiore. Tutte le altre azioni sono al livello superiore.

Poiché il livello superiore è in grado di riconoscere la struttura della query, il numero di handle di cursore da restituire nel messaggio CPMCreateOueryOut sarà sempre corretto. Gli handle del cursore vengono restituiti nell'ordine seguente: il primo handle viene utilizzato per il set di righe non sottoscritto, il secondo al primo set di righe con capitoli, ovvero il raggruppamento dei risultati in base alla prima categoria specificata nel campo CategorizationSet del messaggio CPMCreateQueryIn.

A scopo informativo, si prevede che i livelli più elevati possano eseguire le azioni seguenti, ma non vengono applicati dal client CISP:

-   Usare CPMSetBindingsIn per impostare le associazioni per le singole colonne ed eseguire eventuali azioni successive sul percorso della query
-   Usare CPMGetQueryStatusIn per controllare lo stato di esecuzione di una query.
-   Usare CPMRatioFinishedIn per richiedere la percentuale di completamento della query.

### <a name="3252-receiving-a-cpmgetrowsout-response"></a>3.2.5.2 ricezione di una risposta CPMGetRowsOut

Quando il client riceve una risposta del messaggio CPMGetRowsOut dal server, il client deve eseguire le operazioni seguenti:

-   Controllare che il \_ campo stato nell'intestazione indichi esito positivo o negativo.
-   Se il \_ valore dello stato è un buffer di stato \_ \_ troppo \_ piccolo (0xC0000023), il client deve controllare lo stato dell'ultimo messaggio inviato. Se non contiene un messaggio CPMGetRowsIn, il messaggio ricevuto deve essere ignorato automaticamente. In caso contrario, il client deve inviare al server un nuovo messaggio CPMGetRowsIn con tutti i campi identici a quello archiviato, ad eccezione del fatto che \_ CBREADBUFFER deve essere aumentato di 512 (ma non maggiore di 0x4000). Se \_ lo stato è \_ \_ un buffer di stato troppo \_ piccolo (0XC0000023) e l'ultimo messaggio inviato ha già \_ CBREADBUFFER uguale a 0x4000 client deve segnalare l'errore fino al livello superiore.
-   Se il \_ valore di stato è qualsiasi altro valore di errore, il client deve indicare l'errore fino al livello superiore.
-   Se il \_ valore di stato indica esito positivo, i risultati devono essere indicati fino al livello superiore che richiede le informazioni e altre azioni sono al livello superiore.

A scopo informativo, si prevede che i livelli superiori eseguano in genere le azioni seguenti, ma non vengono applicati dal client del protocollo del servizio di indicizzazione del contenuto:

-   Se i valori nelle righe rappresentano gli ID del documento, il capitolo o il segnalibro gestisce il livello superiore in genere li archivia per l'utilizzo in operazioni successive che coinvolgono ID documento o handle di segnalibro validi.
-   Il livello superiore in genere archivia o Visualizza o utilizza in altro modo i dati dei valori di riga.
-   Per i valori che sono stati contrassegnati come livello superiore posticipato, recupereranno il valore usando i messaggi CPMFetchValueIn.
-   La descrizione della ricerca viene restituita anche a livello superiore e può essere riutilizzata o esaminata dal livello superiore.

A scopo informativo, se il livello superiore ha richiesto handle ai capitoli e ai segnalibri ricevuti nelle righe, è possibile eseguire le operazioni seguenti:

-   Utilizzare CPMGetQueryStatusExIn, per verificare lo stato di esecuzione di una query, nonché informazioni aggiuntive sullo stato, ad esempio il numero di documenti filtrati, i documenti rimanenti da filtrare, il rapporto tra documenti elaborati dalla query, il numero totale di righe nella query e la posizione del segnalibro nel set di righe.
-   Utilizzare CPMGetNotify per richiedere che il server invii notifiche al client delle modifiche dei set di righe.
-   Usare CPMGetApproximatePositionIn per richiedere la posizione approssimativa di un segnalibro in un capitolo.
-   Usare CPMCompareBmkIn per richiedere un confronto tra due segnalibri in un capitolo.
-   Utilizzare CPMRestartPositionIn nel server per modificare la posizione del cursore all'inizio del set di righe.

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a>3.2.5.3 ricezione di una risposta CPMFetchValueOut

Quando il client riceve una risposta del messaggio CPMGetRowsOut dal server, il client deve eseguire le operazioni seguenti:

-   Controllare che il \_ campo stato nell'intestazione indichi esito positivo o negativo. In caso di errore, notificare il livello superiore. In caso contrario, continuare.
-   Controllare \_ fValueExist e, se impostato su 0x00000000, notificare al livello superiore che il valore non è stato trovato.
-   In caso contrario \_ , aggiungere cbValue byte da vValue al valore della proprietà corrente.
-   Se \_ \_ fMoreExists è impostato su 0x00000001, incrementare i \_ byte correnti ricevuti da \_ cbValue e inviare un messaggio CPMFetchValueIn al server, impostando \_ CbSoFar sul valore dei byte correnti ricevuti, \_ cbPropSpec su zero e \_ cbChunk sulle dimensioni del buffer desiderate dal livello superiore.
-   Se \_ fMoreExists è impostato su 0x00000000, indicare il valore della proprietà dal valore della proprietà corrente al livello superiore.

### <a name="3254-receiving-a-cpmfreecursorout-response"></a>3.2.5.4 ricezione di una risposta CPMFreeCursorOut

Quando il client riceve una risposta corretta del messaggio CPMFreeCursorOut dal server, il client deve restituire il \_ valore cCursorsRemaining al livello superiore.

Le informazioni seguenti vengono fornite solo a scopo informativo e non vengono applicate dal client CISP. Si prevede che il livello superiore tenga traccia degli handle del cursore e non di quelli che sono già stati liberati. Quando il numero di \_ cCursorsRemaining è uguale a 0x00000000, il livello superiore può usare la connessione per specificare un'altra query (usando un messaggio CPMCreateQueryIn).

### <a name="326-timer-events"></a>Eventi del timer 3.2.6 nelle

Nessuna.

### <a name="327-other-local-events"></a>3.2.7 altri eventi locali

Nessuna.

## <a name="4-protocol-examples"></a>4 Esempi di protocollo

-   [4,1 esempio 1](#41-example-1)
-   [4,2 esempio 2](#42-example-2)

### <a name="41-example-1"></a>4,1 esempio 1

Nell'esempio seguente viene considerato uno scenario in cui l'utente JOHN sul computer A desidera ottenere le dimensioni dei file che contengono la parola "Microsoft" dal set di documenti archiviati in server X nel sistema di catalogo. Supponiamo che il computer A esegua un sistema operativo Windows XP a 32 bit e che il computer X esegua un sistema operativo Windows Server 2003 a 32 bit.

1.  L'utente avvia un'applicazione di ricerca e immette la query di ricerca. A sua volta, l'applicazione passa la query di ricerca al client del protocollo.
2.  Il client del protocollo stabilisce una connessione con il server di indicizzazione X. Il client del protocollo usa il named pipe \\ pipe \\ ci \_ SKADS per connettersi al server X tramite SMB.
3.  Il client del protocollo prepara quindi un messaggio CPMConnectIn con i valori seguenti:

    L'intestazione del messaggio viene popolata come indicato di seguito:

    -   **\_ msg** è impostato su 0x000000C8, a indicare che si tratta di un messaggio CPMConnectIn.
    -   **\_ status** è impostato su 0x00000000.
    -   **\_ ulChecksum** contiene il checksum, calcolato come specificato nella sezione 3.2.4.
    -   **\_ ulReserved2** è impostato su 0x00000000.

    Il corpo del messaggio viene popolato nel modo seguente:

    -   **\_ iClientVersion** è impostato su 0x00000008, che indica che il server deve convalidare il campo di checksum.
    -   **\_ fClientIsRemote** è impostato su 0x00000001, che indica che il server è un server remoto.
    -   **\_ cbBlob1** è impostato sulle dimensioni, in byte, dei campi cPropSet, PropertySet1 e PropertySet2 combinati.
    -   **\_ cbBlob2** è impostato su 0x00000004 (ovvero senza set di proprietà aggiuntivi).
    -   **MachineName** è impostato su.
    -   **Username** è impostato su John.
    -   **cPropSets** è impostato su 0x00000002.
    -   Il campo **PropertySet1** è di tipo CDbPropSet. La struttura CDbPropSet che comprende il campo PropertySet1 viene popolata come indicato di seguito:
        -   Il campo **GuidPropSet** è impostato su A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ EXT).
        -   il campo **cProperties** è impostato su 0x00000004.
        -   il campo **aProps** è una matrice di strutture CDbProp.

            Per l' **elemento \[ aProps \] 0** :

            -   **PropId** è impostato su 0x00000002 ( \_ nome del \_ catalogo ci DBPROP \_ ).
            -   **DBPROPOPTIONS** è impostato su 0x0000000.
            -   **DBPROPSTATUS** è impostato su 0x00000000.
            -   Per l'elemento **colid** :
                -   **eKind** è impostato su 0x00000001 (dbkind \_ GUID \_ propid)
                -   Il **GUID** è null (tutti zeri), ovvero il valore si applica alla query, non solo a una singola colonna.
                -   **ulID** è impostato su 0x00000000.
            -   Per l'elemento **vValue** :
                -   **vType** è impostato su 0X001F (VT \_ LPWSTR).
                -   **vValue** è impostato su "System", il nome del catalogo desiderato.

            Per l' **elemento \[ aProps \] 1** :

            -   **PropId** è impostato su 0x00000007 ( \_ tipo di \_ query ci DBPROP \_ )
            -   **DBPROPOPTIONS** è impostato su 0x0000000.
            -   **DBPROPSTATUS** è impostato su to0x00000000.
            -   Per l'elemento **colid** :
                -   **eKind** è impostato su 0x00000001 (dbkind \_ GUID \_ propid).
                -   Il **GUID** è null (tutti zeri), ovvero il valore si applica alla query, non solo a una singola colonna.
                -   **ulID** è impostato su 0x00000000.
            -   Per l'elemento **vValue** :
                -   **vType** è impostato su 0X0003 (VT \_ I4).
                -   **vValue** è impostato su 0x00000000 (CiNormal), ovvero una query normale.

            Per l' **elemento \[ aProps \] 2** :

            -   **PropId** è impostato su 0x00000004 ( \_ flag di \_ ambito ci DBPROP \_ ).
            -   **DBPROPOPTIONS** è impostato su 0x0000000.
            -   **DBPROPSTATUS** è impostato su 0x00000000.
            -   Per l'elemento **colid** :
                -   **eKind** è impostato su 0x00000001 (dbkind \_ GUID \_ propid).
                -   Il **GUID** è null (tutti zeri), ovvero il valore si applica alla query, non solo a una singola colonna.
                -   **ulID** è impostato su 0x00000000.
            -   Per l'elemento **vValue** :
                -   **vType**: 0X1003 (VT \_ vector \| VT \_ I4)
                -   **vValue**: 0x00000001/0x00000001 (un elemento con valore 1), che indica le sottocartelle di ricerca

            Per l' **elemento \[ aProps \] 3** :

            -   **PropId**: 0X00000003 (DBPROP \_ ci \_ include \_ ambiti)
            -   **DBPROPOPTIONS**: 0x0000000
            -   **DBPROPSTATUS**: 0x00000000
            -   Per l'elemento **colid** :
                -   **eKind** è impostato su 0x00000001 (dbkind \_ GUID \_ propid).
                -   Il **GUID** è null (tutti zeri), ovvero il valore si applica alla query, non solo a una singola colonna.
                -   **ulID** è impostato su 0x00000000
            -   Per l'elemento **vValue** :
                -   **vType** è impostato su 0X101F (VT \_ vector \| VT \_ LPWSTR).
                -   **vValue** è impostato su 0x00000001/0x00000002/" \\ " (un elemento con una stringa a terminazione null di 2 caratteri), ovvero l'ambito radice.

    -   Il campo **PropertySet2** è di tipo CDbPropSet.

        La struttura CDbPropSet che comprende il campo PropertySet1 viene popolata come indicato di seguito:

        -   **GuidPropSet** è impostato su AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ EXT).
        -   il campo **cProperties** è impostato su 0x00000001.
        -   Il campo **aProps** è una matrice di strutture CDbProp.

            Per l' **elemento \[ aProps \] 0** :

            -   **PropId** è impostato su 0x00000002 ( \_ computer DBPROP).
            -   **DBPROPOPTIONS** è impostato su 0x0000000.
            -   **DBPROPSTATUS** è impostato su 0x00000000.
            -   Per l'elemento **colid** :
                -   **eKind** è impostato su 0x00000001 (dbkind \_ GUID \_ propid),
                -   Il **GUID** è null (tutti zeri), ovvero il valore si applica alla query, non solo a una singola colonna.
                -   **ulID** è impostato su 0x00000000.
            -   Per l'elemento **vValue** :
                -   **vType**: 0x0008 (VT \_ BSTR)
                -   **vValue**: 0x04/"x" (4 byte/stringa Unicode con terminazione null), che significa "x"-nome di un server.

    -   il campo **cExtPropSet** è impostato su 0x00000000.
    -   matrice **aPropertySets** inesistente.
    -   I vari campi di riempimento vengono compilati in base alle esigenze. Il messaggio viene inviato al server.

4.  Il server verifica che il **\_ ulChecksum** sia corretto, verifica che l'utente sia autorizzato a eseguire la richiesta e risponde con un messaggio CPMConnectOut.

    L'intestazione del messaggio viene popolata come indicato di seguito:

    -   **\_ msg** è impostato su 0x000000C8, a indicare che si tratta di un messaggio CPMConnectOut.
    -   **\_ status** è impostato su 0x0000000 per indicare l'esito positivo.
    -   **\_ ulChecksum** è impostato su 0.
    -   **\_ ulReserved2** è impostato su 0x00000000.

    Il corpo del messaggio viene popolato nel modo seguente:

    -   il campo **\_ ServerVersion** è impostato su 0X00000007 (Windows XP 32 o Windows Server 2003 a 32 bit).
    -   i campi **\_ riservati** sono riempiti con dati arbitrari.

5.  Il client prepara un messaggio CPMCreateQueryIn.

    L'intestazione del messaggio viene popolata come indicato di seguito:

    -   **\_ msg** è impostato su 0x000000CA, a indicare che si tratta di un messaggio CPMCreateQueryIn.
    -   **\_ status** è impostato su 0x00000000.
    -   **\_ ulChecksum** contiene il checksum, calcolato in base a 3.2.5.
    -   **\_ ulReserved2** è impostato su 0x00000000.

    Il corpo del messaggio viene popolato nel modo seguente:

    -   Il campo **dimensioni** è impostato sulla dimensione del resto del messaggio.
    -   Il campo **CColumnSetPresent** è impostato su 0x01.
    -   Il campo **columnstore** è di tipo CColumnSet. La struttura CColumnSet che comprende questo campo è impostata nel modo seguente:
        -   il campo **\_ count** è impostato su 0x00000001 per indicare che viene restituita una colonna.
        -   la matrice **indexes** è 0x00000000 che indica la prima voce in \_ aPropSpec.
    -   Il campo **CRestrictionPresent** è impostato su 0x01, che indica che il campo di **restrizione** è presente.
    -   Il campo di **restrizione** è di tipo CRestriction ed è impostato su:
        -   **\_ ulType** è impostato su 0x00000004 (RTContent).
        -   **\_ Weight** è impostato su 0x00000000.
    -   Il resto del campo contiene una struttura CContentRestriction:
        -   La **\_ Proprietà** è impostata su GUID B725F130-47ef-101A-A5F1-02608c9eebac/0x00000001 (per PRSPEC \_ propid)/0x13 che rappresenta il corpo del documento.
        -   **\_ CC** è impostata su 0x00000009.
        -   **\_ pwcsphrase** è impostato sulla stringa "Microsoft".
        -   **\_ LCID** è impostato su 0x409 (per l'inglese).
        -   **\_ ulGenerateMethod** è impostato su 0x00000000 (corrispondenza esatta).
    -   **CSortPresent** è impostato su 0x00.
    -   **CCategorizationSetPresent** è impostato su 0x00.
    -   **RowSetProperties** viene impostato nel modo seguente:
        -   **\_ uBooleanOptions** è impostato su 0x00000001 (sequenziale).
        -   **\_ ulMaxOpenRows** è impostato su 0x00000000.
        -   **\_ ulMemoryUsage** è impostato su 0x00000000.
        -   \_**cMaxResults** è impostato su 0x00000100 (restituisce al massimo 256 righe).
        -   **\_ cCmdTimeOut** è impostato su 0x00000000 (Never timeout).
    -   **PidMapper** è impostato su:
        -   **\_ count** è impostata su 0x00000001.
        -   **\_ aPropSpec** è impostato su GUID B725F130-47ef-101A-a5-F1-02608C9EEBAC/0x00000001 (per PRSPEC \_ propid)/0x0000000c che rappresenta la proprietà dimensioni file di Windows.

6.  Il server lo elabora e risponde con un messaggio CPMCreateQueryOut.

    L'intestazione del messaggio viene popolata come indicato di seguito:

    -   **\_ msg** è impostato su 0x000000CA, a indicare che si tratta di un messaggio CPMCreateQueryOut.
    -   **\_ lo stato** è impostato su esito positivo.
    -   **\_ ulChecksum** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).
    -   **\_ ulReserved2** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).

    Il corpo del messaggio viene popolato nel modo seguente:

    -   **\_ fTrueSeqeuntial** è impostato su 0x00000000, a indicare che la query può utilizzare un indice.
    -   **\_ fWorkIdUnique** è impostato su 0x00000001.
    -   La matrice **aCursors** contiene un solo elemento, che rappresenta un handle del cursore per questa query. Il valore dipende dallo stato del server. Si supponga che il valore restituito sia 0xAAAAAAAA.

7.  Il client invia un messaggio di richiesta CPMSetBindingsIn per definire il formato di una riga.

    L'intestazione del messaggio viene popolata come indicato di seguito:

    -   **\_ msg** è impostato su 0x000000D0, a indicare che si tratta di un messaggio CPMSetBindingsIn.
    -   **\_ lo stato** è impostato su esito positivo.
    -   **\_ ulChecksum** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).
    -   **\_ ulReserved2** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).

    Il corpo del messaggio viene popolato nel modo seguente:

    -   **\_ hCursor** è impostato su 0xAAAAAAAA.
    -   **\_ cbRow** è impostato su 0x10 (abbastanza grande da contenere le colonne).
    -   **\_ cbBindingDesc** è impostato sulle dimensioni dei campi **\_ CColumns** e **\_ aColumns** combinati.
    -   **\_ CColumns** è impostato su 0x00000001.
    -   la matrice **\_ aColumns** è impostata in modo da contenere una struttura CTableColumn contenente:
    -   -   **\_ Campo PROPSPEC** è impostato su GUID b725f130-47ef-101A-a5-F1-02608c9eebac/0x00000001 (per PRSPEC \_ propid)/0x0000000c che rappresenta la proprietà dimensioni file di Windows.
        -   **\_ vType** è impostato su 0x0015 (VT \_ UI8).
        -   **\_ ValueUsed** è impostato su 0x01 (colonna trasferita nella riga).
        -   **\_ ValueOffset** è impostato su 0x0002 (all'inizio della riga).
        -   **\_ ValueSize** è impostato su 0x08 (size of a VT \_ UI8).
        -   **\_ StatusUsed** è impostato su 0x01.
        -   **\_ StatusOffset** è impostato su 0x0A.
        -   **\_ LengthUsed** è impostato su 0x00.

8.  Il server lo elabora e risponde con un messaggio CPMSetBindingsIn.

    L'intestazione del messaggio viene popolata come indicato di seguito:

    -   **\_ msg** è impostato su 0x000000D0.
    -   **\_ lo stato** è impostato su esito positivo.
    -   **\_ ulChecksum** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).
    -   **\_ ulReserved2** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).

9.  Il client invia un messaggio di richiesta CPMGetRowsIn. Si supponga che il client sia pronto ad accettare 100 righe in questo momento e le desideri in ordine crescente.

    L'intestazione del messaggio viene popolata come indicato di seguito:

    -   **\_ msg** è impostato su 0x000000CC, a indicare che si tratta di un messaggio CPMGetRowsIn.
    -   **\_ lo stato** è impostato su 0x00000000
    -   **\_ ulChecksum** contiene il checksum calcolato in base alla sezione 0.
    -   **\_ ulReserved2** è impostato su 0x00000000.

    Il corpo del messaggio viene popolato nel modo seguente:

    -   **\_ hCursor** è impostato su 0xAAAAAAAA.
    -   **\_ cRowsToTransfer** è impostato su 0x00000064.
    -   **\_ cRowWidth** è impostato su 0x00000010 (dalle associazioni).
    -   **\_ cbSeek** è impostato su 0x14, ovvero le dimensioni dei campi etype, \_ Chapt e CRowSeekNext combinati.
    -   **\_ cbReserved** è impostato su 0x18 (0x14 più \_ cbSeek).
    -   **\_ cbReadBuffer** è impostato su 0x800 (0x64 \* 0x10 arrotondato al multiplo successivo di 0x200).
    -   **\_ ulClientBase** è impostato su 0x00000000.
    -   **\_ fBwdfetch** è impostato su 0x00000000 per indicare che le righe devono essere recuperate in ordine di avanzamento.
    -   **etype** è impostato su 0x0000001 che indica che il client desidera le righe successive.
    -   **\_ Chapt** è impostato su 0 (non è un risultato con capitoli).
    -   **SeekDescription** è impostato su CRowSeekNext. La struttura CRowSeekNext contiene i valori seguenti:
        -   **CiTblChapt** è impostato su 0x00000000.
        -   **\_ hRegion** è impostato su 0x00000000.
        -   **\_ cSkip** è impostato su 0 per indicare che il client non desidera ignorare le righe.

10. Il server lo elabora e risponde con un messaggio CPMGetRowsOut. Si supponga che nel server siano stati trovati 100 documenti contenenti la parola "Microsoft".

    L'intestazione del messaggio viene popolata come indicato di seguito:

    -   **\_ msg** è impostato su 0x000000CC, a indicare che si tratta di un messaggio CPMGetRowsOut.
    -   **\_ lo stato** è impostato su esito positivo.
    -   **\_ ulChecksum** è impostato su 0x00000000.
    -   **\_ ulReserved2** è impostato su 0x00000000.

    Il corpo del messaggio viene popolato nel modo seguente:

    -   **\_ CRowsReturned** è impostato su 0x00000064.
    -   **etype** è impostato su 0x00000001.
    -   **\_ Chapt** è impostato su 0x00000000 (non è un risultato con capitoli).
    -   **SeekDescription** contiene una struttura CRowSeekNext, popolata come indicato di seguito:
        -   **CiTblChapt** è impostato su 0x00000000.
        -   **\_ hRegion** è impostato su 0x00000000.
        -   **\_ cSkip** è impostato su 0 per indicare che il client non desidera ignorare le righe.
    -   **Rows** contiene la dimensione dei documenti 100 che contengono la parola "Microsoft". Poiché si tratta di dati a dimensione fissa, viene semplicemente strutturato come un elenco di interi senza segno a 100, a 8 byte.

11. Il client invia un messaggio CPMDisconnect per terminare la connessione.

    L'intestazione del messaggio viene popolata come indicato di seguito:

    -   **\_ msg** è impostato su 0x000000C9, a indicare che si tratta di un messaggio CPMDisconnect.
    -   **\_ status** è impostato su 0x00000000.
    -   **\_ ulChecksum** è impostato su 0x00000000.

12. Il server elabora il messaggio e rimuove tutto lo stato del client.

### <a name="42-example-2"></a>4,2 esempio 2

Nell'esempio precedente la query era piuttosto semplice. Si prenda ora in considerazione una query leggermente più complessa. Si supponga che l'utente desideri recuperare le dimensioni dei documenti che contengono entrambe le parole seguenti: "Microsoft" e "Office". Questa impostazione viene specificata modificando il campo di restrizione contenuto nel messaggio CPMCreateQueryIn inviato nel passaggio 5, come indicato di seguito:

Il campo di **restrizione** è di tipo CRestriction ed è impostato su:

-   -   **\_ ulType** è impostato su 0x00000004 (RTAnd).
    -   **\_ Weight** è impostato su 0x00000000.

Il resto del campo contiene una struttura CNodeRestriction:

-   -   **\_ CNode** è impostato su 0x00000002, a indicare che nella matrice paNode sono presenti due nodi.
    -   Il campo **\_ paNode** è una matrice di due strutture CRestriction.

        **\_ paNode \[ 0 \]** contiene:

        -   -   **\_ ulType** è impostato su 0x00000004 (RTContent).
            -   **\_ Weight** è impostato su 0x00000000.
            -   Il resto del campo contiene una struttura CContentRestriction:
                -   La **\_ Proprietà** è impostata su GUID b725f130-47ef-101A-A5F1-02608c9eebac/0x00000001 (per PRSPEC \_ propid)/0x13.
                -   **\_ CC** è impostata su 0x00000009.
                -   **\_ pwcsphrase** è impostato sulla stringa "Microsoft".
                -   **\_ LCID** è impostato su 0x409 (per l'inglese).
                -   **\_ ulGenerateMethod** è impostato su 0x00000000 (corrispondenza esatta).

        **\_ paNode \[ 1 \]** contiene:

        -   -   **\_ ulType** è impostato su 0x00000004 (RTContent).
            -   **\_ Weight** è impostato su 0x00000000.
            -   Il resto del campo contiene una struttura CContentRestriction:
                -   La **\_ Proprietà** è impostata su GUID b725f130-47ef-101A-A5F1-02608c9eebac/0x00000001 (per PRSPEC \_ propid)/0x13.
                -   **\_ CC** è impostata su 0x00000006.
                -   **\_ pwcsphrase** è impostato sulla stringa "Office".
                -   **\_ LCID** è impostato su 0x409 (per l'inglese).
                -   **\_ ulGenerateMethod** è impostato su 0x00000000 (corrispondenza esatta).

## <a name="5-security"></a>5 Sicurezza

### <a name="51-security-considerations-for-implementers"></a>5.1 Considerazioni sulla sicurezza per i responsabili dell'implementazione

Le implementazioni di indicizzazione che indicizzano il contenuto protetto devono considerare l'utilizzo del contesto utente fornito da SMB \[ MS-SMB \] per tagliare i risultati della ricerca e restituire solo quelli accessibili al chiamante.

### <a name="52-index-of-security-parameters"></a>5.2 Indice dei parametri di sicurezza



| Parametro di sicurezza  | Sezione |
|---------------------|---------|
| Livello di rappresentazione | 2.1     |



 

## <a name="6-index-of-version-specific-behavior"></a>6 Indice del comportamento specifico della versione



| Comportamento specifico della versione                                                                         | Sezione   | Windows 2000 | Windows XP | Windows Server 2003 |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| Questo protocollo viene implementato in Windows 2000, Windows XP, Windows Server 2003 e Windows Vista. | 1.3.2     | X            | X          | X                   |
| Le applicazioni in genere interagiscono con un wrapper di interfaccia OLE DB                                  | 1.4       | X            | X          | X                   |
| Valori NTSTATUS                                                                                   | 1.8       | X            | X          | X                   |
| Il client imposta il \_ campo stato in ogni intestazione del messaggio.                                        | 2.2.2     | X            | X          | X                   |
| il valore cPendingScans è in genere zero                                                               | 2.2.3.1   | X            | X          | X                   |
| valore iClientVersion                                                                              | 2.2.3.6   | X            | X          | X                   |
| \_valore cbChunk                                                                                   | 2.2.3.19  | X            | X          | X                   |
| indirizzi di memoria a 32 bit e a 64 bit                                                                | 3.2.4.2.4 | X            | X          | X                   |



 

 

 





