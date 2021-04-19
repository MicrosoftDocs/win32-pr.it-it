---
description: Rappresenta un elenco di parole che è possibile utilizzare per migliorare il risultato del riconoscimento.
ms.assetid: d189fd13-ec69-45dc-8be4-fea48f337636
title: Classe InkWord (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkWordList
- InkWordList.IInkWordList
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 7f3bbf077758bfd0449f5bca1ba3739342fa3658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317931"
---
# <a name="inkwordlist-class"></a><span data-ttu-id="5ef32-103">Classe InkWord</span><span class="sxs-lookup"><span data-stu-id="5ef32-103">InkWordList class</span></span>

<span data-ttu-id="5ef32-104">Rappresenta un elenco di parole che è possibile utilizzare per migliorare il risultato del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="5ef32-104">Represents a list of words that can be used to improve the recognition result.</span></span>

<span data-ttu-id="5ef32-105">L' **InkWord** è costituito da questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5ef32-105">**InkWordList** has these types of members:</span></span>

-   [<span data-ttu-id="5ef32-106">Interfacce</span><span class="sxs-lookup"><span data-stu-id="5ef32-106">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="5ef32-107">Metodi</span><span class="sxs-lookup"><span data-stu-id="5ef32-107">Methods</span></span>](#methods)

### <a name="interfaces"></a><span data-ttu-id="5ef32-108">Interfacce</span><span class="sxs-lookup"><span data-stu-id="5ef32-108">Interfaces</span></span>

<span data-ttu-id="5ef32-109">La classe **InkWord** definisce queste interfacce.</span><span class="sxs-lookup"><span data-stu-id="5ef32-109">The **InkWordList** class defines these interfaces.</span></span>



| <span data-ttu-id="5ef32-110">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="5ef32-110">Interface</span></span>        | <span data-ttu-id="5ef32-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ef32-111">Description</span></span>                                                           |
|:-----------------|:----------------------------------------------------------------------|
| <span data-ttu-id="5ef32-112">**IInkWordList**</span><span class="sxs-lookup"><span data-stu-id="5ef32-112">**IInkWordList**</span></span> | <span data-ttu-id="5ef32-113">Questo oggetto implementa l'interfaccia com **IInkWordList** .</span><span class="sxs-lookup"><span data-stu-id="5ef32-113">This object implements the **IInkWordList** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="5ef32-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="5ef32-114">Methods</span></span>

<span data-ttu-id="5ef32-115">La classe **InkWord** ha questi metodi.</span><span class="sxs-lookup"><span data-stu-id="5ef32-115">The **InkWordList** class has these methods.</span></span>



| <span data-ttu-id="5ef32-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="5ef32-116">Method</span></span>                                       | <span data-ttu-id="5ef32-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ef32-117">Description</span></span>                                                             |
|:---------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="5ef32-118">**AddWord**</span><span class="sxs-lookup"><span data-stu-id="5ef32-118">**AddWord**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-addword)       | <span data-ttu-id="5ef32-119">Aggiunge una singola parola all'oggetto **InkWord**.</span><span class="sxs-lookup"><span data-stu-id="5ef32-119">Adds a single word to the **InkWordList**.</span></span><br/>                   |
| [<span data-ttu-id="5ef32-120">**Unione**</span><span class="sxs-lookup"><span data-stu-id="5ef32-120">**Merge**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-merge)           | <span data-ttu-id="5ef32-121">Unisce un altro **InkWord** a in questo **InkWord**.</span><span class="sxs-lookup"><span data-stu-id="5ef32-121">Merges another **InkWordList** to into this **InkWordList**.</span></span><br/> |
| [<span data-ttu-id="5ef32-122">**RemoveWord**</span><span class="sxs-lookup"><span data-stu-id="5ef32-122">**RemoveWord**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-removeword) | <span data-ttu-id="5ef32-123">Rimuove una singola parola da un oggetto **InkWord**.</span><span class="sxs-lookup"><span data-stu-id="5ef32-123">Removes a single word from a **InkWordList**.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="5ef32-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ef32-124">Remarks</span></span>

<span data-ttu-id="5ef32-125">È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.</span><span class="sxs-lookup"><span data-stu-id="5ef32-125">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ef32-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ef32-126">Requirements</span></span>



| <span data-ttu-id="5ef32-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ef32-127">Requirement</span></span> | <span data-ttu-id="5ef32-128">Valore</span><span class="sxs-lookup"><span data-stu-id="5ef32-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ef32-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ef32-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5ef32-130">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5ef32-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5ef32-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ef32-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5ef32-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5ef32-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="5ef32-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ef32-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ef32-134"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5ef32-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5ef32-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="5ef32-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="5ef32-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ef32-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="5ef32-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ef32-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ef32-138">**Proprietà WordList**</span><span class="sxs-lookup"><span data-stu-id="5ef32-138">**WordList Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)
</dt> <dt>

[<span data-ttu-id="5ef32-139">Costanti controllo oggetto</span><span class="sxs-lookup"><span data-stu-id="5ef32-139">Factoid Constants</span></span>](factoid-constants.md)
</dt> <dt>

[<span data-ttu-id="5ef32-140">**Classe InkRecognizerContext**</span><span class="sxs-lookup"><span data-stu-id="5ef32-140">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> </dl>

 

