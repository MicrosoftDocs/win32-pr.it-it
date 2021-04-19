---
title: Mediacollection. getAttributeStringCollection, metodo
description: Il metodo getAttributeStringCollection recupera un oggetto StringCollection che rappresenta il set di tutti i valori di un attributo specificato all'interno di un tipo di supporto specificato.
ms.assetid: 75563a75-88f5-419e-983b-d105bce02511
keywords:
- Metodo getAttributeStringCollection Windows Media Player
- Metodo getAttributeStringCollection Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo getAttributeStringCollection
topic_type:
- apiref
api_name:
- MediaCollection.getAttributeStringCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d50d25488a05e6076c99802ce738edf02298ade
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330352"
---
# <a name="mediacollectiongetattributestringcollection-method"></a><span data-ttu-id="10fee-106">Mediacollection. getAttributeStringCollection, metodo</span><span class="sxs-lookup"><span data-stu-id="10fee-106">MediaCollection.getAttributeStringCollection method</span></span>

<span data-ttu-id="10fee-107">Il metodo **getAttributeStringCollection** recupera un oggetto **StringCollection** che rappresenta il set di tutti i valori di un attributo specificato all'interno di un tipo di supporto specificato.</span><span class="sxs-lookup"><span data-stu-id="10fee-107">The **getAttributeStringCollection** method retrieves a **StringCollection** object representing the set of all values for a specified attribute within a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="10fee-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="10fee-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getAttributeStringCollection(
  attribute,
  mediaType
)
```



## <a name="parameters"></a><span data-ttu-id="10fee-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="10fee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10fee-110">*attributo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10fee-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10fee-111">**Stringa** che specifica l'attributo.</span><span class="sxs-lookup"><span data-stu-id="10fee-111">**String** specifying the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="10fee-112">*mediaType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10fee-112">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10fee-113">**Stringa** che rappresenta il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="10fee-113">**String** representing the media type.</span></span> <span data-ttu-id="10fee-114">Contiene uno dei valori seguenti: "audio", "video", "playlist" o "other".</span><span class="sxs-lookup"><span data-stu-id="10fee-114">Contains one of the following values: "Audio", "Video", "Playlist", or "Other".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10fee-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10fee-115">Return value</span></span>

<span data-ttu-id="10fee-116">Questo metodo restituisce un oggetto **StringCollection** .</span><span class="sxs-lookup"><span data-stu-id="10fee-116">This method returns a **StringCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="10fee-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="10fee-117">Remarks</span></span>

<span data-ttu-id="10fee-118">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="10fee-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="10fee-119">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="10fee-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="10fee-120">Per informazioni sugli attributi supportati da Windows Media Player, vedere la sezione [riferimento all'attributo](attribute-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="10fee-120">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md) section.</span></span>

## <a name="examples"></a><span data-ttu-id="10fee-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="10fee-121">Examples</span></span>

<span data-ttu-id="10fee-122">Nell'esempio JScript seguente viene utilizzato *mediacollection*. **getAttributeStringCollection** per visualizzare un elenco di valori che corrispondono a un particolare attributo per gli elementi audio nell'insieme di supporti.</span><span class="sxs-lookup"><span data-stu-id="10fee-122">The following JScript example uses *MediaCollection*.**getAttributeStringCollection** to display a list of values that correspond to a particular attribute for audio items in the media collection.</span></span> <span data-ttu-id="10fee-123">Un elemento HTML SELECT, creato con ID = "Attribute", consente all'utente di selezionare un attributo, ad esempio artista, genere o album.</span><span class="sxs-lookup"><span data-stu-id="10fee-123">An HTML SELECT element, created with ID = "Attribute", allows the user to select an attribute, such as Artist, Genre, or Album.</span></span> <span data-ttu-id="10fee-124">Un elemento TEXTAREA HTML, creato con ID = "AttributeVals", Visualizza il risultato.</span><span class="sxs-lookup"><span data-stu-id="10fee-124">An HTML TEXTAREA element, created with ID = "AttributeVals", displays the result.</span></span> <span data-ttu-id="10fee-125">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="10fee-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Clear the text in the display area.
AttributeVals.value = "";

// Store the mediaCollection object.
var library = Player.mediaCollection;

// Get the string collection for the attribute type the user selects.
var all = library.getAttributeStringCollection(Attribute.value, "Audio");

// Loop through the string collection.
for (i = 0; i < all.count; i++){

    // Display the items one line at a time.
    AttributeVals.value += all.item(i);
    AttributeVals.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="10fee-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10fee-126">Requirements</span></span>



| <span data-ttu-id="10fee-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="10fee-127">Requirement</span></span> | <span data-ttu-id="10fee-128">Valore</span><span class="sxs-lookup"><span data-stu-id="10fee-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="10fee-129">Versione</span><span class="sxs-lookup"><span data-stu-id="10fee-129">Version</span></span><br/> | <span data-ttu-id="10fee-130">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="10fee-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="10fee-131">DLL</span><span class="sxs-lookup"><span data-stu-id="10fee-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="10fee-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10fee-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10fee-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10fee-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10fee-134">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="10fee-134">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="10fee-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="10fee-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="10fee-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="10fee-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="10fee-137">**StringCollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="10fee-137">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





