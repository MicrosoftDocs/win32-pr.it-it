---
title: Metodo IWMPMedia3 getItemInfoByType
description: Il metodo getItemInfoByType restituisce il valore dell'attributo corrispondente al tipo di attributo e all'indice specificati.
ms.assetid: e4cf14b4-3c59-485f-a573-734a0076647b
keywords:
- Metodo getItemInfoByType Windows Media Player
- Metodo getItemInfoByType Windows Media Player, interfaccia IWMPMedia3
- Interfaccia IWMPMedia3 Windows Media Player, metodo getItemInfoByType
topic_type:
- apiref
api_name:
- IWMPMedia3.getItemInfoByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f37992201d5d19397724071f8c2a4b8e851aac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324366"
---
# <a name="iwmpmedia3getiteminfobytype-method"></a><span data-ttu-id="1e585-106">Metodo IWMPMedia3:: getItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="1e585-106">IWMPMedia3::getItemInfoByType method</span></span>

<span data-ttu-id="1e585-107">Il metodo **getItemInfoByType** restituisce il valore dell'attributo corrispondente al tipo di attributo e all'indice specificati.</span><span class="sxs-lookup"><span data-stu-id="1e585-107">The **getItemInfoByType** method returns the value of the attribute corresponding to the specified attribute type and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e585-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e585-108">Syntax</span></span>


```CSharp
public System.Object getItemInfoByType(
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lIndex
);
```


```VB

Public Function getItemInfoByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lIndex As System.Int32 _
) As System.Object
Implements IWMPMedia3.getItemInfoByType
```





## <a name="parameters"></a><span data-ttu-id="1e585-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e585-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e585-110">*bstrType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e585-110">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e585-111">**System. String** che rappresenta il tipo di attributo.</span><span class="sxs-lookup"><span data-stu-id="1e585-111">A **System.String** that is the attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="1e585-112">*bstrLanguage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e585-112">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e585-113">**System. String** che rappresenta il linguaggio.</span><span class="sxs-lookup"><span data-stu-id="1e585-113">A **System.String** that is the language.</span></span> <span data-ttu-id="1e585-114">Se il valore è impostato su null o su una stringa di lunghezza zero (""), viene utilizzata la stringa delle impostazioni locali corrente.</span><span class="sxs-lookup"><span data-stu-id="1e585-114">If the value is set to null or a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="1e585-115">In caso contrario, il valore deve essere una stringa di linguaggio RFC 1766 valida, ad esempio "en-US".</span><span class="sxs-lookup"><span data-stu-id="1e585-115">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="1e585-116">*lIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e585-116">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e585-117">**System. Int32** che rappresenta l'indice dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="1e585-117">A **System.Int32** that is the attribute index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e585-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e585-118">Return value</span></span>

<span data-ttu-id="1e585-119">**Oggetto System. Object** che rappresenta il valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="1e585-119">A **System.Object** that is the value of the attribute.</span></span> <span data-ttu-id="1e585-120">Il tipo su cui eseguire il cast di questo oggetto dipende dal tipo dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="1e585-120">The type to cast this object to depends on the type of the attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e585-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e585-121">Remarks</span></span>

<span data-ttu-id="1e585-122">Questo metodo restituisce i metadati per un singolo elemento multimediale digitale o un elemento multimediale che fa parte di una playlist.</span><span class="sxs-lookup"><span data-stu-id="1e585-122">This method returns the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="1e585-123">Questo metodo supporta attributi con più valori e attributi con valori complessi.</span><span class="sxs-lookup"><span data-stu-id="1e585-123">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="1e585-124">Il metodo **GetItemInfo** non supporta attributi con più valori e attributi con valori complessi.</span><span class="sxs-lookup"><span data-stu-id="1e585-124">The **getItemInfo** method does not support attributes with multiple values and attributes with complex values.</span></span>

<span data-ttu-id="1e585-125">La proprietà **attributeCount** ottiene il numero di nomi di attributi disponibili per un determinato elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="1e585-125">The **attributeCount** property gets the number of attribute names available for a given media item.</span></span> <span data-ttu-id="1e585-126">I numeri di indice possono quindi essere usati con il metodo **GetAttribute** per determinare il nome di ogni attributo disponibile.</span><span class="sxs-lookup"><span data-stu-id="1e585-126">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="1e585-127">I singoli nomi di attributo possono essere passati al parametro *Name* di **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="1e585-127">Individual attribute names can be passed to the *name* parameter of **getItemInfoByType**.</span></span>

<span data-ttu-id="1e585-128">Il metodo **getAttributeCountByType** restituisce il numero di attributi che corrispondono a un nome di attributo specifico per un determinato elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="1e585-128">The **getAttributeCountByType** method returns the number of attributes that correspond to a particular attribute name for a given media item.</span></span> <span data-ttu-id="1e585-129">I numeri di indice possono quindi essere passati al parametro di *Indice* di **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="1e585-129">Index numbers can then be passed to the *index* parameter of **getItemInfoByType**.</span></span> <span data-ttu-id="1e585-130">Questa operazione è utile quando un elemento multimediale è stato categorizzato in più generi, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="1e585-130">This is useful when a media item has been categorized under multiple genres, for example.</span></span>

<span data-ttu-id="1e585-131">Se l'elemento multimediale proviene da una libreria recuperata chiamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), il set di attributi disponibili sarà diverso da quelli su cui è possibile eseguire una query dalla libreria locale recuperata chiamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="1e585-131">If the media item came from a library that was retrieved by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), the set of available attributes will differ from those which can be queried from the local library retrieved by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span></span> <span data-ttu-id="1e585-132">Ad esempio, gli attributi disponibili dalla libreria locale recuperata tramite **IWMPLibrary** saranno un subset degli attributi disponibili dalla libreria locale recuperata mediante **AxWindowsMediaPlayer**.</span><span class="sxs-lookup"><span data-stu-id="1e585-132">For example, the attributes available from the local library retrieved by using **IWMPLibrary** will be a subset of the attributes available from the local library retrieved by using **AxWindowsMediaPlayer**.</span></span> <span data-ttu-id="1e585-133">Il set di attributi disponibili da altre origini (librerie remote, dispositivi portatili o CDs è definito da altre origini).</span><span class="sxs-lookup"><span data-stu-id="1e585-133">The set of attributes available from other sources (remote libraries, portable devices, or CDs is defined by the other sources.</span></span>

<span data-ttu-id="1e585-134">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="1e585-134">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="1e585-135">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1e585-135">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e585-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e585-136">Requirements</span></span>



| <span data-ttu-id="1e585-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e585-137">Requirement</span></span> | <span data-ttu-id="1e585-138">Valore</span><span class="sxs-lookup"><span data-stu-id="1e585-138">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e585-139">Versione</span><span class="sxs-lookup"><span data-stu-id="1e585-139">Version</span></span><br/>   | <span data-ttu-id="1e585-140">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="1e585-140">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1e585-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1e585-141">Namespace</span></span><br/> | <span data-ttu-id="1e585-142">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1e585-142">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1e585-143">Assembly</span><span class="sxs-lookup"><span data-stu-id="1e585-143">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1e585-144"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1e585-144"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e585-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e585-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e585-146">**Interfaccia IWMPMedia3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1e585-146">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1e585-147">**IWMPMedia. attributeCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1e585-147">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1e585-148">**IWMPMedia. GetAttribute (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1e585-148">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1e585-149">**IWMPMedia. getItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1e585-149">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1e585-150">**IWMPMedia3. getAttributeCountByType (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1e585-150">**IWMPMedia3.getAttributeCountByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md)
</dt> </dl>

 

 





