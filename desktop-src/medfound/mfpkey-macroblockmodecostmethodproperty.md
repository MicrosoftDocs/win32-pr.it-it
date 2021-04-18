---
description: Specifica il metodo di costo utilizzato dal codec per determinare la modalità di macroblocco da utilizzare.
ms.assetid: 2ba9b943-0daa-40c1-87ea-2fa647fb7095
title: Proprietà MFPKEY_MACROBLOCKMODECOSTMETHOD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289219300a79c67565891c48cec848851c17bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310624"
---
# <a name="mfpkey_macroblockmodecostmethod-property"></a><span data-ttu-id="a53af-103">\_Proprietà MACROBLOCKMODECOSTMETHOD di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="a53af-103">MFPKEY\_MACROBLOCKMODECOSTMETHOD Property</span></span>

<span data-ttu-id="a53af-104">Specifica il metodo di costo utilizzato dal codec per determinare la modalità di macroblocco da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="a53af-104">Specifies the cost method used by the codec to determine which macroblock mode to use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a53af-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="a53af-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a53af-106">g \_ wszWMVCMacroblockModeCostMethod</span><span class="sxs-lookup"><span data-stu-id="a53af-106">g\_wszWMVCMacroblockModeCostMethod</span></span>

## <a name="data-type"></a><span data-ttu-id="a53af-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a53af-107">Data Type</span></span>

<span data-ttu-id="a53af-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="a53af-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="a53af-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="a53af-109">Default Value</span></span>

<span data-ttu-id="a53af-110">0</span><span class="sxs-lookup"><span data-stu-id="a53af-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="a53af-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a53af-111">Remarks</span></span>

<span data-ttu-id="a53af-112">Questa proprietà può essere impostata su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a53af-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="a53af-113">Valore</span><span class="sxs-lookup"><span data-stu-id="a53af-113">Value</span></span> | <span data-ttu-id="a53af-114">Metodo utilizzato</span><span class="sxs-lookup"><span data-stu-id="a53af-114">Method used</span></span>                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a53af-115">0</span><span class="sxs-lookup"><span data-stu-id="a53af-115">0</span></span>     | <span data-ttu-id="a53af-116">TRISTE/Hadamard.</span><span class="sxs-lookup"><span data-stu-id="a53af-116">SAD/Hadamard.</span></span> <span data-ttu-id="a53af-117">Questa opzione consente di configurare il codec in modo da usare solo la distorsione durante il calcolo dei costi.</span><span class="sxs-lookup"><span data-stu-id="a53af-117">This option configures the codec to use only distortion when computing cost.</span></span>             |
| <span data-ttu-id="a53af-118">1</span><span class="sxs-lookup"><span data-stu-id="a53af-118">1</span></span>     | <span data-ttu-id="a53af-119">Costo RD.</span><span class="sxs-lookup"><span data-stu-id="a53af-119">RD cost.</span></span> <span data-ttu-id="a53af-120">Questa opzione consente di configurare il codec per tenere conto della velocità e della distorsione durante il calcolo dei costi.</span><span class="sxs-lookup"><span data-stu-id="a53af-120">This option configures the codec to account for both rate and distortion when computing cost.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="a53af-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a53af-121">Requirements</span></span>



| <span data-ttu-id="a53af-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a53af-122">Requirement</span></span> | <span data-ttu-id="a53af-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a53af-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a53af-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a53af-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a53af-125">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a53af-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a53af-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a53af-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a53af-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a53af-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a53af-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a53af-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a53af-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a53af-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a53af-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a53af-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a53af-131">\_MOTIONMATCHMETHOD MFPKEY</span><span class="sxs-lookup"><span data-stu-id="a53af-131">MFPKEY\_MOTIONMATCHMETHOD</span></span>](mfpkey-motionmatchmethodproperty.md)
</dt> <dt>

[<span data-ttu-id="a53af-132">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a53af-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




