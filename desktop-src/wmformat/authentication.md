---
title: Autenticazione (Windows Media Format 11 SDK)
description: Authentication
ms.assetid: 9c181615-e864-4588-846f-d04d73824f5f
keywords:
- Windows Media Format SDK, autenticazione
- Windows Media Format SDK, autenticazione di rete
- ASF (Advanced Systems Format), autenticazione
- ASF (formato avanzato dei sistemi), autenticazione
- ASF (Advanced Systems Format), autenticazione di rete
- ASF (formato avanzato dei sistemi), autenticazione di rete
- autenticazione
- autenticazione di rete, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf815881ac7beb354fffbfdb9b5475d040e9e83
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300872"
---
# <a name="authentication-windows-media-format-11-sdk"></a><span data-ttu-id="4c874-111">Autenticazione (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="4c874-111">Authentication (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="4c874-112">L'oggetto Reader può gestire le richieste di autenticazione di rete, tra cui l'autenticazione del digest e l'autenticazione NTLM.</span><span class="sxs-lookup"><span data-stu-id="4c874-112">The reader object can handle network authentication challenges, including digest authentication and NTLM authentication.</span></span> <span data-ttu-id="4c874-113">In alcuni casi l'applicazione deve fornire le credenziali dell'utente tramite un'interfaccia di callback:</span><span class="sxs-lookup"><span data-stu-id="4c874-113">In some cases the application must provide the user's credentials through a callback interface:</span></span>

-   <span data-ttu-id="4c874-114">Autenticazione del digest: l'applicazione deve implementare l'interfaccia **IWMCredentialCallback** , come descritto più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="4c874-114">Digest authentication: The application must implement the **IWMCredentialCallback** interface, as described later in this topic.</span></span>
-   <span data-ttu-id="4c874-115">Autenticazione NTLM: il lettore risponde automaticamente con le credenziali di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4c874-115">NTLM authentication: The reader automatically responds with the user's logon credentials.</span></span> <span data-ttu-id="4c874-116">Se l'utente corrente è autorizzato ad accedere al server, l'applicazione non deve eseguire alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="4c874-116">If the current user is authorized to log on to the server, the application does not have to do anything.</span></span> <span data-ttu-id="4c874-117">Se l'utente non dispone dell'autorizzazione, l'applicazione deve implementare l'interfaccia **IWMCredentialCallback** .</span><span class="sxs-lookup"><span data-stu-id="4c874-117">If the user does not have authorization, the application must implement the **IWMCredentialCallback** interface.</span></span>

    > [!Note]  
    > <span data-ttu-id="4c874-118">Windows Media Services versione 4,1 non supporta l'autenticazione NTLM tramite un server proxy.</span><span class="sxs-lookup"><span data-stu-id="4c874-118">Windows Media Services version 4.1 does not support NTLM authentication through a proxy server.</span></span> <span data-ttu-id="4c874-119">Per l'autenticazione NTLM sono necessari diversi scambi client-server nella stessa connessione e la versione 4,1 non mantiene una connessione persistente con il proxy.</span><span class="sxs-lookup"><span data-stu-id="4c874-119">NTLM authentication requires several client-server exchanges on the same connection, and version 4.1 does not keep a persistent connection with the proxy.</span></span> <span data-ttu-id="4c874-120">Windows Media Services 9 Series in Microsoft Windows Server 2003 supporta l'autenticazione NTLM tramite un server proxy, purché il proxy supporti le connessioni keep-alive.</span><span class="sxs-lookup"><span data-stu-id="4c874-120">Windows Media Services 9 Series in Microsoft Windows Server 2003 supports NTLM authentication through a proxy server, as long as the proxy supports keep-alive connections.</span></span>

     

<span data-ttu-id="4c874-121">Come indicato, in alcuni casi l'applicazione deve fornire le credenziali dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4c874-121">As noted, in some cases the application must provide the user's credentials.</span></span> <span data-ttu-id="4c874-122">Questo problema si verifica tramite l'interfaccia **IWMCredentialCallback** , che ha un singolo metodo, **AcquireCredentials**.</span><span class="sxs-lookup"><span data-stu-id="4c874-122">This occurs through the **IWMCredentialCallback** interface, which has a single method, **AcquireCredentials**.</span></span> <span data-ttu-id="4c874-123">Per supportare l'autenticazione, implementare questa interfaccia nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4c874-123">To support authentication, implement this interface in your application.</span></span> <span data-ttu-id="4c874-124">L'oggetto Reader esegue una query per questa interfaccia chiamando **QueryInterface** sul puntatore [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) ricevuto dall'applicazione nel metodo [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) .</span><span class="sxs-lookup"><span data-stu-id="4c874-124">The reader object queries for this interface by calling **QueryInterface** on the [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) pointer that it received from the application in the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method.</span></span> <span data-ttu-id="4c874-125">Se l'oggetto Reader deve ottenere le credenziali dell'utente, chiama il metodo **AcquireCredentials** dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4c874-125">If the reader object needs to get the user's credentials, it calls the application's **AcquireCredentials** method.</span></span>

<span data-ttu-id="4c874-126">Se le credenziali vengono inviate in rete senza crittografia, il lettore imposta il \_ \_ flag di testo non crittografato delle credenziali WMT \_ nel parametro *pdwFlags* .</span><span class="sxs-lookup"><span data-stu-id="4c874-126">If the credentials will be sent over the network without encryption, the reader sets the WMT\_CREDENTIAL\_CLEAR\_TEXT flag in the *pdwFlags* parameter.</span></span> <span data-ttu-id="4c874-127">Ciò consente all'applicazione di avvisare l'utente che le credenziali verranno inviate in testo normale.</span><span class="sxs-lookup"><span data-stu-id="4c874-127">This gives the application an opportunity to warn the user that his or her credentials will be sent in plain text.</span></span>

<span data-ttu-id="4c874-128">In caso contrario, l'oggetto Reader crittografa automaticamente le credenziali prima di inviarle sulla rete.</span><span class="sxs-lookup"><span data-stu-id="4c874-128">Otherwise, the reader object automatically encrypts the credentials before sending them over the network.</span></span> <span data-ttu-id="4c874-129">L'applicazione può restituirle all'oggetto Reader in testo normale.</span><span class="sxs-lookup"><span data-stu-id="4c874-129">The application can return them to the reader object in plain text.</span></span> <span data-ttu-id="4c874-130">Inoltre, se l'oggetto Reader imposta il \_ \_ flag di crittografia delle credenziali WMT, significa che il lettore supporta la lettura delle credenziali crittografate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4c874-130">In addition, if the reader object sets the WMT\_CREDENTIAL\_ENCRYPT flag, it means the reader supports getting encrypted credentials from the application.</span></span> <span data-ttu-id="4c874-131">In tal caso, l'applicazione può restituire le credenziali in testo normale, altrimenti crittografarle usando la funzione **CryptProtectData** , descritta nella documentazione di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="4c874-131">In that case, the application can either return the credentials in plain text, or else encrypt them itself using the **CryptProtectData** function, which is described in the Platform SDK documentation.</span></span> <span data-ttu-id="4c874-132">Se l'applicazione crittografa le credenziali, deve impostare il \_ \_ flag di crittografia delle credenziali WMT nel parametro *pdwFlags* prima che il metodo restituisca.</span><span class="sxs-lookup"><span data-stu-id="4c874-132">If the application encrypts the credentials, it must set the WMT\_CREDENTIAL\_ENCRYPT flag in the *pdwFlags* parameter before the method returns.</span></span>

<span data-ttu-id="4c874-133">In genere, non è necessario crittografare i dati, perché l'oggetto Reader crittografa i dati, se necessario.</span><span class="sxs-lookup"><span data-stu-id="4c874-133">Generally, it is not necessary to encrypt the data, because the reader object encrypts the data if necessary.</span></span> <span data-ttu-id="4c874-134">Tuttavia, la crittografia può essere utile se l'applicazione mantiene il nome utente e la password in memoria, perché impedisce a un utente malintenzionato di ispezionare un dump della memoria del processo.</span><span class="sxs-lookup"><span data-stu-id="4c874-134">However, encryption might be useful if the application keeps the user name and password in memory, because it prevents an attacker from inspecting a memory dump of the process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c874-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4c874-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c874-136">**Interfaccia IWMCredentialCallback**</span><span class="sxs-lookup"><span data-stu-id="4c874-136">**IWMCredentialCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> <dt>

[<span data-ttu-id="4c874-137">**Interfaccia IWMReader**</span><span class="sxs-lookup"><span data-stu-id="4c874-137">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> </dl>

 

 




