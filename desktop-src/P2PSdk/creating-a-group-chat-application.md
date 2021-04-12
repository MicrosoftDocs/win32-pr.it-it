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
# <a name="creating-a-group-chat-application"></a><span data-ttu-id="5c4ff-103">Creazione di un'applicazione di chat di gruppo</span><span class="sxs-lookup"><span data-stu-id="5c4ff-103">Creating a Group Chat Application</span></span>

<span data-ttu-id="5c4ff-104">In questo argomento vengono forniti esempi di codice rilevanti per i passaggi principali dello sviluppo di un'applicazione di chat con l'API di raggruppamento peer, fornendo un contesto per ogni chiamata API.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-104">This topic provides relevant code samples for the major steps of developing a chat application with the Peer Grouping API, providing a context for each API call.</span></span> <span data-ttu-id="5c4ff-105">I comportamenti dell'interfaccia utente e la struttura complessiva dell'applicazione non sono inclusi.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-105">UI behaviors and overall application structure are not included.</span></span>

> [!Note]  
> <span data-ttu-id="5c4ff-106">L'applicazione di esempio per la chat del gruppo peer completa viene fornita nell'SDK peer.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-106">The complete Peer Group Chat sample application is provided in the Peer SDK.</span></span> <span data-ttu-id="5c4ff-107">Questo argomento fa riferimento alle funzioni fornite nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-107">This topic references functions provided within the sample.</span></span>

 

## <a name="initializing-a-group"></a><span data-ttu-id="5c4ff-108">Inizializzazione di un gruppo</span><span class="sxs-lookup"><span data-stu-id="5c4ff-108">Initializing a Group</span></span>

<span data-ttu-id="5c4ff-109">Il primo passaggio per la creazione di un'applicazione di chat consiste nell'inizializzare l'infrastruttura di raggruppamento peer chiamando [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) con la versione più recente supportata.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-109">The first step when constructing a chat application is to initialize the Peer Grouping Infrastructure by calling [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) with the highest supported version.</span></span> <span data-ttu-id="5c4ff-110">In questo caso, **la \_ \_ versione del gruppo peer** verrà definita nel file di intestazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-110">In this case, **PEER\_GROUP\_VERSION** will be defined in the application header file.</span></span> <span data-ttu-id="5c4ff-111">La versione effettivamente supportata dall'infrastruttura viene restituita in **peerVersion**.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-111">The version actually supported by the infrastructure is returned in **peerVersion**.</span></span>


```C++
    PEER_VERSION_DATA peerVersion;

    hr = PeerGroupStartup(PEER_GROUP_VERSION, &peerVersion);
    if (FAILED(hr))
    {
        return hr;
    }
```



## <a name="creating-a-group"></a><span data-ttu-id="5c4ff-112">Creazione di un gruppo</span><span class="sxs-lookup"><span data-stu-id="5c4ff-112">Creating a Group</span></span>

<span data-ttu-id="5c4ff-113">Un'applicazione di chat deve essere in grado di creare un gruppo peer se non sono disponibili gruppi da unire o se l'utente dell'applicazione vuole crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-113">A chat application must be able to create a peer group if no group is available to join, or if the application user wants to create a new one.</span></span> <span data-ttu-id="5c4ff-114">A tale scopo, è necessario creare una struttura di [**\_ \_ proprietà del gruppo peer**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) e popolarla con le impostazioni iniziali per il gruppo, incluso il classificatore per il gruppo peer, il nome descrittivo, il nome peer del creatore e la durata della presenza.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-114">To do this, you must create a [**PEER\_GROUP\_PROPERTIES**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) structure and populate it with the initial settings for the group, including the classifier for the peer group, the friendly name, the creator's peer name, and the presence lifetime.</span></span> <span data-ttu-id="5c4ff-115">Una volta popolata questa struttura, viene passata a [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).</span><span class="sxs-lookup"><span data-stu-id="5c4ff-115">Once this structure has been populated, you pass it to [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).</span></span>


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



## <a name="issuing-invitations"></a><span data-ttu-id="5c4ff-116">Invio di inviti</span><span class="sxs-lookup"><span data-stu-id="5c4ff-116">Issuing Invitations</span></span>

<span data-ttu-id="5c4ff-117">Quando si invia un invito, è necessario ottenere il GMCs degli invitati.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-117">When issuing an invitation, the GMCs of the invitees must be obtained.</span></span> <span data-ttu-id="5c4ff-118">Questi possono essere ottenuti chiamando [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) nell'invito con il nome dell'identità.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-118">These can obtained by calling [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) on the invitee with their identity name.</span></span> <span data-ttu-id="5c4ff-119">In caso di esito positivo, le informazioni sull'identità (il codice XML che contiene il certificato con codifica base 64 con la chiave pubblica RSA) vengono scritte in un percorso esterno, ovvero un file, in questo esempio, in cui il mittente può ottenerlo e utilizzarlo per creare un invito.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-119">If successful, the identity information (the XML that contains the base-64 encoded certificate with the RSA public key) is written to an external location (a file, in this sample) where the inviter can obtain it and use it to create an invitation.</span></span>

<span data-ttu-id="5c4ff-120">A questo punto, è necessario stabilire un meccanismo per il recapito dell'invito all'invito.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-120">At this point, a mechanism for the delivery of the invitation to the invitee must be established.</span></span> <span data-ttu-id="5c4ff-121">Questo può essere un messaggio di posta elettronica o un altro metodo sicuro per lo scambio di file.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-121">This can be email or another secure method of file exchange.</span></span> <span data-ttu-id="5c4ff-122">Nell'esempio seguente l'invito viene scritto in un file che può quindi essere trasferito al computer dell'invito.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-122">In the sample below, the invitation is written to a file which can then be transferred to the invitee's computer.</span></span>


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



<span data-ttu-id="5c4ff-123">Gli inviti, come le identità, vengono emessi anche esternamente.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-123">Invitations, like identities, are also issued externally.</span></span> <span data-ttu-id="5c4ff-124">In questo esempio, l'invito viene scritto in un file con **fputws** in cui l'invito può ottenerlo e usarlo quando chiama [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span><span class="sxs-lookup"><span data-stu-id="5c4ff-124">In this example, the invitation is written to a file with **fputws** where the invitee can obtain it and use it when it calls [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span>


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



## <a name="joining-a-peer-group"></a><span data-ttu-id="5c4ff-125">Aggiunta a un gruppo peer</span><span class="sxs-lookup"><span data-stu-id="5c4ff-125">Joining a Peer Group</span></span>

<span data-ttu-id="5c4ff-126">Se il peer tenta di partecipare a un gruppo peer creato da un altro peer, sarà necessario un invito da tale peer.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-126">If the peer is attempting to join a peer group created by another peer, it will need an invitation from that peer.</span></span> <span data-ttu-id="5c4ff-127">Gli inviti vengono recapitati da un processo esterno o da un'applicazione all'invito e salvati in un file locale, specificato nell'esempio seguente come *pwzFileName*.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-127">Invitations are delivered by an external process or application to the invitee and saved to a local file, specified in the sample below as *pwzFileName*.</span></span> <span data-ttu-id="5c4ff-128">Il BLOB XML dell'invito viene letto dal file in **wzInvitation** e passato a [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span><span class="sxs-lookup"><span data-stu-id="5c4ff-128">The invitation XML blob is read from the file into **wzInvitation** and passed to [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span>


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



## <a name="register-for-peer-events"></a><span data-ttu-id="5c4ff-129">Registra per eventi peer</span><span class="sxs-lookup"><span data-stu-id="5c4ff-129">Register for Peer Events</span></span>

<span data-ttu-id="5c4ff-130">Prima di connettersi, è necessario registrarsi per ogni evento peer pertinente per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-130">Before connecting, you should register for every peer event pertinent to the application.</span></span> <span data-ttu-id="5c4ff-131">Nell'esempio seguente si esegue la registrazione per gli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="5c4ff-131">In the example below, you register for the following events:</span></span>

-   <span data-ttu-id="5c4ff-132">il record dell'evento del gruppo PEER è stato \_ \_ \_ \_ modificato.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-132">PEER\_GROUP\_EVENT\_RECORD\_CHANGED.</span></span> <span data-ttu-id="5c4ff-133">Poiché i record verranno utilizzati per contenere messaggi di chat pubblici, l'applicazione deve ricevere una notifica ogni volta che ne viene aggiunto uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-133">Since records will be used to contain public chat messages, the application must be notified every time a new one is added.</span></span> <span data-ttu-id="5c4ff-134">Quando viene ricevuto questo evento peer, i dati dell'evento espongono il record con il messaggio di chat.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-134">When this peer event is received, the event data exposes the record with the chat message.</span></span> <span data-ttu-id="5c4ff-135">Le applicazioni devono essere registrate solo per i tipi di record che hanno intenzione di gestire direttamente.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-135">Applications should only register for those record types they intend to handle directly.</span></span>
-   <span data-ttu-id="5c4ff-136">\_membro dell'evento del gruppo peer \_ \_ \_ modificato.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-136">PEER\_GROUP\_EVENT\_MEMBER\_CHANGED.</span></span> <span data-ttu-id="5c4ff-137">L'applicazione deve ricevere una notifica quando i membri partecipano o lasciano il gruppo peer, in modo che l'elenco dei partecipanti possa essere aggiornato di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-137">The application must be notified when members join or leave the peer group so the list of participants can be updated accordingly.</span></span>
-   <span data-ttu-id="5c4ff-138">\_ \_ stato evento gruppo \_ peer \_ modificato.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-138">PEER\_GROUP\_EVENT\_STATUS\_CHANGED.</span></span> <span data-ttu-id="5c4ff-139">Le modifiche allo stato del gruppo peer devono essere comunicate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-139">Changes to the peer group status must be conveyed to the application.</span></span> <span data-ttu-id="5c4ff-140">Un membro del gruppo peer viene considerato disponibile all'interno del gruppo peer solo quando il relativo stato indica che è connesso al gruppo, sincronizzato con il database di record del gruppo peer e in ascolto attivo per registrare gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-140">A peer group member is only considered to be available within the peer group when its status indicates that it is connected to the group, synchronized with the peer group record database, and actively listening to record updates.</span></span>
-   <span data-ttu-id="5c4ff-141">\_connessione diretta agli eventi del gruppo peer \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5c4ff-141">PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION.</span></span> <span data-ttu-id="5c4ff-142">I messaggi privati tra due membri e gli scambi di dati devono essere eseguiti su una connessione diretta, quindi l'applicazione deve essere in grado di gestire le richieste di connessione diretta.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-142">Private messages between two members and exchanges of data must be conducted over a direct connection, so the application must be able to handle direct connection requests.</span></span>
-   <span data-ttu-id="5c4ff-143">\_ \_ \_ dati in ingresso evento gruppo peer \_ .</span><span class="sxs-lookup"><span data-stu-id="5c4ff-143">PEER\_GROUP\_EVENT\_INCOMING\_DATA.</span></span> <span data-ttu-id="5c4ff-144">Dopo l'avvio di una connessione diretta, questo evento peer segnala all'applicazione che è stato ricevuto un messaggio privato.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-144">After a direct connection is initiated, this peer event alerts the application that a private message has been received.</span></span>


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



## <a name="connecting-to-a-peer-group"></a><span data-ttu-id="5c4ff-145">Connessione a un gruppo peer</span><span class="sxs-lookup"><span data-stu-id="5c4ff-145">Connecting to a Peer Group</span></span>

<span data-ttu-id="5c4ff-146">Una volta creato o aggiunto al gruppo e registrato per gli eventi appropriati, è possibile passare alla modalità online e avviare una sessione di chat attiva.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-146">Having either created or joined the group and registered for the appropriate events, it's time to go online and begin an active chat session.</span></span> <span data-ttu-id="5c4ff-147">A tale scopo, chiamare [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) e passare l'handle di gruppo ottenuto da [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) o [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span><span class="sxs-lookup"><span data-stu-id="5c4ff-147">To do this, you call [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) and pass in the group handle obtained from [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) or [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span> <span data-ttu-id="5c4ff-148">Al termine della chiamata, i messaggi di chat verranno ricevuti come \_ eventi di modifica del record dell'evento del gruppo peer \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5c4ff-148">After calling this, chat messages will be received as PEER\_GROUP\_EVENT\_RECORD\_CHANGED events.</span></span>

## <a name="obtaining-a-list-of-peer-group-members"></a><span data-ttu-id="5c4ff-149">Ottenere un elenco di membri del gruppo peer</span><span class="sxs-lookup"><span data-stu-id="5c4ff-149">Obtaining a List of Peer Group Members</span></span>

<span data-ttu-id="5c4ff-150">Il recupero di un elenco di membri connessi al gruppo peer è semplice: chiamare [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) per recuperare l'elenco dei membri del gruppo e quindi chiamare in modo iterativo [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) fino a quando non vengono recuperati tutti i membri.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-150">Obtaining a list of members connected to the peer group is simple: call [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) to retrieve the list of group members, and then iteratively call [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) until all members are retrieved.</span></span> <span data-ttu-id="5c4ff-151">È necessario chiamare [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) dopo aver elaborato ogni struttura del membro ed è necessario chiudere l'enumerazione chiamando [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) al termine dell'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-151">You should call [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) after you process each member structure, and you must close the enumeration by calling [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) when processing is complete.</span></span>


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



## <a name="sending-a-chat-message"></a><span data-ttu-id="5c4ff-152">Invio di un messaggio di chat</span><span class="sxs-lookup"><span data-stu-id="5c4ff-152">Sending a Chat Message</span></span>

<span data-ttu-id="5c4ff-153">In questo esempio viene inviato un messaggio di chat inserendolo nel campo **dati** di una struttura di [**\_ record peer**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="5c4ff-153">In this example, a chat message is sent by placing it in the **data** field of a [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span> <span data-ttu-id="5c4ff-154">Il record viene aggiunto ai record del gruppo peer chiamando [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord), che lo pubblicherà e genererà l' \_ evento di modifica del record di eventi del gruppo peer \_ \_ \_ su tutti i peer che partecipano al gruppo peer.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-154">The record is added to the peer group records by calling [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord), which will publish it and raise the PEER\_GROUP\_EVENT\_RECORD\_CHANGED event on all peers participating in the peer group.</span></span>


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



## <a name="receiving-a-chat-message"></a><span data-ttu-id="5c4ff-155">Ricezione di un messaggio di chat</span><span class="sxs-lookup"><span data-stu-id="5c4ff-155">Receiving a Chat Message</span></span>

<span data-ttu-id="5c4ff-156">Per ricevere il messaggio di chat, creare una funzione di callback per l' \_ evento di modifica del record di eventi del gruppo peer \_ \_ \_ che chiama una funzione simile alla seguente.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-156">To receive the chat message, create a callback function for the PEER\_GROUP\_EVENT\_RECORD\_CHANGED event that calls a function similar to one below.</span></span> <span data-ttu-id="5c4ff-157">Il record viene ottenuto chiamando [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) sui dati dell'evento ricevuti da una precedente chiamata a [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) nella funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-157">The record is obtained by calling [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) on the event data received by a previous call to [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) in the callback function.</span></span> <span data-ttu-id="5c4ff-158">Il messaggio di chat viene archiviato nel campo **dati** di questo record.</span><span class="sxs-lookup"><span data-stu-id="5c4ff-158">The chat message is stored in the **data** field of this record.</span></span>


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



 

 



