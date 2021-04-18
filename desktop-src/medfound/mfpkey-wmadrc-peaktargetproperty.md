---
description: Specifica il livello di volume massimo desiderato per il contenuto audio di output.
ms.assetid: 231b7296-ca80-4918-bae6-674b976db24c
title: Proprietà MFPKEY_WMADRC_PEAKTARGET (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c40fa68e2b580c5d3e8550d6e46c9f6b9fe4bfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310262"
---
# <a name="mfpkey_wmadrc_peaktarget-property"></a><span data-ttu-id="cb2a2-103">MFPKEY \_ WMADRC- \_ Proprietà PEAKTARGET</span><span class="sxs-lookup"><span data-stu-id="cb2a2-103">MFPKEY\_WMADRC\_PEAKTARGET Property</span></span>

<span data-ttu-id="cb2a2-104">Specifica il livello di volume massimo desiderato per il contenuto audio di output.</span><span class="sxs-lookup"><span data-stu-id="cb2a2-104">Specifies the desired maximum volume level of output audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="cb2a2-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="cb2a2-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="cb2a2-106">g \_ wszWMADRCPeakTarget</span><span class="sxs-lookup"><span data-stu-id="cb2a2-106">g\_wszWMADRCPeakTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="cb2a2-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="cb2a2-107">Data Type</span></span>

<span data-ttu-id="cb2a2-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="cb2a2-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="cb2a2-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="cb2a2-109">Default Value</span></span>

<span data-ttu-id="cb2a2-110">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="cb2a2-110">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb2a2-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb2a2-111">Remarks</span></span>

<span data-ttu-id="cb2a2-112">È possibile impostare questo valore nel decodificatore allo scopo di un controllo intervallo dinamico, ma avrà effetto solo se viene impostata la proprietà [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="cb2a2-112">You can set this value on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

<span data-ttu-id="cb2a2-113">Se si richiede il controllo dinamico degli intervalli dal decodificatore quando questa proprietà non è impostata, il codec calcolerà un valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="cb2a2-113">If you request dynamic range control from the decoder when this property is not set, the codec will compute a default value.</span></span>

<span data-ttu-id="cb2a2-114">Usare le proprietà [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) e [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md) per calcolare i valori appropriati per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb2a2-114">Use the [MFPKEY\_WMADRC\_AVGREF](mfpkey-wmadrc-avgrefproperty.md) and [MFPKEY\_WMADRC\_PEAKREF](mfpkey-wmadrc-peakrefproperty.md) properties to compute appropriate values for this property.</span></span>

<span data-ttu-id="cb2a2-115">Per ulteriori informazioni sul controllo dinamico degli intervalli, vedere l'articolo Web [Windows Media audio funzionalità dei codec professionali](/previous-versions/ms867218(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="cb2a2-115">For more information on dynamic range control, see the web article [Windows Media Audio Professional Codec Features](/previous-versions/ms867218(v=msdn.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb2a2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb2a2-116">Requirements</span></span>



| <span data-ttu-id="cb2a2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb2a2-117">Requirement</span></span> | <span data-ttu-id="cb2a2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="cb2a2-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb2a2-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb2a2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cb2a2-120">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cb2a2-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cb2a2-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb2a2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cb2a2-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cb2a2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cb2a2-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb2a2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb2a2-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb2a2-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb2a2-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb2a2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb2a2-126">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cb2a2-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
