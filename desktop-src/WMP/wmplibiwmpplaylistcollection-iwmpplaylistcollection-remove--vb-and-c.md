---
title: Metodo Remove IWMPPlaylistCollection
description: Il metodo Remove rimuove una playlist dalla libreria. | Metodo Remove IWMPPlaylistCollection
ms.assetid: 40c8ee1d-13fa-40d9-9532-4dc8383c4eb3
keywords:
- rimuovere il metodo Windows Media Player
- Metodo Remove Media Player Windows, interfaccia IWMPPlaylistCollection
- Interfaccia IWMPPlaylistCollection Windows Media Player, Remove (metodo)
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99fbaa2f60c769599bd6173b8e38f4d99e9f42d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333912"
---
# <a name="iwmpplaylistcollectionremove-method"></a><span data-ttu-id="d9929-107">Metodo IWMPPlaylistCollection:: Remove</span><span class="sxs-lookup"><span data-stu-id="d9929-107">IWMPPlaylistCollection::remove method</span></span>

<span data-ttu-id="d9929-108">Il metodo **Remove** rimuove una playlist dalla libreria.</span><span class="sxs-lookup"><span data-stu-id="d9929-108">The **remove** method removes a playlist from the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9929-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9929-109">Syntax</span></span>


```CSharp
public void remove(
  IWMPPlaylist pItem
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPPlaylist _
)
Implements IWMPPlaylistCollection.remove
```





## <a name="parameters"></a><span data-ttu-id="d9929-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9929-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9929-111">*pItem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9929-111">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9929-112">Interfaccia **wmplib. IWMPPlaylist** per la playlist che verrà rimossa da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="d9929-112">A **WMPLib.IWMPPlaylist** interface for the playlist that this method will remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9929-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9929-113">Return value</span></span>

<span data-ttu-id="d9929-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d9929-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9929-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9929-115">Remarks</span></span>

<span data-ttu-id="d9929-116">Prima di chiamare questo metodo, è necessario disporre dell'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="d9929-116">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="d9929-117">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="d9929-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9929-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9929-118">Requirements</span></span>



| <span data-ttu-id="d9929-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9929-119">Requirement</span></span> | <span data-ttu-id="d9929-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d9929-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9929-121">Versione</span><span class="sxs-lookup"><span data-stu-id="d9929-121">Version</span></span><br/>   | <span data-ttu-id="d9929-122">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="d9929-122">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="d9929-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d9929-123">Namespace</span></span><br/> | <span data-ttu-id="d9929-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d9929-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d9929-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="d9929-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d9929-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d9929-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9929-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9929-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9929-128">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d9929-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d9929-129">**Interfaccia IWMPPlaylistCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d9929-129">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





