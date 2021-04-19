---
title: Metodo elemento IWMPPlaylistArray
description: Il metodo Item restituisce un'interfaccia IWMPPlaylist che rappresenta la playlist in corrispondenza dell'indice specificato.
ms.assetid: 5cb4b89f-b679-4d92-a5f9-5d0fe686775d
keywords:
- Metodo Item Media Player Windows
- Metodo Item Media Player Windows, interfaccia IWMPPlaylistArray
- Interfaccia IWMPPlaylistArray Windows Media Player, metodo Item
topic_type:
- apiref
api_name:
- IWMPPlaylistArray.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 660e919ef51bbb9584971f25bdf92296d331de23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329901"
---
# <a name="iwmpplaylistarrayitem-method"></a><span data-ttu-id="13fb2-106">Metodo IWMPPlaylistArray:: Item</span><span class="sxs-lookup"><span data-stu-id="13fb2-106">IWMPPlaylistArray::Item method</span></span>

<span data-ttu-id="13fb2-107">Il metodo **Item** restituisce un'interfaccia **IWMPPlaylist** che rappresenta la playlist in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="13fb2-107">The **Item** method returns an **IWMPPlaylist** interface representing the playlist at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="13fb2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13fb2-108">Syntax</span></span>


```CSharp
public IWMPPlaylist Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPPlaylist
Implements IWMPPlaylistArray.Item
```





## <a name="parameters"></a><span data-ttu-id="13fb2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="13fb2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13fb2-110">*lIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13fb2-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13fb2-111">**System. Int32** che contiene l'indice che identifica la playlist che il metodo deve recuperare.</span><span class="sxs-lookup"><span data-stu-id="13fb2-111">A **System.Int32** containing the index that identifies the playlist that the method should retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13fb2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="13fb2-112">Return value</span></span>

<span data-ttu-id="13fb2-113">Interfaccia **wmplib. IWMPPlaylist** per la playlist recuperata.</span><span class="sxs-lookup"><span data-stu-id="13fb2-113">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="13fb2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="13fb2-114">Remarks</span></span>

<span data-ttu-id="13fb2-115">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="13fb2-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="13fb2-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="13fb2-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="13fb2-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13fb2-117">Requirements</span></span>



| <span data-ttu-id="13fb2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="13fb2-118">Requirement</span></span> | <span data-ttu-id="13fb2-119">Valore</span><span class="sxs-lookup"><span data-stu-id="13fb2-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13fb2-120">Versione</span><span class="sxs-lookup"><span data-stu-id="13fb2-120">Version</span></span><br/>   | <span data-ttu-id="13fb2-121">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="13fb2-121">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="13fb2-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="13fb2-122">Namespace</span></span><br/> | <span data-ttu-id="13fb2-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="13fb2-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="13fb2-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="13fb2-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="13fb2-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="13fb2-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13fb2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13fb2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13fb2-127">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="13fb2-127">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="13fb2-128">**Interfaccia IWMPPlaylistArray (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="13fb2-128">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





