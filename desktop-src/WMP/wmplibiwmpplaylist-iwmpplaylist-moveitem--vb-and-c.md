---
title: Metodo IWMPPlaylist moveItem
description: Il metodo moveItem modifica la posizione di un elemento multimediale nella playlist.
ms.assetid: e82c820f-4640-4289-88c1-79a92e520f00
keywords:
- Metodo moveItem Windows Media Player
- Metodo moveItem Windows Media Player, interfaccia IWMPPlaylist
- Interfaccia IWMPPlaylist Windows Media Player, metodo moveItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.moveItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c2d5be745fc3dcf799eb7203e607e493b284b4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330972"
---
# <a name="iwmpplaylistmoveitem-method"></a><span data-ttu-id="fae67-106">Metodo IWMPPlaylist:: moveItem</span><span class="sxs-lookup"><span data-stu-id="fae67-106">IWMPPlaylist::moveItem method</span></span>

<span data-ttu-id="fae67-107">Il metodo **moveItem** modifica la posizione di un elemento multimediale nella playlist.</span><span class="sxs-lookup"><span data-stu-id="fae67-107">The **moveItem** method changes the location of a media item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="fae67-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fae67-108">Syntax</span></span>


```CSharp
public void moveItem(
  System.Int32 lIndexOld,
  System.Int32 lIndexNew
);
```


```VB

Public Sub moveItem( _
  ByVal lIndexOld As System.Int32, _
  ByVal lIndexNew As System.Int32 _
)
Implements IWMPPlaylist.moveItem
```





## <a name="parameters"></a><span data-ttu-id="fae67-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fae67-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fae67-110">*lIndexOld* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fae67-110">*lIndexOld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fae67-111">**System. Int32** che rappresenta l'indice originale.</span><span class="sxs-lookup"><span data-stu-id="fae67-111">A **System.Int32** that is the original index.</span></span>

</dd> <dt>

<span data-ttu-id="fae67-112">*lIndexNew* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fae67-112">*lIndexNew* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fae67-113">**System. Int32** che rappresenta il nuovo indice.</span><span class="sxs-lookup"><span data-stu-id="fae67-113">A **System.Int32** that is the new index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fae67-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fae67-114">Return value</span></span>

<span data-ttu-id="fae67-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="fae67-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fae67-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="fae67-116">Remarks</span></span>

<span data-ttu-id="fae67-117">Per tutti gli elementi dopo l'elemento inserito i numeri di indice aumenteranno di uno.</span><span class="sxs-lookup"><span data-stu-id="fae67-117">All items after the inserted item will have their index numbers increased by one.</span></span>

<span data-ttu-id="fae67-118">Prima di chiamare questo metodo, è necessario disporre dell'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="fae67-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="fae67-119">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="fae67-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fae67-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fae67-120">Requirements</span></span>



| <span data-ttu-id="fae67-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fae67-121">Requirement</span></span> | <span data-ttu-id="fae67-122">Valore</span><span class="sxs-lookup"><span data-stu-id="fae67-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fae67-123">Versione</span><span class="sxs-lookup"><span data-stu-id="fae67-123">Version</span></span><br/>   | <span data-ttu-id="fae67-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="fae67-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="fae67-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fae67-125">Namespace</span></span><br/> | <span data-ttu-id="fae67-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="fae67-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fae67-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="fae67-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fae67-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fae67-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fae67-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fae67-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fae67-130">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fae67-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fae67-131">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fae67-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fae67-132">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fae67-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





