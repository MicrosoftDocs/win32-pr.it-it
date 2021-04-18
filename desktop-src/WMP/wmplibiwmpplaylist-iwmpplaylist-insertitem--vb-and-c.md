---
title: Metodo insertItem IWMPPlaylist
description: Il metodo insertItem inserisce un elemento multimediale in una posizione specificata in una playlist.
ms.assetid: 6e472f0a-13df-41d9-8e6f-8430d87fe978
keywords:
- metodo insertItem Media Player Windows
- metodo insertItem Windows Media Player, interfaccia IWMPPlaylist
- Interfaccia IWMPPlaylist Windows Media Player, metodo insertItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.insertItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ef167a5f3931f34d4cd6fb91b3d044affb9484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330973"
---
# <a name="iwmpplaylistinsertitem-method"></a><span data-ttu-id="1c098-106">Metodo IWMPPlaylist:: insertItem</span><span class="sxs-lookup"><span data-stu-id="1c098-106">IWMPPlaylist::insertItem method</span></span>

<span data-ttu-id="1c098-107">Il metodo **InsertItem** inserisce un elemento multimediale in una posizione specificata in una playlist.</span><span class="sxs-lookup"><span data-stu-id="1c098-107">The **insertItem** method inserts a media item at a specified location in a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c098-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c098-108">Syntax</span></span>


```CSharp
public void insertItem(
  System.Int32 lIndex,
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub insertItem( _
  ByVal lIndex As System.Int32, _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.insertItem
```





## <a name="parameters"></a><span data-ttu-id="1c098-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c098-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c098-110">*lIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c098-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c098-111">**System. Int32** che rappresenta l'indice in base zero in corrispondenza del quale verrà inserito l'elemento multimediale nella playlist.</span><span class="sxs-lookup"><span data-stu-id="1c098-111">A **System.Int32** that is the zero-based index at which the media item will be inserted in the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="1c098-112">*pIWMPMedia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c098-112">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c098-113">Interfaccia **wmplib. IWMPMedia** che rappresenta l'elemento multimediale da inserire.</span><span class="sxs-lookup"><span data-stu-id="1c098-113">A **WMPLib.IWMPMedia** interface that represents the media item to be inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c098-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c098-114">Return value</span></span>

<span data-ttu-id="1c098-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="1c098-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c098-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c098-116">Remarks</span></span>

<span data-ttu-id="1c098-117">Tutti gli elementi multimediali dopo l'elemento inserito avranno indici aumentati di uno.</span><span class="sxs-lookup"><span data-stu-id="1c098-117">All media items after the inserted item will have their indexes increased by one.</span></span>

<span data-ttu-id="1c098-118">Prima di chiamare questo metodo, è necessario disporre dell'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="1c098-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="1c098-119">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1c098-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c098-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c098-120">Requirements</span></span>



| <span data-ttu-id="1c098-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c098-121">Requirement</span></span> | <span data-ttu-id="1c098-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1c098-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c098-123">Versione</span><span class="sxs-lookup"><span data-stu-id="1c098-123">Version</span></span><br/>   | <span data-ttu-id="1c098-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="1c098-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1c098-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1c098-125">Namespace</span></span><br/> | <span data-ttu-id="1c098-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1c098-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1c098-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="1c098-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1c098-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1c098-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c098-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c098-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c098-130">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1c098-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1c098-131">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1c098-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1c098-132">**IWMPPlaylist. removeItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1c098-132">**IWMPPlaylist.removeItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> </dl>

 

 





