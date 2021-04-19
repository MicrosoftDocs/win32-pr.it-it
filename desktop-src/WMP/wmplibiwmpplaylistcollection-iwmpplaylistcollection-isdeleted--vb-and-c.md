---
title: Metodo IWMPPlaylistCollection eliminato
description: Il metodo isvalidd restituisce un valore che indica se la playlist specificata si trova nella cartella Deleted Items.
ms.assetid: 02bc4b9f-6149-4fe2-8417-6484b22f2d74
keywords:
- Metodo eliminato Media Player Windows
- Metodo di eliminazione di Windows Media Player, interfaccia IWMPPlaylistCollection
- Interfaccia IWMPPlaylistCollection Windows Media Player, metodo eliminato
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.isDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4ce4a314378c5a4a211a52b99ea1b36ae1fda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324066"
---
# <a name="iwmpplaylistcollectionisdeleted-method"></a><span data-ttu-id="aef8e-106">Metodo IWMPPlaylistCollection:: IsValid</span><span class="sxs-lookup"><span data-stu-id="aef8e-106">IWMPPlaylistCollection::isDeleted method</span></span>

<span data-ttu-id="aef8e-107">Il **Metodo** isvalidd restituisce un valore che indica se la playlist specificata si trova nella cartella Deleted Items.</span><span class="sxs-lookup"><span data-stu-id="aef8e-107">The **isDeleted** method returns a value indicating whether the specified playlist is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="aef8e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aef8e-108">Syntax</span></span>


```CSharp
public System.Boolean isDeleted(
  IWMPPlaylist pItem
);
```


```VB

Public Function isDeleted( _
  ByVal pItem As IWMPPlaylist _
) As System.Boolean
Implements IWMPPlaylistCollection.isDeleted
```





## <a name="parameters"></a><span data-ttu-id="aef8e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="aef8e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aef8e-110">*pItem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aef8e-110">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aef8e-111">Interfaccia **wmplib. IWMPPlaylist** per la playlist sottoposta a query.</span><span class="sxs-lookup"><span data-stu-id="aef8e-111">A **WMPLib.IWMPPlaylist** interface for the queried playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aef8e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aef8e-112">Return value</span></span>

<span data-ttu-id="aef8e-113">**System. Boolean** che specifica se la playlist è stata eliminata.</span><span class="sxs-lookup"><span data-stu-id="aef8e-113">A **System.Boolean** that specifies whether the playlist was deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="aef8e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aef8e-114">Requirements</span></span>



| <span data-ttu-id="aef8e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="aef8e-115">Requirement</span></span> | <span data-ttu-id="aef8e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="aef8e-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aef8e-117">Versione</span><span class="sxs-lookup"><span data-stu-id="aef8e-117">Version</span></span><br/>   | <span data-ttu-id="aef8e-118">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="aef8e-118">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="aef8e-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="aef8e-119">Namespace</span></span><br/> | <span data-ttu-id="aef8e-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="aef8e-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="aef8e-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="aef8e-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="aef8e-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="aef8e-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aef8e-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aef8e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aef8e-124">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="aef8e-124">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="aef8e-125">**Interfaccia IWMPPlaylistCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="aef8e-125">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





