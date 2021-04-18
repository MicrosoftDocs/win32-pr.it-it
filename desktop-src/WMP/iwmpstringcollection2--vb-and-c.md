---
title: Interfaccia IWMPStringCollection2 (VB e C) (WMP. h)
description: Fornisce metodi che integrano l'interfaccia IWMPStringCollection.
ms.assetid: be93ff47-7f76-4b5e-ad30-3094a75147c8
keywords:
- Interfaccia IWMPStringCollection2 (VB e C) Windows Media Player
- Interfaccia IWMPStringCollection2 (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPStringCollection2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184e1a16ea0e6b33cc5b67eaeac6b050e5cda97a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329200"
---
# <a name="iwmpstringcollection2-vb-and-c-interface"></a><span data-ttu-id="ef9a2-105">Interfaccia IWMPStringCollection2 (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="ef9a2-105">IWMPStringCollection2 (VB and C#) interface</span></span>

<span data-ttu-id="ef9a2-106">Fornisce metodi che integrano l'interfaccia **IWMPStringCollection** .</span><span class="sxs-lookup"><span data-stu-id="ef9a2-106">Provides methods that supplement the **IWMPStringCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="ef9a2-107">Membri</span><span class="sxs-lookup"><span data-stu-id="ef9a2-107">Members</span></span>

<span data-ttu-id="ef9a2-108">L'interfaccia **IWMPStringCollection2 (VB e C#)** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ef9a2-108">The **IWMPStringCollection2 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="ef9a2-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="ef9a2-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ef9a2-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="ef9a2-110">Methods</span></span>

<span data-ttu-id="ef9a2-111">L'interfaccia **IWMPStringCollection2 (VB e C#)** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ef9a2-111">The **IWMPStringCollection2 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="ef9a2-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="ef9a2-112">Method</span></span>                                                                                                                 | <span data-ttu-id="ef9a2-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef9a2-113">Description</span></span>                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef9a2-114">**getAttributeCountByType**</span><span class="sxs-lookup"><span data-stu-id="ef9a2-114">**getAttributeCountByType**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getattributecountbytype--vb-and-c.md) | <span data-ttu-id="ef9a2-115">Restituisce il numero di attributi associati all'indice dell'elemento della raccolta di stringhe, al nome dell'attributo e alla lingua specificati.</span><span class="sxs-lookup"><span data-stu-id="ef9a2-115">Returns the number of attributes associated with the specified string collection item index, attribute name, and language.</span></span><br/> |
| [<span data-ttu-id="ef9a2-116">**getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="ef9a2-116">**getItemInfo**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)                         | <span data-ttu-id="ef9a2-117">Restituisce la stringa corrispondente all'indice e al nome dell'elemento della raccolta di stringhe specificato.</span><span class="sxs-lookup"><span data-stu-id="ef9a2-117">Returns the string corresponding to the specified string collection item index and name.</span></span><br/>                                   |
| [<span data-ttu-id="ef9a2-118">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="ef9a2-118">**getItemInfoByType**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)             | <span data-ttu-id="ef9a2-119">Restituisce il valore corrispondente all'indice dell'elemento della raccolta di stringhe, al nome, alla lingua e all'indice dell'attributo specificati.</span><span class="sxs-lookup"><span data-stu-id="ef9a2-119">Returns the value corresponding to the specified string collection item index, name, language, and attribute index.</span></span><br/>        |
| [<span data-ttu-id="ef9a2-120">**Identico**</span><span class="sxs-lookup"><span data-stu-id="ef9a2-120">**isIdentical**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-isidentical--vb-and-c.md)                         | <span data-ttu-id="ef9a2-121">Restituisce un valore che indica se l'oggetto fornito è uguale a quello corrente.</span><span class="sxs-lookup"><span data-stu-id="ef9a2-121">Returns a value indicating whether the supplied object is the same as the current one.</span></span><br/>                                     |



 

<span data-ttu-id="ef9a2-122">Ottenere un'interfaccia **IWMPStringCollection2** eseguendo il cast del valore restituito dal metodo [**IWMPMediaCollection. getAttributeStringCollection**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getattributestringcollection) .</span><span class="sxs-lookup"><span data-stu-id="ef9a2-122">Get an **IWMPStringCollection2** interface by casting the value returned by the [**IWMPMediaCollection.getAttributeStringCollection**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getattributestringcollection) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef9a2-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef9a2-123">Requirements</span></span>



| <span data-ttu-id="ef9a2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef9a2-124">Requirement</span></span> | <span data-ttu-id="ef9a2-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ef9a2-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef9a2-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef9a2-126">Header</span></span><br/> | <dl> <span data-ttu-id="ef9a2-127"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef9a2-127"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef9a2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef9a2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef9a2-129">**Interfacce per Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="ef9a2-129">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="ef9a2-130">**Interfaccia IWMPStringCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ef9a2-130">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





