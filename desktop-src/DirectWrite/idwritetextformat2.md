---
title: Interfaccia IDWriteTextFormat2
description: Descrive le proprietà dei tipi di carattere e paragrafi usati per formattare il testo e descrive le informazioni sulle impostazioni locali. | Interfaccia IDWriteTextFormat2
ms.assetid: 4396d2b0-240f-ee8b-1d21-c4294fb29b51
keywords:
- Scrittura diretta dell'interfaccia IDWriteTextFormat2
- Scrittura diretta dell'interfaccia IDWriteTextFormat2, descritta
topic_type:
- apiref
api_name:
- IDWriteTextFormat2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06abf78095953f684ed6ec3fd241c699b2b37db4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321663"
---
# <a name="idwritetextformat2-interface"></a><span data-ttu-id="0b9e2-106">Interfaccia IDWriteTextFormat2</span><span class="sxs-lookup"><span data-stu-id="0b9e2-106">IDWriteTextFormat2 interface</span></span>

<span data-ttu-id="0b9e2-107">Descrive le proprietà dei tipi di carattere e paragrafi usati per formattare il testo e descrive le informazioni sulle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="0b9e2-107">Describes the font and paragraph properties used to format text, and it describes locale information.</span></span>

## <a name="members"></a><span data-ttu-id="0b9e2-108">Membri</span><span class="sxs-lookup"><span data-stu-id="0b9e2-108">Members</span></span>

<span data-ttu-id="0b9e2-109">L'interfaccia **IDWriteTextFormat2** eredita da [**IDWriteTextFormat1**](idwritetextformat1.md).</span><span class="sxs-lookup"><span data-stu-id="0b9e2-109">The **IDWriteTextFormat2** interface inherits from [**IDWriteTextFormat1**](idwritetextformat1.md).</span></span> <span data-ttu-id="0b9e2-110">**IDWriteTextFormat2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0b9e2-110">**IDWriteTextFormat2** also has these types of members:</span></span>

-   [<span data-ttu-id="0b9e2-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="0b9e2-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0b9e2-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="0b9e2-112">Methods</span></span>

<span data-ttu-id="0b9e2-113">L'interfaccia **IDWriteTextFormat2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0b9e2-113">The **IDWriteTextFormat2** interface has these methods.</span></span>



| <span data-ttu-id="0b9e2-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="0b9e2-114">Method</span></span>                                                      | <span data-ttu-id="0b9e2-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b9e2-115">Description</span></span>                                                                      |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="0b9e2-116">**GetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="0b9e2-116">**GetLineSpacing**</span></span>](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritetextformat2-getlinespacing) | <span data-ttu-id="0b9e2-117">Ottiene il set di regolazioni per spaziatura riga per un paragrafo di testo su più righe.</span><span class="sxs-lookup"><span data-stu-id="0b9e2-117">Gets the line spacing adjustment set for a multiline text paragraph.</span></span> <br/> |
| [<span data-ttu-id="0b9e2-118">**SetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="0b9e2-118">**SetLineSpacing**</span></span>](idwritetextformat2-setlinespacing.md) | <span data-ttu-id="0b9e2-119">Imposta spaziatura riga.</span><span class="sxs-lookup"><span data-stu-id="0b9e2-119">Set line spacing.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="0b9e2-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b9e2-120">Requirements</span></span>



| <span data-ttu-id="0b9e2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b9e2-121">Requirement</span></span> | <span data-ttu-id="0b9e2-122">Valore</span><span class="sxs-lookup"><span data-stu-id="0b9e2-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b9e2-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b9e2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0b9e2-124">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0b9e2-124">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="0b9e2-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b9e2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0b9e2-126">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0b9e2-126">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="0b9e2-127">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b9e2-127">Minimum supported phone</span></span><br/>  | <span data-ttu-id="0b9e2-128">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="0b9e2-128">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="0b9e2-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="0b9e2-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="0b9e2-130"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b9e2-130"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0b9e2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0b9e2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b9e2-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b9e2-132"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0b9e2-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b9e2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b9e2-134">**IDWriteTextFormat1**</span><span class="sxs-lookup"><span data-stu-id="0b9e2-134">**IDWriteTextFormat1**</span></span>](idwritetextformat1.md)
</dt> </dl>

 

