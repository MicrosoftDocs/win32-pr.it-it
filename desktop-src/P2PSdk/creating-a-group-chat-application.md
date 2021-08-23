---
description: Questo argomento fornisce esempi di codice pertinenti per i passaggi principali dello sviluppo di un'applicazione di chat con l'API di raggruppamento di peer, fornendo un contesto per ogni chiamata API.
ms.assetid: 47bb8606-0b7b-4e71-9d6f-c400d6a82e43
title: Creazione di un'applicazione di chat di gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb8f9458f8e01bea86e42f0cd976395e951bda52f13af46952479d5810e46c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011659"
---
# <a name="creating-a-group-chat-application"></a>Creazione di un'applicazione di chat di gruppo

Questo argomento fornisce esempi di codice pertinenti per i passaggi principali dello sviluppo di un'applicazione di chat con l'API di raggruppamento di peer, fornendo un contesto per ogni chiamata API. I comportamenti dell'interfaccia utente e la struttura complessiva dell'applicazione non sono inclusi.

> [!Note]  
> L'applicazione di esempio Peer Group Chat completa è disponibile in Peer SDK. Questo argomento fa riferimento alle funzioni fornite all'interno dell'esempio.

 

## <a name="initializing-a-group"></a>Inizializzazione di un gruppo

Il primo passaggio durante la creazione di un'applicazione di chat consiste nell'inizializzare l'infrastruttura di raggruppamento peer chiamando [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) con la versione più recente supportata. In questo caso, **PEER \_ GROUP \_ VERSION** verrà definito nel file di intestazione dell'applicazione. La versione effettivamente supportata dall'infrastruttura viene restituita in **peerVersion.**


```C++
    PEER_VERSION_DATA peerVersion;

    hr = PeerGroupStartup(PEER_GROUP_VERSION, &peerVersion);
    if (FAILED(hr))
    {
        return hr;
    }
```



## <a name="creating-a-group"></a>Creazione di un gruppo

Un'applicazione di chat deve essere in grado di creare un gruppo peer se non è disponibile alcun gruppo per l'aggiunta o se l'utente dell'applicazione vuole crearne uno nuovo. A tale scopo, è necessario creare una struttura [**PEER \_ GROUP \_ PROPERTIES**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) e popolarla con le impostazioni iniziali per il gruppo, inclusi il classificatore per il gruppo peer, il nome descrittivo, il nome peer dell'autore e la durata della presenza. Dopo aver popolato questa struttura, passarla a [**PeerGroupCreate.**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)


```C++
//-----------------------------------------------------------------------------
// Function: CreateGroup
//
// Purpose:  Creates a new group with the friendly name.
//
// Returns:  HRESULT
//
HRESULT CreateGroup(PCWSTR pwzName, PCWSTR pwzIdentity)
{
    HRESULT hr = S_OK;
    PEER_GROUP_PROPERTIES props = {0};

    if (SUCCEEDED(hr))
    {
        if ((NULL == pwzName) || (0 == *pwzName))
        {
            hr = E_INVALIDARG;
            DisplayHrError(L"Please enter a group name.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        CleanupGroup( );

        props.dwSize = sizeof(props);
        props.pwzClassifier = L"SampleChatGroup";
        props.pwzFriendlyName = (PWSTR) pwzName;
        props.pwzCreatorPeerName = (PWSTR) pwzIdentity;

        hr = PeerGroupCreate(&props, &g_hGroup);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to create a new group.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = PrepareToChat( );
    }

    return hr;
}
```



## <a name="issuing-invitations"></a>Emissione di inviti

Quando si invia un invito, è necessario ottenere i gmc degli invitati. Questi valori possono essere ottenuti chiamando [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) sull'invitato con il nome dell'identità. In caso di esito positivo, le informazioni sull'identità (il codice XML che contiene il certificato con codifica Base 64 con la chiave pubblica RSA) vengono scritte in un percorso esterno (un file, in questo esempio) in cui il mittente dell'invito può ottenerlo e usarlo per creare un invito.

A questo punto, deve essere stabilito un meccanismo per il recapito dell'invito all'invitato. Può trattarsi di un messaggio di posta elettronica o di un altro metodo sicuro di scambio di file. Nell'esempio seguente l'invito viene scritto in un file che può quindi essere trasferito al computer dell'invitato.


```C++
//-----------------------------------------------------------------------------
// Function: SaveIdentityInfo
//
// Purpose:  Saves the information for an identity to a file.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT SaveIdentityInfo(PCWSTR pwzIdentity, PCWSTR pwzFile)
{
    PWSTR pwzXML = NULL;
    HRESULT hr = PeerIdentityGetXML(pwzIdentity, &pwzXML);

    if (FAILED(hr))
    {
        DisplayHrError(L"Unable to retrieve the XML data for the identity.", hr);
    }
    else
    {
        FILE *fp = NULL;
        errno_t err = 0;

        err = _wfopen_s(&fp, pwzFile, L"wb");
        if (err != 0)
        {
            hr = E_FAIL;
            DisplayHrError(L"Please choose a valid path", hr);
        }
        else
        {
            if (fputws(pwzXML, fp) == WEOF)
            {
                hr = E_FAIL;
                DisplayHrError(L"End of file error.", hr);
            }
            fclose(fp);
        }

        PeerFreeData(pwzXML);
    }

    return hr;
}
```



Anche gli inviti, come le identità, vengono emessi esternamente. In questo esempio l'invito viene scritto in un file con **fputws** in cui l'invitato può ottenerlo e usarlo quando chiama [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).


```C++
//-----------------------------------------------------------------------------
// Function: CreateInvitation
//
// Purpose:  Creates an invitation file for an identity.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT CreateInvitation(PCWSTR wzIdentityInfoPath, PCWSTR wzInvitationPath)
{
    HRESULT hr = S_OK;
    WCHAR wzIdentityInfo[MAX_INVITATION] = {0};
    PWSTR pwzInvitation = NULL;
    errno_t  err  = 0;
    FILE *file = NULL;
        
    err = _wfopen_s(&file, wzIdentityInfoPath, L"rb");
    if (err != 0)
    {
        hr = E_FAIL;
        DisplayHrError(L"Please choose a valid path to the identity information file.", hr);
    }
    else
    {
        fread(wzIdentityInfo, sizeof(WCHAR), MAX_INVITATION, file);
        if (ferror(file))
        {
            hr = E_FAIL;
            DisplayHrError(L"File read error occurred.", hr);
        }
        fclose(file);
    }

    if (SUCCEEDED(hr))
    {
        ULONGLONG ulExpire; // adjust time using this structure
        GetSystemTimeAsFileTime((FILETIME *)&ulExpire);

        // 15days in 100 nanoseconds resolution
        ulExpire += ((ULONGLONG) (60 * 60 * 24 * 15)) * ((ULONGLONG)1000*1000*10);

        hr = PeerGroupCreateInvitation(g_hGroup, wzIdentityInfo, (FILETIME*)&ulExpire, 1, (PEER_ROLE_ID*) &PEER_GROUP_ROLE_MEMBER, &pwzInvitation);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to create the invitation.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        err = _wfopen_s(&file, wzInvitationPath, L"wb");
        if (err != 0)
        {
            hr = E_FAIL;
            DisplayHrError(L"Please choose a valid path to the invitation file.", hr);
        }
        else
        {
            if (fputws(pwzInvitation, file) == WEOF)
            {
                hr = E_FAIL;
                DisplayHrError(L"End of file error.", hr);
            }
            fclose(file);
        }
    }

    PeerFreeData(pwzInvitation);
    return hr;
}
```



## <a name="joining-a-peer-group"></a>Aggiunta di un gruppo peer

Se il peer sta tentando di partecipare a un gruppo peer creato da un altro peer, sarà necessario un invito da tale peer. Gli inviti vengono recapitati da un processo esterno o da un'applicazione all'invitato e salvati in un file locale, specificato nell'esempio seguente *come pwzFileName*. Il BLOB XML di invito viene letto dal file in **wzInvitation** e passato a [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).


```C++
//-----------------------------------------------------------------------------
// Function: JoinGroup
//
// Purpose:  Uses the invitation to join a group with a specific identity.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT JoinGroup(PCWSTR pwzIdentity, PCWSTR pwzFileName)
{
    HRESULT hr = S_OK;
    WCHAR wzInvitation[MAX_INVITATION] = {0};
    FILE        *file = NULL;
    errno_t     err;

    err = _wfopen_s(&file, pwzFileName, L"rb");
    if (err !=  0)
    {
        hr = E_FAIL;
        DisplayHrError(L"Error opening group invitation file", hr);
        return hr;
    }
    else
    {
        fread(wzInvitation, sizeof(WCHAR), MAX_INVITATION, file);
        if (ferror(file))
        {
            hr = E_FAIL;
            DisplayHrError(L"File read error occurred.", hr);
        }
        fclose(file);

        hr = PeerGroupJoin(pwzIdentity, wzInvitation, NULL, &g_hGroup);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to join group.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = PrepareToChat( );
    }

    return hr;
}
```



## <a name="register-for-peer-events"></a>Eseguire la registrazione per gli eventi peer

Prima di connettersi, è necessario registrarsi per ogni evento peer pertinente all'applicazione. Nell'esempio seguente si registra per gli eventi seguenti:

-   RECORD \_ DI EVENTI DEL GRUPPO DI PEER \_ \_ \_ MODIFICATO. Poiché i record verranno usati per contenere messaggi di chat pubblici, l'applicazione deve ricevere una notifica ogni volta che ne viene aggiunta una nuova. Quando viene ricevuto questo evento peer, i dati dell'evento espongono il record con il messaggio di chat. Le applicazioni devono registrarsi solo per i tipi di record che intendono gestire direttamente.
-   MEMBRO EVENTO GRUPPO PEER \_ \_ \_ \_ MODIFICATO. L'applicazione deve ricevere una notifica quando i membri si uniscono o lasciano il gruppo di peer in modo che l'elenco dei partecipanti possa essere aggiornato di conseguenza.
-   STATO \_ \_ DELL'EVENTO \_ DEL GRUPPO PEER \_ MODIFICATO. Le modifiche apportate allo stato del gruppo di peer devono essere comunicate all'applicazione. Un membro del gruppo peer viene considerato disponibile all'interno del gruppo peer solo quando il relativo stato indica che è connesso al gruppo, sincronizzato con il database dei record del gruppo peer e attivamente in ascolto degli aggiornamenti dei record.
-   CONNESSIONE \_ DIRETTA A EVENTI DEL GRUPPO \_ \_ \_ PEER. I messaggi privati tra due membri e gli scambi di dati devono essere eseguiti tramite una connessione diretta, quindi l'applicazione deve essere in grado di gestire le richieste di connessione diretta.
-   DATI \_ IN INGRESSO DEGLI EVENTI DEL GRUPPO \_ \_ \_ PEER. Dopo l'avvio di una connessione diretta, questo evento peer avvisa l'applicazione che è stato ricevuto un messaggio privato.


```C++
//-----------------------------------------------------------------------------
// Function: RegisterForEvents
//
// Purpose:  Registers the EventCallback function so it will be called for only
//           those events that are specified.
//
// Returns:  HRESULT
//
HRESULT RegisterForEvents(void)
{
    HRESULT hr = S_OK;
    PEER_GROUP_EVENT_REGISTRATION regs[] = {
        { PEER_GROUP_EVENT_RECORD_CHANGED, &RECORD_TYPE_CHAT_MESSAGE },
        { PEER_GROUP_EVENT_MEMBER_CHANGED, 0 },
        { PEER_GROUP_EVENT_STATUS_CHANGED, 0 },
        { PEER_GROUP_EVENT_DIRECT_CONNECTION, &DATA_TYPE_WHISPER_MESSAGE },
        { PEER_GROUP_EVENT_INCOMING_DATA, 0 },
    };

    g_hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (g_hEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    else
    {
        hr = PeerGroupRegisterEvent(g_hGroup, g_hEvent, celems(regs), regs,  &g_hPeerEvent);
    }

    if (SUCCEEDED(hr))
    {
        if (!RegisterWaitForSingleObject(&g_hWait, g_hEvent, EventCallback, NULL, INFINITE, WT_EXECUTEDEFAULT))
        {
            hr = E_UNEXPECTED;
        }
    }

    return hr;
}
```



## <a name="connecting-to-a-peer-group"></a>Connessione a un gruppo peer

Dopo aver creato o aggiunto il gruppo e aver registrato gli eventi appropriati, è possibile passare alla modalità online e avviare una sessione di chat attiva. A tale scopo, chiamare [**PeerGroupConnect e**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) passare l'handle di gruppo ottenuto da [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) [**o PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin). Dopo aver chiamato questo metodo, i messaggi di chat verranno ricevuti come eventi PEER \_ GROUP \_ EVENT RECORD \_ \_ CHANGED.

## <a name="obtaining-a-list-of-peer-group-members"></a>Recupero di un elenco di membri del gruppo peer

Ottenere un elenco di membri connessi al gruppo peer è semplice: chiamare [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) per recuperare l'elenco dei membri del gruppo e quindi chiamare in modo iterativo [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) finché non vengono recuperati tutti i membri. È consigliabile [**chiamare PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) dopo l'elaborazione di ogni struttura del membro ed è necessario chiudere l'enumerazione chiamando [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) al termine dell'elaborazione.


```C++
//-----------------------------------------------------------------------------
// Function: UpdateParticipantList
//
// Purpose:  Update the list of partipants.
//
// Returns:  nothing
//
void UpdateParticipantList(void)
{
    HRESULT          hr = S_OK;
    HPEERENUM        hPeerEnum = NULL;
    PEER_MEMBER   ** ppMember = NULL;

    ClearParticipantList( );
    if (NULL == g_hGroup)
    {
        return;
    }

    // Retrieve only the members currently present in the group.
    hr = PeerGroupEnumMembers(g_hGroup, PEER_MEMBER_PRESENT, NULL, &hPeerEnum);
    if (SUCCEEDED(hr))
    {
        while (SUCCEEDED(hr))
        {
            ULONG cItem = 1;
            hr = PeerGetNextItem(hPeerEnum, &cItem, (PVOID **) &ppMember);
            if (SUCCEEDED(hr))
            {
                if (0 == cItem)
                {
                    PeerFreeData(ppMember);
                    break;
                }
            }

            if (SUCCEEDED(hr))
            {
                if (0 != ((*ppMember)->dwFlags & PEER_MEMBER_PRESENT))
                {
                    AddParticipantName((*ppMember)->pwzIdentity, (*ppMember)->pCredentialInfo->pwzFriendlyName);
                }
                PeerFreeData(ppMember);
            }
        }

        PeerEndEnumeration(hPeerEnum);
    }
}
```



## <a name="sending-a-chat-message"></a>Invio di un messaggio di chat

In questo esempio viene inviato un messaggio di chat inserendolo nel campo **dati** di una [**struttura PEER \_ RECORD.**](/windows/desktop/api/P2P/ns-p2p-peer_record) Il record viene aggiunto ai record del gruppo peer chiamando [**PeerGroupAddRecord,**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)che lo pubblicherà e genererà l'evento PEER GROUP EVENT RECORD CHANGED in tutti i peer che partecipano al \_ \_ gruppo \_ \_ peer.


```C++
//-----------------------------------------------------------------------------
// Function: AddChatRecord
//
// Purpose:  This adds a new chat message record to the group.
//
// Returns:  HRESULT
//
HRESULT AddChatRecord(PCWSTR pwzMessage)
{
    HRESULT     hr = S_OK;
    PEER_RECORD record = {0};
    GUID        idRecord;
    ULONGLONG   ulExpire;
    ULONG cch = (ULONG) wcslen(pwzMessage);

    GetSystemTimeAsFileTime((FILETIME *) &ulExpire);

    // Calculate a 2 minute expiration time in 100 nanosecond resolution
    ulExpire += ((ULONGLONG) 60 * 2) * ((ULONGLONG)1000*1000*10);

    // Set up the record
    record.dwSize = sizeof(record);
    record.data.cbData = (cch+1) * sizeof(WCHAR);
    record.data.pbData = (PBYTE) pwzMessage;
    memcpy(&record.ftExpiration, &ulExpire, sizeof(ulExpire));

    PeerGroupUniversalTimeToPeerTime(g_hGroup, &record.ftExpiration, &record.ftExpiration);

    // Set the record type GUID
    record.type = RECORD_TYPE_CHAT_MESSAGE;

    // Add the record to the database
    hr = PeerGroupAddRecord(g_hGroup, &record, &idRecord);
    if (FAILED(hr))
    {
        DisplayHrError(L"Failed to add a chat record to the group.", hr);
    }

    return hr;
}
```



## <a name="receiving-a-chat-message"></a>Ricezione di un messaggio di chat

Per ricevere il messaggio di chat, creare una funzione di callback per l'evento PEER GROUP EVENT RECORD CHANGED che chiama una \_ \_ funzione simile alla \_ \_ seguente. Il record viene ottenuto chiamando [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) sui dati dell'evento ricevuti da una precedente chiamata a [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) nella funzione di callback. Il messaggio di chat viene archiviato nel **campo dati** di questo record.


```C++
//-----------------------------------------------------------------------------
// Function: ProcessRecordChanged
//
// Purpose:  Processes the PEER_GROUP_EVENT_RECORD_CHANGED event.
//
// Returns:  nothing
//
void ProcessRecordChanged(PEER_EVENT_RECORD_CHANGE_DATA * pData)
{
    switch (pData->changeType)
    {
        case PEER_RECORD_ADDED:
            if (IsEqualGUID(&pData->recordType, &RECORD_TYPE_CHAT_MESSAGE))
            {
                PEER_RECORD * pRecord = {0};
                HRESULT hr = PeerGroupGetRecord(g_hGroup, &pData->recordId, &pRecord);
                if (SUCCEEDED(hr))
                {
                    DisplayChatMessage(pRecord->pwzCreatorId, (PCWSTR) pRecord->data.pbData);
                    PeerFreeData(pRecord);
                }
            }
            break;

        case PEER_RECORD_UPDATED:
        case PEER_RECORD_DELETED:
        case PEER_RECORD_EXPIRED:
            break;

        default:
            break;
    }
}
```



 

 



