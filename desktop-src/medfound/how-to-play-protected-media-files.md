---
description: Come riprodurre file che contengono supporti protetti da DRM.
ms.assetid: 85d98f49-8af2-42ce-9b36-a025aee93f73
title: Come riprodurre file multimediali protetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f8f7af78881e43f2f7f85e8f333ab31b1bc2de
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320647"
---
# <a name="how-to-play-protected-media-files"></a><span data-ttu-id="a7f03-103">Come riprodurre file multimediali protetti</span><span class="sxs-lookup"><span data-stu-id="a7f03-103">How to Play Protected Media Files</span></span>

<span data-ttu-id="a7f03-104">Un file multimediale protetto è un file multimediale con regole associate per l'utilizzo del contenuto.</span><span class="sxs-lookup"><span data-stu-id="a7f03-104">A protected media file is any media file that has associated rules for using the content.</span></span> <span data-ttu-id="a7f03-105">In alcuni casi, un file multimediale protetto viene crittografato con una forma di crittografia Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="a7f03-105">In some cases, a protected media file is encrypted using some form of digital rights management (DRM) encryption.</span></span> <span data-ttu-id="a7f03-106">Per riprodurre un file multimediale protetto, la riproduzione deve essere eseguita all'interno del percorso del supporto protetto (PMP).</span><span class="sxs-lookup"><span data-stu-id="a7f03-106">To play a protected media file, playback must occur inside the protected media path (PMP).</span></span> <span data-ttu-id="a7f03-107">Inoltre, l'utente potrebbe dover acquisire i diritti per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="a7f03-107">In addition, the user might have to acquire rights to the content.</span></span>

<span data-ttu-id="a7f03-108">Il termine acquisizione dei diritti si riferisce a qualsiasi azione che l'applicazione deve eseguire prima che l'utente possa riprodurre il contenuto.</span><span class="sxs-lookup"><span data-stu-id="a7f03-108">The term rights acquisition refers to any action that the application must perform before the user can play the content.</span></span> <span data-ttu-id="a7f03-109">L'esempio più comune è ottenere una licenza DRM, ma Media Foundation definisce un meccanismo generico che può supportare altri tipi di acquisizione dei diritti.</span><span class="sxs-lookup"><span data-stu-id="a7f03-109">The most common example is obtaining a DRM license, but Media Foundation defines a generic mechanism that can support other types of rights acquisition.</span></span> <span data-ttu-id="a7f03-110">L'interfaccia [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) definisce questo meccanismo generico.</span><span class="sxs-lookup"><span data-stu-id="a7f03-110">The [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface defines this generic mechanism.</span></span>

<span data-ttu-id="a7f03-111">L'acquisizione dei diritti deve essere eseguita all'esterno del PMP, dal processo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a7f03-111">Rights acquisition must be done outside of the PMP, from the application process.</span></span> <span data-ttu-id="a7f03-112">La sessione multimediale invia una notifica all'applicazione tramite l'interfaccia [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) , implementata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a7f03-112">The Media Session notifies the application through the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface, which is implemented by the application.</span></span> <span data-ttu-id="a7f03-113">La sessione multimediale usa l'interfaccia **IMFContentProtectionManager** per l'invio di un oggetto Enabler contenuto all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a7f03-113">The Media Session uses the **IMFContentProtectionManager** interface to forward a content enabler object to the application.</span></span> <span data-ttu-id="a7f03-114">Gli attivatori del contenuto implementano l'interfaccia [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .</span><span class="sxs-lookup"><span data-stu-id="a7f03-114">Content enablers implement the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span> <span data-ttu-id="a7f03-115">L'applicazione usa questa interfaccia per acquisire i diritti necessari.</span><span class="sxs-lookup"><span data-stu-id="a7f03-115">The application uses this interface to acquire the necessary rights.</span></span>

<span data-ttu-id="a7f03-116">Un abilitatore del contenuto potrebbe supportare l'acquisizione automatica dei diritti, nel qual caso l'attivatore del contenuto implementa l'intero processo e l'applicazione monitora semplicemente lo stato.</span><span class="sxs-lookup"><span data-stu-id="a7f03-116">A content enabler might support automatic rights acquisition, in which case the content enabler implements the entire process, and the application simply monitors the status.</span></span> <span data-ttu-id="a7f03-117">In caso contrario, l'applicazione deve usare l'acquisizione di diritti non invisibile all'utente, che è un processo in cui l'applicazione invia i dati HTTP POST a un URL fornito da Content Enabler.</span><span class="sxs-lookup"><span data-stu-id="a7f03-117">Otherwise, the application must use non-silent rights acquisition, which is a process where the application sends HTTP POST data to a URL provided by the content enabler.</span></span>

<span data-ttu-id="a7f03-118">Per riprodurre supporti protetti, un'applicazione segue gli stessi passaggi illustrati nell'argomento [come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md), con i seguenti passaggi aggiuntivi:</span><span class="sxs-lookup"><span data-stu-id="a7f03-118">To play protected media, an application follows the same steps given in the topic [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md), with the following additional steps:</span></span>

1.  <span data-ttu-id="a7f03-119">Eseguire una query per verificare se l'origine del supporto contiene contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="a7f03-119">Query whether the media source contains protected content.</span></span> <span data-ttu-id="a7f03-120">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a7f03-120">(Optional.)</span></span>
2.  <span data-ttu-id="a7f03-121">Creare la sessione multimediale nel processo PMP invece che nel processo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a7f03-121">Create the Media Session in the PMP process, instead of the application process.</span></span>
3.  <span data-ttu-id="a7f03-122">Eseguire l'acquisizione dei diritti, se notificata a tale scopo dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="a7f03-122">Perform rights acquisition, if notified to do so by the Media Session.</span></span> <span data-ttu-id="a7f03-123">Questa operazione viene eseguita in modo asincrono dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a7f03-123">This operation is performed asynchronously by the application.</span></span>
4.  <span data-ttu-id="a7f03-124">Completare l'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="a7f03-124">Complete the asynchronous operation.</span></span>

## <a name="query-for-protected-content"></a><span data-ttu-id="a7f03-125">Query per contenuto protetto</span><span class="sxs-lookup"><span data-stu-id="a7f03-125">Query for Protected Content</span></span>

<span data-ttu-id="a7f03-126">Per eseguire una query sull'origine del supporto che contiene contenuto protetto, chiamare la funzione [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) sul descrittore di presentazione dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="a7f03-126">To query whether a media source contains protected content, call the [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) function on the media source's presentation descriptor.</span></span> <span data-ttu-id="a7f03-127">Se la funzione restituisce S \_ OK, è necessario usare il PMP per riprodurre il contenuto.</span><span class="sxs-lookup"><span data-stu-id="a7f03-127">If the function returns S\_OK, you must use the PMP to play the content.</span></span> <span data-ttu-id="a7f03-128">Se la funzione restituisce \_ false, il file PMP non è obbligatorio ed è possibile creare la sessione multimediale nel processo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a7f03-128">If the function returns S\_FALSE, the PMP is not required, and you can create the Media Session in the application process.</span></span> <span data-ttu-id="a7f03-129">In alternativa, è possibile usare il file PMP per riprodurre entrambi i tipi di contenuto, protetto e non protetto.</span><span class="sxs-lookup"><span data-stu-id="a7f03-129">Alternatively, you can use the PMP to play both types of content, protected and unprotected.</span></span> <span data-ttu-id="a7f03-130">In tal caso, non è necessario chiamare **MFRequireProtectedEnvironment**.</span><span class="sxs-lookup"><span data-stu-id="a7f03-130">If you do that, you do not need to call **MFRequireProtectedEnvironment**.</span></span>

<span data-ttu-id="a7f03-131">Per ulteriori informazioni sui descrittori di presentazione, vedere [descrittori di presentazione](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="a7f03-131">For more information about presentation descriptors, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

## <a name="create-the-pmp-media-session"></a><span data-ttu-id="a7f03-132">Creare la sessione multimediale PMP</span><span class="sxs-lookup"><span data-stu-id="a7f03-132">Create the PMP Media Session</span></span>

<span data-ttu-id="a7f03-133">Per creare la sessione multimediale in PMP, chiamare [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span><span class="sxs-lookup"><span data-stu-id="a7f03-133">To create the Media Session in the PMP, call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="a7f03-134">Questa funzione è simile a [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession), ma anziché creare la sessione multimediale nel processo dell'applicazione, crea la sessione multimediale nel processo PMP.</span><span class="sxs-lookup"><span data-stu-id="a7f03-134">This function is similar to [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession), but instead of creating the Media Session in the application's process, it creates the Media Session in the PMP process.</span></span> <span data-ttu-id="a7f03-135">L'applicazione riceve un puntatore a un oggetto proxy per la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="a7f03-135">The application receives a pointer to a proxy object for the Media Session.</span></span> <span data-ttu-id="a7f03-136">L'applicazione chiama i metodi [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) sull'oggetto proxy, esattamente come si farebbe per la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="a7f03-136">The application calls [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) methods on the proxy object, just as it would on the Media Session.</span></span> <span data-ttu-id="a7f03-137">L'oggetto proxy esegue il inoltro delle chiamate alla sessione multimediale attraverso il limite di processo.</span><span class="sxs-lookup"><span data-stu-id="a7f03-137">The proxy object forwards the calls to the Media Session across the process boundary.</span></span>

<span data-ttu-id="a7f03-138">Creare la sessione multimediale PMP come segue:</span><span class="sxs-lookup"><span data-stu-id="a7f03-138">Create the PMP Media Session as follows:</span></span>

1.  <span data-ttu-id="a7f03-139">Creare un nuovo archivio di attributi chiamando [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span><span class="sxs-lookup"><span data-stu-id="a7f03-139">Create a new attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="a7f03-140">Impostare l'attributo [**MF \_ Session \_ Content \_ Protection \_ Manager**](mf-session-content-protection-manager-attribute.md) nell'archivio di attributi.</span><span class="sxs-lookup"><span data-stu-id="a7f03-140">Set the [**MF\_SESSION\_CONTENT\_PROTECTION\_MANAGER**](mf-session-content-protection-manager-attribute.md) attribute on the attribute store.</span></span> <span data-ttu-id="a7f03-141">Il valore di questo attributo è un puntatore all'implementazione dell'applicazione di [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager).</span><span class="sxs-lookup"><span data-stu-id="a7f03-141">The value of this attribute is a pointer to your application's implementation of [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager).</span></span> <span data-ttu-id="a7f03-142">Chiamare [**IMFAttributes:: Unknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) per impostare l'attributo.</span><span class="sxs-lookup"><span data-stu-id="a7f03-142">Call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) to set the attribute.</span></span>
3.  <span data-ttu-id="a7f03-143">Chiamare [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) per creare la sessione multimediale nel processo PMP.</span><span class="sxs-lookup"><span data-stu-id="a7f03-143">Call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the Media Session in the PMP process.</span></span> <span data-ttu-id="a7f03-144">Il parametro *pConfiguration* è un puntatore all'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) dell'archivio di attributi.</span><span class="sxs-lookup"><span data-stu-id="a7f03-144">The *pConfiguration* parameter is a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface of the attribute store.</span></span>


```C++
IMFAttributes *pAttributes = NULL;
IMFMediaSession *pSession = NULL;

// Create the attribute store.
hr = MFCreateAttributes(&pAttributes, 1);

// Set the IMFContentProtectionManager pointer.
if (SUCCEEDED(hr))
{
    hr = pAttributes->SetUnknown(
        MF_SESSION_CONTENT_PROTECTION_MANAGER, 
        pCPM  // Your implementation of IMFContentProtectionManager.
        );
}

// Create the Media Session.
if (SUCCEEDED(hr))
{
    hr = MFCreatePMPMediaSession(
        0,
        pAttributes, 
        &pSession,
        NULL
    );
}

SAFE_RELEASE(pAttributes); // Release the attribute store.
// Use the Media Session to control playback (not shown).
```



<span data-ttu-id="a7f03-145">Successivamente, creare una topologia di riproduzione e accodarla nella sessione multimediale, come descritto in [creazione di topologie di riproduzione](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="a7f03-145">Next, create a playback topology and queue it on the Media Session, as described in [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

## <a name="perform-rights-acquisition"></a><span data-ttu-id="a7f03-146">Eseguire l'acquisizione dei diritti</span><span class="sxs-lookup"><span data-stu-id="a7f03-146">Perform Rights Acquisition</span></span>

<span data-ttu-id="a7f03-147">Se la riproduzione richiede l'acquisizione dei diritti, la sessione multimediale chiama [**IMFContentProtectionManager:: BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span><span class="sxs-lookup"><span data-stu-id="a7f03-147">If playback requires rights acquisition, the Media Session calls [**IMFContentProtectionManager::BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span></span> <span data-ttu-id="a7f03-148">Il parametro *pEnablerActivate* di questo metodo è un puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="a7f03-148">The *pEnablerActivate* parameter of this method is a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="a7f03-149">Usare questa interfaccia per creare l'oggetto Enabler contenuto, che espone l'interfaccia [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .</span><span class="sxs-lookup"><span data-stu-id="a7f03-149">Use this interface to create the content enabler object, which exposes the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span> <span data-ttu-id="a7f03-150">Usare quindi il Content Enabler per eseguire il passaggio di acquisizione dei diritti.</span><span class="sxs-lookup"><span data-stu-id="a7f03-150">Then use the content enabler to perform the rights acquisition step.</span></span>

<span data-ttu-id="a7f03-151">Per creare l'Enabler del contenuto, chiamare [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject):</span><span class="sxs-lookup"><span data-stu-id="a7f03-151">To create the content enabler, call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject):</span></span>


```C++
IMFContentEnabler *pEnabler = NULL;
hr = pEnablerActivate->ActivateObject(
    IID_IMFContentEnabler, 
    (void**)&pEnabler
    );
```



<span data-ttu-id="a7f03-152">Eseguire una query sul puntatore [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) restituito per l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="a7f03-152">Query the returned [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) pointer for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="a7f03-153">Usare questa interfaccia per ottenere gli eventi dall'oggetto Enabler del contenuto.</span><span class="sxs-lookup"><span data-stu-id="a7f03-153">Use this interface to get events from the content enabler object.</span></span> <span data-ttu-id="a7f03-154">Per ulteriori informazioni sugli eventi, vedere [generatori di eventi multimediali](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="a7f03-154">For more information about events, see [Media Event Generators](media-event-generators.md).</span></span>

<span data-ttu-id="a7f03-155">Per sapere se l'Enabler del contenuto supporta l'acquisizione automatica, chiamare [**IMFContentEnabler:: IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported).</span><span class="sxs-lookup"><span data-stu-id="a7f03-155">To find out whether the content enabler supports automatic acquisition, call [**IMFContentEnabler::IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported).</span></span> <span data-ttu-id="a7f03-156">Se questo metodo restituisce il valore **true**, l'applicazione deve usare l'acquisizione automatica.</span><span class="sxs-lookup"><span data-stu-id="a7f03-156">If this method returns the value **TRUE**, the application should use automatic acquisition.</span></span> <span data-ttu-id="a7f03-157">In caso contrario, usare l'acquisizione non invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="a7f03-157">Otherwise, use non-silent acquisition.</span></span>

<span data-ttu-id="a7f03-158">Il metodo [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) è asincrono.</span><span class="sxs-lookup"><span data-stu-id="a7f03-158">The [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) method is asynchronous.</span></span> <span data-ttu-id="a7f03-159">L'applicazione deve eseguire il passaggio di acquisizione nel thread dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a7f03-159">The application should perform the acquisition step on the application's thread.</span></span> <span data-ttu-id="a7f03-160">Un approccio consiste nell'inviare un messaggio di finestra privata alla finestra principale dell'applicazione, inviando una notifica al thread dell'applicazione per eseguire l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="a7f03-160">One approach is to post a private window message to the application's main window, notifying the application thread to perform the acquisition.</span></span> <span data-ttu-id="a7f03-161">Mentre l'operazione è in sospeso, l'applicazione deve archiviare il puntatore di callback e l'oggetto di stato ricevuti nei parametri *pCallback* e *punkState* di **BeginEnableContent**.</span><span class="sxs-lookup"><span data-stu-id="a7f03-161">While the operation is pending, the application must store the callback pointer and the state object that it received in the *pCallback* and *punkState* parameters of **BeginEnableContent**.</span></span> <span data-ttu-id="a7f03-162">Questi verranno usati per completare l'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="a7f03-162">These will be used to complete the asynchronous operation.</span></span>

### <a name="automatic-acquisition"></a><span data-ttu-id="a7f03-163">Acquisizione automatica</span><span class="sxs-lookup"><span data-stu-id="a7f03-163">Automatic Acquisition</span></span>

<span data-ttu-id="a7f03-164">Per eseguire l'acquisizione automatica, chiamare [**IMFContentEnabler:: AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable).</span><span class="sxs-lookup"><span data-stu-id="a7f03-164">To perform automatic acquisition, call [**IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable).</span></span> <span data-ttu-id="a7f03-165">Questo metodo è asincrono.</span><span class="sxs-lookup"><span data-stu-id="a7f03-165">This method is asynchronous.</span></span> <span data-ttu-id="a7f03-166">Al termine dell'operazione, l'attivatore di contenuto invia un evento [MEEnablerCompleted](meenablercompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="a7f03-166">When the operation is completed, the content enabler sends an [MEEnablerCompleted](meenablercompleted.md) event.</span></span> <span data-ttu-id="a7f03-167">Il codice di stato dell'evento indica se l'operazione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="a7f03-167">The event's status code indicates whether the operation was successful.</span></span> <span data-ttu-id="a7f03-168">Se il codice di stato dell'evento MEEnablerCompleted è NS \_ E \_ DRM \_ License \_ NOTACQUIRED, l'applicazione dovrebbe provare a usare l'acquisizione non invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="a7f03-168">If the status code from the MEEnablerCompleted event is NS\_E\_DRM\_LICENSE\_NOTACQUIRED, the application should try using non-silent acquisition.</span></span>

<span data-ttu-id="a7f03-169">Mentre è in corso l'operazione di acquisizione, l'oggetto Enabler potrebbe inviare l'evento [MEEnablerProgress](meenablerprogress.md) per indicare lo stato di avanzamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a7f03-169">While the acquisition operation is in progress, the enabler object might send the [MEEnablerProgress](meenablerprogress.md) event to indicate the progress of the operation.</span></span> <span data-ttu-id="a7f03-170">Per annullare l'operazione, chiamare [**IMFContentEnabler:: Cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel).</span><span class="sxs-lookup"><span data-stu-id="a7f03-170">To cancel the operation, call [**IMFContentEnabler::Cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel).</span></span>

### <a name="non-silent-acquisition"></a><span data-ttu-id="a7f03-171">Acquisizione non invisibile all'utente</span><span class="sxs-lookup"><span data-stu-id="a7f03-171">Non-Silent Acquisition</span></span>

<span data-ttu-id="a7f03-172">Se il metodo [**IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) restituisce **false** o il metodo [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) ha esito negativo con il codice di errore NS \_ E \_ DRM \_ License \_ NOTACQUIRED, l'applicazione deve eseguire un'acquisizione non invisibile all'utente, come descritto nei passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a7f03-172">If the [**IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) method returns **FALSE** or the [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) method fails with the error code NS\_E\_DRM\_LICENSE\_NOTACQUIRED, the application should perform non-silent acquisition as described in the following steps:</span></span>

1.  <span data-ttu-id="a7f03-173">Chiamare [**IMFContentEnabler:: GetEnableURL**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) per ottenere l'URL per l'acquisizione dei diritti.</span><span class="sxs-lookup"><span data-stu-id="a7f03-173">Call [**IMFContentEnabler::GetEnableURL**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) to get the URL for the rights acquisition.</span></span> <span data-ttu-id="a7f03-174">Questo metodo restituisce anche un flag che indica se l'URL è attendibile.</span><span class="sxs-lookup"><span data-stu-id="a7f03-174">This method also returns a flag indicating whether the URL is trusted.</span></span>
2.  <span data-ttu-id="a7f03-175">Chiamare [**IMFContentEnabler:: GetEnableData**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) per ottenere i dati http post.</span><span class="sxs-lookup"><span data-stu-id="a7f03-175">Call [**IMFContentEnabler::GetEnableData**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) to get the HTTP POST data.</span></span>
3.  <span data-ttu-id="a7f03-176">Chiamare [**IMFContentEnabler:: MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable).</span><span class="sxs-lookup"><span data-stu-id="a7f03-176">Call [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable).</span></span> <span data-ttu-id="a7f03-177">Questo metodo fa in modo che l'attivatore del contenuto monitori lo stato di avanzamento dell'azione di acquisizione dei diritti.</span><span class="sxs-lookup"><span data-stu-id="a7f03-177">This method causes the content enabler to monitor the progress of the rights acquisition action.</span></span>

4.  <span data-ttu-id="a7f03-178">Inviare i dati all'URL di acquisizione dei diritti usando un'azione HTTP POST.</span><span class="sxs-lookup"><span data-stu-id="a7f03-178">Submit the data to the rights acquisition URL by using an HTTP POST action.</span></span> <span data-ttu-id="a7f03-179">È possibile utilizzare il controllo Internet Explorer o le API di Windows Internet (WinINet).</span><span class="sxs-lookup"><span data-stu-id="a7f03-179">You can use the Internet Explorer control or the Windows Internet (WinINet) APIs.</span></span>

<span data-ttu-id="a7f03-180">Il codice seguente illustra i passaggi da 1 a 3.</span><span class="sxs-lookup"><span data-stu-id="a7f03-180">The following code shows steps 1–3.</span></span> <span data-ttu-id="a7f03-181">Il passaggio 4 dipende dai requisiti specifici dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a7f03-181">Step 4 depends on your application's particular requirements.</span></span>


```C++
WCHAR   *sURL = NULL;  // URL.
DWORD   cchURL = 0;    // Size of the URL in characters.

// Trust status of the URL.
MF_URL_TRUST_STATUS  trustStatus = MF_LICENSE_URL_UNTRUSTED;

BYTE    *pPostData = NULL;  // Buffer to hold HTTP POST data.
DWORD   cbPostDataSize = 0; // Size of the buffer, in bytes.

HRESULT hr = S_OK;

// Get the URL. 
hr = m_pEnabler->GetEnableURL(&sURL, &cchURL, &trustStatus);

if (SUCCEEDED(hr))
{
    if (trustStatus != MF_LICENSE_URL_TRUSTED)
    {
        // The URL is not trusted. Do not proceed.
        hr = E_FAIL;
    }
}

// Monitor the rights acquisition. 
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->MonitorEnable();
}

// Get the HTTP POST data.
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->GetEnableData(&pPostData, &cbPostDataSize);
}

// Open the URL and send the HTTP POST data. (Not shown.)

// Release the buffers.
CoTaskMemFree(pPostData);
CoTaskMemFree(sURL);
```



<span data-ttu-id="a7f03-182">Al termine dell'operazione, l'attivatore di contenuto invia un evento [MEEnablerCompleted](meenablercompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="a7f03-182">When the operation is completed, the content enabler sends an [MEEnablerCompleted](meenablercompleted.md) event.</span></span>

## <a name="complete-the-asynchronous-operation"></a><span data-ttu-id="a7f03-183">Completa l'operazione asincrona</span><span class="sxs-lookup"><span data-stu-id="a7f03-183">Complete the Asynchronous Operation</span></span>

<span data-ttu-id="a7f03-184">Quando l'acquisizione dei diritti viene completata correttamente o in caso contrario, l'applicazione deve inviare una notifica alla sessione multimediale richiamando il puntatore di callback fornito nel metodo [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) .</span><span class="sxs-lookup"><span data-stu-id="a7f03-184">When the rights acquisition is completed, successfully or otherwise, the application must notify the Media Session, by invoking the callback pointer given in the [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) method.</span></span>

1.  <span data-ttu-id="a7f03-185">Creare un oggetto risultato asincrono chiamando [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult).</span><span class="sxs-lookup"><span data-stu-id="a7f03-185">Create an asynchronous result object by calling [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult).</span></span>
2.  <span data-ttu-id="a7f03-186">Richiamare il callback della sessione multimediale chiamando [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span><span class="sxs-lookup"><span data-stu-id="a7f03-186">Invoke the Media Session's callback by calling [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span></span>
3.  <span data-ttu-id="a7f03-187">La sessione multimediale chiamerà [**IMFContentProtectionManager:: EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent).</span><span class="sxs-lookup"><span data-stu-id="a7f03-187">The Media Session will call [**IMFContentProtectionManager::EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent).</span></span> <span data-ttu-id="a7f03-188">Nell'implementazione di questo metodo rilasciare tutti i puntatori o le risorse allocati all'interno di [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span><span class="sxs-lookup"><span data-stu-id="a7f03-188">In your implementation of this method, release any pointers or resources that you allocated inside [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span></span> <span data-ttu-id="a7f03-189">Restituisce un valore **HRESULT** che indica l'esito positivo complessivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a7f03-189">Return an **HRESULT** that indicates the overall success of the operation.</span></span> <span data-ttu-id="a7f03-190">Se l'acquisizione dei diritti ha avuto esito negativo o l'utente ha annullato prima del completamento, restituire un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="a7f03-190">If the rights acquisition failed or the user canceled before it was completed, return an error code.</span></span>

<span data-ttu-id="a7f03-191">Nel codice seguente viene illustrato come creare il risultato asincrono e richiamare il callback.</span><span class="sxs-lookup"><span data-stu-id="a7f03-191">The following code shows how to create the asynchronous result and invoke the callback.</span></span>


```C++
IMFAsyncResult  *pResult = NULL;

// Create the asynchronous result object.
hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);

// Invoke the callback.
if (SUCCEEDED(hr))
{
    pResult->SetStatus(hrStatus);
    hr = MFInvokeCallback(pResult);
}
SAFE_RELEASE(pResult);
```



## <a name="related-topics"></a><span data-ttu-id="a7f03-192">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a7f03-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7f03-193">Sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="a7f03-193">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="a7f03-194">Riproduzione di audio/video</span><span class="sxs-lookup"><span data-stu-id="a7f03-194">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



