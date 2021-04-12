---
description: In questo argomento vengono forniti esempi di codice rilevanti per i passaggi principali dello sviluppo di un'applicazione di chat con l'API di raggruppamento peer, fornendo un contesto per ogni chiamata API.
ms.assetid: 47bb8606-0b7b-4e71-9d6f-c400d6a82e43
title: Creazione di un'applicazione di chat di gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676d4e9913934024df3131c0f965a5d85477d148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345541"
---
# <a name="creating-a-group-chat-application"></a>Creazione di un'applicazione di chat di gruppo

In questo argomento vengono forniti esempi di codice rilevanti per i passaggi principali dello sviluppo di un'applicazione di chat con l'API di raggruppamento peer, fornendo un contesto per ogni chiamata API. I comportamenti dell'interfaccia utente e la struttura complessiva dell'applicazione non sono inclusi.

> [!Note]  
> L'applicazione di esempio per la chat del gruppo peer completa viene fornita nell'SDK peer. Questo argomento fa riferimento alle funzioni fornite nell'esempio.

 

## <a name="initializing-a-group"></a>Inizializzazione di un gruppo

Il primo passaggio per la creazione di un'applicazione di chat consiste nell'inizializzare l'infrastruttura di raggruppamento peer chiamando [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) con la versione più recente supportata. In questo caso, **la \_ \_ versione del gruppo peer** verrà definita nel file di intestazione dell'applicazione. La versione effettivamente supportata dall'infrastruttura viene restituita in **peerVersion**.


```C++
    PEER_VERSION_DATA peerVersion;

    hr = PeerGroupStartup(PEER_GROUP_VERSION, &peerVersion);
    if (FAILED(hr))
    {
        return hr;
    }
```



## <a name="creating-a-group"></a>Creazione di un gruppo

Un'applicazione di chat deve essere in grado di creare un gruppo peer se non sono disponibili gruppi da unire o se l'utente dell'applicazione vuole crearne uno nuovo. A tale scopo, è necessario creare una struttura di [**\_ \_ proprietà del gruppo peer**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) e popolarla con le impostazioni iniziali per il gruppo, incluso il classificatore per il gruppo peer, il nome descrittivo, il nome peer del creatore e la durata della presenza. Una volta popolata questa struttura, viene passata a [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).


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



## <a name="issuing-invitations"></a>Invio di inviti

Quando si invia un invito, è necessario ottenere il GMCs degli invitati. Questi possono essere ottenuti chiamando [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) nell'invito con il nome dell'identità. In caso di esito positivo, le informazioni sull'identità (il codice XML che contiene il certificato con codifica base 64 con la chiave pubblica RSA) vengono scritte in un percorso esterno, ovvero un file, in questo esempio, in cui il mittente può ottenerlo e utilizzarlo per creare un invito.

A questo punto, è necessario stabilire un meccanismo per il recapito dell'invito all'invito. Questo può essere un messaggio di posta elettronica o un altro metodo sicuro per lo scambio di file. Nell'esempio seguente l'invito viene scritto in un file che può quindi essere trasferito al computer dell'invito.


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



Gli inviti, come le identità, vengono emessi anche esternamente. In questo esempio, l'invito viene scritto in un file con **fputws** in cui l'invito può ottenerlo e usarlo quando chiama [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).


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



## <a name="joining-a-peer-group"></a>Aggiunta a un gruppo peer

Se il peer tenta di partecipare a un gruppo peer creato da un altro peer, sarà necessario un invito da tale peer. Gli inviti vengono recapitati da un processo esterno o da un'applicazione all'invito e salvati in un file locale, specificato nell'esempio seguente come *pwzFileName*. Il BLOB XML dell'invito viene letto dal file in **wzInvitation** e passato a [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).


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



## <a name="register-for-peer-events"></a>Registra per eventi peer

Prima di connettersi, è necessario registrarsi per ogni evento peer pertinente per l'applicazione. Nell'esempio seguente si esegue la registrazione per gli eventi seguenti:

-   il record dell'evento del gruppo PEER è stato \_ \_ \_ \_ modificato. Poiché i record verranno utilizzati per contenere messaggi di chat pubblici, l'applicazione deve ricevere una notifica ogni volta che ne viene aggiunto uno nuovo. Quando viene ricevuto questo evento peer, i dati dell'evento espongono il record con il messaggio di chat. Le applicazioni devono essere registrate solo per i tipi di record che hanno intenzione di gestire direttamente.
-   \_membro dell'evento del gruppo peer \_ \_ \_ modificato. L'applicazione deve ricevere una notifica quando i membri partecipano o lasciano il gruppo peer, in modo che l'elenco dei partecipanti possa essere aggiornato di conseguenza.
-   \_ \_ stato evento gruppo \_ peer \_ modificato. Le modifiche allo stato del gruppo peer devono essere comunicate all'applicazione. Un membro del gruppo peer viene considerato disponibile all'interno del gruppo peer solo quando il relativo stato indica che è connesso al gruppo, sincronizzato con il database di record del gruppo peer e in ascolto attivo per registrare gli aggiornamenti.
-   \_connessione diretta agli eventi del gruppo peer \_ \_ \_ . I messaggi privati tra due membri e gli scambi di dati devono essere eseguiti su una connessione diretta, quindi l'applicazione deve essere in grado di gestire le richieste di connessione diretta.
-   \_ \_ \_ dati in ingresso evento gruppo peer \_ . Dopo l'avvio di una connessione diretta, questo evento peer segnala all'applicazione che è stato ricevuto un messaggio privato.


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

Una volta creato o aggiunto al gruppo e registrato per gli eventi appropriati, è possibile passare alla modalità online e avviare una sessione di chat attiva. A tale scopo, chiamare [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) e passare l'handle di gruppo ottenuto da [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) o [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin). Al termine della chiamata, i messaggi di chat verranno ricevuti come \_ eventi di modifica del record dell'evento del gruppo peer \_ \_ \_ .

## <a name="obtaining-a-list-of-peer-group-members"></a>Ottenere un elenco di membri del gruppo peer

Il recupero di un elenco di membri connessi al gruppo peer è semplice: chiamare [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) per recuperare l'elenco dei membri del gruppo e quindi chiamare in modo iterativo [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) fino a quando non vengono recuperati tutti i membri. È necessario chiamare [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) dopo aver elaborato ogni struttura del membro ed è necessario chiudere l'enumerazione chiamando [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) al termine dell'elaborazione.


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

In questo esempio viene inviato un messaggio di chat inserendolo nel campo **dati** di una struttura di [**\_ record peer**](/windows/desktop/api/P2P/ns-p2p-peer_record) . Il record viene aggiunto ai record del gruppo peer chiamando [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord), che lo pubblicherà e genererà l' \_ evento di modifica del record di eventi del gruppo peer \_ \_ \_ su tutti i peer che partecipano al gruppo peer.


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

Per ricevere il messaggio di chat, creare una funzione di callback per l' \_ evento di modifica del record di eventi del gruppo peer \_ \_ \_ che chiama una funzione simile alla seguente. Il record viene ottenuto chiamando [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) sui dati dell'evento ricevuti da una precedente chiamata a [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) nella funzione di callback. Il messaggio di chat viene archiviato nel campo **dati** di questo record.


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



 

 



