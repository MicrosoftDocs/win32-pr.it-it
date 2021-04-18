---
description: Disabilita l'uso di trasformazioni di Media Foundation basate su hardware (MFTs) nel motore di acquisizione.
ms.assetid: 1C687FEC-276D-4759-A3B8-9A2A31CB0DE1
title: Attributo MF_CAPTURE_ENGINE_DISABLE_HARDWARE_TRANSFORMS (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9631804c61fab953793c3f89d1eac3dc2e8f4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309583"
---
# <a name="mf_capture_engine_disable_hardware_transforms-attribute"></a><span data-ttu-id="f337f-103">\_Attributo di \_ disabilitazione dell'hardware per le \_ \_ \_ trasformazioni MF motore di acquisizione</span><span class="sxs-lookup"><span data-stu-id="f337f-103">MF\_CAPTURE\_ENGINE\_DISABLE\_HARDWARE\_TRANSFORMS attribute</span></span>

<span data-ttu-id="f337f-104">Disabilita l'uso di trasformazioni di Media Foundation basate su hardware (MFTs) nel motore di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="f337f-104">Disables the use of hardware-based Media Foundation transforms (MFTs) in the capture engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="f337f-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f337f-105">Data type</span></span>

<span data-ttu-id="f337f-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f337f-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f337f-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="f337f-107">Remarks</span></span>

<span data-ttu-id="f337f-108">Per impostazione predefinita, il motore di acquisizione USA decodificatori o codificatori hardware.</span><span class="sxs-lookup"><span data-stu-id="f337f-108">By default, the capture engine uses hardware decoders or encoders.</span></span> <span data-ttu-id="f337f-109">Per disabilitare l'utilizzo di MFTs hardware, impostare questo attributo su **true** quando si crea il motore di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="f337f-109">To disable the use of hardware MFTs, set this attribute to **TRUE** when you create the capture engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="f337f-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f337f-110">Requirements</span></span>



| <span data-ttu-id="f337f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f337f-111">Requirement</span></span> | <span data-ttu-id="f337f-112">Valore</span><span class="sxs-lookup"><span data-stu-id="f337f-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f337f-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f337f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f337f-114">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f337f-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="f337f-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f337f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f337f-116">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f337f-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f337f-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f337f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="f337f-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="f337f-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f337f-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f337f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f337f-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f337f-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f337f-121">Attributi del motore di acquisizione</span><span class="sxs-lookup"><span data-stu-id="f337f-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="f337f-122">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="f337f-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




