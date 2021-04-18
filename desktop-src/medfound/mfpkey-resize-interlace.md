---
description: Specifica se il flusso di input è interlacciato.
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: Proprietà MFPKEY_RESIZE_INTERLACE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a27504bd6da92bc48fee04afc999568a514fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310609"
---
# <a name="mfpkey_resize_interlace-property"></a><span data-ttu-id="c5282-103">MFPKEY \_ Ridimensiona la \_ Proprietà interlacciamento</span><span class="sxs-lookup"><span data-stu-id="c5282-103">MFPKEY\_RESIZE\_INTERLACE Property</span></span>

<span data-ttu-id="c5282-104">Specifica se il flusso di input è interlacciato.</span><span class="sxs-lookup"><span data-stu-id="c5282-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c5282-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c5282-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c5282-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="c5282-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="c5282-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c5282-107">Data Type</span></span>

<span data-ttu-id="c5282-108">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="c5282-108">VT\_BOOL</span></span>

## <a name="applies-to"></a><span data-ttu-id="c5282-109">Si applica a</span><span class="sxs-lookup"><span data-stu-id="c5282-109">Applies To</span></span>

-   [<span data-ttu-id="c5282-110">Ridimensionamento video DSP</span><span class="sxs-lookup"><span data-stu-id="c5282-110">Video Resizer DSP</span></span>](videoresizer.md)

## <a name="remarks"></a><span data-ttu-id="c5282-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5282-111">Remarks</span></span>

<span data-ttu-id="c5282-112">Usare uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="c5282-112">Use one of the following values:</span></span>



| <span data-ttu-id="c5282-113">Valore</span><span class="sxs-lookup"><span data-stu-id="c5282-113">Value</span></span>     | <span data-ttu-id="c5282-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5282-114">Description</span></span> |
|-----------|-------------|
| <span data-ttu-id="c5282-115">VT \_ false</span><span class="sxs-lookup"><span data-stu-id="c5282-115">VT\_FALSE</span></span> | <span data-ttu-id="c5282-116">Progressivo</span><span class="sxs-lookup"><span data-stu-id="c5282-116">Progressive</span></span> |
| <span data-ttu-id="c5282-117">VT \_ true</span><span class="sxs-lookup"><span data-stu-id="c5282-117">VT\_TRUE</span></span>  | <span data-ttu-id="c5282-118">Interlaced</span><span class="sxs-lookup"><span data-stu-id="c5282-118">Interlaced</span></span>  |



 

<span data-ttu-id="c5282-119">Se questa proprietà non è impostata, il DSP usa il tipo di supporto di input per determinare se il video è interlacciato.</span><span class="sxs-lookup"><span data-stu-id="c5282-119">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="c5282-120">È possibile impostare questa proprietà per sostituire l'impostazione del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="c5282-120">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5282-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5282-121">Requirements</span></span>



| <span data-ttu-id="c5282-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5282-122">Requirement</span></span> | <span data-ttu-id="c5282-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c5282-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5282-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5282-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c5282-125">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c5282-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c5282-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5282-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c5282-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c5282-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c5282-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5282-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5282-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5282-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5282-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5282-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5282-131">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c5282-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
