---
description: 'MFPKEY_COLORCONV_MODE proprietà : specifica se il flusso di input è interlacciato.'
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: MFPKEY_COLORCONV_MODE proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c3f2d6256c4d7a9410264fb18703eea251e9c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087579"
---
# <a name="mfpkey_colorconv_mode-property"></a><span data-ttu-id="3b99b-103">Proprietà MFPKEY \_ COLORCONV \_ MODE</span><span class="sxs-lookup"><span data-stu-id="3b99b-103">MFPKEY\_COLORCONV\_MODE Property</span></span>

<span data-ttu-id="3b99b-104">Specifica se il flusso di input è interlacciato.</span><span class="sxs-lookup"><span data-stu-id="3b99b-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="3b99b-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="3b99b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="3b99b-106">Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)</span><span class="sxs-lookup"><span data-stu-id="3b99b-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="3b99b-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3b99b-107">Data Type</span></span>

<span data-ttu-id="3b99b-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="3b99b-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="3b99b-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="3b99b-109">Default Value</span></span>

<span data-ttu-id="3b99b-110">Calcolato dal DSP dal video di origine.</span><span class="sxs-lookup"><span data-stu-id="3b99b-110">Computed by the DSP from the source video.</span></span>

## <a name="applies-to"></a><span data-ttu-id="3b99b-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="3b99b-111">Applies To</span></span>

-   [<span data-ttu-id="3b99b-112">DSP convertitore di colori</span><span class="sxs-lookup"><span data-stu-id="3b99b-112">Color Converter DSP</span></span>](colorconverter.md)

## <a name="remarks"></a><span data-ttu-id="3b99b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b99b-113">Remarks</span></span>

<span data-ttu-id="3b99b-114">Usare uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3b99b-114">Use one of the following values.</span></span>



| <span data-ttu-id="3b99b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3b99b-115">Value</span></span> | <span data-ttu-id="3b99b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b99b-116">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="3b99b-117">0</span><span class="sxs-lookup"><span data-stu-id="3b99b-117">0</span></span>     | <span data-ttu-id="3b99b-118">Progressivo</span><span class="sxs-lookup"><span data-stu-id="3b99b-118">Progressive</span></span> |
| <span data-ttu-id="3b99b-119">2</span><span class="sxs-lookup"><span data-stu-id="3b99b-119">2</span></span>     | <span data-ttu-id="3b99b-120">Interlaced</span><span class="sxs-lookup"><span data-stu-id="3b99b-120">Interlaced</span></span>  |



 

<span data-ttu-id="3b99b-121">Se questa proprietà non è impostata, il DSP usa il tipo di supporto di input per determinare se il video è interlacciato.</span><span class="sxs-lookup"><span data-stu-id="3b99b-121">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="3b99b-122">È possibile impostare questa proprietà per eseguire l'override dell'impostazione del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="3b99b-122">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b99b-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b99b-123">Requirements</span></span>



| <span data-ttu-id="3b99b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b99b-124">Requirement</span></span> | <span data-ttu-id="3b99b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3b99b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b99b-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b99b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3b99b-127">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3b99b-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3b99b-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b99b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3b99b-129">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b99b-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3b99b-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b99b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b99b-131"><dt>Wmcodecdsp.h</dt></span><span class="sxs-lookup"><span data-stu-id="3b99b-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b99b-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b99b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b99b-133">Media Foundation proprietà</span><span class="sxs-lookup"><span data-stu-id="3b99b-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
