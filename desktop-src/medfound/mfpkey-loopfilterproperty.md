---
description: Specifica se il codec deve usare il filtro di deblocco in ciclo durante la codifica.
ms.assetid: 395a356a-5f58-46b4-b2ff-47f98106f487
title: Proprietà MFPKEY_LOOPFILTER (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fbb723c4145f9769cc157d5db8eb7893d89b389
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310626"
---
# <a name="mfpkey_loopfilter-property"></a><span data-ttu-id="199cc-103">\_Proprietà LOOPFILTER di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="199cc-103">MFPKEY\_LOOPFILTER Property</span></span>

<span data-ttu-id="199cc-104">Specifica se il codec deve usare il filtro di deblocco in ciclo durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="199cc-104">Specifies whether the codec should use the in-loop deblocking filter during encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="199cc-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="199cc-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="199cc-106">g \_ wszWMVCLoopFilter</span><span class="sxs-lookup"><span data-stu-id="199cc-106">g\_wszWMVCLoopFilter</span></span>

## <a name="data-type"></a><span data-ttu-id="199cc-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="199cc-107">Data Type</span></span>

<span data-ttu-id="199cc-108">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="199cc-108">VT\_BOOL</span></span>

## <a name="remarks"></a><span data-ttu-id="199cc-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="199cc-109">Remarks</span></span>

<span data-ttu-id="199cc-110">Il filtro in ciclo è un metodo di deblocco che viene applicato durante la codifica e la decodifica, per ridurre gli artefatti di blocco in fase di codifica ("nel ciclo"), in modo che i fotogrammi P futuri e i fotogrammi B non li portino avanti.</span><span class="sxs-lookup"><span data-stu-id="199cc-110">The in-loop filter is a deblocking method that is applied during both encoding and decoding, to reduce blocking artifacts at encoding time ("in the loop") so that future P-frames and B-frames don't carry them forward.</span></span>

<span data-ttu-id="199cc-111">L'effetto dell'applicazione del filtro in ciclo è che i bordi dei blocchi macro nei fotogrammi video di output sono meno evidenti.</span><span class="sxs-lookup"><span data-stu-id="199cc-111">The effect of applying the in-loop filter is that the edges of the macro-blocks in the output video frames are less noticeable.</span></span> <span data-ttu-id="199cc-112">Allo stesso tempo l'immagine può diventare più flessibile.</span><span class="sxs-lookup"><span data-stu-id="199cc-112">At the same time the image can become softer in appearance.</span></span>

<span data-ttu-id="199cc-113">Sebbene il filtro in ciclo possa comportare una riduzione del dettaglio delle immagini in alcuni frame, la qualità complessiva del video trarrà vantaggio notevolmente.</span><span class="sxs-lookup"><span data-stu-id="199cc-113">Although the in-loop filter can lead to reduced image detail in some frames, the overall video quality will benefit noticeably.</span></span> <span data-ttu-id="199cc-114">Lo svantaggio principale dell'uso del filtro in ciclo è il costo aggiuntivo per le prestazioni di decodifica.</span><span class="sxs-lookup"><span data-stu-id="199cc-114">The biggest disadvantage to using in-loop filtering is the additional decoding performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="199cc-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="199cc-115">Requirements</span></span>



| <span data-ttu-id="199cc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="199cc-116">Requirement</span></span> | <span data-ttu-id="199cc-117">Valore</span><span class="sxs-lookup"><span data-stu-id="199cc-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="199cc-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="199cc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="199cc-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="199cc-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="199cc-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="199cc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="199cc-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="199cc-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="199cc-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="199cc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="199cc-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="199cc-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="199cc-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="199cc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="199cc-125">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="199cc-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




