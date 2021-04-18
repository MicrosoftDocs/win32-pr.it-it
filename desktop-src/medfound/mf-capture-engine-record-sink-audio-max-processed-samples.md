---
description: Imposta il numero massimo di campioni elaborati che possono essere memorizzati nel buffer nel percorso audio del sink di record.
ms.assetid: 216886DB-B206-4944-925A-C2106331F1CB
title: Attributo MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_PROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d1ce4d649c75106545eb2ff39d4f3ea742e6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526905"
---
# <a name="mf_capture_engine_record_sink_audio_max_processed_samples-attribute"></a><span data-ttu-id="eb4ab-103">\_Attributo degli esempi di record del motore di acquisizione MF \_ \_ \_ \_ \_ Max \_ elaborati \_</span><span class="sxs-lookup"><span data-stu-id="eb4ab-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_AUDIO\_MAX\_PROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="eb4ab-104">Imposta il numero massimo di campioni elaborati che possono essere memorizzati nel buffer nel percorso audio del sink di record.</span><span class="sxs-lookup"><span data-stu-id="eb4ab-104">Sets the maximum number of processed samples that can be buffered in the record sink audio path.</span></span>

## <a name="data-type"></a><span data-ttu-id="eb4ab-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="eb4ab-105">Data type</span></span>

<span data-ttu-id="eb4ab-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="eb4ab-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="eb4ab-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb4ab-107">Remarks</span></span>

<span data-ttu-id="eb4ab-108">Per configurare questo attributo nel motore di acquisizione, aggiungerlo al parametro *pAttributes* quando si chiama [**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span><span class="sxs-lookup"><span data-stu-id="eb4ab-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="eb4ab-109">Il valore massimo per questo attributo è 100.</span><span class="sxs-lookup"><span data-stu-id="eb4ab-109">The maximum value for this attribute is 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb4ab-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb4ab-110">Requirements</span></span>



| <span data-ttu-id="eb4ab-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb4ab-111">Requirement</span></span> | <span data-ttu-id="eb4ab-112">Valore</span><span class="sxs-lookup"><span data-stu-id="eb4ab-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb4ab-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb4ab-113">Minimum supported client</span></span><br/> | <span data-ttu-id="eb4ab-114">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="eb4ab-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="eb4ab-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb4ab-115">Minimum supported server</span></span><br/> | <span data-ttu-id="eb4ab-116">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="eb4ab-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="eb4ab-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb4ab-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb4ab-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb4ab-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb4ab-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb4ab-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb4ab-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eb4ab-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="eb4ab-121">Attributi del motore di acquisizione</span><span class="sxs-lookup"><span data-stu-id="eb4ab-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="eb4ab-122">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="eb4ab-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




