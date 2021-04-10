---
title: Novità (Windows Media Format 11 SDK)
description: Novità
ms.assetid: af04b99a-4653-4c82-944a-7005cf1181fe
keywords:
- Windows Media Format SDK, novità
- Windows Media Format SDK, funzionalità
- Windows Media Format SDK, nuove funzionalità
- Windows Media Format SDK, API client estese
- Windows Media Format SDK, aggiornamenti DRM
- Windows Media Format SDK, aggiornamenti dei codec
- Windows Media Format SDK, immagini di anteprima
- Digital Rights Management (DRM), nuove funzionalità
- DRM (Digital Rights Management), nuove funzionalità
- anteprime in miniatura delle immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63d85f00f89f940ab22754d1f6f458430868d7c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739503"
---
# <a name="whats-new-windows-media-format-11-sdk"></a><span data-ttu-id="eeae2-113">Novità (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="eeae2-113">What's New (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="eeae2-114">Windows Media Format 11 SDK introduce nuove funzionalità di Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="eeae2-114">The Windows Media Format 11 SDK introduces new digital rights management (DRM) features.</span></span> <span data-ttu-id="eeae2-115">Le modifiche seguenti sono state apportate all'SDK dalla versione 9,5.</span><span class="sxs-lookup"><span data-stu-id="eeae2-115">The following changes have been made to the SDK since the 9.5 release.</span></span>

## <a name="windows-media-drm-client-extended-apis"></a><span data-ttu-id="eeae2-116">API estese del client Windows Media DRM</span><span class="sxs-lookup"><span data-stu-id="eeae2-116">Windows Media DRM Client Extended APIs</span></span>

<span data-ttu-id="eeae2-117">Windows Media Format 11 SDK viene fornito con un nuovo set di API di DRM.</span><span class="sxs-lookup"><span data-stu-id="eeae2-117">The Windows Media Format 11 SDK ships with a new set of DRM APIs.</span></span> <span data-ttu-id="eeae2-118">Queste API sono implementate nella propria libreria.</span><span class="sxs-lookup"><span data-stu-id="eeae2-118">These APIs are implemented in their own library.</span></span> <span data-ttu-id="eeae2-119">Molte delle funzionalità DRM supportate dagli oggetti di Windows Media Format SDK sono supportate anche dalle API estese del client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="eeae2-119">Many of the DRM features supported by the objects of the Windows Media Format SDK are also supported by the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="eeae2-120">La differenza principale tra le nuove API è che non si basano su un file ASF da usare.</span><span class="sxs-lookup"><span data-stu-id="eeae2-120">The primary difference in the new APIs is that they do not rely on having an ASF file to work.</span></span> <span data-ttu-id="eeae2-121">Al contrario, le nuove API gestiscono direttamente l'archivio licenze locale, usando spesso l'ID chiave per identificare le licenze.</span><span class="sxs-lookup"><span data-stu-id="eeae2-121">Instead, the new APIs deal with the local license store directly, often using the key ID to identify licenses.</span></span>

<span data-ttu-id="eeae2-122">Per ulteriori informazioni, vedere la documentazione sulle [API estese del client Windows Media DRM](windows-media-drm-client-extended-apis.md) .</span><span class="sxs-lookup"><span data-stu-id="eeae2-122">For more information, see the [Windows Media DRM Client Extended APIs](windows-media-drm-client-extended-apis.md) documentation.</span></span>

## <a name="updated-codecs"></a><span data-ttu-id="eeae2-123">Codec aggiornati</span><span class="sxs-lookup"><span data-stu-id="eeae2-123">Updated Codecs</span></span>

<span data-ttu-id="eeae2-124">Il codec del profilo avanzato Windows Media Video 9 è stato aggiornato per produrre un flusso di bit compresso che è conforme allo standard SMPTE VC-1 pubblicato.</span><span class="sxs-lookup"><span data-stu-id="eeae2-124">The Windows Media Video 9 Advanced Profile codec has been updated to produce a compressed bit stream that is compliant with the published SMPTE VC-1 standard.</span></span>

<span data-ttu-id="eeae2-125">Il codec Windows Media Audio 10 Professional è incluso anche in questa versione dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="eeae2-125">The Windows Media Audio 10 Professional codec is also included in this release of the SDK.</span></span> <span data-ttu-id="eeae2-126">Il nuovo codec audio presenta una qualità migliorata a velocità in bit inferiori.</span><span class="sxs-lookup"><span data-stu-id="eeae2-126">The new audio codec features improved quality at lower bit rates.</span></span>

## <a name="thumbnail-right"></a><span data-ttu-id="eeae2-127">Anteprima a destra</span><span class="sxs-lookup"><span data-stu-id="eeae2-127">Thumbnail Right</span></span>

<span data-ttu-id="eeae2-128">Le applicazioni possono richiedere una nuova azione DRM per leggere da video per creare un'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="eeae2-128">Applications can request a new DRM action to read from video to create a thumbnail image.</span></span> <span data-ttu-id="eeae2-129">Ciò consente alle applicazioni di creare e visualizzare immagini di anteprima per file video senza aprire il file per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="eeae2-129">This enables applications to create and display thumbnail images for video files without opening the file for playback.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eeae2-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eeae2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeae2-131">**Informazioni su Windows Media Format SDK**</span><span class="sxs-lookup"><span data-stu-id="eeae2-131">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




