---
description: Specifica il modello di conformità del dispositivo che si vuole usare per la codifica video.
ms.assetid: cd2c068a-dbbc-42c5-bc92-bbb73f0259d1
title: Proprietà MFPKEY_DECODERCOMPLEXITYREQUESTED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e017361d7e8267d33ecb2cfdbce2a6e79758fac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310639"
---
# <a name="mfpkey_decodercomplexityrequested-property"></a><span data-ttu-id="d2a4f-103">\_Proprietà DECODERCOMPLEXITYREQUESTED di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="d2a4f-103">MFPKEY\_DECODERCOMPLEXITYREQUESTED Property</span></span>

<span data-ttu-id="d2a4f-104">Specifica il modello di conformità del dispositivo che si vuole usare per la codifica video.</span><span class="sxs-lookup"><span data-stu-id="d2a4f-104">Specifies the device conformance template that you want to use for video encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="d2a4f-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d2a4f-105">Data Type</span></span>

<span data-ttu-id="d2a4f-106">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="d2a4f-106">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="d2a4f-107">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="d2a4f-107">Default Value</span></span>

<span data-ttu-id="d2a4f-108">1</span><span class="sxs-lookup"><span data-stu-id="d2a4f-108">1</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d2a4f-109">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d2a4f-109">Constant for IPropertyBag</span></span>

<span data-ttu-id="d2a4f-110">g \_ wszWMVCDecoderComplexityRequested</span><span class="sxs-lookup"><span data-stu-id="d2a4f-110">g\_wszWMVCDecoderComplexityRequested</span></span>

## <a name="data-type-for-ipropertybag"></a><span data-ttu-id="d2a4f-111">Tipo di dati per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d2a4f-111">Data Type for IPropertyBag</span></span>

<span data-ttu-id="d2a4f-112">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="d2a4f-112">VT\_BSTR</span></span>

## <a name="default-value-for-ipropertybag"></a><span data-ttu-id="d2a4f-113">Valore predefinito per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d2a4f-113">Default Value for IPropertyBag</span></span>

<span data-ttu-id="d2a4f-114">MP</span><span class="sxs-lookup"><span data-stu-id="d2a4f-114">"MP"</span></span>

## <a name="remarks"></a><span data-ttu-id="d2a4f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2a4f-115">Remarks</span></span>

<span data-ttu-id="d2a4f-116">Il codec tenterà di codificare il contenuto usando il modello di conformità del dispositivo specificato da questo valore.</span><span class="sxs-lookup"><span data-stu-id="d2a4f-116">The codec will attempt to encode the content using the device conformance template specified by this value.</span></span> <span data-ttu-id="d2a4f-117">Il modello effettivo in cui è conforme il contenuto codificato può essere recuperato dalla proprietà [MFPKEY \_ DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md) dopo la codifica.</span><span class="sxs-lookup"><span data-stu-id="d2a4f-117">The actual template to which the encoded content conforms can be retrieved from the [MFPKEY\_DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md) property after encoding.</span></span>

<span data-ttu-id="d2a4f-118">Questa proprietà deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d2a4f-118">This property must be one of the following values.</span></span>



| <span data-ttu-id="d2a4f-119">Valore per IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="d2a4f-119">Value for IPropertyStore</span></span> | <span data-ttu-id="d2a4f-120">Valore per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d2a4f-120">Value for IPropertyBag</span></span> | <span data-ttu-id="d2a4f-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2a4f-121">Description</span></span>         |
|--------------------------|------------------------|---------------------|
| <span data-ttu-id="d2a4f-122">0</span><span class="sxs-lookup"><span data-stu-id="d2a4f-122">0</span></span>                        | <span data-ttu-id="d2a4f-123">SP</span><span class="sxs-lookup"><span data-stu-id="d2a4f-123">"SP"</span></span>                   | <span data-ttu-id="d2a4f-124">Profilo semplice</span><span class="sxs-lookup"><span data-stu-id="d2a4f-124">simple profile</span></span>      |
| <span data-ttu-id="d2a4f-125">1</span><span class="sxs-lookup"><span data-stu-id="d2a4f-125">1</span></span>                        | <span data-ttu-id="d2a4f-126">MP</span><span class="sxs-lookup"><span data-stu-id="d2a4f-126">"MP"</span></span>                   | <span data-ttu-id="d2a4f-127">profilo principale</span><span class="sxs-lookup"><span data-stu-id="d2a4f-127">main profile</span></span>        |
| <span data-ttu-id="d2a4f-128">2</span><span class="sxs-lookup"><span data-stu-id="d2a4f-128">2</span></span>                        | <span data-ttu-id="d2a4f-129">CP</span><span class="sxs-lookup"><span data-stu-id="d2a4f-129">"CP"</span></span>                   | <span data-ttu-id="d2a4f-130">non più supportato</span><span class="sxs-lookup"><span data-stu-id="d2a4f-130">no longer supported</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d2a4f-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2a4f-131">Requirements</span></span>



| <span data-ttu-id="d2a4f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2a4f-132">Requirement</span></span> | <span data-ttu-id="d2a4f-133">Valore</span><span class="sxs-lookup"><span data-stu-id="d2a4f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a4f-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2a4f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d2a4f-135">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d2a4f-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d2a4f-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2a4f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d2a4f-137">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d2a4f-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d2a4f-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2a4f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2a4f-139"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2a4f-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2a4f-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2a4f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2a4f-141">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d2a4f-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




