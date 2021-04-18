---
title: IWMPPlaylist-proprietà conteggio
description: La proprietà Count ottiene il numero di elementi multimediali in una playlist.
ms.assetid: dbff3c86-2d42-4d47-a5cb-b8199efac728
keywords:
- conteggio delle proprietà di Windows Media Player
- Proprietà Count Media Player Windows, interfaccia IWMPPlaylist
- Interfaccia IWMPPlaylist Windows Media Player, proprietà Count
topic_type:
- apiref
api_name:
- IWMPPlaylist.count
- IWMPPlaylist.get_count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d988fefc436b65652d2b0765320ca289417c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330977"
---
# <a name="iwmpplaylistcount-property"></a><span data-ttu-id="b9f98-106">Proprietà IWMPPlaylist:: count</span><span class="sxs-lookup"><span data-stu-id="b9f98-106">IWMPPlaylist::count property</span></span>

<span data-ttu-id="b9f98-107">La proprietà **count** ottiene il numero di elementi multimediali in una playlist.</span><span class="sxs-lookup"><span data-stu-id="b9f98-107">The **count** property gets the number of media items in a playlist.</span></span>

<span data-ttu-id="b9f98-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b9f98-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9f98-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9f98-109">Syntax</span></span>


```CSharp
public System.Int32 count {get;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="b9f98-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b9f98-110">Property value</span></span>

<span data-ttu-id="b9f98-111">**System. Int32** che rappresenta il numero di elementi multimediali nella playlist.</span><span class="sxs-lookup"><span data-stu-id="b9f98-111">A **System.Int32** that is the number of media items in the playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9f98-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9f98-112">Remarks</span></span>

<span data-ttu-id="b9f98-113">Prima di utilizzare questa proprietà, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="b9f98-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="b9f98-114">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b9f98-114">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="b9f98-115">Per il codice di esempio che usa questa proprietà, vedere la proprietà [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) .</span><span class="sxs-lookup"><span data-stu-id="b9f98-115">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9f98-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9f98-116">Requirements</span></span>



| <span data-ttu-id="b9f98-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9f98-117">Requirement</span></span> | <span data-ttu-id="b9f98-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b9f98-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9f98-119">Versione</span><span class="sxs-lookup"><span data-stu-id="b9f98-119">Version</span></span><br/>   | <span data-ttu-id="b9f98-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="b9f98-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b9f98-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b9f98-121">Namespace</span></span><br/> | <span data-ttu-id="b9f98-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b9f98-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b9f98-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="b9f98-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b9f98-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b9f98-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9f98-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9f98-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9f98-126">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b9f98-126">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





