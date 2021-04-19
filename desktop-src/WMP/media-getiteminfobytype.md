---
title: Media. getItemInfoByType, metodo
description: Il metodo getItemInfoByType Recupera il valore dell'attributo corrispondente al nome dell'attributo, alla lingua e all'indice specificati.
ms.assetid: 9d3377c2-7ae8-48ce-a42e-9c965f6b79f9
keywords:
- Metodo getItemInfoByType Windows Media Player
- Metodo getItemInfoByType Windows Media Player, classe media
- Media class Media Player Windows, metodo getItemInfoByType
topic_type:
- apiref
api_name:
- Media.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2aff2bee7641075bbac1dd04526ee751ea077a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332549"
---
# <a name="mediagetiteminfobytype-method"></a><span data-ttu-id="2a629-106">Media. getItemInfoByType, metodo</span><span class="sxs-lookup"><span data-stu-id="2a629-106">Media.getItemInfoByType method</span></span>

<span data-ttu-id="2a629-107">Il metodo **getItemInfoByType** Recupera il valore dell'attributo corrispondente al nome dell'attributo, alla lingua e all'indice specificati.</span><span class="sxs-lookup"><span data-stu-id="2a629-107">The **getItemInfoByType** method retrieves the value of the attribute corresponding to the specified attribute name, language, and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a629-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a629-108">Syntax</span></span>


```JScript
retVal = Media.getItemInfoByType(
  name,
  language,
  index
)
```



## <a name="parameters"></a><span data-ttu-id="2a629-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a629-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a629-110">*nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a629-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a629-111">**Stringa** contenente il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="2a629-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="2a629-112">Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="2a629-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a629-113">*lingua* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="2a629-113">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a629-114">**Stringa** che rappresenta la lingua.</span><span class="sxs-lookup"><span data-stu-id="2a629-114">**String** representing the language.</span></span> <span data-ttu-id="2a629-115">Se il valore è impostato su null o su "" (stringa vuota) viene utilizzata la stringa delle impostazioni locali corrente.</span><span class="sxs-lookup"><span data-stu-id="2a629-115">If the value is set to null or "" (empty string) the current locale string is used.</span></span> <span data-ttu-id="2a629-116">In caso contrario, il valore deve essere una stringa di linguaggio RFC 1766 valida, ad esempio "en-US".</span><span class="sxs-lookup"><span data-stu-id="2a629-116">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="2a629-117">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="2a629-117">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a629-118">**Numero** (**Long**) che contiene l'indice in base zero del valore da recuperare dall'attributo.</span><span class="sxs-lookup"><span data-stu-id="2a629-118">**Number** (**long**) containing the zero-based index of the value to retrieve from the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a629-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a629-119">Return value</span></span>

<span data-ttu-id="2a629-120">Questo metodo restituisce un oggetto **Number**, **String**, **MetadataPicture** o **MetadataText** come indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2a629-120">This method returns a **Number**, **String**, **MetadataPicture** object, or **MetadataText** object as indicated in the following table.</span></span>



| <span data-ttu-id="2a629-121">Attributo</span><span class="sxs-lookup"><span data-stu-id="2a629-121">Attribute</span></span>                   | <span data-ttu-id="2a629-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a629-122">Return value</span></span>                   |
|-----------------------------|--------------------------------|
| <span data-ttu-id="2a629-123">**SyncState**</span><span class="sxs-lookup"><span data-stu-id="2a629-123">**SyncState**</span></span>               | <span data-ttu-id="2a629-124">**Numero** (**unsigned long**)</span><span class="sxs-lookup"><span data-stu-id="2a629-124">**Number** (**unsigned long**)</span></span> |
| <span data-ttu-id="2a629-125">**WM/lyrics \_ sincronizzati**</span><span class="sxs-lookup"><span data-stu-id="2a629-125">**WM/Lyrics\_Synchronised**</span></span> | <span data-ttu-id="2a629-126">Oggetto **MetadataText**</span><span class="sxs-lookup"><span data-stu-id="2a629-126">**MetadataText** object</span></span>        |
| <span data-ttu-id="2a629-127">**WM/immagine**</span><span class="sxs-lookup"><span data-stu-id="2a629-127">**WM/Picture**</span></span>              | <span data-ttu-id="2a629-128">Oggetto **MetadataPicture**</span><span class="sxs-lookup"><span data-stu-id="2a629-128">**MetadataPicture** object</span></span>     |
| <span data-ttu-id="2a629-129">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="2a629-129">**WM/UserWebURL**</span></span>           | <span data-ttu-id="2a629-130">Oggetto **MetadataText**</span><span class="sxs-lookup"><span data-stu-id="2a629-130">**MetadataText** object</span></span>        |
| <span data-ttu-id="2a629-131">Tutti gli altri attributi</span><span class="sxs-lookup"><span data-stu-id="2a629-131">All other attributes</span></span>        | <span data-ttu-id="2a629-132">**Stringa**</span><span class="sxs-lookup"><span data-stu-id="2a629-132">**String**</span></span>                     |



 

<span data-ttu-id="2a629-133">Per gli attributi il cui valore sottostante è **booleano**, questo metodo restituisce la stringa "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="2a629-133">For attributes whose underlying value is **Boolean**, this method returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="2a629-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a629-134">Remarks</span></span>

<span data-ttu-id="2a629-135">Questo metodo recupera i metadati per un singolo elemento multimediale digitale o un elemento multimediale che fa parte di una playlist.</span><span class="sxs-lookup"><span data-stu-id="2a629-135">This method retrieves the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="2a629-136">Questo metodo supporta attributi con più valori e attributi con valori complessi.</span><span class="sxs-lookup"><span data-stu-id="2a629-136">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="2a629-137">Il metodo **GetItemInfo** non supporta attributi con più valori e attributi con valori complessi.</span><span class="sxs-lookup"><span data-stu-id="2a629-137">The **getItemInfo** method does not support attributes with multiple values and attributes with complex values.</span></span>

<span data-ttu-id="2a629-138">La proprietà **attributeCount** contiene il numero di nomi di attributi disponibili per un determinato oggetto **multimediale** .</span><span class="sxs-lookup"><span data-stu-id="2a629-138">The **attributeCount** property contains the number of attribute names available for a given **Media** object.</span></span> <span data-ttu-id="2a629-139">I numeri di indice possono quindi essere usati con il metodo **GetAttribute** per determinare il nome di ogni attributo disponibile.</span><span class="sxs-lookup"><span data-stu-id="2a629-139">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="2a629-140">I singoli nomi di attributo possono essere passati al parametro *Name* di **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="2a629-140">Individual attribute names can be passed to the *name* parameter of **getItemInfoByType**.</span></span>

<span data-ttu-id="2a629-141">Il metodo **getAttributeCountByType** restituisce il numero di attributi che corrispondono a un nome di attributo specifico per un determinato oggetto **multimediale** .</span><span class="sxs-lookup"><span data-stu-id="2a629-141">The **getAttributeCountByType** method returns the number of attributes that correspond to a particular attribute name for a given **Media** object.</span></span> <span data-ttu-id="2a629-142">I numeri di indice possono quindi essere passati al parametro di *Indice* di **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="2a629-142">Index numbers can then be passed to the *index* parameter of **getItemInfoByType**.</span></span> <span data-ttu-id="2a629-143">Questa operazione è utile quando un elemento multimediale digitale è stato categorizzato in più generi, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="2a629-143">This is useful when a digital media item has been categorized under multiple genres, for example.</span></span>

<span data-ttu-id="2a629-144">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="2a629-144">To use this method, read access to the library is required.</span></span> <span data-ttu-id="2a629-145">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2a629-145">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="2a629-146">Questo metodo può causare errori.</span><span class="sxs-lookup"><span data-stu-id="2a629-146">This method can cause errors.</span></span> <span data-ttu-id="2a629-147">Quando si chiama questo metodo, è necessario includere il codice di gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="2a629-147">You should include error-handling code when you call this method.</span></span> <span data-ttu-id="2a629-148">In JScript, ad esempio, è possibile implementare la gestione degli errori usando il **try... rileva... Infine** , struttura.</span><span class="sxs-lookup"><span data-stu-id="2a629-148">For example, in JScript you can implement error handling by using the **try...catch...finally** structure.</span></span>

<span data-ttu-id="2a629-149">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="2a629-149">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a629-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a629-150">Requirements</span></span>



| <span data-ttu-id="2a629-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a629-151">Requirement</span></span> | <span data-ttu-id="2a629-152">Valore</span><span class="sxs-lookup"><span data-stu-id="2a629-152">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2a629-153">Versione</span><span class="sxs-lookup"><span data-stu-id="2a629-153">Version</span></span><br/> | <span data-ttu-id="2a629-154">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="2a629-154">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="2a629-155">DLL</span><span class="sxs-lookup"><span data-stu-id="2a629-155">DLL</span></span><br/>     | <dl> <span data-ttu-id="2a629-156"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a629-156"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a629-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a629-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a629-158">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="2a629-158">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="2a629-159">**Media. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="2a629-159">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="2a629-160">**Media. getAttributeCountByType**</span><span class="sxs-lookup"><span data-stu-id="2a629-160">**Media.getAttributeCountByType**</span></span>](media-getattributecountbytype.md)
</dt> <dt>

[<span data-ttu-id="2a629-161">**Media. GetAttribute**</span><span class="sxs-lookup"><span data-stu-id="2a629-161">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="2a629-162">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="2a629-162">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="2a629-163">**Media. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="2a629-163">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="2a629-164">**Oggetto MetadataPicture**</span><span class="sxs-lookup"><span data-stu-id="2a629-164">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
</dt> <dt>

[<span data-ttu-id="2a629-165">**Oggetto MetadataText**</span><span class="sxs-lookup"><span data-stu-id="2a629-165">**MetadataText Object**</span></span>](metadatatext-object.md)
</dt> <dt>

[<span data-ttu-id="2a629-166">**Lettura di valori di attributo**</span><span class="sxs-lookup"><span data-stu-id="2a629-166">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="2a629-167">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2a629-167">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="2a629-168">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2a629-168">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





