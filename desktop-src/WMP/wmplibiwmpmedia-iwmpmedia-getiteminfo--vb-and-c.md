---
title: Metodo IWMPMedia getItemInfo
description: Il metodo getItemInfo restituisce il valore dell'attributo specificato per l'elemento multimediale.
ms.assetid: b95fa61d-a600-4f31-a930-d80516204034
keywords:
- metodo getItemInfo Windows Media Player
- metodo getItemInfo Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, metodo getItemInfo
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 523e57e68d13df55395cd4deca6e09904723bbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332406"
---
# <a name="iwmpmediagetiteminfo-method"></a><span data-ttu-id="73d80-106">Metodo IWMPMedia:: getItemInfo</span><span class="sxs-lookup"><span data-stu-id="73d80-106">IWMPMedia::getItemInfo method</span></span>

<span data-ttu-id="73d80-107">Il metodo **GetItemInfo** restituisce il valore dell'attributo specificato per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="73d80-107">The **getItemInfo** method returns the value of the specified attribute for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="73d80-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73d80-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPMedia.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="73d80-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="73d80-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73d80-110">*bstrItemName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73d80-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73d80-111">**System. String** che rappresenta il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="73d80-111">A **System.String** that is the name of the attribute.</span></span> <span data-ttu-id="73d80-112">Per informazioni sugli attributi supportati da Windows Media Player, vedere il [riferimento all'attributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="73d80-112">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73d80-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="73d80-113">Return value</span></span>

<span data-ttu-id="73d80-114">**System. String** che corrisponde al valore dell'attributo specificato.</span><span class="sxs-lookup"><span data-stu-id="73d80-114">A **System.String** that is the value of the specified attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="73d80-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="73d80-115">Remarks</span></span>

<span data-ttu-id="73d80-116">Questo metodo restituisce i metadati per un singolo elemento multimediale o un elemento multimediale che fa parte di una playlist.</span><span class="sxs-lookup"><span data-stu-id="73d80-116">This method returns the metadata for an individual media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="73d80-117">La proprietà **attributeCount** ottiene il numero di nomi di attributi disponibili per un determinato elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="73d80-117">The **attributeCount** property gets the number of attribute names available for a given media item.</span></span> <span data-ttu-id="73d80-118">I numeri di indice possono quindi essere usati con il metodo **GetAttribute** per determinare il nome di ogni attributo disponibile.</span><span class="sxs-lookup"><span data-stu-id="73d80-118">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="73d80-119">I singoli nomi di attributo possono essere passati a **GetItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="73d80-119">Individual attribute names can be passed to **getItemInfo**.</span></span>

<span data-ttu-id="73d80-120">Per recuperare gli attributi con più valori e attributi con valori complessi, usare il metodo **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="73d80-120">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="73d80-121">Se l'elemento multimediale proviene da una libreria recuperata chiamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), il set di attributi disponibili sarà diverso da quelli su cui è possibile eseguire una query dalla libreria locale recuperata chiamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="73d80-121">If the media item came from a library that was retrieved by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), the set of available attributes will differ from those which can be queried from the local library retrieved by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span></span> <span data-ttu-id="73d80-122">Ad esempio, gli attributi disponibili dalla libreria locale recuperata tramite **IWMPLibrary** saranno un subset degli attributi disponibili dalla libreria locale recuperata mediante **IWMPCore**.</span><span class="sxs-lookup"><span data-stu-id="73d80-122">For example, the attributes available from the local library retrieved by using **IWMPLibrary** will be a subset of the attributes available from the local library retrieved by using **IWMPCore**.</span></span> <span data-ttu-id="73d80-123">Il set di attributi disponibili da altre origini (librerie remote, dispositivi portatili o CDs) viene definito dalle altre origini.</span><span class="sxs-lookup"><span data-stu-id="73d80-123">The set of attributes available from other sources (remote libraries, portable devices, or CDs) is defined by the other sources.</span></span>

<span data-ttu-id="73d80-124">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="73d80-124">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="73d80-125">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="73d80-125">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="73d80-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73d80-126">Requirements</span></span>



| <span data-ttu-id="73d80-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="73d80-127">Requirement</span></span> | <span data-ttu-id="73d80-128">Valore</span><span class="sxs-lookup"><span data-stu-id="73d80-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73d80-129">Versione</span><span class="sxs-lookup"><span data-stu-id="73d80-129">Version</span></span><br/>   | <span data-ttu-id="73d80-130">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="73d80-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="73d80-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="73d80-131">Namespace</span></span><br/> | <span data-ttu-id="73d80-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="73d80-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="73d80-133">Assembly</span><span class="sxs-lookup"><span data-stu-id="73d80-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="73d80-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="73d80-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73d80-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73d80-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73d80-136">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="73d80-136">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="73d80-137">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="73d80-137">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="73d80-138">**IWMPMedia. attributeCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="73d80-138">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="73d80-139">**IWMPMedia. GetAttribute (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="73d80-139">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="73d80-140">**IWMPMedia. setItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="73d80-140">**IWMPMedia.setItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="73d80-141">**IWMPMedia3. getItemInfoByType (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="73d80-141">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





