---
title: Oggetto transcryptr DRM
description: Oggetto transcryptr DRM
ms.assetid: 50c041b3-6621-4618-843f-6ef9b8e741ab
keywords:
- Windows Media Format SDK, oggetti transcryptor DRM
- ASF (Advanced Systems Format), oggetti transcryptor DRM
- ASF (Advanced Systems Format), oggetti transcryptor DRM
- oggetti, oggetti Transcriptor DRM
- Oggetti transcryptor DRM
- Windows Media Format SDK, oggetti transcryptor
- ASF (Advanced Systems Format), oggetti Transcriptor
- ASF (Advanced Systems Format), oggetti transcryptor
- oggetti, oggetti Transcriptor
- oggetti Transcriptor
- Digital Rights Management (DRM), oggetti Transcriptor
- DRM (Digital Rights Management), oggetti Transcriptor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46213dd7ebfbe48ff22039c201dbff3aab462f5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117379"
---
# <a name="drm-transcryptor-object"></a><span data-ttu-id="e92d4-115">Oggetto transcryptr DRM</span><span class="sxs-lookup"><span data-stu-id="e92d4-115">DRM Transcryptor Object</span></span>

<span data-ttu-id="e92d4-116">L'oggetto transcryptor DRM converte i file ASF protetti da DRM in flussi di dati pronti per l'invio ai dispositivi di rete che usano Windows Media DRM 10 per i dispositivi di rete.</span><span class="sxs-lookup"><span data-stu-id="e92d4-116">The DRM transcryptor object converts DRM-protected ASF files into data streams ready to be sent to network devices that use Windows Media DRM 10 for Network Devices.</span></span>

<span data-ttu-id="e92d4-117">L'oggetto transcryptor DRM viene creato dalla funzione [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) , che imposta un puntatore sull'interfaccia [**IWMDRMTranscryptor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) .</span><span class="sxs-lookup"><span data-stu-id="e92d4-117">The DRM transcryptor object is created by the [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) function, which sets a pointer to the [**IWMDRMTranscryptor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) interface.</span></span> <span data-ttu-id="e92d4-118">**IUnknown** e **IWMDRMTranscryptor** sono le uniche interfacce supportate da questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="e92d4-118">**IUnknown** and **IWMDRMTranscryptor** are the only interfaces supported by this object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e92d4-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e92d4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e92d4-120">**Oggetti**</span><span class="sxs-lookup"><span data-stu-id="e92d4-120">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




