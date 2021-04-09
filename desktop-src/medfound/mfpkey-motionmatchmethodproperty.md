---
description: Specifica il metodo da usare per la corrispondenza di movimento.
ms.assetid: 75bbc189-3092-4813-9f45-54e8e48b05cd
title: Proprietà MFPKEY_MOTIONMATCHMETHOD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09496e714633dd394f55122b7461f29a2daa3656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967168"
---
# <a name="mfpkey_motionmatchmethod-property"></a><span data-ttu-id="40a7b-103">\_Proprietà MOTIONMATCHMETHOD di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="40a7b-103">MFPKEY\_MOTIONMATCHMETHOD Property</span></span>

<span data-ttu-id="40a7b-104">Specifica il metodo da usare per la corrispondenza di movimento.</span><span class="sxs-lookup"><span data-stu-id="40a7b-104">Specifies the method to use for motion matching.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="40a7b-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="40a7b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="40a7b-106">g \_ wszWMVCMotionMatchMethod</span><span class="sxs-lookup"><span data-stu-id="40a7b-106">g\_wszWMVCMotionMatchMethod</span></span>

## <a name="data-type"></a><span data-ttu-id="40a7b-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="40a7b-107">Data Type</span></span>

<span data-ttu-id="40a7b-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="40a7b-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="40a7b-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="40a7b-109">Default Value</span></span>

<span data-ttu-id="40a7b-110">0</span><span class="sxs-lookup"><span data-stu-id="40a7b-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="40a7b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="40a7b-111">Remarks</span></span>

<span data-ttu-id="40a7b-112">Questa proprietà può essere impostata su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="40a7b-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="40a7b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="40a7b-113">Value</span></span> | <span data-ttu-id="40a7b-114">Metodo utilizzato</span><span class="sxs-lookup"><span data-stu-id="40a7b-114">Method used</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="40a7b-115">0</span><span class="sxs-lookup"><span data-stu-id="40a7b-115">0</span></span>     | <span data-ttu-id="40a7b-116">somma delle differenze assolute (SAD)</span><span class="sxs-lookup"><span data-stu-id="40a7b-116">sum of absolute differences (SAD)</span></span> |
| <span data-ttu-id="40a7b-117">1</span><span class="sxs-lookup"><span data-stu-id="40a7b-117">1</span></span>     | <span data-ttu-id="40a7b-118">Hadamard</span><span class="sxs-lookup"><span data-stu-id="40a7b-118">Hadamard</span></span>                          |
| <span data-ttu-id="40a7b-119">-1</span><span class="sxs-lookup"><span data-stu-id="40a7b-119">-1</span></span>    | <span data-ttu-id="40a7b-120">Macroblocco-Adaptive.</span><span class="sxs-lookup"><span data-stu-id="40a7b-120">Macroblock-adaptive.</span></span>              |



 

<span data-ttu-id="40a7b-121">La somma delle differenze assolute (SAD) è un metodo più veloce ma meno accurato rispetto alla trasformazione Hadamard.</span><span class="sxs-lookup"><span data-stu-id="40a7b-121">The sum of absolute differences (SAD) is a faster but less accurate method than the Hadamard transform.</span></span> <span data-ttu-id="40a7b-122">La trasformazione Hadamard è più accurata ma a elevato utilizzo di calcolo.</span><span class="sxs-lookup"><span data-stu-id="40a7b-122">The Hadamard transform is more accurate but computationally intensive.</span></span> <span data-ttu-id="40a7b-123">La modalità adattiva macroblocco fornisce un ragionevole compromesso tra i due metodi scegliendo dinamicamente tra le due trasformazioni, selezionando la trasformazione Hadamard solo quando appropriato.</span><span class="sxs-lookup"><span data-stu-id="40a7b-123">The macroblock-adaptive mode provides a reasonable compromise between the two methods by dynamically choosing between the two transforms, selecting the Hadamard transform only when appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="40a7b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40a7b-124">Requirements</span></span>



| <span data-ttu-id="40a7b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="40a7b-125">Requirement</span></span> | <span data-ttu-id="40a7b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="40a7b-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40a7b-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40a7b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="40a7b-128">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="40a7b-128">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="40a7b-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40a7b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="40a7b-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="40a7b-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="40a7b-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40a7b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="40a7b-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="40a7b-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40a7b-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40a7b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40a7b-134">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="40a7b-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




