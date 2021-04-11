---
description: Specifica il livello di volume medio desiderato per il contenuto audio di output.
ms.assetid: 2e59537f-ee14-4186-b312-297225e91120
title: Proprietà MFPKEY_WMADRC_AVGTARGET (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4503161ac6e392a50fd7535592b84ea92d6136
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226916"
---
# <a name="mfpkey_wmadrc_avgtarget-property"></a><span data-ttu-id="d7fd6-103">MFPKEY \_ WMADRC- \_ Proprietà AVGTARGET</span><span class="sxs-lookup"><span data-stu-id="d7fd6-103">MFPKEY\_WMADRC\_AVGTARGET Property</span></span>

<span data-ttu-id="d7fd6-104">Specifica il livello di volume medio desiderato per il contenuto audio di output.</span><span class="sxs-lookup"><span data-stu-id="d7fd6-104">Specifies the desired average volume level of output audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d7fd6-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d7fd6-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d7fd6-106">g \_ wszWMADRCAverageTarget</span><span class="sxs-lookup"><span data-stu-id="d7fd6-106">g\_wszWMADRCAverageTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="d7fd6-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d7fd6-107">Data Type</span></span>

<span data-ttu-id="d7fd6-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="d7fd6-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="d7fd6-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="d7fd6-109">Default Value</span></span>

<span data-ttu-id="d7fd6-110">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="d7fd6-110">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7fd6-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7fd6-111">Remarks</span></span>

<span data-ttu-id="d7fd6-112">È possibile impostare questo valore nel decodificatore allo scopo di un controllo intervallo dinamico, ma avrà effetto solo se viene impostata la proprietà [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="d7fd6-112">You can set this value on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

> [!Note]  
> <span data-ttu-id="d7fd6-113">Non è consigliabile impostare il valore di destinazione medio.</span><span class="sxs-lookup"><span data-stu-id="d7fd6-113">Setting the average target value is not recommended.</span></span> <span data-ttu-id="d7fd6-114">La regolazione del valore medio non influisce sulla differenza tra sonorità e suoni morbidi.</span><span class="sxs-lookup"><span data-stu-id="d7fd6-114">Adjusting the average value does not affect the difference between loud and soft sounds.</span></span> <span data-ttu-id="d7fd6-115">Viene invece tagliato o incrementato il volume medio complessivo che può causare una distorsione indesiderata durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="d7fd6-115">Instead, it cuts or boosts the overall average volume which may cause undesirable distortion during playback.</span></span>

 

<span data-ttu-id="d7fd6-116">Se si richiede il controllo dinamico degli intervalli dal decodificatore quando questa proprietà non è impostata, il codec calcolerà un valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="d7fd6-116">If you request dynamic range control from the decoder when this property is not set, the codec will compute a default value.</span></span>

<span data-ttu-id="d7fd6-117">Usare le proprietà [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) e [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md) per calcolare i valori appropriati per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="d7fd6-117">Use the [MFPKEY\_WMADRC\_AVGREF](mfpkey-wmadrc-avgrefproperty.md) and [MFPKEY\_WMADRC\_PEAKREF](mfpkey-wmadrc-peakrefproperty.md) properties to compute appropriate values for this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7fd6-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7fd6-118">Requirements</span></span>



| <span data-ttu-id="d7fd6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7fd6-119">Requirement</span></span> | <span data-ttu-id="d7fd6-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d7fd6-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7fd6-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7fd6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d7fd6-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d7fd6-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d7fd6-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7fd6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d7fd6-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d7fd6-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d7fd6-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d7fd6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7fd6-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7fd6-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7fd6-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7fd6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7fd6-128">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d7fd6-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




