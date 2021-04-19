---
title: IWMPStringCollection-proprietà conteggio
description: La proprietà Count ottiene il numero di elementi nell'insieme di stringhe.
ms.assetid: 0ba2d158-fa54-46a8-9124-8a412e71bd09
keywords:
- conteggio delle proprietà di Windows Media Player
- Proprietà Count Media Player Windows, interfaccia IWMPStringCollection
- Interfaccia IWMPStringCollection Windows Media Player, proprietà Count
topic_type:
- apiref
api_name:
- IWMPStringCollection.count
- IWMPStringCollection.get_count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00c520ab346737d1599d79d80ea3acd36c9b84fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333100"
---
# <a name="iwmpstringcollectioncount-property"></a><span data-ttu-id="d7e16-106">Proprietà IWMPStringCollection:: count</span><span class="sxs-lookup"><span data-stu-id="d7e16-106">IWMPStringCollection::count property</span></span>

<span data-ttu-id="d7e16-107">La proprietà **count** ottiene il numero di elementi nell'insieme di stringhe.</span><span class="sxs-lookup"><span data-stu-id="d7e16-107">The **count** property gets the number of items in the string collection.</span></span>

<span data-ttu-id="d7e16-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d7e16-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7e16-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7e16-109">Syntax</span></span>


```CSharp
public System.Int32 count {get;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="d7e16-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d7e16-110">Property value</span></span>

<span data-ttu-id="d7e16-111">**System. Int32** che rappresenta il numero di elementi nell'insieme di stringhe.</span><span class="sxs-lookup"><span data-stu-id="d7e16-111">A **System.Int32** that is the number of items in the string collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7e16-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7e16-112">Remarks</span></span>

<span data-ttu-id="d7e16-113">Prima di utilizzare questa proprietà, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="d7e16-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="d7e16-114">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="d7e16-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7e16-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7e16-115">Requirements</span></span>



| <span data-ttu-id="d7e16-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7e16-116">Requirement</span></span> | <span data-ttu-id="d7e16-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d7e16-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7e16-118">Versione</span><span class="sxs-lookup"><span data-stu-id="d7e16-118">Version</span></span><br/>   | <span data-ttu-id="d7e16-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="d7e16-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d7e16-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d7e16-120">Namespace</span></span><br/> | <span data-ttu-id="d7e16-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d7e16-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d7e16-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="d7e16-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d7e16-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d7e16-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7e16-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7e16-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7e16-125">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d7e16-125">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d7e16-126">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d7e16-126">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d7e16-127">**Interfaccia IWMPStringCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d7e16-127">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





