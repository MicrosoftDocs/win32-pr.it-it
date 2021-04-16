---
description: Specifica una larghezza del frame intermedia per il video codificato.
ms.assetid: 805bd587-31af-49b8-b5ab-2dcf2a3f81c5
title: Proprietà MFPKEY_FORCEFRAMEWIDTH (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea4c8c7ac025de1c089c592a591136df966797d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528669"
---
# <a name="mfpkey_forceframewidth-property"></a><span data-ttu-id="c10a9-103">\_Proprietà FORCEFRAMEWIDTH di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="c10a9-103">MFPKEY\_FORCEFRAMEWIDTH Property</span></span>

<span data-ttu-id="c10a9-104">Specifica una larghezza del frame intermedia per il video codificato.</span><span class="sxs-lookup"><span data-stu-id="c10a9-104">Specifies an intermediate frame width for encoded video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c10a9-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c10a9-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c10a9-106">g \_ wszWMVCForceFrameWidth</span><span class="sxs-lookup"><span data-stu-id="c10a9-106">g\_wszWMVCForceFrameWidth</span></span>

## <a name="data-type"></a><span data-ttu-id="c10a9-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c10a9-107">Data Type</span></span>

<span data-ttu-id="c10a9-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c10a9-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="c10a9-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="c10a9-109">Remarks</span></span>

<span data-ttu-id="c10a9-110">È possibile impostare questo valore e la [proprietà \_ FORCEFRAMEHEIGHT di MFPKEY](mfpkey-forceframeheightproperty.md) per forzare il codificatore a codificare il flusso video con una dimensione del frame inferiore alle dimensioni del frame di input o di output.</span><span class="sxs-lookup"><span data-stu-id="c10a9-110">You can set this value and the [MFPKEY\_FORCEFRAMEHEIGHT](mfpkey-forceframeheightproperty.md) property to force the encoder to encode the video stream with a frame size that is smaller than the input or output frame sizes.</span></span> <span data-ttu-id="c10a9-111">Una volta decodificato, il video verrà ridimensionato in base alla risoluzione di input originale.</span><span class="sxs-lookup"><span data-stu-id="c10a9-111">When decoded, the video will be resized to its original input resolution.</span></span>

<span data-ttu-id="c10a9-112">Dimensioni del frame valide su entrambi gli assi sono da 2 a 8192 pixel.</span><span class="sxs-lookup"><span data-stu-id="c10a9-112">Valid frame dimensions on either axis are 2 to 8192 pixels.</span></span> <span data-ttu-id="c10a9-113">Le dimensioni del frame devono essere divisibili per 2.</span><span class="sxs-lookup"><span data-stu-id="c10a9-113">Frame dimensions must be divisible by 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="c10a9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c10a9-114">Requirements</span></span>



| <span data-ttu-id="c10a9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c10a9-115">Requirement</span></span> | <span data-ttu-id="c10a9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c10a9-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c10a9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c10a9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c10a9-118">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c10a9-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c10a9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c10a9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c10a9-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c10a9-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c10a9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c10a9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c10a9-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c10a9-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c10a9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c10a9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c10a9-124">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c10a9-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




