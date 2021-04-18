---
description: Specifica se il flusso di bit video codificato contiene un valore di completezza del buffer con ogni fotogramma chiave.
ms.assetid: 5574ee3c-ccb3-4ff6-8280-efe5626e6dd6
title: Proprietà MFPKEY_BUFFERFULLNESSINFIRSTBYTE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fbcdb6306faeb7481f1cc7be20088ff0cedd5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318401"
---
# <a name="mfpkey_bufferfullnessinfirstbyte-property"></a><span data-ttu-id="26e24-103">\_Proprietà BUFFERFULLNESSINFIRSTBYTE di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="26e24-103">MFPKEY\_BUFFERFULLNESSINFIRSTBYTE Property</span></span>

<span data-ttu-id="26e24-104">Specifica se il flusso di bit video codificato contiene un valore di completezza del buffer con ogni fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="26e24-104">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="26e24-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="26e24-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="26e24-106">g \_ wszWMVCBufferFullnessInFirstByte</span><span class="sxs-lookup"><span data-stu-id="26e24-106">g\_wszWMVCBufferFullnessInFirstByte</span></span>

## <a name="data-type"></a><span data-ttu-id="26e24-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="26e24-107">Data Type</span></span>

<span data-ttu-id="26e24-108">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="26e24-108">VT\_BOOL</span></span>

## <a name="remarks"></a><span data-ttu-id="26e24-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="26e24-109">Remarks</span></span>

<span data-ttu-id="26e24-110">Prima di ottenere questo valore, è necessario impostare un tipo di output.</span><span class="sxs-lookup"><span data-stu-id="26e24-110">You must set an output type before getting this value.</span></span>

<span data-ttu-id="26e24-111">È possibile ottenere il valore di questa proprietà utilizzando [IWMCodecProps:: GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span><span class="sxs-lookup"><span data-stu-id="26e24-111">You can get the value of this property using [IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span></span> <span data-ttu-id="26e24-112">Se si usa **IPropertyBag**, è innanzitutto necessario impostare il valore fourcc del formato compresso desiderato con la proprietà [MFPKEY \_ fourcc](mfpkey-fourccproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="26e24-112">If you use **IPropertyBag**, you must first set the FOURCC value of the desired compressed format with the [MFPKEY\_FOURCC](mfpkey-fourccproperty.md) property.</span></span>

<span data-ttu-id="26e24-113">La completezza del buffer nel primo byte di tutti i fotogrammi chiave consente di determinare le dimensioni del buffer necessarie per la concatenazione di flussi video compressi.</span><span class="sxs-lookup"><span data-stu-id="26e24-113">Having the buffer fullness in the first byte of all key frames enables you to determine the buffer size required when concatenating compressed video streams.</span></span>

## <a name="requirements"></a><span data-ttu-id="26e24-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26e24-114">Requirements</span></span>



| <span data-ttu-id="26e24-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="26e24-115">Requirement</span></span> | <span data-ttu-id="26e24-116">Valore</span><span class="sxs-lookup"><span data-stu-id="26e24-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26e24-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26e24-117">Minimum supported client</span></span><br/> | <span data-ttu-id="26e24-118">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="26e24-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="26e24-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26e24-119">Minimum supported server</span></span><br/> | <span data-ttu-id="26e24-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="26e24-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="26e24-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26e24-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="26e24-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="26e24-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26e24-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26e24-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26e24-124">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="26e24-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




