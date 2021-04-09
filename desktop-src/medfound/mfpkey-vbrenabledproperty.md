---
description: Specifica se il codificatore utilizza la codifica con velocità in bit variabile (VBR).
ms.assetid: e6826802-99b7-4a38-9b58-8a9cb8b753fb
title: Proprietà MFPKEY_VBRENABLED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9061abcc6ac7d7338b63eb5a7cd1a13ad22bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880773"
---
# <a name="mfpkey_vbrenabled-property"></a><span data-ttu-id="96f5a-103">\_Proprietà VBRENABLED di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="96f5a-103">MFPKEY\_VBRENABLED Property</span></span>

<span data-ttu-id="96f5a-104">Specifica se il codificatore utilizza la codifica con velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="96f5a-104">Specifies whether the encoder uses variable-bit-rate (VBR) encoding.</span></span> <span data-ttu-id="96f5a-105">Lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="96f5a-105">Read-write.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="96f5a-106">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="96f5a-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="96f5a-107">**g \_ wszWMVCVBREnabled**, **g \_ wszWMCPAudioVBRSupported**</span><span class="sxs-lookup"><span data-stu-id="96f5a-107">**g\_wszWMVCVBREnabled**, **g\_wszWMCPAudioVBRSupported**</span></span>

## <a name="data-type"></a><span data-ttu-id="96f5a-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="96f5a-108">Data Type</span></span>

<span data-ttu-id="96f5a-109">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="96f5a-109">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="96f5a-110">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="96f5a-110">Default Value</span></span>

<span data-ttu-id="96f5a-111">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="96f5a-111">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="96f5a-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="96f5a-112">Remarks</span></span>

<span data-ttu-id="96f5a-113">Questo valore deve essere impostato su **Variant \_ true** per qualsiasi altra proprietà VBR che verrà usata dal codec.</span><span class="sxs-lookup"><span data-stu-id="96f5a-113">This value must be set to **VARIANT\_TRUE** for any of the other VBR properties to be used by the codec.</span></span>

<span data-ttu-id="96f5a-114">Dopo aver impostato questo valore su **Variant \_ true** nel codificatore audio, i tipi di output recuperati usando il metodo [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) sono tipi VBR.</span><span class="sxs-lookup"><span data-stu-id="96f5a-114">After you set this value to **VARIANT\_TRUE** on the audio encoder, the output types retrieved by using the [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) method are VBR types.</span></span>

## <a name="requirements"></a><span data-ttu-id="96f5a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96f5a-115">Requirements</span></span>



| <span data-ttu-id="96f5a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="96f5a-116">Requirement</span></span> | <span data-ttu-id="96f5a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="96f5a-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96f5a-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96f5a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="96f5a-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="96f5a-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="96f5a-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96f5a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="96f5a-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="96f5a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="96f5a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96f5a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="96f5a-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="96f5a-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96f5a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96f5a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96f5a-125">**MFPKEY \_ vincolato \_ VBRQUALITY enumerato \_**</span><span class="sxs-lookup"><span data-stu-id="96f5a-125">**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**</span></span>](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[<span data-ttu-id="96f5a-126">**MFPKEY \_ desired \_ VBRQUALITY**</span><span class="sxs-lookup"><span data-stu-id="96f5a-126">**MFPKEY\_DESIRED\_VBRQUALITY**</span></span>](mfpkey-desired-vbrqualityproperty.md)
</dt> <dt>

[<span data-ttu-id="96f5a-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="96f5a-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
