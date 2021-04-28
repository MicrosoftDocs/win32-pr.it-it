---
description: 'MFPKEY_RESIZE_INTERLACE proprietà : specifica se il flusso di input è interlacciato.'
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: MFPKEY_RESIZE_INTERLACE proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d0efe93901a08322a05dbed2515f76b04a214b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092879"
---
# <a name="mfpkey_resize_interlace-property"></a><span data-ttu-id="76395-103">Proprietà \_ INTERLACE MFPKEY RESIZE \_</span><span class="sxs-lookup"><span data-stu-id="76395-103">MFPKEY\_RESIZE\_INTERLACE Property</span></span>

<span data-ttu-id="76395-104">Specifica se il flusso di input è interlacciato.</span><span class="sxs-lookup"><span data-stu-id="76395-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="76395-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="76395-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="76395-106">Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)</span><span class="sxs-lookup"><span data-stu-id="76395-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="76395-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="76395-107">Data Type</span></span>

<span data-ttu-id="76395-108">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="76395-108">VT\_BOOL</span></span>

## <a name="applies-to"></a><span data-ttu-id="76395-109">Si applica a</span><span class="sxs-lookup"><span data-stu-id="76395-109">Applies To</span></span>

-   [<span data-ttu-id="76395-110">DSP di Ridimensionamento video</span><span class="sxs-lookup"><span data-stu-id="76395-110">Video Resizer DSP</span></span>](videoresizer.md)

## <a name="remarks"></a><span data-ttu-id="76395-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="76395-111">Remarks</span></span>

<span data-ttu-id="76395-112">Usare uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="76395-112">Use one of the following values:</span></span>



| <span data-ttu-id="76395-113">Valore</span><span class="sxs-lookup"><span data-stu-id="76395-113">Value</span></span>     | <span data-ttu-id="76395-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76395-114">Description</span></span> |
|-----------|-------------|
| <span data-ttu-id="76395-115">VT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="76395-115">VT\_FALSE</span></span> | <span data-ttu-id="76395-116">Progressivo</span><span class="sxs-lookup"><span data-stu-id="76395-116">Progressive</span></span> |
| <span data-ttu-id="76395-117">VT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="76395-117">VT\_TRUE</span></span>  | <span data-ttu-id="76395-118">Interlaced</span><span class="sxs-lookup"><span data-stu-id="76395-118">Interlaced</span></span>  |



 

<span data-ttu-id="76395-119">Se questa proprietà non è impostata, il DSP usa il tipo di supporto di input per determinare se il video è interlacciato.</span><span class="sxs-lookup"><span data-stu-id="76395-119">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="76395-120">È possibile impostare questa proprietà per eseguire l'override dell'impostazione del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="76395-120">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="76395-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76395-121">Requirements</span></span>



| <span data-ttu-id="76395-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="76395-122">Requirement</span></span> | <span data-ttu-id="76395-123">Valore</span><span class="sxs-lookup"><span data-stu-id="76395-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76395-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76395-124">Minimum supported client</span></span><br/> | <span data-ttu-id="76395-125">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="76395-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="76395-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76395-126">Minimum supported server</span></span><br/> | <span data-ttu-id="76395-127">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="76395-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="76395-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76395-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="76395-129"><dt>Wmcodecdsp.h</dt></span><span class="sxs-lookup"><span data-stu-id="76395-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76395-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76395-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76395-131">Media Foundation proprietà</span><span class="sxs-lookup"><span data-stu-id="76395-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
