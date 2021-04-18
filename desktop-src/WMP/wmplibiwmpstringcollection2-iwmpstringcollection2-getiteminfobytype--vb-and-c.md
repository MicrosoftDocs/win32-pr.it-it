---
title: Metodo IWMPStringCollection2 getItemInfobyType
description: Il metodo getItemInfoByType restituisce il valore corrispondente all'indice dell'elemento della raccolta di stringhe, al nome, alla lingua e all'indice dell'attributo specificati.
ms.assetid: 51035fed-51ce-4cd2-a936-4c99802128f2
keywords:
- Metodo getItemInfobyType Windows Media Player
- Metodo getItemInfobyType Windows Media Player, interfaccia IWMPStringCollection2
- Interfaccia IWMPStringCollection2 Windows Media Player, metodo getItemInfobyType
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfobyType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e227d6471ecf41c8f48420ded61c6f4e7eaac8cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331726"
---
# <a name="iwmpstringcollection2getiteminfobytype-method"></a><span data-ttu-id="27fc9-106">Metodo IWMPStringCollection2:: getItemInfobyType</span><span class="sxs-lookup"><span data-stu-id="27fc9-106">IWMPStringCollection2::getItemInfobyType method</span></span>

<span data-ttu-id="27fc9-107">Il metodo **getItemInfoByType** restituisce il valore corrispondente all'indice dell'elemento della raccolta di stringhe, al nome, alla lingua e all'indice dell'attributo specificati.</span><span class="sxs-lookup"><span data-stu-id="27fc9-107">The **getItemInfoByType** method returns the value corresponding to the specified string collection item index, name, language, and attribute index.</span></span>

## <a name="syntax"></a><span data-ttu-id="27fc9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27fc9-108">Syntax</span></span>


```CSharp
public System.Object getItemInfobyType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lAttributeIndex
);
```


```VB

Public Function getItemInfobyType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lAttributeIndex As System.Int32 _
) As System.Object
Implements IWMPStringCollection2.getItemInfobyType
```





## <a name="parameters"></a><span data-ttu-id="27fc9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="27fc9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27fc9-110">*lCollectionIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27fc9-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27fc9-111">**System. Int32** che rappresenta l'indice in base zero dell'elemento della raccolta di stringhe da cui ottenere l'attributo.</span><span class="sxs-lookup"><span data-stu-id="27fc9-111">The **System.Int32** that is the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="27fc9-112">*bstrType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27fc9-112">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27fc9-113">**System. String** che rappresenta il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="27fc9-113">The **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="27fc9-114">*bstrLanguage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27fc9-114">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27fc9-115">**System. String** che indica il linguaggio.</span><span class="sxs-lookup"><span data-stu-id="27fc9-115">The **System.String** that indicates the language.</span></span> <span data-ttu-id="27fc9-116">Se il valore è impostato su null o su una stringa di lunghezza zero (""), viene utilizzata la stringa delle impostazioni locali corrente.</span><span class="sxs-lookup"><span data-stu-id="27fc9-116">If the value is set to null or to a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="27fc9-117">In caso contrario, il valore deve essere una stringa di linguaggio RFC 1766 valida, ad esempio "en-US".</span><span class="sxs-lookup"><span data-stu-id="27fc9-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="27fc9-118">*lAttributeIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27fc9-118">*lAttributeIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27fc9-119">**System. Int32** che rappresenta l'indice in base zero dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="27fc9-119">A **System.Int32** that is the zero-based index of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27fc9-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27fc9-120">Return value</span></span>

<span data-ttu-id="27fc9-121">**Oggetto System. Object** che rappresenta l'elemento della raccolta di stringhe.</span><span class="sxs-lookup"><span data-stu-id="27fc9-121">A **System.Object** that is the string collection item.</span></span>

## <a name="remarks"></a><span data-ttu-id="27fc9-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="27fc9-122">Remarks</span></span>

<span data-ttu-id="27fc9-123">Questo metodo supporta attributi con più valori e attributi con valori complessi.</span><span class="sxs-lookup"><span data-stu-id="27fc9-123">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="27fc9-124">Il metodo **GetItemInfo** non supporta attributi con più valori o attributi con valori complessi.</span><span class="sxs-lookup"><span data-stu-id="27fc9-124">The **getItemInfo** method does not support attributes with multiple values or attributes with complex values.</span></span>

<span data-ttu-id="27fc9-125">Passando il valore "Child ' nel parametro *bstrType* , è possibile recuperare una nuova raccolta di stringhe che contiene gli elementi figlio di uno degli elementi nella raccolta di stringhe padre.</span><span class="sxs-lookup"><span data-stu-id="27fc9-125">By passing the value "ChildList" in the *bstrType* parameter, you can retrieve a new string collection that contains the children of one of the items in the parent string collection.</span></span> <span data-ttu-id="27fc9-126">Se, ad esempio, la raccolta padre contiene un elenco di AlbumIDs, è possibile usare questo metodo per ottenere una raccolta di stringhe figlio contenente tutte le tracce per uno degli album.</span><span class="sxs-lookup"><span data-stu-id="27fc9-126">For instance, if the parent collection contains a list of AlbumIDs, you can use this method to obtain a child string collection that contains all the tracks for one of the albums.</span></span> <span data-ttu-id="27fc9-127">Questo approccio è più rapido ed efficiente rispetto alla chiamata del metodo **IWMPMediaCollection2. getStringCollectionByQuery** due volte; una volta per ottenere una raccolta di AlbumIDs e una seconda volta per ottenere una raccolta di tracce per un determinato AlbumID.</span><span class="sxs-lookup"><span data-stu-id="27fc9-127">This approach is faster and more efficient than calling the **IWMPMediaCollection2.getStringCollectionByQuery** method twice; once to get a collection of AlbumIDs, and a second time to get a collection of tracks for a particular AlbumID.</span></span> <span data-ttu-id="27fc9-128">Per utilizzare l'elemento figlio nel modo appena descritto, è necessario che la raccolta di stringhe padre venga ottenuta da una raccolta di supporti tramite **IWMPLibraryServices** e non tramite la proprietà **AxWindowsMediaPlayer. mediacollection** .</span><span class="sxs-lookup"><span data-stu-id="27fc9-128">To use ChildList in the way just described, the parent string collection must be obtained from a media collection through **IWMPLibraryServices**, and not by using the **AxWindowsMediaPlayer.mediaCollection** property.</span></span>

<span data-ttu-id="27fc9-129">Quando si utilizza l'elemento figlio, passare il valore "Child ' nel parametro *bstrType* e il valore 0 nel parametro *lAttributeIndex* .</span><span class="sxs-lookup"><span data-stu-id="27fc9-129">When using ChildList, pass the value "ChildList" in the *bstrType* parameter, and the value 0 in the *lAttributeIndex* parameter.</span></span> <span data-ttu-id="27fc9-130">È quindi possibile eseguire il cast dell'oggetto restituito a un'interfaccia **IWMPStringCollection2** per accedere all'elenco figlio.</span><span class="sxs-lookup"><span data-stu-id="27fc9-130">You can then cast the object that is returned to an **IWMPStringCollection2** interface to access the child list.</span></span>

<span data-ttu-id="27fc9-131">Per utilizzare questo metodo, è necessario disporre dell'accesso in lettura alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="27fc9-131">To use this method, you must have read access to the library.</span></span> <span data-ttu-id="27fc9-132">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="27fc9-132">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="27fc9-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27fc9-133">Requirements</span></span>



| <span data-ttu-id="27fc9-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="27fc9-134">Requirement</span></span> | <span data-ttu-id="27fc9-135">Valore</span><span class="sxs-lookup"><span data-stu-id="27fc9-135">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27fc9-136">Versione</span><span class="sxs-lookup"><span data-stu-id="27fc9-136">Version</span></span><br/>   | <span data-ttu-id="27fc9-137">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="27fc9-137">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="27fc9-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="27fc9-138">Namespace</span></span><br/> | <span data-ttu-id="27fc9-139">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="27fc9-139">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="27fc9-140">Assembly</span><span class="sxs-lookup"><span data-stu-id="27fc9-140">Assembly</span></span><br/>  | <dl> <span data-ttu-id="27fc9-141"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="27fc9-141"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27fc9-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27fc9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27fc9-143">**Attributo AlbumID**</span><span class="sxs-lookup"><span data-stu-id="27fc9-143">**AlbumID Attribute**</span></span>](albumid-attribute.md)
</dt> <dt>

[<span data-ttu-id="27fc9-144">**Interfaccia IWMPLibraryServices (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="27fc9-144">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="27fc9-145">**IWMPMediaCollection2. getStringCollectionByQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="27fc9-145">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="27fc9-146">**Interfaccia IWMPStringCollection2**</span><span class="sxs-lookup"><span data-stu-id="27fc9-146">**IWMPStringCollection2 Interface**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="27fc9-147">**IWMPStringCollection2. getItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="27fc9-147">**IWMPStringCollection2.getItemInfo (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





