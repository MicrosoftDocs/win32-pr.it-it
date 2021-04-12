---
title: Utilizzo di Dynamic Data Exchange
description: In questo argomento vengono forniti esempi di codice relativi a Dynamic Data Exchange.
ms.assetid: 6d94403b-64b4-4763-868a-3b94431dab79
keywords:
- Dynamic Data Exchange (DDE), conversazioni
- DDE (Dynamic Data Exchange), conversazioni
- scambio di dati, Dynamic Data Exchange (DDE)
- Dynamic Data Exchange (DDE), esempi
- DDE (Dynamic Data Exchange), esempi
- Dynamic Data Exchange (DDE), comandi nelle applicazioni server
- DDE (Dynamic Data Exchange), comandi nelle applicazioni server
- Dynamic Data Exchange (DDE), collegamenti dati
- DDE (Dynamic Data Exchange), collegamenti dati
- Dynamic Data Exchange (DDE), elementi
- DDE (Dynamic Data Exchange), elementi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe20c4dedc38303fe9bcb9c4b0fae42d03ee536
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337911"
---
# <a name="using-dynamic-data-exchange"></a>Utilizzo di Dynamic Data Exchange

Questa sezione contiene esempi di codice sulle attività seguenti:

-   [Avvio di una conversazione](#initiating-a-conversation)
-   [Trasferimento di un singolo elemento](#transferring-a-single-item)
    -   [Recupero di un elemento dal server](#retrieving-an-item-from-the-server)
    -   [Invio di un elemento al server](#submitting-an-item-to-the-server)
-   [Creazione di un collegamento dati permanente](#establishing-a-permanent-data-link)
    -   [Avvio di un collegamento dati](#initiating-a-data-link)
    -   [Avvio di un collegamento dati con il comando Incolla collegamento](#initiating-a-data-link-with-the-paste-link-command)
    -   [Notifica al client che i dati sono stati modificati](#notifying-the-client-that-data-has-changed)
    -   [Terminazione di un collegamento dati](#terminating-a-data-link)
-   [Esecuzione di comandi in un'applicazione server](#carrying-out-commands-in-a-server-application)
-   [Terminazione di una conversazione](#terminating-a-conversation)

## <a name="initiating-a-conversation"></a>Avvio di una conversazione

Per avviare una conversazione di Dynamic Data Exchange (DDE), il client invia un messaggio di [**\_ \_ inizializzazione di WM DDE**](wm-dde-initiate.md) . In genere, il client trasmette questo messaggio chiamando [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), con-1 come primo parametro. Se l'applicazione dispone già dell'handle di finestra per l'applicazione server, il messaggio può essere inviato direttamente a tale finestra. Il client prepara gli atomi per il nome dell'applicazione e il nome dell'argomento chiamando [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma). Il client può richiedere conversazioni con qualsiasi applicazione server potenziale e per qualsiasi potenziale argomento fornendo atomi **null** (carattere jolly) per l'applicazione e l'argomento.

Nell'esempio seguente viene illustrata la modalità di avvio di una conversazione da parte del client, in cui vengono specificati sia l'applicazione che l'argomento.


```
    static BOOL fInInitiate = FALSE; 
    char *szApplication; 
    char *szTopic; 
    atomApplication = *szApplication == 0 ? 
    NULL     : GlobalAddAtom((LPSTR) szApplication); 
    atomTopic = *szTopic == 0 ? 
    NULL     : GlobalAddAtom((LPSTR) szTopic); 
 
    fInInitiate = TRUE; 
    SendMessage((HWND) HWND_BROADCAST, // broadcasts message 
        WM_DDE_INITIATE,               // initiates conversation 
        (WPARAM) hwndClientDDE,        // handle to client DDE window 
        MAKELONG(atomApplication,      // application-name atom 
            atomTopic));               // topic-name atom 
    fInInitiate = FALSE; 
    if (atomApplication != NULL) 
        GlobalDeleteAtom(atomApplication); 
    if (atomTopic != NULL) 
        GlobalDeleteAtom(atomTopic);
```



> [!Note]  
> Se l'applicazione usa atomi **null** , non è necessario usare le funzioni [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) e [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) . In questo esempio, l'applicazione client crea due atomi globali che contengono rispettivamente il nome del server e il nome dell'argomento.

 

L'applicazione client invia un messaggio di [**\_ \_ inizializzazione del DDE WM**](wm-dde-initiate.md) con questi due atomi nel parametro *lParam* del messaggio. Nella chiamata alla funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , l'handle di finestra speciale – 1 indica al sistema di inviare il messaggio a tutte le altre applicazioni attive. **SendMessage** non torna all'applicazione client fino a quando tutte le applicazioni che ricevono il messaggio non hanno a sua volta restituito il controllo al sistema. Ciò significa che tutti i messaggi di [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) inviati in risposta dalle applicazioni server vengono elaborati dal client nel momento in cui la chiamata **SendMessage** ha restituito.

Dopo la restituzione di [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , l'applicazione client elimina gli atomi globali.

Le applicazioni server rispondono secondo la logica illustrata nel diagramma seguente.

![logica di risposta dell'applicazione server](images/csdde-01.png)

Per confermare uno o più argomenti, il server deve creare atomi per ogni conversazione (richiedendo atomi di nome applicazione duplicati se sono presenti più argomenti) e inviare un messaggio di [**\_ \_ ACK DDE WM**](wm-dde-ack.md) per ogni conversazione, come illustrato nell'esempio seguente.


```
if ((atomApplication = GlobalAddAtom("Server")) != 0) 
{ 
    if ((atomTopic = GlobalAddAtom(szTopic)) != 0) 
    { 
        SendMessage(hwndClientDDE, 
            WM_DDE_ACK, 
            (WPARAM) hwndServerDDE, 
            MAKELONG(atomApplication, atomTopic)); 
        GlobalDeleteAtom(atomApplication); 
    } 
 
    GlobalDeleteAtom(atomTopic); 
} 
 
if ((atomApplication == 0) || (atomTopic == 0)) 
{ 
    // Handle errors. 
}
```



Quando un server risponde con un messaggio [**\_ \_ ACK DDE WM**](wm-dde-ack.md) , l'applicazione client deve salvare un handle per la finestra del server. Il client che riceve l'handle come parametro *wParam* del messaggio **\_ \_ ACK DDE WM** invia quindi tutti i messaggi DDE successivi alla finestra del server identificata da questo handle.

Se l'applicazione client utilizza un Atom **null** per il nome dell'applicazione o dell'argomento, si prevede che l'applicazione riceva i riconoscimenti da più di un'applicazione server. Più riconoscimenti possono provenire da più istanze di un server DDE, anche se l'applicazione client non **utilizza gli** atomi. Un server deve sempre usare una finestra univoca per ogni conversazione. La routine della finestra nell'applicazione client può utilizzare un handle per la finestra del server (fornito come parametro *lParam* dell' [**\_ \_ avvio di WM DDE**](wm-dde-initiate.md)) per tenere traccia di più conversazioni. Ciò consente a una singola finestra client di elaborare diverse conversazioni senza dover terminare e riconnettersi a una nuova finestra del client per ogni conversazione.

## <a name="transferring-a-single-item"></a>Trasferimento di un singolo elemento

Una volta stabilita una conversazione DDE, il client può recuperare il valore di un elemento di dati dal server inviando il messaggio di [**\_ \_ richiesta DDE di WM**](wm-dde-request.md) oppure inviare un valore dell'elemento di dati al server eseguendo il [**\_ \_ poke DDE di WM**](wm-dde-poke.md).

-   [Recupero di un elemento dal server](#retrieving-an-item-from-the-server)
-   [Invio di un elemento al server](#submitting-an-item-to-the-server)

### <a name="retrieving-an-item-from-the-server"></a>Recupero di un elemento dal server

Per recuperare un elemento dal server, il client invia al server un messaggio [**di \_ \_ richiesta DDE WM**](wm-dde-request.md) che specifica l'elemento e il formato da recuperare, come illustrato nell'esempio seguente.


```
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndServerDDE, 
            WM_DDE_REQUEST, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_REQUEST, CF_TEXT, atomItem))) 
    {
        GlobalDeleteAtom(atomItem); 
    }
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
}
```



In questo esempio, il client specifica il formato degli Appunti del **\_ testo CF** come formato preferito per l'elemento di dati richiesto.

Il ricevitore (Server) del messaggio [**di \_ \_ richiesta DDE di WM**](wm-dde-request.md) deve in genere eliminare il Atom dell'elemento, ma se la chiamata al [**messaggio**](/windows/desktop/api/winuser/nf-winuser-postmessagea) non riesce, il client deve eliminare il formato Atom.

Se il server ha accesso all'elemento richiesto ed è in grado di eseguirne il rendering nel formato richiesto, il server copia il valore dell'elemento come oggetto Shared Memory e invia al client un messaggio di [**\_ \_ dati DDE di WM**](wm-dde-data.md) , come illustrato nell'esempio seguente.


```
// Allocate the size of the DDE data header, plus the data: a 
// string,<CR><LF><NULL>. The byte for the string's terminating 
// null character is counted by DDEDATA.Value[1].

size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hData = GlobalAlloc(GMEM_MOVEABLE,
  (LONG) sizeof(DDEDATA) + *pcch + 2)))  
{
    return; 
}
 
if (!(lpData = (DDEDATA FAR*) GlobalLock(hData)))  
{
    GlobalFree(hData); 
    return; 
} 
 
lpData->cfFormat = CF_TEXT;
hResult = StringCchCopy((LPSTR) lpData->Value, *pcch +1, (LPCSTR) szItemValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
 
// Each line of CF_TEXT data is terminated by CR/LF. 
hResult = StringCchCat((LPSTR) lpData->Value, *pcch + 3, (LPCSTR) "\r\n");
if (FAILED(hResult)
{
// TODO: Write error handler.
 return;
} 
GlobalUnlock(hData); 
if ((atomItem = GlobalAddAtom((LPSTR) szItemName)) != 0) 
{ 
    lParam = PackDDElParam(WM_DDE_ACK, (UINT) hData, atomItem); 
    if (!PostMessage(hwndClientDDE, 
            WM_DDE_DATA, 
            (WPARAM) hwndServerDDE, 
            lParam)) 
    { 
        GlobalFree(hData); 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_ACK, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors.  
}
```



In questo esempio, l'applicazione server alloca un oggetto memoria per contenere l'elemento dati. L'oggetto dati viene inizializzato come struttura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) .

L'applicazione server imposta quindi il membro **cfFormat** della struttura su testo CF \_ per informare l'applicazione client che i dati sono in formato testo. Il client risponde copiando il valore dei dati richiesti nel membro del **valore** della struttura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) . Dopo che il server ha riempito l'oggetto dati, il server Sblocca i dati e crea un Atom globale contenente il nome dell'elemento di dati.

Infine, il server emette il messaggio di [**\_ \_ dati DDE di WM**](wm-dde-data.md) chiamando [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea). L'handle per l'oggetto dati e il formato Atom contenente il nome dell'elemento vengono compressi nel parametro *lParam* del messaggio tramite la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) .

Se [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) ha esito negativo, il server deve usare la funzione [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) per liberare il parametro *lParam* compresso. Il server deve inoltre liberare il parametro *lParam* compresso per il messaggio di [**\_ \_ richiesta DDE WM**](wm-dde-request.md) ricevuto.

Se il server non è in grado di soddisfare la richiesta, invia un messaggio [**\_ \_ ACK DDE**](wm-dde-ack.md) negativo al client, come illustrato nell'esempio seguente.


```
// Negative acknowledgment. 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 0, atomItem));
```



Al momento della ricezione di un messaggio di [**\_ \_ dati DDE di WM**](wm-dde-data.md) , il client elabora il valore dell'elemento di dati in base alle esigenze. Se quindi il membro **fAckReq** a cui puntava il messaggio di **\_ \_ dati DDE di WM** è 1, il client deve inviare al server un messaggio [**\_ \_ ACK DDE positivo WM**](wm-dde-ack.md) , come illustrato nell'esempio seguente.


```
UnpackDDElParam(WM_DDE_DATA, lParam, (PUINT) &hData, 
    (PUINT) &atomItem); 
if (!(lpDDEData = (DDEDATA FAR*) GlobalLock(hData)) 
        || (lpDDEData->cfFormat != CF_TEXT)) 
{ 
    PostMessage(hwndServerDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_ACK, 0, atomItem)); // Negative ACK. 
} 
 
// Copy data from lpDDEData here. 
 
if (lpDDEData->fAckReq) 
{ 
    PostMessage(hwndServerDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_ACK, 0x8000, 
            atomItem)); // Positive ACK 
} 
 
bRelease = lpDDEData->fRelease; 
GlobalUnlock(hData); 
if (bRelease) 
    GlobalFree(hData);
```



In questo esempio, il client esamina il formato dei dati. Se il formato non è **un \_ testo CF** (o se il client non è in grado di bloccare la memoria per i dati), il client invia un messaggio [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) negativo per indicare che non è in grado di elaborare i dati. Se il client non è in grado di bloccare un handle di dati perché l'handle contiene il membro **fAckReq** , il client non deve inviare un messaggio **\_ \_ ACK DDE di WM** negativo. Al contrario, il client deve terminare la conversazione.

Se un client invia un riconoscimento negativo in risposta a un messaggio [**di \_ \_ dati DDE di WM**](wm-dde-data.md) , il server è responsabile della liberazione della memoria (ma non del parametro *lParam* ) a cui fa riferimento il messaggio di **\_ \_ dati DDE di WM** associato al riconoscimento negativo.

Se è in grado di elaborare i dati, il client esamina il membro **fAckReq** della struttura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) per determinare se il server ha richiesto di essere informato che il client ha ricevuto ed elaborato correttamente i dati. Se il server ha richiesto queste informazioni, il client invia al server un messaggio [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) positivo.

Poiché lo sblocco dei dati invalida il puntatore ai dati, il client salva il valore del membro **fRelease** prima di sbloccare l'oggetto dati. Dopo aver salvato il valore, il client lo esamina per determinare se l'applicazione server ha richiesto al client di liberare la memoria contenente i dati. il client agisce di conseguenza.

Al momento della ricezione di un messaggio [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) negativo, il client può richiedere di nuovo lo stesso valore dell'elemento, specificando un formato degli Appunti diverso. In genere, un client richiederà per prima cosa il formato più complesso che può supportare, quindi eseguire un'istruzione per difetto con formati progressivamente più semplici fino a quando non ne troverà uno che il server è in grado di fornire.

Se il server supporta l'elemento formats dell'argomento System, il client può determinare una volta il formato degli appunti supportato dal server, anziché determinarli ogni volta che il client richiede un elemento.

### <a name="submitting-an-item-to-the-server"></a>Invio di un elemento al server

Il client può inviare un valore dell'elemento al server tramite il messaggio [**di \_ \_ poke DDE di WM**](wm-dde-poke.md) . Il client esegue il rendering dell'elemento da inviare e invia il messaggio di **\_ \_ poke DDE di WM** , come illustrato nell'esempio seguente.


```
size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hPokeData = GlobalAlloc(GMEM_MOVEABLE,
  (LONG) sizeof(DDEPOKE) + *pcch + 2))) 
{
    return; 
}
 
if (!(lpPokeData = (DDEPOKE *) GlobalLock(hPokeData))) 
{ 
    GlobalFree(hPokeData); 
    return; 
} 
 
lpPokeData->fRelease = TRUE; 
lpPokeData->cfFormat = CF_TEXT;
hResult = StringCchCopy((LPSTR) lpPokeData->Value, *pcch +1, (LPCSTR) szValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}  
 
// Each line of CF_TEXT data is terminated by CR/LF. 
hResult = StringCchCat((LPSTR) lpPokeData->Value, *pcch + 3, (LPCSTR) "\r\n");
if (FAILED(hResult)
{
// TODO: Write error handler.
 return;
}
GlobalUnlock(hPokeData); 
if ((atomItem = GlobalAddAtom((LPSTR) szItem)) != 0) 
{ 
 
        if (!PostMessage(hwndServerDDE, 
                WM_DDE_POKE, 
                (WPARAM) hwndClientDDE, 
                PackDDElParam(WM_DDE_POKE, (UINT) hPokeData, 
                    atomItem))) 
        { 
            GlobalDeleteAtom(atomItem); 
            GlobalFree(hPokeData); 
        } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
} 
```



> [!Note]  
> L'invio di dati tramite un messaggio [**\_ \_ poke DDE di WM**](wm-dde-poke.md) è essenzialmente analogo all'invio tramite [**\_ \_ dati DDE**](wm-dde-data.md)di WM, ad eccezione del fatto che **WM \_ DDE \_ poke** viene inviato dal client al server.

 

Se il server è in grado di accettare il valore dell'elemento di dati nel formato di cui è stato eseguito il rendering dal client, il server elabora il valore dell'elemento in base alle esigenze e invia al client un messaggio [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) positivo. Se non è in grado di elaborare il valore dell'elemento, a causa del formato o per altri motivi, il server invia al client un messaggio **\_ \_ ACK DDE di WM** negativo.


```
UnpackDDElParam(WM_DDE_POKE, lParam, (PUINT) &hPokeData, 
    (PUINT) &atomItem); 
GlobalGetAtomName(atomItem, szItemName, ITEM_NAME_MAX_SIZE); 
if (!(lpPokeData = (DDEPOKE *) GlobalLock(hPokeData)) 
        || lpPokeData->cfFormat != CF_TEXT 
        || !IsItemSupportedByServer(szItemName)) 
{ 
    PostMessage(hwndClientDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndServerDDE, 
        PackDDElParam(WM_DDE_ACK, 0, atomItem)); // negative ACK  
}
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
} 
hResult = StringCchCopy(szItemValue, *pcch +1, lpPokeData->Value); // copies value 
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}  
bRelease = lpPokeData->fRelease; 
GlobalUnlock(hPokeData); 
if (bRelease) 
{ 
    GlobalFree(hPokeData); 
} 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 
         0x8000, atomItem));    // positive ACK.
```



In questo esempio, il server chiama [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) per recuperare il nome dell'elemento inviato dal client. Il server determina quindi se supporta l'elemento e se viene eseguito il rendering dell'elemento nel formato corretto (ovvero il testo CF \_ ). Se l'elemento non è supportato e non viene sottoposto a rendering nel formato corretto o se il server non è in grado di bloccare la memoria per i dati, il server invia un riconoscimento negativo all'applicazione client. Si noti che in questo caso, l'invio di un riconoscimento negativo è corretto perché per i messaggi [**\_ \_ poke DDE di WM**](wm-dde-poke.md) si presuppone sempre che sia impostato il membro **fAckReq** . Il server deve ignorare il membro.

Se un server invia un riconoscimento negativo in risposta a un messaggio [**\_ \_ poke DDE WM**](wm-dde-poke.md) , il client è responsabile della liberazione della memoria (ma non del parametro *lParam* ) a cui fa riferimento il messaggio **di \_ \_ poke DDE di WM** associato al riconoscimento negativo.

## <a name="establishing-a-permanent-data-link"></a>Creazione di un collegamento dati permanente

Un'applicazione client può utilizzare DDE per stabilire un collegamento a un elemento in un'applicazione server. Dopo aver stabilito un collegamento di questo tipo, il server invia aggiornamenti periodici dell'elemento collegato al client, in genere ogni volta che viene modificato il valore dell'elemento. Viene pertanto stabilito un flusso di dati permanente tra le due applicazioni; Questo flusso di dati rimane attivo fino a quando non viene disconnesso in modo esplicito.

### <a name="initiating-a-data-link"></a>Avvio di un collegamento dati

Il client avvia un collegamento dati pubblicando un messaggio [**di \_ \_ notifica DDE di WM**](wm-dde-advise.md) , come illustrato nell'esempio seguente.


```
if (!(hOptions = GlobalAlloc(GMEM_MOVEABLE, 
        sizeof(DDEADVISE)))) 
    return; 
if (!(lpOptions = (DDEADVISE FAR*) GlobalLock(hOptions))) 
{ 
    GlobalFree(hOptions); 
    return; 
} 
 
lpOptions->cfFormat = CF_TEXT; 
lpOptions->fAckReq = TRUE; 
lpOptions->fDeferUpd = FALSE; 
GlobalUnlock(hOptions); 
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!(PostMessage(hwndServerDDE, 
            WM_DDE_ADVISE, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_ADVISE, (UINT) hOptions, 
                atomItem)))) 
    { 
        GlobalDeleteAtom(atomItem); 
        GlobalFree(hOptions); 
        FreeDDElParam(WM_DDE_ADVISE, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors 
 
}
```



In questo esempio, l'applicazione client imposta il flag **FDeferUpd** del messaggio [**di \_ \_ avviso DDE di WM**](wm-dde-advise.md) su **false**. In questo modo l'applicazione server invia i dati al client ogni volta che i dati vengono modificati.

Se il server non è in grado di servire la richiesta di [**\_ \_ notifica DDE di WM**](wm-dde-advise.md) , invia al client un messaggio di [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) negativo. Tuttavia, se il server ha accesso all'elemento e può eseguirne il rendering nel formato richiesto, il server annota il nuovo collegamento, chiamando i flag specificati nel parametro *hOptions* , e invia al client un messaggio **\_ \_ ACK DDE** positivo. Da quel momento in poi, fino a quando il client non emette un messaggio di avviso [**\_ \_ DDE di WM**](wm-dde-unadvise.md) corrispondente, il server invia i nuovi dati al client ogni volta che il valore dell'elemento viene modificato nel server.

Il messaggio di [**\_ \_ notifica DDE di WM**](wm-dde-advise.md) stabilisce il formato dei dati da scambiare durante il collegamento. Se il client tenta di stabilire un altro collegamento con lo stesso elemento, ma usa un formato dati diverso, il server può scegliere di rifiutare il secondo formato dati o tentare di supportarlo. Se è stato stabilito un collegamento a caldo per qualsiasi elemento di dati, il server può supportare un solo formato dati alla volta. Questo è dovuto al fatto che il messaggio di [**\_ \_ dati DDE di WM**](wm-dde-data.md) per un collegamento a caldo ha un handle di dati **null** , che altrimenti contiene le informazioni sul formato. Pertanto, un server deve rifiutare tutti i collegamenti caldi per un elemento già collegato e deve rifiutare tutti i collegamenti per un elemento con collegamenti caldi. Un'altra interpretazione potrebbe essere che il server modifica il formato e lo stato attivo o caldo di un collegamento quando viene richiesto un secondo collegamento per lo stesso elemento di dati.

In generale, le applicazioni client non devono tentare di stabilire più di un collegamento alla volta per un elemento di dati.

### <a name="initiating-a-data-link-with-the-paste-link-command"></a>Avvio di un collegamento dati con il comando Incolla collegamento

Le applicazioni che supportano i collegamenti dati ad accesso frequente o caldo in genere supportano un formato degli Appunti registrato denominato collegamento. Quando è associato ai comandi copia e Incolla collegamento dell'applicazione, questo formato degli Appunti consente all'utente di stabilire conversazioni DDE tra le applicazioni semplicemente copiando un elemento di dati nell'applicazione server e incollarlo nell'applicazione client.

Un'applicazione server supporta il formato degli Appunti di collegamento inserendo negli Appunti una stringa contenente i nomi dell'applicazione, dell'argomento e dell'elemento quando l'utente sceglie il comando **Copy** dal menu **modifica** . Di seguito è riportato il formato di collegamento standard:

*applicazione ***\\ 0*** argomento ***\\ 0*** elemento * * \\ 0 0 \\**

Un singolo carattere null separa i nomi e due caratteri null terminano l'intera stringa.

Le applicazioni client e server devono registrare il formato degli Appunti di collegamento, come illustrato:


```
cfLink = RegisterClipboardFormat("Link");
```



Un'applicazione client supporta il formato degli Appunti di collegamento per mezzo di un comando Incolla collegamento nel menu Modifica. Quando l'utente sceglie questo comando, l'applicazione client analizza i nomi dell'applicazione, dell'argomento e degli elementi dai dati degli Appunti in formato di collegamento. Usando questi nomi, l'applicazione client avvia una conversazione per l'applicazione e l'argomento, se tale conversazione non esiste già. L'applicazione client invia quindi un messaggio di [**\_ \_ notifica DDE di WM**](wm-dde-advise.md) all'applicazione server, specificando il nome dell'elemento contenuto nei dati degli Appunti in formato collegamento.

Di seguito è riportato un esempio di risposta di un'applicazione client quando l'utente sceglie il comando Incolla collegamento.


```
void DoPasteLink(hwndClientDDE) 
HWND hwndClientDDE; 
{ 
    HANDLE hData; 
    LPSTR lpData; 
    HWND hwndServerDDE; 
    CHAR szApplication[APP_MAX_SIZE + 1]; 
    CHAR szTopic[TOPIC_MAX_SIZE + 1]; 
    CHAR szItem[ITEM_MAX_SIZE + 1]; 
    size_t * nBufLen; 
 HRESULT hResult;
 
    if (OpenClipboard(hwndClientDDE)) 
    { 
        if (!(hData = GetClipboardData(cfLink)) || 
                !(lpData = GlobalLock(hData))) 
        { 
            CloseClipboard(); 
            return; 
        } 
 
        // Parse the clipboard data.
  hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
// TODO: Write error handler.
  return;
 }
 if (*nBufLen >= APP_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }
 hResult = StringCchCopy(szApplication, APP_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
// TODO: Write error handler.
  return;
 }
        lpData += (*nBufLen + 1); // skips over null
 hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
 // TODO: Write error handler.
  return;
 }
 if (*nBufLen >= TOPIC_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }
 hResult = StringCchCopy(szTopic, TOPIC_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
 // TODO: Write error handler.
  return;
 }
        lpData += (nBufLen + 1); // skips over null
 hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
 // TODO: Write error handler.
  return;
 }
 if (*nBufLen >= ITEM_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }

 hResult = StringCchCopy(szItem, ITEM_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
 // TODO: Write error handler.
  return;
 } 
        GlobalUnlock(hData); 
        CloseClipboard(); 
 
        if (hwndServerDDE = 
                FindServerGivenAppTopic(szApplication, szTopic)) 
        { 
            // App/topic conversation is already started. 
 
            if (DoesAdviseAlreadyExist(hwndServerDDE, szItem)) 
            {
                MessageBox(hwndMain, 
                    "Advisory already established", 
                    "Client", MB_ICONEXCLAMATION | MB_OK); 
            }
            else SendAdvise(hwndClientDDE, hwndServerDDE, szItem); 
        } 
        else 
        { 
            // Client must initiate a new conversation first. 
            SendInitiate(szApplication, szTopic); 
            if (hwndServerDDE = 
                    FindServerGivenAppTopic(szApplication, 
                        szTopic)) 
            {
                SendAdvise(hwndClientDDE, hwndServerDDE, szItem); 
            }
        } 
    } 
    return; 
}
```



In questo esempio, l'applicazione client apre gli appunti e determina se contiene dati nel formato di collegamento (ovvero cfLink) precedentemente registrato. In caso contrario, o se non è in grado di bloccare i dati negli Appunti, il client restituisce.

Quando l'applicazione client recupera un puntatore ai dati degli Appunti, analizza i dati per estrarre i nomi dell'applicazione, dell'argomento e dell'elemento.

L'applicazione client determina se una conversazione nell'argomento esiste già tra l'applicazione e l'applicazione server. Se esiste una conversazione, il client verifica se esiste già un collegamento per l'elemento dati. Se esiste un collegamento di questo tipo, il client visualizza una finestra di messaggio all'utente; in caso contrario, chiama la propria funzione *SendAdvise* per inviare un messaggio di [**\_ \_ notifica DDE di WM**](wm-dde-advise.md) al server per l'elemento.

Se una conversazione nell'argomento non esiste già tra il client e il server, il client chiama prima la propria funzione *SendInitiate* per trasmettere il messaggio di [**\_ \_ inizializzazione di WM DDE**](wm-dde-initiate.md) per richiedere una conversazione e, in secondo luogo, chiama la propria funzione *FindServerGivenAppTopic* per stabilire la conversazione con la finestra che risponde per conto dell'applicazione server. Una volta iniziata la conversazione, l'applicazione client chiama *SendAdvise* per richiedere il collegamento.

### <a name="notifying-the-client-that-data-has-changed"></a>Notifica al client che i dati sono stati modificati

Quando il client stabilisce un collegamento usando il messaggio [**di \_ \_ notifica DDE di WM**](wm-dde-advise.md) , con il membro **FDeferUpd** non impostato (ovvero uguale a zero) nella struttura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) , il client ha richiesto al server di inviare l'elemento dati ogni volta che il valore dell'elemento cambia. In questi casi, il server esegue il rendering del nuovo valore dell'elemento di dati nel formato specificato in precedenza e invia al client un messaggio di [**\_ \_ dati DDE WM**](wm-dde-data.md) , come illustrato nell'esempio seguente.


```
// Allocate the size of a DDE data header, plus data (a string), 
// plus a <CR><LF><NULL> 

size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hData = GlobalAlloc(GMEM_MOVEABLE,
  sizeof(DDEDATA) + *pcch + 3))) 
{
    return; 
}
if (!(lpData = (DDEDATA FAR*) GlobalLock(hData))) 
{ 
    GlobalFree(hData); 
    return; 
} 
lpData->fAckReq = bAckRequest;       // as in original WM_DDE_ADVISE 
lpData->cfFormat = CF_TEXT;
hResult = StringCchCopy(lpData->Value, *pcch +1, szItemValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
// add CR/LF for CF_TEXT format
hResult = StringCchCat(lpData->Value, *pcch + 3, "\r\n");
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
GlobalUnlock(hData); 
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndClientDDE, 
            WM_DDE_DATA, 
            (WPARAM) hwndServerDDE, 
            PackDDElParam(WM_DDE_DATA, (UINT) hData, atomItem))) 
    { 
        GlobalFree(hData); 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_DATA, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
 
}
```



In questo esempio, il client elabora il valore dell'elemento in base alle esigenze. Se viene impostato il flag **fAckReq** per l'elemento, il client invia al server un messaggio [**\_ \_ ACK DDE positivo WM**](wm-dde-ack.md) .

Quando il client stabilisce il collegamento con il set di membri **FDeferUpd** (ovvero, uguale a 1), il client ha richiesto che solo una notifica, non i dati stessi, venga inviata ogni volta che i dati cambiano. In questi casi, quando il valore dell'elemento viene modificato, il server non esegue il rendering del valore ma invia semplicemente al client un messaggio di [**\_ \_ dati DDE WM**](wm-dde-data.md) con un handle di dati null, come illustrato nell'esempio seguente.


```
if (bDeferUpd)      // check whether flag was set in WM_DDE_ADVISE
{
    if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
    { 
        if (!PostMessage(hwndClientDDE, 
                WM_DDE_DATA, 
                (WPARAM) hwndServerDDE, 
                PackDDElParam(WM_DDE_DATA, 0, 
                    atomItem)))                  // NULL data
        {
            GlobalDeleteAtom(atomItem); 
            FreeDDElParam(WM_DDE_DATA, lParam); 
        } 
    } 
} 
 
if (atomItem == 0) 
{ 
     // Handle errors. 
} 
```



Se necessario, il client può richiedere il valore più recente dell'elemento di dati emettendo un normale messaggio [**di \_ \_ richiesta DDE di WM**](wm-dde-request.md) oppure ignorare semplicemente l'avviso dal server in cui sono stati modificati i dati. In entrambi i casi, se **fAckReq** è uguale a 1, il client deve inviare al server un messaggio di [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) positivo.

### <a name="terminating-a-data-link"></a>Terminazione di un collegamento dati

Se il client richiede la terminazione di un collegamento dati specifico, il client invia al server un messaggio di [**\_ \_ Unadvise DDE di WM**](wm-dde-unadvise.md) , come illustrato nell'esempio seguente.


```
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndServerDDE, 
            WM_DDE_UNADVISE, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_UNADVISE, 0, atomItem))) 
    { 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_UNADVISE, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
}
```



Il server verifica se il client dispone attualmente di un collegamento all'elemento specifico di questa conversazione. Se esiste un collegamento, il server invia al client un messaggio [**\_ \_ ACK DDE**](wm-dde-ack.md) positivo. il server non è più necessario per inviare aggiornamenti sull'elemento. Se non esiste alcun collegamento, il server invia al client un **messaggio \_ \_ ACK DDE di WM** negativo.

Il messaggio di [**\_ \_ Unadvise DDE WM**](wm-dde-unadvise.md) specifica un formato dati. Il formato zero indica al server di arrestare tutti i collegamenti per l'elemento specificato, anche se vengono stabiliti diversi collegamenti sensibili e ognuno usa un formato diverso.

Per terminare tutti i collegamenti per una conversazione, l'applicazione client invia al server un messaggio di annullamento dell' [**\_ \_ avviso DDE di WM**](wm-dde-unadvise.md) con un Atom elemento null. Il server determina se per la conversazione è attualmente stabilito almeno un collegamento. Se esiste un collegamento, il server invia al client un messaggio [**\_ \_ ACK DDE**](wm-dde-ack.md) positivo. il server non deve più inviare aggiornamenti nella conversazione. Se non esiste alcun collegamento, il server invia al client un **messaggio \_ \_ ACK DDE di WM** negativo.

## <a name="carrying-out-commands-in-a-server-application"></a>Esecuzione di comandi in un'applicazione server

Le applicazioni possono utilizzare il messaggio di [**\_ \_ esecuzione DDE di WM**](wm-dde-execute.md) per fare in modo che venga eseguito un determinato comando o una serie di comandi in un'altra applicazione. A tale scopo, il client invia al server un messaggio di **\_ \_ esecuzione DDE WM** contenente un handle a una stringa di comando, come illustrato nell'esempio seguente.


```
HRESULT hResult;
  
if (!(hCommand = GlobalAlloc(GMEM_MOVEABLE, 
        sizeof(szCommandString) + 1))) 
{
    return; 
}
if (!(lpCommand = GlobalLock(hCommand))) 
{ 
    GlobalFree(hCommand); 
    return; 
} 

hResult = StringCbCopy(lpCommand, sizeof(szCommandString), szCommandString);
if (hResult != S_OK)
{
// TODO: Write error handler.
 return;
}
 
GlobalUnlock(hCommand); 
if (!PostMessage(hwndServerDDE, 
        WM_DDE_EXECUTE, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_EXECUTE, 0, (UINT) hCommand))) 
{ 
    GlobalFree(hCommand); 
    FreeDDElParam(WM_DDE_EXECUTE, lParam); 
}
```



In questo esempio, il server tenta di eseguire la stringa di comando specificata. Se ha esito positivo, il server invia al client un [**messaggio \_ \_ ACK DDE**](wm-dde-ack.md) positivo. in caso contrario, invia un messaggio di **\_ \_ ACK DDE WM** negativo. Questo messaggio di **\_ \_ ACK DDE WM** riutilizza l'handle *hCommand* passato nel messaggio [**\_ \_ Execute DDE**](wm-dde-execute.md) originale di WM.

Se la stringa di esecuzione dei comandi del client richiede che il server termini, il server deve rispondere inviando un messaggio [**\_ \_ ACK DDE positivo WM**](wm-dde-ack.md) e quindi inviare un messaggio di [**\_ \_ terminazione DDE WM**](wm-dde-terminate.md) prima di terminare. Tutti gli altri comandi inviati con un messaggio di [**\_ \_ esecuzione DDE di WM**](wm-dde-execute.md) devono essere eseguiti in modo sincrono, ovvero il server deve inviare un messaggio **\_ \_ ACK DDE WM** solo dopo aver completato correttamente il comando.

## <a name="terminating-a-conversation"></a>Terminazione di una conversazione

Il client o il server può emettere un messaggio [**di \_ \_ terminazione DDE di WM**](wm-dde-terminate.md) per terminare una conversazione in qualsiasi momento. Analogamente, entrambe le applicazioni client e server devono essere preparate a ricevere questo messaggio in qualsiasi momento. Un'applicazione deve terminare tutte le conversazioni prima di arrestarsi.

Nell'esempio seguente, l'applicazione che termina la conversazione invia un messaggio [**di \_ \_ terminazione DDE di WM**](wm-dde-terminate.md) .


```
PostMessage(hwndServerDDE, WM_DDE_TERMINATE, 
    (WPARAM) hwndClientDDE, 0);
```



In questo modo si informa l'altra applicazione che l'applicazione mittente non invierà altri messaggi e il destinatario potrà chiudere la finestra. Il destinatario è previsto in tutti i casi per rispondere tempestivamente inviando un messaggio di [**\_ \_ terminazione del DDE WM**](wm-dde-terminate.md) . Il destinatario non deve inviare un messaggio [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) negativo, occupato o positivo.

Dopo che un'applicazione ha inviato il messaggio di [**\_ \_ terminazione del DDE WM**](wm-dde-terminate.md) al partner in una conversazione DDE, non deve rispondere ai messaggi provenienti da tale partner, perché il partner potrebbe avere eliminato definitivamente la finestra a cui verrebbe inviata la risposta.

Se un'applicazione riceve un messaggio DDE diverso da [**WM \_ DDE \_ Terminate**](wm-dde-terminate.md) dopo la pubblicazione **di \_ WM DDE \_ Terminate**, deve liberare tutti gli oggetti associati ai messaggi ricevuti, ad eccezione degli handle di dati per i [**\_ \_ dati DDE WM**](wm-dde-data.md) o i messaggi [**\_ \_ poke DDE di WM**](wm-dde-poke.md) per i quali **non** è impostato il membro **fRelease** .

Quando un'applicazione sta per terminare, deve terminare tutte le conversazioni DDE attive prima di completare l'elaborazione del messaggio [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) . Tuttavia, se un'applicazione non termina le conversazioni DDE attive, il sistema interromperà tutte le conversazioni DDE associate a una finestra quando la finestra viene distrutta. Nell'esempio seguente viene illustrato il modo in cui un'applicazione server termina tutte le conversazioni DDE.


```
void TerminateConversations(hwndServerDDE) 
HWND hwndServerDDE; 
{ 
    HWND hwndClientDDE; 
 
    // Terminate each active conversation. 
 
    while (hwndClientDDE = GetNextLink(hwndClientDDE)) 
    { 
        SendTerminate(hwndServerDDE, hwndClientDDE); 
    } 
    return; 
} 
 
BOOL AtLeastOneLinkActive(VOID) 
{ 
    return TRUE; 
} 
 
HWND GetNextLink(hwndDummy) 
    HWND hwndDummy; 
{ 
    return (HWND) 1; 
} 
 
VOID SendTerminate(HWND hwndServerDDE, HWND hwndClientDDE) 
{ 
    return; 
}
```



 

 