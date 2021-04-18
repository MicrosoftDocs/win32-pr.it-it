---
title: Interfaccia IDWriteTextLayout3
description: Rappresenta un blocco di testo dopo che è stato completamente analizzato e formattato. | Interfaccia IDWriteTextLayout3
ms.assetid: a7741740-9524-caf0-650b-56808abcf328
keywords:
- Scrittura diretta dell'interfaccia IDWriteTextLayout3
- Scrittura diretta dell'interfaccia IDWriteTextLayout3, descritta
topic_type:
- apiref
api_name:
- IDWriteTextLayout3
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78a7a9203245939e40b522e0ef5998be0764085a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321695"
---
# <a name="idwritetextlayout3-interface"></a><span data-ttu-id="8fcb0-106">Interfaccia IDWriteTextLayout3</span><span class="sxs-lookup"><span data-stu-id="8fcb0-106">IDWriteTextLayout3 interface</span></span>

<span data-ttu-id="8fcb0-107">Rappresenta un blocco di testo dopo che è stato completamente analizzato e formattato.</span><span class="sxs-lookup"><span data-stu-id="8fcb0-107">Represents a block of text after it has been fully analyzed and formatted.</span></span>

## <a name="members"></a><span data-ttu-id="8fcb0-108">Membri</span><span class="sxs-lookup"><span data-stu-id="8fcb0-108">Members</span></span>

<span data-ttu-id="8fcb0-109">L'interfaccia **IDWriteTextLayout3** eredita da [**IDWriteTextLayout2**](idwritetextlayout2.md).</span><span class="sxs-lookup"><span data-stu-id="8fcb0-109">The **IDWriteTextLayout3** interface inherits from [**IDWriteTextLayout2**](idwritetextlayout2.md).</span></span> <span data-ttu-id="8fcb0-110">**IDWriteTextLayout3** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8fcb0-110">**IDWriteTextLayout3** also has these types of members:</span></span>

-   [<span data-ttu-id="8fcb0-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="8fcb0-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8fcb0-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="8fcb0-112">Methods</span></span>

<span data-ttu-id="8fcb0-113">L'interfaccia **IDWriteTextLayout3** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="8fcb0-113">The **IDWriteTextLayout3** interface has these methods.</span></span>



| <span data-ttu-id="8fcb0-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="8fcb0-114">Method</span></span>                                                          | <span data-ttu-id="8fcb0-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fcb0-115">Description</span></span>                                                                                                                                                                                                                                                          |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8fcb0-116">**GetLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="8fcb0-116">**GetLineMetrics**</span></span>](idwritetextlayout3-getlinemetrics.md)     | <span data-ttu-id="8fcb0-117">Recupera le proprietà di ogni riga.</span><span class="sxs-lookup"><span data-stu-id="8fcb0-117">Retrieves properties of each line.</span></span><br/>                                                                                                                                                                                                                        |
| [<span data-ttu-id="8fcb0-118">**GetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="8fcb0-118">**GetLineSpacing**</span></span>](idwritetextlayout3-getlinespacing.md)     | <span data-ttu-id="8fcb0-119">Ottiene le informazioni sulla spaziatura riga.</span><span class="sxs-lookup"><span data-stu-id="8fcb0-119">Gets line spacing information.</span></span><br/>                                                                                                                                                                                                                            |
| [<span data-ttu-id="8fcb0-120">**InvalidateLayout**</span><span class="sxs-lookup"><span data-stu-id="8fcb0-120">**InvalidateLayout**</span></span>](idwritetextlayout3-invalidatelayout.md) | <span data-ttu-id="8fcb0-121">Invalida il layout, forzando il layout da rimisurare prima di chiamare le metriche o le funzioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="8fcb0-121">Invalidates the layout, forcing layout to remeasure before calling the metrics or drawing functions.</span></span> <span data-ttu-id="8fcb0-122">Questa operazione è utile se la località di un tipo di carattere viene modificata e il layout deve essere ridisegnato o se le dimensioni di un client implementate IDWriteInlineObject cambiano.</span><span class="sxs-lookup"><span data-stu-id="8fcb0-122">This is useful if the locality of a font changes, and layout should be redrawn, or if the size of a client implemented IDWriteInlineObject changes.</span></span> <br/> |
| [<span data-ttu-id="8fcb0-123">**SetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="8fcb0-123">**SetLineSpacing**</span></span>](idwritetextlayout3-setlinespacing.md)     | <span data-ttu-id="8fcb0-124">Imposta spaziatura riga.</span><span class="sxs-lookup"><span data-stu-id="8fcb0-124">Set line spacing.</span></span><br/>                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="8fcb0-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fcb0-125">Requirements</span></span>



| <span data-ttu-id="8fcb0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fcb0-126">Requirement</span></span> | <span data-ttu-id="8fcb0-127">Valore</span><span class="sxs-lookup"><span data-stu-id="8fcb0-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fcb0-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fcb0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8fcb0-129">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8fcb0-129">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="8fcb0-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fcb0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8fcb0-131">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8fcb0-131">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="8fcb0-132">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fcb0-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="8fcb0-133">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="8fcb0-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="8fcb0-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="8fcb0-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="8fcb0-135"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8fcb0-135"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8fcb0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8fcb0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fcb0-137"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fcb0-137"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8fcb0-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fcb0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fcb0-139">**IDWriteTextLayout2**</span><span class="sxs-lookup"><span data-stu-id="8fcb0-139">**IDWriteTextLayout2**</span></span>](idwritetextlayout2.md)
</dt> </dl>

 

 





