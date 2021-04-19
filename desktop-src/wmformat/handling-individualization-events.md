---
title: Gestione degli eventi di individualizzazione
description: Gestione degli eventi di individualizzazione
ms.assetid: f533978f-f366-4900-b784-f51e88393984
keywords:
- Windows Media Format SDK, gestione di eventi di individualizzazione
- Windows Media Format SDK, eventi di individualizzazione
- Formato di sistemi avanzati (ASF), gestione di eventi di individualizzazione
- ASF (formato avanzato dei sistemi), gestione di eventi di individualizzazione
- ASF (Advanced Systems Format), eventi di individualizzazione
- ASF (formato avanzato dei sistemi), eventi di individualizzazione
- Digital Rights Management (DRM), gestione di eventi di individualizzazione
- DRM (Digital Rights Management), gestione di eventi di individualizzazione
- Digital Rights Management (DRM), eventi di individualizzazione
- DRM (Digital Rights Management), eventi di individualizzazione
- eventi di individualizzazione
- eventi, eventi di individualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e74df94bf871ec62ec2acb94658785969812640
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299412"
---
# <a name="handling-individualization-events"></a><span data-ttu-id="69b4b-115">Gestione degli eventi di individualizzazione</span><span class="sxs-lookup"><span data-stu-id="69b4b-115">Handling Individualization Events</span></span>

<span data-ttu-id="69b4b-116">Quando un'applicazione abilitata per il DRM tenta di aprire un file protetto, il componente DRM esamina l'attributo [**DRM \_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md) nel file, che specifica il livello di versione minimo necessario per accedere al contenuto.</span><span class="sxs-lookup"><span data-stu-id="69b4b-116">When a DRM-enabled application attempts to open a protected file, the DRM component examines the [**DRM\_DRMHeader\_IndividualizedVersion**](drm-drmheader-individualizedversion.md) attribute in the file, which specifies the minimum version level required to access the content.</span></span> <span data-ttu-id="69b4b-117">Tutti i livelli del componente DRM funzionano con tutte le versioni 7,0 e successive di Windows Media Player e Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="69b4b-117">All levels of the DRM component work with all 7.0 and later versions of Windows Media Player and the Windows Media Format SDK.</span></span> <span data-ttu-id="69b4b-118">Se il livello di versione individualizzato del componente DRM è inferiore alla versione richiesta, il componente DRM invierà un evento **WMT \_ needs \_ individualation** al metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="69b4b-118">If the DRM component's individualized version level is lower than the required version, the DRM component will send a **WMT\_NEEDS\_INDIVIDUALIZATION** event to the application's [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="69b4b-119">Nell'applicazione deve quindi essere visualizzato un messaggio o una finestra di dialogo in cui viene richiesto agli utenti di avviare o annullare l'aggiornamento della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="69b4b-119">The application must then display a message or dialog box prompting users to either start or cancel the security upgrade.</span></span> <span data-ttu-id="69b4b-120">Questa richiesta è necessaria perché, per motivi di privacy, gli utenti devono concedere l'autorizzazione prima che nel computer venga installato un aggiornamento della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="69b4b-120">This prompt is necessary because, for privacy reasons, users must give their permission before a security upgrade is installed on their computer.</span></span>

> [!Note]  
> <span data-ttu-id="69b4b-121">L'intestazione del contenuto specifica solo le prime due cifre per DRM \_ DRMVersion \_ IndividualizedVersion.</span><span class="sxs-lookup"><span data-stu-id="69b4b-121">The header of the content specifies only the first two digits for DRM\_DRMVersion\_IndividualizedVersion.</span></span> <span data-ttu-id="69b4b-122">In altre parole, per richiedere un componente 2.2.0.1 DRM di livello, l'intestazione conterrebbe "2,2".</span><span class="sxs-lookup"><span data-stu-id="69b4b-122">In other words, to require a level 2.2.0.1 DRM component, the header would contain "2.2".</span></span>

 

<span data-ttu-id="69b4b-123">Per avviare l'aggiornamento della sicurezza e/o attivare l'individualizzazione, chiamare il metodo [**IWMDRMReader:: individualizzato**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) con il parametro *dwFlags* impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="69b4b-123">To start the security upgrade and/or trigger individualization, call the [**IWMDRMReader::Individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) method with the *dwFlags* parameter set to 1.</span></span>

<span data-ttu-id="69b4b-124">È necessario gestire l'evento **WMT di \_ personalizzazione** dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="69b4b-124">You must handle the **WMT\_INDIVIDUALIZE** event in your application.</span></span> <span data-ttu-id="69b4b-125">Questo evento verrà generato più volte dal componente DRM con lo stato del processo di individualizzazione indicato nel parametro *pValue* , di cui viene eseguito il cast su un puntatore a una struttura di [**\_ \_ stato di personalizzazione WM**](wm-individualize-status.md) .</span><span class="sxs-lookup"><span data-stu-id="69b4b-125">This event will be fired multiple times by the DRM component with the status of the individualization process indicated in the *pValue* parameter, which is cast to a pointer to a [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

<span data-ttu-id="69b4b-126">Una volta che il componente DRM è stato personalizzato correttamente, l'applicazione riceverà un evento **WMT \_ No \_ Rights \_** , che indica che l'applicazione può ora procedere con l'acquisizione di una licenza per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="69b4b-126">After the DRM component is successfully individualized, the application will receive a **WMT\_NO\_RIGHTS\_EX** event, indicating that the application can now proceed to acquire a license for the content.</span></span>

> [!Note]  
> <span data-ttu-id="69b4b-127">Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="69b4b-127">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="69b4b-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="69b4b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69b4b-129">**Gestione degli eventi di acquisizione delle licenze**</span><span class="sxs-lookup"><span data-stu-id="69b4b-129">**Handling License Acquisition Events**</span></span>](handling-license-acquisition-events.md)
</dt> <dt>

[<span data-ttu-id="69b4b-130">**Applicazioni DRM individualizzazione**</span><span class="sxs-lookup"><span data-stu-id="69b4b-130">**Individualizing DRM Applications**</span></span>](individualizing-drm-applications.md)
</dt> <dt>

[<span data-ttu-id="69b4b-131">**Interfaccia IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="69b4b-131">**IWMDRMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> </dl>

 

 




