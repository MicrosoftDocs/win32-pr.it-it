---
title: Metodo IWMPMedia getItemInfoByAtom
description: Il metodo getItemInfoByAtom restituisce il valore dell'attributo con il numero di indice specificato.
ms.assetid: d9a4b737-add1-4bbd-8e03-e58f45d65a62
keywords:
- Metodo getItemInfoByAtom Windows Media Player
- Metodo getItemInfoByAtom Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, metodo getItemInfoByAtom
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfoByAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb37243960360120fbfe508a39db31e37728ac39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332403"
---
# <a name="iwmpmediagetiteminfobyatom-method"></a><span data-ttu-id="a808c-106">Metodo IWMPMedia:: getItemInfoByAtom</span><span class="sxs-lookup"><span data-stu-id="a808c-106">IWMPMedia::getItemInfoByAtom method</span></span>

<span data-ttu-id="a808c-107">Il metodo **getItemInfoByAtom** restituisce il valore dell'attributo con il numero di indice specificato.</span><span class="sxs-lookup"><span data-stu-id="a808c-107">The **getItemInfoByAtom** method returns the value of the attribute with the specified index number.</span></span>

## <a name="syntax"></a><span data-ttu-id="a808c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a808c-108">Syntax</span></span>


```CSharp
public System.String getItemInfoByAtom(
  System.Int32 lAtom
);
```


```VB

Public Function getItemInfoByAtom( _
  ByVal lAtom As System.Int32 _
) As System.String
Implements IWMPMedia.getItemInfoByAtom
```





## <a name="parameters"></a><span data-ttu-id="a808c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a808c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a808c-110">*latore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a808c-110">*lAtom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a808c-111">**System. Int32** che specifica l'indice in corrispondenza del quale si trova l'attributo richiesto all'interno del set di attributi disponibili.</span><span class="sxs-lookup"><span data-stu-id="a808c-111">A **System.Int32** that specifies the index at which the requested attribute resides within the set of available attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a808c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a808c-112">Return value</span></span>

<span data-ttu-id="a808c-113">**System. String** che rappresenta il valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="a808c-113">A **System.String** that is the value of the attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="a808c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a808c-114">Remarks</span></span>

<span data-ttu-id="a808c-115">Questo metodo può essere utilizzato per recuperare i metadati per un elemento multimediale specifico utilizzando un numero di indice dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="a808c-115">This method can be used to retrieve metadata for a specific media item by using an attribute index number.</span></span> <span data-ttu-id="a808c-116">È possibile utilizzare la proprietà **attributeCount** per determinare il numero di attributi disponibili per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="a808c-116">The **attributeCount** property can be used to determine the number of attributes available for the media item.</span></span>

<span data-ttu-id="a808c-117">Il metodo **getMediaAtom** dell'interfaccia **IWMPMediaCollection** può essere utilizzato anche per recuperare l'indice di un attributo specifico.</span><span class="sxs-lookup"><span data-stu-id="a808c-117">The **getMediaAtom** method of the **IWMPMediaCollection** interface can also be used to retrieve the index of a particular attribute.</span></span> <span data-ttu-id="a808c-118">Questa tecnica è in genere più efficiente rispetto ai metodi **GetItemInfo** o **getItemInfoByType** quando si lavora con playlist di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="a808c-118">This technique is generally more efficient than the **getItemInfo** or **getItemInfoByType** methods when working with large playlists.</span></span>

<span data-ttu-id="a808c-119">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="a808c-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="a808c-120">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a808c-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a808c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a808c-121">Requirements</span></span>



| <span data-ttu-id="a808c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a808c-122">Requirement</span></span> | <span data-ttu-id="a808c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a808c-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a808c-124">Versione</span><span class="sxs-lookup"><span data-stu-id="a808c-124">Version</span></span><br/>   | <span data-ttu-id="a808c-125">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a808c-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a808c-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a808c-126">Namespace</span></span><br/> | <span data-ttu-id="a808c-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a808c-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a808c-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="a808c-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a808c-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a808c-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a808c-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a808c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a808c-131">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a808c-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a808c-132">**IWMPMedia. attributeCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a808c-132">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a808c-133">**IWMPMedia. getItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a808c-133">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a808c-134">**IWMPMedia. setItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a808c-134">**IWMPMedia.setItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a808c-135">**IWMPMedia3. getItemInfoByType (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a808c-135">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a808c-136">**IWMPMediaCollection. getMediaAtom (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a808c-136">**IWMPMediaCollection.getMediaAtom (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)
</dt> </dl>

 

 





