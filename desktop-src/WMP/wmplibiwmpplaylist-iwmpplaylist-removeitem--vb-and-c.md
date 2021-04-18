---
title: Metodo IWMPPlaylist removeItem
description: Il metodo removeItem rimuove l'elemento multimediale specificato dalla playlist.
ms.assetid: 8b5a4c34-863d-4963-97c8-cc5aa2223ab5
keywords:
- Metodo removeItem Windows Media Player
- Metodo removeItem Windows Media Player, interfaccia IWMPPlaylist
- Interfaccia IWMPPlaylist Windows Media Player, metodo removeItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.removeItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec845b7657e04f17c47119dd169032ebe5815786
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325966"
---
# <a name="iwmpplaylistremoveitem-method"></a><span data-ttu-id="05d3b-106">Metodo IWMPPlaylist:: removeItem</span><span class="sxs-lookup"><span data-stu-id="05d3b-106">IWMPPlaylist::removeItem method</span></span>

<span data-ttu-id="05d3b-107">Il metodo **RemoveItem** rimuove l'elemento multimediale specificato dalla playlist.</span><span class="sxs-lookup"><span data-stu-id="05d3b-107">The **removeItem** method removes the specified media item from the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="05d3b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05d3b-108">Syntax</span></span>


```CSharp
public void removeItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub removeItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.removeItem
```





## <a name="parameters"></a><span data-ttu-id="05d3b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="05d3b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05d3b-110">*pIWMPMedia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05d3b-110">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05d3b-111">Interfaccia **wmplib. IWMPMedia** che rappresenta l'elemento multimediale da rimuovere dalla playlist.</span><span class="sxs-lookup"><span data-stu-id="05d3b-111">A **WMPLib.IWMPMedia** interface that represents the media item to remove from the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05d3b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="05d3b-112">Return value</span></span>

<span data-ttu-id="05d3b-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="05d3b-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="05d3b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="05d3b-114">Remarks</span></span>

<span data-ttu-id="05d3b-115">Se l'elemento rimosso è la traccia attualmente in esecuzione, la riproduzione viene arrestata e l'elemento successivo nella playlist diventa quello corrente.</span><span class="sxs-lookup"><span data-stu-id="05d3b-115">If the item removed is the currently playing track, playback stops and the next item in the playlist becomes the current one.</span></span>

<span data-ttu-id="05d3b-116">Se non è presente alcun elemento successivo, viene usato l'elemento precedente.</span><span class="sxs-lookup"><span data-stu-id="05d3b-116">If there is no next item, the previous item is used.</span></span> <span data-ttu-id="05d3b-117">Se non sono presenti altri elementi, la proprietà **AxWindowsMediaPlayer. currentMedia** restituirà **null**.</span><span class="sxs-lookup"><span data-stu-id="05d3b-117">If there are no other items, then the **AxWindowsMediaPlayer.currentMedia** property will return **NULL**.</span></span>

<span data-ttu-id="05d3b-118">Prima di chiamare questo metodo, è necessario disporre dell'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="05d3b-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="05d3b-119">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="05d3b-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05d3b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05d3b-120">Requirements</span></span>



| <span data-ttu-id="05d3b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="05d3b-121">Requirement</span></span> | <span data-ttu-id="05d3b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="05d3b-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05d3b-123">Versione</span><span class="sxs-lookup"><span data-stu-id="05d3b-123">Version</span></span><br/>   | <span data-ttu-id="05d3b-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="05d3b-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="05d3b-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="05d3b-125">Namespace</span></span><br/> | <span data-ttu-id="05d3b-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="05d3b-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="05d3b-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="05d3b-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="05d3b-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="05d3b-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05d3b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05d3b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05d3b-130">**AxWindowsMediaPlayer. currentMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="05d3b-130">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="05d3b-131">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="05d3b-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="05d3b-132">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="05d3b-132">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="05d3b-133">**IWMPPlaylist. insertItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="05d3b-133">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="05d3b-134">**IWMPPlaylist. Item (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="05d3b-134">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="05d3b-135">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="05d3b-135">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="05d3b-136">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="05d3b-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





