---
description: Specifica se il flusso di input è interlacciato.
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: Proprietà MFPKEY_COLORCONV_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8c01a6dce595eb270b734947492deea014259
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755495"
---
# <a name="mfpkey_colorconv_mode-property"></a><span data-ttu-id="73b9b-103">\_Proprietà modalità COLORCONV di MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="73b9b-103">MFPKEY\_COLORCONV\_MODE Property</span></span>

<span data-ttu-id="73b9b-104">Specifica se il flusso di input è interlacciato.</span><span class="sxs-lookup"><span data-stu-id="73b9b-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="73b9b-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="73b9b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="73b9b-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="73b9b-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="73b9b-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="73b9b-107">Data Type</span></span>

<span data-ttu-id="73b9b-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="73b9b-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="73b9b-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="73b9b-109">Default Value</span></span>

<span data-ttu-id="73b9b-110">Calcolato dal DSP dal video di origine.</span><span class="sxs-lookup"><span data-stu-id="73b9b-110">Computed by the DSP from the source video.</span></span>

## <a name="applies-to"></a><span data-ttu-id="73b9b-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="73b9b-111">Applies To</span></span>

-   [<span data-ttu-id="73b9b-112">Convertitore di colori DSP</span><span class="sxs-lookup"><span data-stu-id="73b9b-112">Color Converter DSP</span></span>](colorconverter.md)

## <a name="remarks"></a><span data-ttu-id="73b9b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="73b9b-113">Remarks</span></span>

<span data-ttu-id="73b9b-114">Usare uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="73b9b-114">Use one of the following values.</span></span>



| <span data-ttu-id="73b9b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="73b9b-115">Value</span></span> | <span data-ttu-id="73b9b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73b9b-116">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="73b9b-117">0</span><span class="sxs-lookup"><span data-stu-id="73b9b-117">0</span></span>     | <span data-ttu-id="73b9b-118">Progressivo</span><span class="sxs-lookup"><span data-stu-id="73b9b-118">Progressive</span></span> |
| <span data-ttu-id="73b9b-119">2</span><span class="sxs-lookup"><span data-stu-id="73b9b-119">2</span></span>     | <span data-ttu-id="73b9b-120">Interlaced</span><span class="sxs-lookup"><span data-stu-id="73b9b-120">Interlaced</span></span>  |



 

<span data-ttu-id="73b9b-121">Se questa proprietà non è impostata, il DSP usa il tipo di supporto di input per determinare se il video è interlacciato.</span><span class="sxs-lookup"><span data-stu-id="73b9b-121">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="73b9b-122">È possibile impostare questa proprietà per sostituire l'impostazione del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="73b9b-122">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="73b9b-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73b9b-123">Requirements</span></span>



| <span data-ttu-id="73b9b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="73b9b-124">Requirement</span></span> | <span data-ttu-id="73b9b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="73b9b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73b9b-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73b9b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="73b9b-127">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="73b9b-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="73b9b-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73b9b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="73b9b-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="73b9b-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="73b9b-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="73b9b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="73b9b-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="73b9b-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73b9b-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73b9b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73b9b-133">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="73b9b-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
