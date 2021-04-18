---
title: Aggiornamento delle licenze per gli archivi con logo PlaysForSure
description: Aggiornamento delle licenze per gli archivi con logo PlaysForSure
ms.assetid: d08d6b6e-937e-4dec-b7ca-376cdad069f9
keywords:
- Windows Media Player Online Stores, aggiornamento delle licenze
- negozi online, aggiornamento delle licenze
- Windows Media Player Online Stores, aggiornamento delle licenze
- archivi online, aggiornamento delle licenze
- Windows Media Player Online Stores, logo PlaysForSure
- negozi online, logo PlaysForSure
- aggiornamento delle licenze
- licenze, aggiornamento
- PlaysForSure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e48a3ddfd2b0670e3720f7c71587d0330a69a7
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104117399"
---
# <a name="refreshing-licenses-for-stores-that-have-the-playsforsure-logo"></a><span data-ttu-id="89a19-112">Aggiornamento delle licenze per gli archivi con logo PlaysForSure</span><span class="sxs-lookup"><span data-stu-id="89a19-112">Refreshing Licenses for Stores That Have the PlaysForSure Logo</span></span>

<span data-ttu-id="89a19-113">Alcuni archivi musicali online hanno il logo PlaysForSure, ma non sono integrati con Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="89a19-113">Certain online music stores have the PlaysForSure logo but are not integrated with Windows Media Player 11.</span></span> <span data-ttu-id="89a19-114">Questi archivi devono fornire un documento ServiceInfo e un componente leggero, in modo che Windows Media Player 11 possa ottenere e aggiornare le licenze per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="89a19-114">Those stores must provide a ServiceInfo document and a lightweight component so that Windows Media Player 11 can obtain and update licenses for their content.</span></span>

<span data-ttu-id="89a19-115">Nell'esempio seguente viene illustrato il funzionamento del processo di aggiornamento delle licenze.</span><span class="sxs-lookup"><span data-stu-id="89a19-115">The following example illustrates how the license updating process works.</span></span>

1.  <span data-ttu-id="89a19-116">L'utente ottiene 50 brani musicali dallo Store online di proseware.</span><span class="sxs-lookup"><span data-stu-id="89a19-116">The user obtains 50 music tracks from the Proseware online store.</span></span> <span data-ttu-id="89a19-117">Ogni traccia è un file con estensione WMA.</span><span class="sxs-lookup"><span data-stu-id="89a19-117">Each track is a file with the .wma file name extension.</span></span> <span data-ttu-id="89a19-118">Insieme alle tracce, l'utente ottiene le licenze per riprodurre le tracce.</span><span class="sxs-lookup"><span data-stu-id="89a19-118">Along with the tracks, the user obtains licenses to play the tracks.</span></span>
2.  <span data-ttu-id="89a19-119">L'utente copia le tracce 50 in un nuovo computer in cui è installato Windows Media Player 11 e aggiunge le tracce alla libreria di Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="89a19-119">The user copies the 50 tracks to a new computer that has Windows Media Player 11 installed and adds the tracks to the Windows Media Player library.</span></span>
3.  <span data-ttu-id="89a19-120">In un secondo momento, il modulo di aggiornamento della licenza (LRM), che fa parte di Windows Media Player 11, esamina i metadati nelle tracce 50 e determina che Proseware è il provider di contenuti.</span><span class="sxs-lookup"><span data-stu-id="89a19-120">At some later time, the License Refresh Module (LRM), which is part of Windows Media Player 11, inspects the metadata in the fifty tracks and determines that Proseware is the content provider.</span></span>
    > [!Note]  
    > <span data-ttu-id="89a19-121">Windows Media Player è in grado di identificare il provider di contenuti controllando l'attributo **contentdistributor** in un file multimediale.</span><span class="sxs-lookup"><span data-stu-id="89a19-121">Windows Media Player is able to identify the content provider by inspecting the **ContentDistributor** attribute in a media file.</span></span> <span data-ttu-id="89a19-122">Se un negozio online con il logo PlaysForSure fornisce un file multimediale che usa Windows Media Digital Rights Management (WMDRM), l'archivio online deve inserire l'attributo **contentdistributor** nel file multimediale.</span><span class="sxs-lookup"><span data-stu-id="89a19-122">If an online store that has the PlaysForSure logo provides a media file that uses Windows Media Digital Rights Management (WMDRM), the online store must place the **ContentDistributor** attribute in the media file.</span></span> <span data-ttu-id="89a19-123">Per ulteriori informazioni, vedere Aggiunta dell'attributo content Distributor in Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="89a19-123">For more information, see Adding the Content Distributor Attribute in the Windows Media Player SDK.</span></span>

     

4.  <span data-ttu-id="89a19-124">Il LRM cerca l'URL del documento ServiceInfo di Proseware, Scarica il documento ed esamina l'elemento di **installazione** del documento per ottenere l'URL di un pacchetto che il LRM può usare per installare il componente di proseware.</span><span class="sxs-lookup"><span data-stu-id="89a19-124">The LRM looks up the URL of Proseware's ServiceInfo document, downloads the document, and inspects the document's **Install** element to obtain the URL of a package that the LRM can use to install Proseware's component.</span></span> <span data-ttu-id="89a19-125">Il LRM installa e carica il componente.</span><span class="sxs-lookup"><span data-stu-id="89a19-125">The LRM installs and loads the component.</span></span>
5.  <span data-ttu-id="89a19-126">Per ognuna delle tracce 50, LRM chiama il metodo [IWMPSubscriptionService:: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) del componente proseware.</span><span class="sxs-lookup"><span data-stu-id="89a19-126">For each of the 50 tracks, the LRM calls the Proseware component's [IWMPSubscriptionService::allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) method.</span></span> <span data-ttu-id="89a19-127">Il metodo **allowPlay** inserisce una licenza per la singola traccia nel nuovo computer e restituisce **true** nel parametro *pfAllowPlay* .</span><span class="sxs-lookup"><span data-stu-id="89a19-127">The **allowPlay** method places a license for the individual track on the new computer and returns **TRUE** in the *pfAllowPlay* parameter.</span></span>
    > [!Note]  
    > <span data-ttu-id="89a19-128">Il componente Proseware deve fornire tutte le licenze necessarie per riprodurre la singola traccia. Ovvero, se necessario, il componente deve fornire una licenza radice e una licenza foglia.</span><span class="sxs-lookup"><span data-stu-id="89a19-128">The Proseware component must provide all licenses required to play the individual track. That is, the component must provide both a root license and a leaf license if needed.</span></span>

     

    <span data-ttu-id="89a19-129">Durante la prima chiamata al metodo **allowPlay** , il componente Proseware deve visualizzare una finestra di dialogo per verificare che l'utente corrente disponga di un account Proseware e abbia il diritto di riprodurre la traccia. Durante le chiamate successive a **allowPlay**, il componente può usare le credenziali ottenute nella prima chiamata per verificare che l'utente abbia il diritto di riprodurre le tracce rimanenti.</span><span class="sxs-lookup"><span data-stu-id="89a19-129">During the first call to the **allowPlay** method, the Proseware component must display a dialog box to verify that the current user has a Proseware account and has the right to play the track. During subsequent calls to **allowPlay**, the component can use the credentials that it obtained in the first call to verify that the user has the right to play the remaining tracks.</span></span>

<span data-ttu-id="89a19-130">Il componente, scritto dall'archivio online, deve implementare il metodo **allowPlay** dell'interfaccia **IWMPSubscriptionService** .</span><span class="sxs-lookup"><span data-stu-id="89a19-130">The component, which is written by the online store, must implement the **allowPlay** method of the **IWMPSubscriptionService** interface.</span></span> <span data-ttu-id="89a19-131">Il componente deve restituire E \_ NOTIMPL da ognuno degli altri tre metodi: **allowCDBurn**, **allowPDATransfer** e **startBackgroundProcessing**.</span><span class="sxs-lookup"><span data-stu-id="89a19-131">The component must return E\_NOTIMPL from each of the other three methods: **allowCDBurn**, **allowPDATransfer**, and **startBackgroundProcessing**.</span></span> <span data-ttu-id="89a19-132">Inoltre, il componente deve impostare il valore della voce del registro di sistema **capabilities** su 1; ovvero è \_ necessario impostare il flag della funzionalità Cap della sottoscrizione \_ ALLOWPLAY e tutti gli altri flag di funzionalità devono essere cancellati.</span><span class="sxs-lookup"><span data-stu-id="89a19-132">Also, the component must set the value of the **Capabilities** registry entry to 1; that is, the SUBSCRIPTION\_CAP\_ALLOWPLAY capability flag must be set, and all other capability flags must be cleared.</span></span> <span data-ttu-id="89a19-133">Per ulteriori informazioni sulla registrazione del componente, vedere [chiavi e voci del registro di sistema per un archivio di tipo 2 online](registry-keys-and-entries-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="89a19-133">For more information about registering the component, see [Registry Keys and Entries for a Type 2 Online Store](registry-keys-and-entries-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="89a19-134">Per informazioni sulla creazione di un componente che implementa l'interfaccia **IWMPSubscriptionService** , vedere [compilazione del plug-in per un negozio online di tipo 2](building-the-plug-in-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="89a19-134">For information about creating a component that implements the **IWMPSubscriptionService** interface, see [Building the Plug-in for a Type 2 Online Store](building-the-plug-in-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="89a19-135">Per informazioni su come fornire a Microsoft un documento ServiceInfo, inviare un messaggio di posta elettronica al team di servizi virtuali di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="89a19-135">For information about providing Microsoft with a ServiceInfo document, send email to the Windows Media Player Virtual Services team.</span></span> <span data-ttu-id="89a19-136">L'indirizzo di posta elettronica del team è mpsvctm@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="89a19-136">The team's email address is mpsvctm@microsoft.com.</span></span>

<span data-ttu-id="89a19-137">Per istruzioni tecniche sull'utilizzo di un'ampia gamma di SDK per Windows Media per creare un servizio che offra contenuti multimediali digitali con licenza, visitare il [centro per sviluppatori Microsoft Windows Media](https://msdn.microsoft.com/windowsmedia/default.aspx) e cercare "creazione di un Windows Media Player 10 sottoscrizione online store".</span><span class="sxs-lookup"><span data-stu-id="89a19-137">For technical guidance on using a variety of Windows Media SDKs to create a service that offers licensed digital media content, go to the [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx) and search for "Creating a Windows Media Player 10 Subscription Online Store".</span></span>

## <a name="related-topics"></a><span data-ttu-id="89a19-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="89a19-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89a19-139">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="89a19-139">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="89a19-140">**Windows Media Player Online Stores**</span><span class="sxs-lookup"><span data-stu-id="89a19-140">**Windows Media Player Online Stores**</span></span>](windows-media-player-online-stores.md)
</dt> </dl>

 

 




