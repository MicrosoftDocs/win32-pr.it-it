---
description: Specifica il numero di thread che il codificatore utilizzerà.
ms.assetid: 2f463cba-2512-455d-9ce1-8797682d4d67
title: Proprietà MFPKEY_NUMTHREADS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c93f6d38e3bb79bbb692f9bec1b1dc0edb232d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528663"
---
# <a name="mfpkey_numthreads-property"></a><span data-ttu-id="2f301-103">\_Proprietà numThreads di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="2f301-103">MFPKEY\_NUMTHREADS Property</span></span>

<span data-ttu-id="2f301-104">Specifica il numero di thread che il codificatore utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="2f301-104">Specifies the number of threads that the encoder will use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2f301-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="2f301-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2f301-106">g \_ wszWMVCNumThreads</span><span class="sxs-lookup"><span data-stu-id="2f301-106">g\_wszWMVCNumThreads</span></span>

## <a name="data-type"></a><span data-ttu-id="2f301-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2f301-107">Data Type</span></span>

<span data-ttu-id="2f301-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="2f301-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="2f301-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="2f301-109">Default Value</span></span>

<span data-ttu-id="2f301-110">1</span><span class="sxs-lookup"><span data-stu-id="2f301-110">1</span></span>

## <a name="remarks"></a><span data-ttu-id="2f301-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f301-111">Remarks</span></span>

<span data-ttu-id="2f301-112">Questo valore è destinato a dividere la codifica in più thread per sfruttare i vantaggi dei computer con più processori.</span><span class="sxs-lookup"><span data-stu-id="2f301-112">This value is intended to divide encoding into multiple threads to take advantage of computers with multiple processors.</span></span> <span data-ttu-id="2f301-113">Suddividere le attività di codifica in più thread può causare una lieve riduzione della qualità rispetto a un singolo thread.</span><span class="sxs-lookup"><span data-stu-id="2f301-113">Splitting encoding tasks into multiple threads can cause a slight decrease in quality as compared to a single thread.</span></span>

<span data-ttu-id="2f301-114">Per il codificatore video (wmvencod.dll) rilasciato con Windows XP e Windows Vista, questa proprietà deve essere impostata su 1, 2 o 4.</span><span class="sxs-lookup"><span data-stu-id="2f301-114">For the video encoder (wmvencod.dll) released with Windows XP and Windows Vista, this property should be set to 1, 2, or 4.</span></span> <span data-ttu-id="2f301-115">Gli altri valori verranno arrotondati per difetto.</span><span class="sxs-lookup"><span data-stu-id="2f301-115">Other values will be rounded down.</span></span>

<span data-ttu-id="2f301-116">Per il codificatore video (wmvencod.dll) rilasciato con Windows 7, questa proprietà deve essere impostata su 1, 2, 4 o 8.</span><span class="sxs-lookup"><span data-stu-id="2f301-116">For the video encoder (wmvencod.dll) released with Windows 7, this property should be set to 1, 2, 4, or 8.</span></span> <span data-ttu-id="2f301-117">Gli altri valori verranno arrotondati per difetto.</span><span class="sxs-lookup"><span data-stu-id="2f301-117">Other values will be rounded down.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f301-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f301-118">Requirements</span></span>



| <span data-ttu-id="2f301-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f301-119">Requirement</span></span> | <span data-ttu-id="2f301-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2f301-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f301-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f301-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2f301-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2f301-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2f301-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f301-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2f301-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2f301-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2f301-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f301-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f301-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f301-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f301-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f301-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f301-128">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2f301-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




