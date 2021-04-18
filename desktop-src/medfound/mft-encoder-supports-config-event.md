---
description: Specifica che il codificatore MFT supporta la ricezione di eventi MEEncodingParameter durante il flusso.
ms.assetid: 8DE04537-641C-4154-9C7F-A7D025CA4C39
title: Attributo MFT_ENCODER_SUPPORTS_CONFIG_EVENT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49c688abc4d372a463115c369e4616babe3bcaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310224"
---
# <a name="mft_encoder_supports_config_event-attribute"></a><span data-ttu-id="631a2-103">Il \_ codificatore MFT \_ supporta l' \_ attributo dell' \_ evento config</span><span class="sxs-lookup"><span data-stu-id="631a2-103">MFT\_ENCODER\_SUPPORTS\_CONFIG\_EVENT attribute</span></span>

<span data-ttu-id="631a2-104">Specifica che il codificatore MFT supporta la ricezione di eventi [MEEncodingParameter](meencodingparameters.md) durante il flusso.</span><span class="sxs-lookup"><span data-stu-id="631a2-104">Specifies that the MFT encoder supports receiving [MEEncodingParameter](meencodingparameters.md) events while streaming.</span></span>

## <a name="data-type"></a><span data-ttu-id="631a2-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="631a2-105">Data type</span></span>

<span data-ttu-id="631a2-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="631a2-106">**Bool** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="631a2-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="631a2-107">Remarks</span></span>

<span data-ttu-id="631a2-108">Inviato dal codificatore MFT tramite [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span><span class="sxs-lookup"><span data-stu-id="631a2-108">Sent by the MFT encoder through [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span></span>

## <a name="requirements"></a><span data-ttu-id="631a2-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="631a2-109">Requirements</span></span>



| <span data-ttu-id="631a2-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="631a2-110">Requirement</span></span> | <span data-ttu-id="631a2-111">Valore</span><span class="sxs-lookup"><span data-stu-id="631a2-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="631a2-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="631a2-112">Minimum supported client</span></span><br/> | <span data-ttu-id="631a2-113">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="631a2-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="631a2-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="631a2-114">Minimum supported server</span></span><br/> | <span data-ttu-id="631a2-115">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="631a2-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="631a2-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="631a2-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="631a2-117"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="631a2-117"><dt>Mftransform.h</dt></span></span> </dl>   |
| <span data-ttu-id="631a2-118">IDL</span><span class="sxs-lookup"><span data-stu-id="631a2-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="631a2-119"><dt>Mftransform. idl</dt></span><span class="sxs-lookup"><span data-stu-id="631a2-119"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="631a2-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="631a2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="631a2-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="631a2-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="631a2-122">**IMFTransform::P rocessEvent**</span><span class="sxs-lookup"><span data-stu-id="631a2-122">**IMFTransform::ProcessEvent**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
</dt> </dl>

 

 




