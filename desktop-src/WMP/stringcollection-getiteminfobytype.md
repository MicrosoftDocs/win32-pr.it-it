---
title: StringCollection. getItemInfoByType, metodo
description: Il metodo getItemInfoByType Recupera il valore corrispondente all'indice Stringacollection, al nome, alla lingua e all'indice dell'attributo specificati.
ms.assetid: 32a25c69-9399-4857-84c1-143c529be58f
keywords:
- Metodo getItemInfoByType Windows Media Player
- Metodo getItemInfoByType Windows Media Player, classe StringCollection
- StringCollection (classe) Windows Media Player, metodo getItemInfoByType
topic_type:
- apiref
api_name:
- StringCollection.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b3aa8c5bc367095765f24f19f107dd7cb986ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326448"
---
# <a name="stringcollectiongetiteminfobytype-method"></a><span data-ttu-id="8c587-106">StringCollection. getItemInfoByType, metodo</span><span class="sxs-lookup"><span data-stu-id="8c587-106">StringCollection.getItemInfoByType method</span></span>

<span data-ttu-id="8c587-107">Il metodo **getItemInfoByType** Recupera il valore corrispondente all'indice **stringacollection** , al nome, alla lingua e all'indice dell'attributo specificati.</span><span class="sxs-lookup"><span data-stu-id="8c587-107">The **getItemInfoByType** method retrieves the value corresponding to the specified **StringCollection** index, name, language, and attribute index.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c587-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c587-108">Syntax</span></span>


```JScript
retVal = StringCollection.getItemInfoByType(
  index,
  name,
  language,
  attributeIndex
)
```



## <a name="parameters"></a><span data-ttu-id="8c587-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c587-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c587-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8c587-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c587-111">**Numero** (**Long**) che specifica l'indice in base zero dell'elemento **StringCollection** da cui ottenere l'attributo.</span><span class="sxs-lookup"><span data-stu-id="8c587-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="8c587-112">*nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c587-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c587-113">**Stringa** contenente il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="8c587-113">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="8c587-114">*lingua* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8c587-114">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c587-115">**Stringa** contenente il linguaggio.</span><span class="sxs-lookup"><span data-stu-id="8c587-115">**String** containing the language.</span></span> <span data-ttu-id="8c587-116">Se il valore è impostato su null o la stringa vuota ("") viene utilizzata la stringa delle impostazioni locali corrente.</span><span class="sxs-lookup"><span data-stu-id="8c587-116">If the value is set to null or the empty string ("") the current locale string is used.</span></span> <span data-ttu-id="8c587-117">In caso contrario, il valore deve essere una stringa di linguaggio RFC 1766 valida, ad esempio "en-US".</span><span class="sxs-lookup"><span data-stu-id="8c587-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="8c587-118">*attributeIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c587-118">*attributeIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c587-119">**Numero** (**Long**) che contiene l'indice in base zero del valore da recuperare dall'attributo.</span><span class="sxs-lookup"><span data-stu-id="8c587-119">**Number** (**long**) containing the zero-based index of the value to retrieve from the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c587-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8c587-120">Return value</span></span>

<span data-ttu-id="8c587-121">Questo metodo restituisce un oggetto **Number**, **String**, **MetadataPicture** o **MetadataText** come indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8c587-121">This method returns a **Number**, **String**, **MetadataPicture** object, or **MetadataText** object as indicated in the following table.</span></span>



| <span data-ttu-id="8c587-122">Attributo</span><span class="sxs-lookup"><span data-stu-id="8c587-122">Attribute</span></span>                   | <span data-ttu-id="8c587-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8c587-123">Return value</span></span>                   |
|-----------------------------|--------------------------------|
| <span data-ttu-id="8c587-124">**SyncState**</span><span class="sxs-lookup"><span data-stu-id="8c587-124">**SyncState**</span></span>               | <span data-ttu-id="8c587-125">**Numero** (**unsigned long**)</span><span class="sxs-lookup"><span data-stu-id="8c587-125">**Number** (**unsigned long**)</span></span> |
| <span data-ttu-id="8c587-126">**WM/lyrics \_ sincronizzati**</span><span class="sxs-lookup"><span data-stu-id="8c587-126">**WM/Lyrics\_Synchronised**</span></span> | <span data-ttu-id="8c587-127">Oggetto **MetadataText**</span><span class="sxs-lookup"><span data-stu-id="8c587-127">**MetadataText** object</span></span>        |
| <span data-ttu-id="8c587-128">**WM/immagine**</span><span class="sxs-lookup"><span data-stu-id="8c587-128">**WM/Picture**</span></span>              | <span data-ttu-id="8c587-129">Oggetto **MetadataPicture**</span><span class="sxs-lookup"><span data-stu-id="8c587-129">**MetadataPicture** object</span></span>     |
| <span data-ttu-id="8c587-130">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="8c587-130">**WM/UserWebURL**</span></span>           | <span data-ttu-id="8c587-131">Oggetto **MetadataText**</span><span class="sxs-lookup"><span data-stu-id="8c587-131">**MetadataText** object</span></span>        |
| <span data-ttu-id="8c587-132">Tutti gli altri attributi</span><span class="sxs-lookup"><span data-stu-id="8c587-132">All other attributes</span></span>        | <span data-ttu-id="8c587-133">string</span><span class="sxs-lookup"><span data-stu-id="8c587-133">String</span></span>                         |



 

<span data-ttu-id="8c587-134">Per gli attributi il cui valore sottostante è **booleano**, questo metodo restituisce la stringa "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="8c587-134">For attributes whose underlying value is **Boolean**, this method returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="8c587-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c587-135">Remarks</span></span>

<span data-ttu-id="8c587-136">Questo metodo supporta attributi con più valori e attributi con valori complessi.</span><span class="sxs-lookup"><span data-stu-id="8c587-136">This method supports attributes with multiple values, and attributes with complex values.</span></span> <span data-ttu-id="8c587-137">Il metodo **GetItemInfo** non supporta attributi con valori multipli o complessi.</span><span class="sxs-lookup"><span data-stu-id="8c587-137">The **getItemInfo** method does not support attributes with multiple or complex values.</span></span>

<span data-ttu-id="8c587-138">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="8c587-138">To use this method, read access to the library is required.</span></span> <span data-ttu-id="8c587-139">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="8c587-139">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c587-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c587-140">Requirements</span></span>



| <span data-ttu-id="8c587-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c587-141">Requirement</span></span> | <span data-ttu-id="8c587-142">Valore</span><span class="sxs-lookup"><span data-stu-id="8c587-142">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8c587-143">Versione</span><span class="sxs-lookup"><span data-stu-id="8c587-143">Version</span></span><br/> | <span data-ttu-id="8c587-144">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="8c587-144">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="8c587-145">DLL</span><span class="sxs-lookup"><span data-stu-id="8c587-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="8c587-146"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c587-146"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c587-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c587-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c587-148">**Oggetto MetadataPicture**</span><span class="sxs-lookup"><span data-stu-id="8c587-148">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
</dt> <dt>

[<span data-ttu-id="8c587-149">**Oggetto MetadataText**</span><span class="sxs-lookup"><span data-stu-id="8c587-149">**MetadataText Object**</span></span>](metadatatext-object.md)
</dt> <dt>

[<span data-ttu-id="8c587-150">**StringCollection. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="8c587-150">**StringCollection.getItemInfo**</span></span>](stringcollection-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="8c587-151">**StringCollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="8c587-151">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





