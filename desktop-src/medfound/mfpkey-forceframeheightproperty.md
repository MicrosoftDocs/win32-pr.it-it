---
description: Specifica un'altezza del frame intermedia per il video codificato.
ms.assetid: 7382ec31-6d59-4e8c-94eb-804786074038
title: Proprietà MFPKEY_FORCEFRAMEHEIGHT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e4662ce56ea4c20d44abdd05641219bc6b94ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227009"
---
# <a name="mfpkey_forceframeheight-property"></a><span data-ttu-id="c293c-103">\_Proprietà FORCEFRAMEHEIGHT di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="c293c-103">MFPKEY\_FORCEFRAMEHEIGHT Property</span></span>

<span data-ttu-id="c293c-104">Specifica un'altezza del frame intermedia per il video codificato.</span><span class="sxs-lookup"><span data-stu-id="c293c-104">Specifies an intermediate frame height for encoded video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c293c-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c293c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c293c-106">g \_ wszWMVCForceFrameHeight</span><span class="sxs-lookup"><span data-stu-id="c293c-106">g\_wszWMVCForceFrameHeight</span></span>

## <a name="data-type"></a><span data-ttu-id="c293c-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c293c-107">Data Type</span></span>

<span data-ttu-id="c293c-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c293c-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="c293c-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="c293c-109">Remarks</span></span>

<span data-ttu-id="c293c-110">È possibile impostare questo valore e la [proprietà \_ FORCEFRAMEWIDTH di MFPKEY](mfpkey-forceframewidthproperty.md) per forzare il codificatore a codificare il flusso video con una dimensione del frame inferiore alle dimensioni del frame di input o di output.</span><span class="sxs-lookup"><span data-stu-id="c293c-110">You can set this value and the [MFPKEY\_FORCEFRAMEWIDTH](mfpkey-forceframewidthproperty.md) property to force the encoder to encode the video stream with a frame size that is smaller than the input or output frame sizes.</span></span> <span data-ttu-id="c293c-111">Una volta decodificato, il video verrà ridimensionato in base alla risoluzione di input originale.</span><span class="sxs-lookup"><span data-stu-id="c293c-111">When decoded, the video will be resized to its original input resolution.</span></span>

<span data-ttu-id="c293c-112">Dimensioni del frame valide su entrambi gli assi sono da 2 a 8192 pixel.</span><span class="sxs-lookup"><span data-stu-id="c293c-112">Valid frame dimensions on either axis are 2 to 8192 pixels.</span></span> <span data-ttu-id="c293c-113">Le dimensioni del frame devono essere divisibili per 2.</span><span class="sxs-lookup"><span data-stu-id="c293c-113">Frame dimensions must be divisible by 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="c293c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c293c-114">Requirements</span></span>



| <span data-ttu-id="c293c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c293c-115">Requirement</span></span> | <span data-ttu-id="c293c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c293c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c293c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c293c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c293c-118">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c293c-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c293c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c293c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c293c-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c293c-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c293c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c293c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c293c-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c293c-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c293c-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c293c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c293c-124">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c293c-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




