---
description: Specifica la modalità di controllo dell'intervallo dinamico che viene utilizzata dal decodificatore audio.
ms.assetid: 0dbe0c40-39ac-4c1b-9da2-9b142b5bb0eb
title: Proprietà MFPKEY_WMADEC_DRCMODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb612e08ff8bd799ec94faae68763f04db8ad052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226539"
---
# <a name="mfpkey_wmadec_drcmode-property"></a><span data-ttu-id="ee775-103">MFPKEY \_ WMADEC- \_ Proprietà DRCMODE</span><span class="sxs-lookup"><span data-stu-id="ee775-103">MFPKEY\_WMADEC\_DRCMODE Property</span></span>

<span data-ttu-id="ee775-104">Specifica la modalità di controllo dell'intervallo dinamico che viene utilizzata dal decodificatore audio.</span><span class="sxs-lookup"><span data-stu-id="ee775-104">Specifies the dynamic range control mode that the audio decoder will use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ee775-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ee775-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ee775-106">g \_ wszWMACDRCSetting</span><span class="sxs-lookup"><span data-stu-id="ee775-106">g\_wszWMACDRCSetting</span></span>

## <a name="data-type"></a><span data-ttu-id="ee775-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ee775-107">Data Type</span></span>

<span data-ttu-id="ee775-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ee775-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="ee775-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="ee775-109">Default Value</span></span>

<span data-ttu-id="ee775-110">0</span><span class="sxs-lookup"><span data-stu-id="ee775-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="ee775-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee775-111">Remarks</span></span>

<span data-ttu-id="ee775-112">Questo valore integer è compreso tra 0 e 2.</span><span class="sxs-lookup"><span data-stu-id="ee775-112">This integer value ranges from 0 to 2.</span></span> <span data-ttu-id="ee775-113">Maggiore è il valore, minore è l'intervallo dinamico dell'output audio non compresso.</span><span class="sxs-lookup"><span data-stu-id="ee775-113">The greater the value, the smaller the dynamic range of the uncompressed audio output.</span></span> <span data-ttu-id="ee775-114">Il valore 0 indica che il codec non esegue alcun controllo di intervallo dinamico, ovvero il codec non modifica l'intervallo dinamico intrinseco del contenuto codificato.</span><span class="sxs-lookup"><span data-stu-id="ee775-114">A value of 0 signals the codec to perform no dynamic range control, that is, the codec will not alter the inherent dynamic range of the encoded content.</span></span>

<span data-ttu-id="ee775-115">Se questo valore è impostato su 1 o 2, il codec utilizzerà le proprietà seguenti per determinare il controllo intervallo dinamico necessario:</span><span class="sxs-lookup"><span data-stu-id="ee775-115">If this value is set to 1 or 2, the codec will use the following properties to determine the needed dynamic range control:</span></span>

-   [<span data-ttu-id="ee775-116">MFPKEY \_ WMADRC \_ AVGREF</span><span class="sxs-lookup"><span data-stu-id="ee775-116">MFPKEY\_WMADRC\_AVGREF</span></span>](mfpkey-wmadrc-avgrefproperty.md)
-   [<span data-ttu-id="ee775-117">MFPKEY \_ WMADRC \_ PEAKREF</span><span class="sxs-lookup"><span data-stu-id="ee775-117">MFPKEY\_WMADRC\_PEAKREF</span></span>](mfpkey-wmadrc-peakrefproperty.md)
-   [<span data-ttu-id="ee775-118">MFPKEY \_ WMADRC \_ AVGTARGET</span><span class="sxs-lookup"><span data-stu-id="ee775-118">MFPKEY\_WMADRC\_AVGTARGET</span></span>](mfpkey-wmadrc-avgtargetproperty.md)
-   [<span data-ttu-id="ee775-119">MFPKEY \_ WMADRC \_ PEAKTARGET</span><span class="sxs-lookup"><span data-stu-id="ee775-119">MFPKEY\_WMADRC\_PEAKTARGET</span></span>](mfpkey-wmadrc-peaktargetproperty.md)

<span data-ttu-id="ee775-120">Se non si specificano valori di destinazione, il codec fornirà un proprio.</span><span class="sxs-lookup"><span data-stu-id="ee775-120">If you do not provide target values, the codec will provide its own.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee775-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee775-121">Requirements</span></span>



| <span data-ttu-id="ee775-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee775-122">Requirement</span></span> | <span data-ttu-id="ee775-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ee775-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee775-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee775-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ee775-125">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ee775-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ee775-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee775-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ee775-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ee775-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ee775-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee775-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee775-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee775-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee775-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee775-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee775-131">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ee775-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




