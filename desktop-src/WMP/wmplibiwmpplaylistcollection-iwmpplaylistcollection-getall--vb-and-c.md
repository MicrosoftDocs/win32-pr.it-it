---
title: Metodo IWMPPlaylistCollection getAll
description: Il metodo getAll restituisce un'interfaccia IWMPPlaylistArray che fornisce l'accesso a tutte le playlist nella libreria.
ms.assetid: d36dbc5c-ccb0-400a-ab5b-918598c218f1
keywords:
- Metodo getAll Windows Media Player
- Metodo getAll Windows Media Player, interfaccia IWMPPlaylistCollection
- Interfaccia IWMPPlaylistCollection Windows Media Player, metodo getAll
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4260f5c960650cf6c04a1dd8b39d887f711fb8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329899"
---
# <a name="iwmpplaylistcollectiongetall-method"></a><span data-ttu-id="95097-106">Metodo IWMPPlaylistCollection:: getAll</span><span class="sxs-lookup"><span data-stu-id="95097-106">IWMPPlaylistCollection::getAll method</span></span>

<span data-ttu-id="95097-107">Il metodo **GetAll** restituisce un'interfaccia **IWMPPlaylistArray** che fornisce l'accesso a tutte le playlist nella libreria.</span><span class="sxs-lookup"><span data-stu-id="95097-107">The **getAll** method returns an **IWMPPlaylistArray** interface that provides access to all of the playlists in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="95097-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95097-108">Syntax</span></span>


```CSharp
public IWMPPlaylistArray getAll();
```


```VB

Public Function getAll() As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getAll
```





## <a name="parameters"></a><span data-ttu-id="95097-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="95097-109">Parameters</span></span>

<span data-ttu-id="95097-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="95097-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="95097-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95097-111">Return value</span></span>

<span data-ttu-id="95097-112">Interfaccia **wmplib. IWMPPlaylistArray** per la matrice di playlist recuperata.</span><span class="sxs-lookup"><span data-stu-id="95097-112">A **WMPLib.IWMPPlaylistArray** interface for the retrieved array of playlists.</span></span>

## <a name="remarks"></a><span data-ttu-id="95097-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="95097-113">Remarks</span></span>

<span data-ttu-id="95097-114">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="95097-114">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="95097-115">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="95097-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95097-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95097-116">Requirements</span></span>



| <span data-ttu-id="95097-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="95097-117">Requirement</span></span> | <span data-ttu-id="95097-118">Valore</span><span class="sxs-lookup"><span data-stu-id="95097-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95097-119">Versione</span><span class="sxs-lookup"><span data-stu-id="95097-119">Version</span></span><br/>   | <span data-ttu-id="95097-120">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="95097-120">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="95097-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="95097-121">Namespace</span></span><br/> | <span data-ttu-id="95097-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="95097-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="95097-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="95097-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="95097-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="95097-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95097-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95097-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95097-126">**Interfaccia IWMPPlaylistArray (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="95097-126">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="95097-127">**Interfaccia IWMPPlaylistCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="95097-127">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





