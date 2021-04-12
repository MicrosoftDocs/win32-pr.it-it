---
title: EC_WMT_EVENT (Windows Media Format 11 SDK)
description: '\_evento WMT \_ EC'
ms.assetid: 51d51659-8e7d-49b7-83f2-a80e99d39d78
keywords:
- Windows Media Format SDK, EC_WMT_EVENT
- DirectShow, EC_WMT_EVENT
- EC_WMT_EVENT
- Digital Rights Management (DRM), EC_WMT_EVENT
- DRM (Digital Rights Management), EC_WMT_EVENT
- Formato Advanced Systems (ASF), EC_WMT_EVENT
- ASF (formato avanzato dei sistemi), EC_WMT_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe74baaba676a97e609b4c03cd4db9010bd8f6a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474855"
---
# <a name="ec_wmt_event-windows-media-format-11-sdk"></a><span data-ttu-id="a54ca-110">EC_WMT_EVENT (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="a54ca-110">EC_WMT_EVENT (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="a54ca-111">Inviato da Windows Media Format SDK quando un'applicazione usa il filtro di lettura ASF per riprodurre file ASF protetti da Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="a54ca-111">Sent by the Windows Media Format SDK when an application uses the ASF Reader filter to play ASF files protected by digital rights management (DRM).</span></span>

<span data-ttu-id="a54ca-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="a54ca-112">Parameters</span></span>

<span data-ttu-id="a54ca-113">*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a54ca-113">*lParam1*</span></span>

<span data-ttu-id="a54ca-114">Può essere uno dei seguenti valori di \_ stato di WMT.</span><span class="sxs-lookup"><span data-stu-id="a54ca-114">Can be one of the following WMT\_STATUS values.</span></span>



| <span data-ttu-id="a54ca-115">\_Messaggio di stato WMT</span><span class="sxs-lookup"><span data-stu-id="a54ca-115">WMT\_STATUS Message</span></span>           | <span data-ttu-id="a54ca-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a54ca-116">Description</span></span>                                                                                                                    |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a54ca-117">\_nessun \_ diritto di WMT</span><span class="sxs-lookup"><span data-stu-id="a54ca-117">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="a54ca-118">Il file è protetto con DRM versione 1 e l'applicazione non ha diritti per eseguire l'azione richiesta.</span><span class="sxs-lookup"><span data-stu-id="a54ca-118">The file is protected with DRM version 1 and the application has no rights to perform the requested action.</span></span>                    |
| <span data-ttu-id="a54ca-119">\_licenza di acquisizione WMT \_</span><span class="sxs-lookup"><span data-stu-id="a54ca-119">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="a54ca-120">Il processo di acquisizione della licenza è stato completato.</span><span class="sxs-lookup"><span data-stu-id="a54ca-120">The license acquisition process has been completed.</span></span> <span data-ttu-id="a54ca-121">Questo non significa necessariamente che sia stata acquisita correttamente una licenza.</span><span class="sxs-lookup"><span data-stu-id="a54ca-121">(This does not necessarily mean that a license was successfully acquired.)</span></span> |
| <span data-ttu-id="a54ca-122">WMT \_ No \_ Rights \_</span><span class="sxs-lookup"><span data-stu-id="a54ca-122">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="a54ca-123">Il file è protetto con DRM versione 7 e l'applicazione non ha diritti per eseguire l'azione richiesta.</span><span class="sxs-lookup"><span data-stu-id="a54ca-123">The file is protected with DRM version 7 and the application has no rights to perform the requested action.</span></span>                    |
| <span data-ttu-id="a54ca-124">WMT \_ richiede l' \_ individualizzazione</span><span class="sxs-lookup"><span data-stu-id="a54ca-124">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="a54ca-125">La licenza consente solo alle applicazioni individuali di eseguire l'azione richiesta.</span><span class="sxs-lookup"><span data-stu-id="a54ca-125">The license allows only individualized applications to perform the requested action.</span></span>                                           |
| <span data-ttu-id="a54ca-126">WMT di \_ personalizzazione</span><span class="sxs-lookup"><span data-stu-id="a54ca-126">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="a54ca-127">Il processo di individualizzazione viene ora eseguito o completato.</span><span class="sxs-lookup"><span data-stu-id="a54ca-127">The individualization process is now being performed or has been completed.</span></span>                                                    |



 

<span data-ttu-id="a54ca-128">*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a54ca-128">*lParam2*</span></span>

<span data-ttu-id="a54ca-129">Puntatore a una struttura di **\_ dati dell' \_ evento \_ am WMT** che contiene informazioni sull'evento nel puntatore del membro **pData** , nonché un codice di stato **HRESULT** inviato da Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="a54ca-129">Pointer to an **AM\_WMT\_EVENT\_DATA** structure that contains information about the event in the **pData** member pointer, as well as an **HRESULT** status code sent by the Windows Media Format SDK.</span></span> <span data-ttu-id="a54ca-130">Il valore di *lParam2* dipende dal valore di *lParam1*, come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a54ca-130">The value of *lParam2* depends on the value of *lParam1*, as described in the following table.</span></span> <span data-ttu-id="a54ca-131">(Le strutture "WM \_ " sono definite in Windows Media Format SDK).</span><span class="sxs-lookup"><span data-stu-id="a54ca-131">(The "WM\_" structures are defined in the Windows Media Format SDK.)</span></span>



| <span data-ttu-id="a54ca-132">Se lParam1 è...</span><span class="sxs-lookup"><span data-stu-id="a54ca-132">If lParam1 is...</span></span>              | <span data-ttu-id="a54ca-133">\_ \_ I dati dell'evento am WMT \_ . pData è...</span><span class="sxs-lookup"><span data-stu-id="a54ca-133">AM\_WMT\_EVENT\_DATA.pData is...</span></span>                            |
|-------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="a54ca-134">\_nessun \_ diritto di WMT</span><span class="sxs-lookup"><span data-stu-id="a54ca-134">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="a54ca-135">Puntatore a una stringa **WCHAR** contenente un URL della richiesta di verifica.</span><span class="sxs-lookup"><span data-stu-id="a54ca-135">A pointer to a **WCHAR** string containing a challenge URL.</span></span> |
| <span data-ttu-id="a54ca-136">\_licenza di acquisizione WMT \_</span><span class="sxs-lookup"><span data-stu-id="a54ca-136">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="a54ca-137">Puntatore a una struttura **di \_ \_ \_ dati di licenza WM Get** .</span><span class="sxs-lookup"><span data-stu-id="a54ca-137">A pointer to a **WM\_GET\_LICENSE\_DATA** structure.</span></span>        |
| <span data-ttu-id="a54ca-138">WMT \_ No \_ Rights \_</span><span class="sxs-lookup"><span data-stu-id="a54ca-138">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="a54ca-139">Puntatore a una struttura **di \_ \_ \_ dati di licenza WM Get** .</span><span class="sxs-lookup"><span data-stu-id="a54ca-139">A pointer to a **WM\_GET\_LICENSE\_DATA** structure.</span></span>        |
| <span data-ttu-id="a54ca-140">WMT \_ richiede l' \_ individualizzazione</span><span class="sxs-lookup"><span data-stu-id="a54ca-140">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="a54ca-141">NULL</span><span class="sxs-lookup"><span data-stu-id="a54ca-141">NULL.</span></span>                                                       |
| <span data-ttu-id="a54ca-142">WMT di \_ personalizzazione</span><span class="sxs-lookup"><span data-stu-id="a54ca-142">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="a54ca-143">Puntatore a una struttura **di \_ \_ stato di personalizzazione WM** .</span><span class="sxs-lookup"><span data-stu-id="a54ca-143">A pointer to a **WM\_INDIVIDUALIZE\_STATUS** structure.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="a54ca-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a54ca-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a54ca-145">**Funzionalità di Rights Management digitali**</span><span class="sxs-lookup"><span data-stu-id="a54ca-145">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="a54ca-146">**Informazioni di riferimento su DirectShow QASF**</span><span class="sxs-lookup"><span data-stu-id="a54ca-146">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="a54ca-147">**Abilitazione del supporto DRM**</span><span class="sxs-lookup"><span data-stu-id="a54ca-147">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




