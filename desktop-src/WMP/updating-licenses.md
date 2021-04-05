---
title: Aggiornamento delle licenze
description: Aggiornamento delle licenze
ms.assetid: b298badf-efcf-423c-8cc7-c3f50ab288a0
keywords:
- Windows Media Player Online Stores, aggiornamento delle licenze
- archivi online, aggiornamento delle licenze
- digitare 1 negozi online, aggiornamento delle licenze
- Windows Media Player Online Stores, aggiornamento delle licenze
- negozi online, aggiornamento delle licenze
- digitare 1 negozi online, aggiornamento delle licenze
- aggiornamento delle licenze
- licenze, aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154959b01c93719184e310b60dffaa91fe2dcfa0
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336329"
---
# <a name="updating-licenses"></a><span data-ttu-id="44b36-111">Aggiornamento delle licenze</span><span class="sxs-lookup"><span data-stu-id="44b36-111">Updating Licenses</span></span>

<span data-ttu-id="44b36-112">Gli archivi online possono fornire contenuti con licenza per un periodo di tempo specifico o fino a una determinata data.</span><span class="sxs-lookup"><span data-stu-id="44b36-112">Online stores can deliver content that is licensed for a specific period of time or until a certain date.</span></span> <span data-ttu-id="44b36-113">Si tratta di una situazione normale per il contenuto musicale fornito come parte di un contratto di servizio di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="44b36-113">This would be normal for music content delivered as part of a subscription service agreement.</span></span> <span data-ttu-id="44b36-114">In questo caso, lo Store online deve avere la possibilità di aggiornare le licenze prima della scadenza, presumendo, ovviamente, che l'utente abbia pagato per rinnovare la propria sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="44b36-114">In this case, the online store needs an opportunity to update these licenses before they expire, assuming, of course, that the user has paid to renew his or her subscription.</span></span> <span data-ttu-id="44b36-115">Se l'utente non ha rinnovato la sottoscrizione, le licenze possono semplicemente essere lasciate scadere.</span><span class="sxs-lookup"><span data-stu-id="44b36-115">(If the user has not renewed the subscription, the licenses can simply be left to expire.)</span></span>

<span data-ttu-id="44b36-116">Windows Media Player esegue una query sul plug-in del partner di contenuti circa la quantità di avvisi di anticipo che il lettore deve fornire per una licenza che sta per scadere.</span><span class="sxs-lookup"><span data-stu-id="44b36-116">Windows Media Player queries the content partner plug-in about how much advance warning the Player should provide about a license that is about to expire.</span></span> <span data-ttu-id="44b36-117">Questa operazione viene eseguita chiamando [IWMPContentPartner:: GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo), passando la costante g \_ szContentPartnerInfo \_ LicenseRefreshAdvanceWarning tramite il parametro *bstrInfoName* .</span><span class="sxs-lookup"><span data-stu-id="44b36-117">It does this by calling [IWMPContentPartner::GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo), passing the constant g\_szContentPartnerInfo\_LicenseRefreshAdvanceWarning through the *bstrInfoName* parameter.</span></span> <span data-ttu-id="44b36-118">Per avvisare il plug-in sulle licenze che stanno per scadere, Windows Media Player chiama [IWMPContentPartner:: RefreshLicense](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense).</span><span class="sxs-lookup"><span data-stu-id="44b36-118">To alert the plug-in about licenses that are about to expire, Windows Media Player calls [IWMPContentPartner::RefreshLicense](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense).</span></span> <span data-ttu-id="44b36-119">Questa chiamata accetta parametri che forniscono dettagli sul file da aggiornare, ad esempio se il file si trova nel computer dell'utente e il percorso del file.</span><span class="sxs-lookup"><span data-stu-id="44b36-119">This call takes parameters that provide details about the file being refreshed, such as whether the file is on the user's computer, and the path to the file.</span></span> <span data-ttu-id="44b36-120">Se la licenza viene aggiornata nell'ambito di un'operazione di sincronizzazione del dispositivo, il parametro *pReasonContext* fornisce il nome cannonical del dispositivo</span><span class="sxs-lookup"><span data-stu-id="44b36-120">If the license is being refreshed as part of a device synchronization operation, the *pReasonContext* parameter supplies the cannonical name of the device</span></span>

<span data-ttu-id="44b36-121">Quando Windows Media Player chiama **RefreshLicence**, passa un cookie che identifica la richiesta di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="44b36-121">When Windows Media Player calls **RefreshLicence**, it passes a cookie that identifies the update request.</span></span> <span data-ttu-id="44b36-122">Al termine dell'elaborazione della richiesta di aggiornamento, il plug-in Invia una notifica a Windows Media Player chiamando [IWMPContentPartnerCallback:: RefreshLicenseComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete), passando il cookie, l'ID dell'elemento multimediale e un valore **HRESULT** che indica se l'aggiornamento è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="44b36-122">When the plug-in has finished processing the update request, it notifies Windows Media Player by calling [IWMPContentPartnerCallback::RefreshLicenseComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete), passing the cookie, the ID of the media item, and an **HRESULT** that indicates whether the update was successful.</span></span>

<span data-ttu-id="44b36-123">I plug-in di Store online possono anche eseguire l'ispezione e gli aggiornamenti delle licenze come processo in background.</span><span class="sxs-lookup"><span data-stu-id="44b36-123">Online store plug-ins can also do license inspection and updates as a background process.</span></span> <span data-ttu-id="44b36-124">Windows Media Player notifica al plug-in informazioni sugli orari in cui è consentito eseguire attività di elaborazione in background chiamando [IWMPContentPartner:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify).</span><span class="sxs-lookup"><span data-stu-id="44b36-124">Windows Media Player notifies the plug-in about times when it is permissible to perform background processing tasks by calling [IWMPContentPartner::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify).</span></span> <span data-ttu-id="44b36-125">Per segnalare al plug-in di avviare l'elaborazione in background, il giocatore passa il valore di enumerazione [WMPPartnerNotification](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) wmpsnBackgroundProcessingBegin; per segnalare al plug-in di arrestare l'elaborazione in background, il giocatore passa il valore wmpsnBackgroundProcessingEnd.</span><span class="sxs-lookup"><span data-stu-id="44b36-125">To signal the plug-in to start background processing, the Player passes the [WMPPartnerNotification](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) enumeration value wmpsnBackgroundProcessingBegin; to signal the plug-in to stop background processing, the Player passes the value wmpsnBackgroundProcessingEnd.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44b36-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="44b36-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44b36-127">**Guida per programmatori per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="44b36-127">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




