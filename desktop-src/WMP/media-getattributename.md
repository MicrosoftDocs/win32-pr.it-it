---
title: Media. GetAttribute (metodo)
description: Il metodo GetAttribute Recupera il nome dell'attributo corrispondente all'indice specificato.
ms.assetid: f74d81c6-49f8-4b1e-a367-acb4a0914c5a
keywords:
- Metodo GetAttributeName Windows Media Player
- Metodo GetAttribute Media Player Windows, classe media
- Media class Media Player Windows, metodo GetAttribute
topic_type:
- apiref
api_name:
- Media.getAttributeName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7134b68837a7a5d1b765c64320ae68c56c6fc56
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326123"
---
# <a name="mediagetattributename-method"></a><span data-ttu-id="2f74d-106">Media. GetAttribute (metodo)</span><span class="sxs-lookup"><span data-stu-id="2f74d-106">Media.getAttributeName method</span></span>

<span data-ttu-id="2f74d-107">Il metodo **GetAttribute** Recupera il nome dell'attributo corrispondente all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="2f74d-107">The **getAttributeName** method retrieves the name of the attribute corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f74d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f74d-108">Syntax</span></span>


```JScript
strRetVal = Media.getAttributeName(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="2f74d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f74d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f74d-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="2f74d-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f74d-111">**Numero** (**Long**) che contiene l'indice dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="2f74d-111">**Number** (**long**) containing the index of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f74d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f74d-112">Return value</span></span>

<span data-ttu-id="2f74d-113">Questo metodo restituisce una **stringa** che specifica il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="2f74d-113">This method returns a **String** specifying the name of the attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f74d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f74d-114">Remarks</span></span>

<span data-ttu-id="2f74d-115">Il nome dell'attributo restituito può essere utilizzato insieme a **GetItemInfo** per recuperare il valore per un attributo denominato specifico.</span><span class="sxs-lookup"><span data-stu-id="2f74d-115">The attribute name returned can be used in conjunction with **getItemInfo** to retrieve the value for a specific named attribute.</span></span>

<span data-ttu-id="2f74d-116">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="2f74d-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="2f74d-117">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2f74d-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="2f74d-118">Per informazioni sugli attributi supportati da Windows Media Player, vedere le informazioni di [riferimento sull'attributo](attribute-reference.md)Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="2f74d-118">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

<span data-ttu-id="2f74d-119">**Windows Media Player 10 Mobile:** Gli attributi per un elemento multimediale sono disponibili solo durante la riproduzione, a meno che non vengano recuperati dall'elemento tramite la raccolta di supporti.</span><span class="sxs-lookup"><span data-stu-id="2f74d-119">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="examples"></a><span data-ttu-id="2f74d-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="2f74d-120">Examples</span></span>

<span data-ttu-id="2f74d-121">Nell'esempio JScript seguente viene usato il *supporto*. **GetAttribute** per riempire un'area di testo HTML denominata text con l'indice e il nome di ogni attributo per l'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="2f74d-121">The following JScript example uses *Media*.**getAttributeName** to fill an HTML text area named myText with the index and name of each attribute for the current media item.</span></span> <span data-ttu-id="2f74d-122">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="2f74d-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Get the number of attributes for the current media. 
var atCount = cm.attributeCount;

// Loop through the attribute list.
for(var i=0; i < atCount; i++){
   
   // Print each attribute index and name.   
   myText.value += "Attribute " + i +": ";
   myText.value += cm.getAttributeName(i);
   myText.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="2f74d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f74d-123">Requirements</span></span>



| <span data-ttu-id="2f74d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f74d-124">Requirement</span></span> | <span data-ttu-id="2f74d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="2f74d-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2f74d-126">Versione</span><span class="sxs-lookup"><span data-stu-id="2f74d-126">Version</span></span><br/> | <span data-ttu-id="2f74d-127">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="2f74d-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2f74d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2f74d-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="2f74d-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f74d-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f74d-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f74d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f74d-131">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="2f74d-131">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="2f74d-132">**Media. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="2f74d-132">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="2f74d-133">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="2f74d-133">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="2f74d-134">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2f74d-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="2f74d-135">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2f74d-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





