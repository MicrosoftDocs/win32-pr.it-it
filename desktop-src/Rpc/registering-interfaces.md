---
title: Registrazione di interfacce
description: Registrazione di un'interfaccia RPC (Remote Procedure Call).
ms.assetid: c22e3fa8-98be-461a-b06d-292d3f655ffc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ea9e851e8c9663c8f66d983d3400b1ee398a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220906"
---
# <a name="registering-interfaces"></a>Registrazione di interfacce

In questa sezione viene presentata una descrizione dettagliata del processo di registrazione di un'interfaccia RPC.

Le informazioni contenute in questa sezione sono illustrate negli argomenti seguenti:

-   [Funzioni di registrazione dell'interfaccia](#interface-registration-functions)
-   [Vettori di punti di ingresso](#entry-point-vectors)
-   [EPV Manager](#manager-epvs)
-   [Registrazione di una singola implementazione di un'interfaccia](#registering-a-single-implementation-of-an-interface)
-   [Registrazione di più implementazioni di un'interfaccia](#registering-multiple-implementations-of-an-interface)
-   [Regole per la chiamata delle routine di gestione](#rules-for-invoking-manager-routines)
-   [Invio di una chiamata di procedura remota a una routine Server-Manager](#dispatching-a-remote-procedure-call-to-a-server-manager-routine)
-   [Fornire una funzione di Object-Inquiry personalizzata](#supplying-your-own-object-inquiry-function)

## <a name="interface-registration-functions"></a>Funzioni di registrazione dell'interfaccia

I server registrano le interfacce chiamando la funzione [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) . I programmi server complessi supportano spesso più di un'interfaccia. Le applicazioni server devono chiamare questa funzione una volta per ogni interfaccia supportata.

Inoltre, i server possono supportare più versioni della stessa interfaccia, ognuna con la propria implementazione delle funzioni dell'interfaccia. Se il programma server esegue questa operazione, deve fornire un set di punti di ingresso. Un punto di ingresso è una routine di gestione che invia le chiamate per una versione di un'interfaccia. Deve essere presente un punto di ingresso per ogni versione dell'interfaccia. Il gruppo di punti di ingresso è denominato vettore del punto di ingresso. Per informazioni dettagliate, vedere [vettori di punti di ingresso](#entry-point-vectors).

Oltre alla funzione standard [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), RPC supporta anche altre funzioni di registrazione dell'interfaccia. La funzione [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) estende le funzionalità di **RpcServerRegisterIf** consentendo di specificare un set di flag di registrazione (vedere [flag di registrazione delle interfacce](interface-registration-flags.md)), il numero massimo di richieste simultanee di chiamate di procedura remota che il server può accettare e le dimensioni massime in byte dei blocchi di dati in arrivo.

La libreria RPC contiene anche una funzione denominata [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex). Analogamente alla funzione [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) , questa funzione registra un'interfaccia. Il programma server può usare questa funzione anche per specificare un set di flag di registrazione (vedere [flag di registrazione delle interfacce](interface-registration-flags.md)), il numero massimo di richieste di chiamata di procedura remota simultanee che il server può accettare e una funzione di callback di sicurezza.

Le funzioni [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)e [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) impostano i valori nella tabella del registro di sistema dell'interfaccia interna. Questa tabella viene usata per eseguire il mapping dell'UUID dell'interfaccia e degli UUID degli oggetti a un EPV di gestione. Il EPV di gestione è una matrice di puntatori a funzione che contiene esattamente un puntatore a funzione per ogni prototipo di funzione nell'interfaccia specificata nel file IDL.

Per informazioni su come fornire più EPV per fornire più implementazioni dell'interfaccia, vedere [implementazioni di più interfacce](#registering-multiple-implementations-of-an-interface).

La libreria di runtime usa la tabella del registro di sistema Interface (impostata dalle chiamate alla funzione [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)) e la tabella del registro di sistema Object (impostata dalle chiamate alla funzione [**RPCOBJECTSETTYPE**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)) per eseguire il mapping degli UUID dell'interfaccia e dell'oggetto al puntatore a funzione.

Quando si desidera che il programma server rimuova un'interfaccia dal registro di sistema della libreria di runtime RPC, chiamare la funzione [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) . Una volta rimossa l'interfaccia dal registro di sistema, la libreria di runtime RPC non accetterà più nuove chiamate per tale interfaccia.

## <a name="entry-point-vectors"></a>Vettori di punti di ingresso

Il vettore del punto di ingresso di gestione (EPV) è una matrice di puntatori a funzione che puntano alle implementazioni delle funzioni specificate nel file IDL. Il numero di elementi nella matrice corrisponde al numero di funzioni specificate nel file IDL. RPC supporta più vettori di punti di ingresso che rappresentano più implementazioni delle funzioni specificate nell'interfaccia.

Il compilatore MIDL genera automaticamente un tipo di dati Manager EPV da usare per la costruzione di EPV Manager. Il tipo di dati è denominato * if-name ***\_ server \_ EPV**, dove *if-name* specifica l'identificatore di interfaccia nel file IDL.

Il compilatore MIDL crea e inizializza automaticamente un manager predefinito EPV sul presupposto che esista una routine di gestione con lo stesso nome per ogni procedura nell'interfaccia e che sia specificata nel file IDL.

Quando un server offre più implementazioni della stessa interfaccia, il server deve creare un EPV di gestione aggiuntivo per ogni implementazione. Ogni EPV deve contenere esattamente un punto di ingresso (indirizzo di una funzione) per ogni procedura definita nel file IDL. L'applicazione server dichiara e Inizializza una variabile EPV di gestione di tipo *if-name * * * \_ server \_ EPV** per ogni implementazione aggiuntiva dell'interfaccia. Per registrare il EPV, chiama [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) una volta per ogni tipo di oggetto supportato.

Quando il client effettua una chiamata di procedura remota al server, il EPV contenente il puntatore a funzione viene selezionato in base all'UUID dell'interfaccia e al tipo di oggetto. Il tipo di oggetto deriva dall'UUID dell'oggetto da parte della funzione di richiesta di oggetti o dal mapping basato su tabella controllato da [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype).

## <a name="manager-epvs"></a>EPV Manager

Per impostazione predefinita, il compilatore MIDL usa i nomi di stored procedure del file IDL di un'interfaccia per generare un EPV di gestione, che il compilatore inserisce direttamente nello stub del server. Questo EPV predefinito viene inizializzato in modo statico utilizzando i nomi delle procedure dichiarati nella definizione dell'interfaccia.

Per registrare un gestore usando il EPV predefinito, specificare **null** come valore del parametro *MgrEpv* in una chiamata alla funzione [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) . Se i nomi di routine usati da un responsabile corrispondono a quelli della definizione dell'interfaccia, è possibile registrare questo gestore usando il valore predefinito di EPV dell'interfaccia generata dal compilatore MIDL. È anche possibile registrare un responsabile usando una EPV fornita dall'applicazione server.

Un server può (e talvolta necessario) creare e registrare un EPV di gestione non **null** per un'interfaccia. Per selezionare un'applicazione server fornita da EPV, passare l'indirizzo di un EPV il cui valore è stato dichiarato dal server come valore di *MgrEpv* a parametro. Un valore non **null** per *MgrEpv* un parametro sostituisce sempre un EPV predefinito nello stub del server.

Il compilatore MIDL genera automaticamente un tipo di dati Manager EPV (RPC \_ Mgr \_ EPV) per un'applicazione server da usare per la costruzione di EPV di gestione. Un EPV di gestione deve contenere esattamente un punto di ingresso (indirizzo della funzione) per ogni procedura definita nel file IDL.

Un server deve fornire un EPV non **null** nei casi seguenti:

-   Quando i nomi delle routine di gestione sono diversi da quelli dichiarati nella definizione di interfaccia
-   Quando il server utilizza il EPV predefinito per la registrazione di un'altra implementazione dell'interfaccia

Un server dichiara un EPV di gestione inizializzando una variabile di tipo *if-name * * * \_ server \_ EPV** per ogni implementazione dell'interfaccia.

## <a name="registering-a-single-implementation-of-an-interface"></a>Registrazione di una singola implementazione di un'interfaccia

Quando un server offre solo un'implementazione di un'interfaccia, il server chiama [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) una sola volta. Nel caso standard, il server utilizza il EPV di gestione predefinito. L'eccezione si verifica quando il gestore utilizza nomi di routine diversi da quelli dichiarati nell'interfaccia.

Per il caso standard, è necessario specificare i valori seguenti per le chiamate a [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2):

-   EPV Manager

    Per usare il valore predefinito di EPV, specificare un valore **null** per il parametro *MgrEpv* .

-   UUID di tipo Manager

    Quando si usa il EPV predefinito, registrare l'interfaccia con un UUID del tipo di gestione Nil specificando un valore **null** o un UUID nil per il *MgrTypeUuid* un parametro. In questo caso, tutte le chiamate a procedure remote, indipendentemente dall'UUID dell'oggetto nel rispettivo handle di associazione, vengono inviate al EPV predefinito, presupponendo che non siano state effettuate chiamate [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) .

    È anche possibile specificare un UUID di tipo Manager non Nil. In questo caso, è necessario chiamare anche la routine [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) .

## <a name="registering-multiple-implementations-of-an-interface"></a>Registrazione di più implementazioni di un'interfaccia

È possibile specificare più di un'implementazione delle procedure remote specificate nel file IDL. L'applicazione server chiama [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) per eseguire il mapping degli UUID degli oggetti al tipo UUID e chiama [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) per associare il gestore EPV a un UUID di tipo. Quando arriva una chiamata di procedura remota con il relativo UUID dell'oggetto, la libreria di runtime del server RPC esegue il mapping dell'UUID dell'oggetto a un tipo UUID. L'applicazione server usa quindi il tipo UUID e l'UUID dell'interfaccia per selezionare il gestore EPV.

È anche possibile specificare una funzione personalizzata per risolvere il mapping dall'UUID dell'oggetto al tipo di gestione UUID. La funzione di mapping viene specificata quando si chiama [**RpcObjectSetInqFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsetinqfn).

Per offrire più implementazioni di un'interfaccia, un server deve registrare ogni implementazione chiamando [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) separatamente. Per ogni implementazione registrata da un server, fornisce lo stesso *IfSpec* a un parametro, ma una coppia diversa di *MgrTypeUuid* e *MgrEpv* di parametri.

Nel caso di più responsabili, usare [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) come indicato di seguito:

-   EPV Manager

    Per offrire più implementazioni di un'interfaccia, un server deve:

    -   Creare un EPV di gestione non **null** per ogni implementazione aggiuntiva.
    -   Specificare un valore non **null** per *MgrEpv* un parametro in [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2).

    Si noti che il server può anche eseguire la registrazione con il EPV di gestione predefinito.

-   UUID di tipo Manager

    Fornire un UUID di tipo Manager per ogni EPV dell'interfaccia. UUID di tipo Nil (o valore **null** ) per *MgrTypeUuid* è possibile specificare un parametro per uno dei EPV di gestione. Ogni UUID di tipo deve essere diverso.

## <a name="rules-for-invoking-manager-routines"></a>Regole per la chiamata delle routine di gestione

La libreria di runtime RPC invia una chiamata di procedura remota in ingresso a un responsabile che offre l'interfaccia RPC richiesta. Quando più responsabili sono registrati per un'interfaccia, la libreria di runtime RPC deve selezionarne una. Per selezionare un Manager, la libreria di runtime RPC usa l'UUID dell'oggetto specificato dall'handle di associazione della chiamata.

La libreria di runtime applica le seguenti regole durante l'interpretazione dell'UUID dell'oggetto di una chiamata di procedura remota:

-   UUID oggetto Nil

    All'UUID di un oggetto nil viene assegnato automaticamente l'UUID di tipo nil. non è consentito specificare un UUID di oggetto nil nella routine [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) . Una chiamata di procedura remota il cui handle di associazione contiene un UUID di oggetto nil viene pertanto inviata automaticamente al gestore registrato con l'UUID di tipo Nil, se presente.

-   UUID di oggetti non nIl

    In linea di principio, una chiamata di procedura remota il cui handle di associazione contiene un UUID di oggetto diverso da Nil deve essere elaborata da un gestore il cui tipo UUID corrisponde al tipo di UUID dell'oggetto. Tuttavia, per identificare il gestore corretto, è necessario che il server abbia specificato il tipo di UUID dell'oggetto chiamando la routine [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) .

    Se un server non è in grado di chiamare la routine [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) per un UUID di oggetto diverso da Nil, una chiamata di procedura remota per tale UUID viene indirizzata al EPV Manager che esegue chiamate a procedure remote con un UUID dell'oggetto Nil, ovvero l'UUID di tipo nil.

    Non è possibile eseguire chiamate di procedure remote con un UUID di oggetto non nIl nell'handle di binding se il server ha assegnato all'UUID un oggetto diverso da un UUID di tipo chiamando la routine [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) , ma non ha anche registrato un EPV di gestione per quel tipo UUID chiamando [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2).

Nella tabella seguente sono riepilogate le azioni che la libreria di runtime utilizza per selezionare la routine del Manager.



| UUID oggetto della chiamata | Tipo di set di server per UUID oggetto? | Tipo di EPV registrato dal server | Azione di invio                                                                                                                                 |
|---------------------|----------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Nil                 | Non applicabile                   | Sì                         | Usa il Manager con l'UUID di tipo nil.                                                                                                           |
| Nil                 | Non applicabile                   | No                          | Errore ( \_ \_ \_ tipo non supportato RPC); rifiuta la chiamata di procedura remota.                                                                              |
| Non nIl             | Sì                              | Sì                         | Usa il gestore con lo stesso UUID di tipo.                                                                                                          |
| Non nIl             | No                               | Ignorato                     | Usa il Manager con l'UUID di tipo nil. Se nessun responsabile con UUID di tipo Nil, Error (RPC \_ S \_ UNSUPPORTEDTYPE); rifiuta la chiamata di procedura remota. |
| Non nIl             | Sì                              | No                          | Error (RPC \_ S \_ UNSUPPORTEDTYPE); rifiuta la chiamata di procedura remota.                                                                                |



 

L'UUID dell'oggetto della chiamata è l'UUID dell'oggetto trovato in un handle di binding per una chiamata di procedura remota.

Il server imposta il tipo di UUID dell'oggetto chiamando [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) per specificare il tipo UUID per un oggetto.

Il server registra il tipo per il EPV di gestione chiamando [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) usando lo stesso UUID di tipo.

> [!Note]  
> All'UUID dell'oggetto nil viene sempre assegnato automaticamente l'UUID di tipo nil. Non è consentito specificare un UUID dell'oggetto nil nella routine [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) .

 

## <a name="dispatching-a-remote-procedure-call-to-a-server-manager-routine"></a>Invio di una chiamata di procedura remota a una routine di gestione server

Nelle tabelle seguenti vengono illustrati i passaggi necessari per la libreria di runtime RPC per inviare una chiamata di procedura remota a una routine di gestione server.

Un caso semplice in cui il server registra il EPV di gestione predefinito, è descritto nelle tabelle seguenti.

**Tabella del registro di sistema Interface**



| UUID interfaccia | UUID di tipo Manager | Vettore punto di ingresso |
|----------------|-------------------|--------------------|
| *uuid1*        | Nil               | EPV predefinito        |



 

**Tabella del registro oggetti**



| UUID oggetto             | Tipo di oggetto |
|-------------------------|-------------|
| Nil                     | Nil         |
| (Qualsiasi altro UUID di oggetto) | Nil         |



 

**Mapping dell'handle di associazione a un vettore del punto di ingresso (EPV)**



| UUID interfaccia (dall'handle di associazione client) | UUID oggetto (dall'handle di associazione client) | Tipo di oggetto (tabella del registro di sistema degli oggetti) | Manager EPV (dalla tabella del registro di sistema Interface) |
|---------------------------------------------|------------------------------------------|------------------------------------------|---------------------------------------------|
| *uuid1*                                     | Nil                                      | Nil                                      | EPV predefinito                                 |
| Vedere sopra.                               | *UUID*                                  | Nil                                      | EPV predefinito                                 |



 

Nei passaggi seguenti vengono descritte le azioni accettate dalla libreria di runtime del server RPC, come illustrato nelle tabelle precedenti, quando un client con interfaccia UUID *uuid1* lo chiama.

1.  Il server chiama [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) per associare un'interfaccia offerta con l'UUID del tipo di gestione nil e con il EPV di gestione predefinito generato da MIDL. Questa chiamata aggiunge una voce nella tabella del registro di sistema Interface. L'UUID dell'interfaccia è contenuto nel parametro *IfSpec* .
2.  Per impostazione predefinita, la tabella del registro di sistema dell'oggetto associa tutti gli UUID degli oggetti con UUID di tipo nil. In questo esempio, il server non chiama [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype).
3.  La libreria di runtime del server riceve un codice di procedura remota contenente l'UUID dell'interfaccia a cui appartiene la chiamata e l'UUID dell'oggetto dall'handle di associazione della chiamata.

    Per informazioni sulle modalità di impostazione dell'UUID di un oggetto in un handle di binding, vedere le seguenti voci di riferimento per le funzioni:

    -   [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
    -   [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
    -   [**Errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
    -   [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

4.  Utilizzando l'UUID dell'interfaccia dalla chiamata RPC, la libreria di runtime del server individua tale UUID dell'interfaccia nella tabella del registro di sistema Interface.

    Se il server non ha registrato l'interfaccia usando [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2), la chiamata di procedura remota viene restituita al chiamante con un \_ codice di \_ stato sconosciuto di RPC \_ se.

5.  Utilizzando l'UUID dell'oggetto dall'handle di binding, la libreria di runtime del server individua l'UUID dell'oggetto nella tabella del registro di sistema dell'oggetto. In questo esempio, tutti gli UUID degli oggetti vengono mappati al tipo di oggetto Nil.
6.  La libreria di runtime del server individua il tipo di gestione nil nella tabella del registro di sistema dell'interfaccia.
7.  La combinazione dell'UUID dell'interfaccia e del tipo nil nella tabella del registro di sistema viene risolta nel EPV predefinito, che contiene le routine di gestione server da eseguire per l'UUID dell'interfaccia presente nella chiamata di procedura remota.

Si supponga che il server offra più interfacce e più implementazioni di ogni interfaccia, come descritto nelle tabelle seguenti.

**Tabella del registro di sistema Interface**



| UUID interfaccia | UUID di tipo Manager | Vettore punto di ingresso |
|----------------|-------------------|--------------------|
| *uuid1*        | Nil               | *epv1*             |
| *uuid1*        | *uuid3*           | *epv4*             |
| *uuid2*        | *uuid4*           | *epv2*             |
| *uuid2*        | *uuid7*           | *epv3*             |



 

**Tabella del registro oggetti**



| UUID oggetto      | Tipo di oggetto |
|------------------|-------------|
| *UUID*          | *uuid3*     |
| *uuidB*          | *uuid7*     |
| *uuidC*          | *uuid7*     |
| *UUID*          | *uuid3*     |
| *UUID*          | *uuid3*     |
| *uuidF*          | *uuid8*     |
| Nil              | Nil         |
| (Qualsiasi altro UUID) | Nil         |



 

**Mapping dell'handle di associazione a un vettore del punto di ingresso**



| UUID interfaccia (dall'handle di associazione client) | UUID oggetto (dall'handle di associazione client) | Tipo di oggetto (tabella del registro di sistema degli oggetti) | Manager EPV (dalla tabella del registro di sistema Interface) |
|---------------------------------------------|------------------------------------------|------------------------------------------|---------------------------------------------|
| *uuid1*                                     | Nil                                      | Nil                                      | *epv1*                                      |
| *uuid1*                                     | *UUID*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid1*                                     | *UUID*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid1*                                     | *UUID*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid2*                                     | *uuidB*                                  | *uuid7*                                  | *epv3*                                      |
| *uuid2*                                     | *uuidC*                                  | *uuid7*                                  | *epv3*                                      |



 

I passaggi seguenti descrivono le azioni eseguite dalla libreria di runtime del server, come illustrato nelle tabelle precedenti, quando un client con interfaccia UUID *UUID2* e l'UUID dell'oggetto *uuidC* lo chiama.

1.  Il server chiama [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) per associare le interfacce offerte con i diversi EPV di gestione. Le voci nella tabella del registro di sistema Interface riflettono quattro chiamate di [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) per offrire due interfacce, con due implementazioni (EPV) per ogni interfaccia.
2.  Il server chiama [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) per stabilire il tipo di ogni oggetto che offre. Oltre all'associazione predefinita dell'oggetto Nil a un tipo Nil, tutti gli altri UUID degli oggetti non trovati in modo esplicito nella tabella del registro di sistema dell'oggetto vengono mappati anche all'UUID di tipo nil.

    In questo esempio, il server chiama la routine [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) sei volte.

3.  La libreria di runtime del server riceve una chiamata di procedura remota contenente l'UUID dell'interfaccia a cui appartiene la chiamata e un UUID dell'oggetto dall'handle di associazione della chiamata.
4.  Utilizzando l'UUID dell'interfaccia dalla chiamata RPC, la libreria di runtime del server individua l'UUID dell'interfaccia nella tabella del registro di sistema Interface.
5.  Utilizzando l'UUID dell'oggetto *uuidC* dall'handle di binding, la libreria di runtime del server individua l'UUID dell'oggetto nella tabella del registro di sistema dell'oggetto e rileva che esegue il mapping al tipo *uuid7*.
6.  Per individuare il tipo di gestore, la libreria di runtime del server combina l'UUID dell'interfaccia, *UUID2* e il tipo *uuid7* nella tabella del registro di sistema Interface. Questa operazione viene risolta in *epv3*, che contiene la routine di Server Manager da eseguire per la chiamata RPC.

Le routine in *epv2* non verranno mai eseguite perché il server non ha chiamato la routine [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) per aggiungere tutti gli oggetti con un tipo UUID di *uuid4* alla tabella del registro di sistema dell'oggetto.

Una chiamata di procedura remota con interfaccia UUID *UUID2* e l'UUID dell'oggetto *uuidF* restituisce al chiamante un \_ codice di stato del tipo di \_ gestione sconosciuto RPC \_ \_ perché il server non ha chiamato [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) per registrare l'interfaccia con un tipo di Manager *uuid8*.

## <a name="return-values"></a>Valori restituiti

Questa funzione restituisce uno dei valori seguenti.



| Valore                             | Significato                      |
|-----------------------------------|------------------------------|
| RPC \_ S \_ OK                        | Operazione riuscita                      |
| il \_ tipo RPC è \_ \_ già \_ registrato | UUID di tipo già registrato |



 

## <a name="supplying-your-own-object-inquiry-function"></a>Fornire una funzione di richiesta di oggetti personalizzata

Si consideri un server che gestisce migliaia di oggetti di molti tipi diversi. Ogni volta che il server è stato avviato, l'applicazione server deve chiamare la funzione [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) per ognuno degli oggetti, anche se i client possono fare riferimento solo ad alcuni di essi (o richiedere molto tempo per farvi riferimento). È probabile che queste migliaia di oggetti si trovino sul disco, pertanto il recupero dei tipi potrebbe richiedere molto tempo. Inoltre, la tabella interna che sta eseguendo il mapping dell'UUID dell'oggetto all'UUID di tipo Manager dovrebbe essenzialmente duplicare il mapping gestito con gli oggetti stessi.

Per praticità, il set di funzioni RPC include la funzione [**RpcObjectSetInqFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsetinqfn). Con questa funzione è possibile fornire la propria funzione di richiesta oggetti.

Ad esempio, è possibile fornire la propria funzione di richiesta oggetti quando si esegue il mapping di oggetti da 100 a 199 al tipo numero 1, 200 – 299 al tipo numero 2 e così via. La funzione di richiesta di oggetti può essere estesa anche a una file system distribuita, in cui l'applicazione server non dispone di un elenco di tutti i file (UUID degli oggetti) disponibili o quando l'UUID dell'oggetto esegue il nome dei file nel file system e non si desidera precaricare tutti i mapping tra gli UUID degli oggetti e gli UUID di tipo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
</dt> <dt>

[**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)
</dt> <dt>

[**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)
</dt> <dt>

[**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
</dt> <dt>

[**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
</dt> <dt>

[**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 




