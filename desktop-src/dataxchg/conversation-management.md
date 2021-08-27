---
title: Gestione delle conversazioni
description: Questo argomento illustra le conversazioni tra un client e un server.
ms.assetid: 4e5ff1a1-d46a-4e2a-a37c-8df951f2a1ee
keywords:
- Windows Interfaccia utente,Dynamic Data Exchange (DDE)
- Dynamic Data Exchange (DDE), conversazioni
- DDE (Dynamic Data Exchange), conversazioni
- scambio di dati,Dynamic Data Exchange (DDE)
- Windows Interfaccia utente,Dynamic Data Exchange Management Library (DDEML)
- Dynamic Data Exchange Management Library (DDEML), conversations
- DDEML (Dynamic Data Exchange Management Library), conversazioni
- scambio di dati, Dynamic Data Exchange Management Library (DDEML)
- Dynamic Data Exchange (DDE), più conversazioni
- DDE (Dynamic Data Exchange),più conversazioni
- Dynamic Data Exchange Management Library (DDEML), più conversazioni
- DDEML (Dynamic Data Exchange Management Library), più conversazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3531cc396a3b4d0eca5d7c11e3677aec9ea2ee35dcdac110455daee252f798
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991331"
---
# <a name="conversation-management"></a>Gestione delle conversazioni

Una conversazione tra un client e un server viene sempre stabilita su richiesta del client. Quando viene stabilita una conversazione, ogni partner riceve un handle che identifica la conversazione. I partner usano questo handle in altre Dynamic Data Exchange Management Library (DDEML) per inviare transazioni e gestire la conversazione. Un client può richiedere una conversazione con un singolo server oppure può richiedere più conversazioni con uno o più server.

Negli argomenti seguenti viene descritto come un'applicazione stabilisce nuove conversazioni e ottiene informazioni sulle conversazioni esistenti.

-   [Conversazioni singole](#single-conversations)
-   [Più conversazioni](#multiple-conversations)

## <a name="single-conversations"></a>Conversazioni singole

Un'applicazione client richiede una singola conversazione con un server chiamando la funzione [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) e specificando handle di stringa che identificano le stringhe contenenti il nome del servizio dell'applicazione server e il nome dell'argomento per la conversazione. DDEML risponde inviando la transazione [**XTYP \_ CONNECT**](xtyp-connect.md) alla funzione di callback Dynamic Data Exchange (DDE) di ogni applicazione server che ha registrato un nome di servizio corrispondente a quello specificato in **DdeConnect** o ha disattivato il filtro dei nomi del servizio chiamando [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice). Un server può anche filtrare le transazioni **XTYP \_ CONNECT** specificando il flag di filtro CBF \_ FAIL CONNECTIONS nella funzione \_ [**DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) Durante la **transazione XTYP \_ CONNECT,** DDEML passa il nome del servizio e il nome dell'argomento al server. Il server deve esaminare i nomi e restituire **TRUE** se supporta la coppia di nomi di servizio e argomento oppure **FALSE** in caso contrario.

Se nessun server risponde in modo positivo alla richiesta di connessione del client, il client riceve **NULL** da [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) e non viene stabilita alcuna conversazione. Se un server restituisce **TRUE,** viene stabilita una conversazione e il client riceve un handle di conversazione, ovvero un **valore DWORD** che identifica la conversazione. Il client usa l'handle nelle chiamate DDEML successive per ottenere dati dal server. Il server riceve la transazione [**XTYP \_ CONNECT \_ CONFIRM**](xtyp-connect-confirm.md) (a meno che il server non ha specificato il flag di filtro CBF \_ SKIP CONNECT \_ \_ CONFIRMS). Questa transazione passa l'handle di conversazione al server.

Nell'esempio seguente viene richiesta una conversazione nell'argomento System con un server che riconosce il nome del servizio MyServer. I *parametri hszServName* e *hszSysTopic* sono handle di stringa creati in precedenza.


```
HCONV hConv;         // conversation handle 
HWND hwndParent;     // parent window handle 
HSZ hszServName;     // service name string handle 
HSZ hszSysTopic;     // System topic string handle 
 
hConv = DdeConnect( 
    idInst,               // instance identifier 
    hszServName,          // service name string handle 
    hszSysTopic,          // System topic string handle 
    (PCONVCONTEXT) NULL); // use default context 
 
if (hConv == NULL) 
{ 
    MessageBox(hwndParent, "MyServer is unavailable.", 
        (LPSTR) NULL, MB_OK); 
    return FALSE; 
} 
```



Nell'esempio precedente [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) fa sì che la funzione di callback DDE dell'applicazione MyServer riceva una [**transazione XTYP \_ CONNECT.**](xtyp-connect.md)

Nell'esempio seguente il server risponde alla transazione [**XTYP \_ CONNECT**](xtyp-connect.md) confrontando la stringa del nome dell'argomento che gestisce il codice DDEML passato al server con ogni elemento nella matrice di stringhe di nomi di argomento supportate dal server. Se il server trova una corrispondenza, stabilisce la conversazione.


```
#define CTOPICS 5 
 
HSZ hsz1;                  // string handle passed by DDEML 
HSZ ahszTopics[CTOPICS];   // array of supported topics 
int i;                     // loop counter 
 
// Use a switch statement to examine transaction types. 
// Here is the connect case.
 
    case XTYP_CONNECT: 
        for (i = 0; i < CTOPICS; i++) 
        { 
            if (hsz1 == ahszTopics[i]) 
                return TRUE;   // establish a conversation 
        } 
 
        return FALSE; // Topic not supported; deny conversation.  
 
// Process other transaction types. 
```



Se il server restituisce **TRUE** in risposta alla transazione [**XTYP \_ CONNECT,**](xtyp-connect.md) DDEML invia una [**transazione XTYP \_ CONNECT \_ CONFIRM**](xtyp-connect-confirm.md) alla funzione di callback DDE del server. Il server può ottenere l'handle per la conversazione elaborando questa transazione.

Un client può stabilire una conversazione con caratteri jolly specificando **NULL** per l'handle di stringa del nome del servizio, l'handle della stringa del nome dell'argomento o entrambi in una chiamata a [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect). Se almeno uno degli handle di stringa è **NULL,** DDEML invia la transazione [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) alle funzioni di callback di tutte le applicazioni DDE (ad eccezione di quelle che filtrano la transazione **XTYP \_ WILDCONNECT).** Ogni applicazione server deve rispondere restituisce un handle di dati che identifica una matrice con terminazione Null di [**strutture HSZPAIR.**](/windows/win32/api/ddeml/ns-ddeml-hszpair) Se l'applicazione server non ha chiamato [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) per registrare i nomi dei servizi e se il filtro è on, il server non riceve transazioni **XTYP \_ WILDCONNECT.** Per altre informazioni sugli handle di dati, [vedere Gestione dati](data-management.md).

La matrice deve contenere una struttura per ogni coppia nome servizio e nome argomento corrispondente alla coppia specificata dal client. DDEML seleziona una delle coppie per stabilire una conversazione e restituisce al client un handle che identifica la conversazione. DDEML invia la [**transazione XTYP \_ CONNECT \_ CONFIRM**](xtyp-connect-confirm.md) al server (a meno che il server non filtri questa transazione). Nell'esempio seguente viene illustrata una tipica risposta del server alla [**transazione XTYP \_ WILDCONNECT.**](xtyp-wildconnect.md)


```
#define CTOPICS 2 
 
UINT uType; 
HSZPAIR ahszp[(CTOPICS + 1)]; 
HSZ ahszTopicList[CTOPICS]; 
HSZ hszServ, hszTopic; 
WORD i, j; 
 
if (uType == XTYP_WILDCONNECT) 
{ 
    // Scan the topic list and create an array of HSZPAIR structures. 
 
    j = 0; 
    for (i = 0; i < CTOPICS; i++) 
    { 
        if (hszTopic == (HSZ) NULL || 
                hszTopic == ahszTopicList[i]) 
        { 
            ahszp[j].hszSvc = hszServ; 
            ahszp[j++].hszTopic = ahszTopicList[i]; 
        } 
    } 
 
    // End the list with an HSZPAIR structure that contains NULL 
    // string handles as its members. 
 
    ahszp[j].hszSvc = NULL; 
    ahszp[j++].hszTopic = NULL; 
 
    // Return a handle to a global memory object containing the 
    // HSZPAIR structures. 
 
    return DdeCreateDataHandle( 
        idInst,          // instance identifier 
        (LPBYTE) &ahszp, // pointer to HSZPAIR array 
        sizeof(HSZ) * j, // length of the array 
        0,               // start at the beginning 
        (HSZ) NULL,      // no item name string 
        0,               // return the same format 
        0);              // let the system own it 
} 
```



Il client o il server può terminare una conversazione in qualsiasi momento chiamando la [**funzione DdeDisconnect.**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) Questa funzione fa sì che la funzione di callback del partner nella conversazione riceva la [**transazione XTYP \_ DISCONNECT**](xtyp-disconnect.md) (a meno che il partner non ha specificato il flag di filtro CBF \_ SKIP \_ DISCONNECTS). In genere, un'applicazione risponde alla transazione **XTYP \_ DISCONNECT** usando la [**funzione DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) per ottenere informazioni sulla conversazione terminata. Dopo che la funzione di callback ha restituito dall'elaborazione **della transazione DISCONNECT XTYP, \_** l'handle di conversazione non è più valido.

Un'applicazione client che riceve una transazione [**DISCONNECT XTYP \_**](xtyp-disconnect.md) nella funzione di callback DDE può tentare di ristabilire la conversazione chiamando la [**funzione DdeReconnect.**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) Il client deve chiamare **DdeReconnect dall'interno** della funzione di callback DDE.

## <a name="multiple-conversations"></a>Più conversazioni

Un'applicazione client può usare [**la funzione DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) per determinare se nel sistema sono disponibili server di interesse. Un client specifica un nome di servizio e un nome di argomento quando chiama **DdeConnectList**, causando la trasmissione della transazione [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) alle funzioni di callback DDE di tutti i server che corrispondono al nome del servizio (ad eccezione di quelli che filtrano la transazione). La funzione di callback di un server deve restituire un handle di dati che identifica una matrice con terminazione Null di [**strutture HSZPAIR.**](/windows/win32/api/ddeml/ns-ddeml-hszpair) La matrice deve contenere una struttura per ogni coppia nome servizio e nome argomento corrispondente alla coppia specificata dal client. DDEML stabilisce una conversazione per ogni **struttura HSZPAIR** riempita dal server e restituisce un handle dell'elenco di conversazioni al client. Il server riceve l'handle di conversazione tramite la [**transazione XTYP \_ CONNECT**](xtyp-connect.md) (a meno che il server non filtri questa transazione).

Un client può specificare **NULL per** il nome del servizio, il nome dell'argomento o entrambi quando chiama [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist). Se il nome del servizio è **NULL,** tutti i server nel sistema che supportano il nome dell'argomento specificato rispondono. Viene stabilita una conversazione con ogni server che risponde, incluse più istanze dello stesso server. Se il nome dell'argomento **è NULL,** viene stabilita una conversazione in ogni argomento riconosciuto da ogni server che corrisponde al nome del servizio.

Un client può usare [**le funzioni DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) e [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) per identificare i server che rispondono a [**DdeConnectList.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) **DdeQueryNextServer** restituisce l'handle di conversazione successivo in un elenco di conversazioni e **DdeQueryConvInfo** riempie una struttura [**CONVINFO**](/windows/win32/api/ddeml/ns-ddeml-convinfo) con informazioni sulla conversazione. Il client può mantenere gli handle di conversazione di cui ha bisogno e rimuovere il resto dall'elenco delle conversazioni.

L'esempio seguente usa [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) per stabilire conversazioni con tutti i server che supportano l'argomento System e quindi usa le funzioni [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) e [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) per ottenere gli handle della stringa del nome del servizio dei server e archiviarli in un buffer.


```
HCONVLIST hconvList; // conversation list 
DWORD idInst;        // instance identifier 
HSZ hszSystem;       // System topic 
HCONV hconv = NULL;  // conversation handle 
CONVINFO ci;         // holds conversation data 
UINT cConv = 0;      // count of conv. handles 
HSZ *pHsz, *aHsz;    // point to string handles 
 
// Connect to all servers that support the System topic. 
 
hconvList = DdeConnectList(idInst, NULL, hszSystem, NULL, NULL); 
 
// Count the number of handles in the conversation list. 
 
while ((hconv = DdeQueryNextServer(hconvList, hconv)) != NULL) 
    cConv++; 
 
// Allocate a buffer for the string handles. 
 
hconv = NULL; 
aHsz = (HSZ *) LocalAlloc(LMEM_FIXED, cConv * sizeof(HSZ)); 
 
// Copy the string handles to the buffer. 
 
pHsz = aHsz; 
while ((hconv = DdeQueryNextServer(hconvList, hconv)) != NULL) 
{ 
    DdeQueryConvInfo(hconv, QID_SYNC, (PCONVINFO) &ci); 
    DdeKeepStringHandle(idInst, ci.hszSvcPartner); 
    *pHsz++ = ci.hszSvcPartner; 
} 
 
// Use the handles; converse with the servers. 
 
// Free the memory and terminate the conversations. 
 
LocalFree((HANDLE) aHsz); 
DdeDisconnectList(hconvList); 
```



Un'applicazione può terminare una singola conversazione in un elenco di conversazioni chiamando la [**funzione DdeDisconnect.**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) Un'applicazione può terminare tutte le conversazioni in un elenco di conversazioni chiamando la [**funzione DdeDisconnectList.**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) Entrambe le funzioni determinano l'invio di [**transazioni DISCONNECT \_ XTYP**](xtyp-disconnect.md) da parte di DDEML alla funzione di callback DDE di ogni partner. **DdeDisconnectList** invia una **transazione DISCONNECT XTYP \_** per ogni handle di conversazione nell'elenco.

Un client può recuperare un elenco di handle di conversazione in un elenco di conversazioni passando un handle di elenco di conversazioni esistente a [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist). Il processo di enumerazione rimuove gli handle delle conversazioni terminate dall'elenco e vengono aggiunte conversazioni nonduplicate che si adattano al nome del servizio e al nome dell'argomento specificati.

Se [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) specifica un handle di elenco di conversazioni esistente, la funzione crea un nuovo elenco di conversazioni che contiene gli handle di qualsiasi nuova conversazione e gli handle dell'elenco esistente.

Se sono presenti conversazioni duplicate, [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) tenta di impedire handle di conversazione duplicati nell'elenco delle conversazioni. Una conversazione duplicata è una seconda conversazione con lo stesso server nello stesso nome del servizio e nello stesso nome dell'argomento. Due conversazioni di questo tipo hanno handle diversi, ma identificano la stessa conversazione.

 

 




