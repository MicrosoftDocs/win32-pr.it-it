---
title: Media. attributeCount
description: La proprietà attributeCount Recupera il numero di attributi che è possibile sottoporre a query e/o impostare per l'elemento multimediale.
ms.assetid: d2a5286f-dde1-48b5-b486-6cee1be463f9
keywords:
- Media Player Windows Media. attributeCount
topic_type:
- apiref
api_name:
- Media.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df4979f670cdd6a79b1b309bc3eceff5a2798223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331386"
---
# <a name="mediaattributecount"></a><span data-ttu-id="c8725-104">Media. attributeCount</span><span class="sxs-lookup"><span data-stu-id="c8725-104">Media.attributeCount</span></span>

<span data-ttu-id="c8725-105">La proprietà **attributeCount** Recupera il numero di attributi che è possibile sottoporre a query e/o impostare per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="c8725-105">The **attributeCount** property retrieves the number of attributes that can be queried and/or set for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8725-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8725-106">Syntax</span></span>

<span data-ttu-id="c8725-107">*Player*. *currentMedia*. **attributeCount**</span><span class="sxs-lookup"><span data-stu-id="c8725-107">*player*.*currentMedia*.**attributeCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="c8725-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="c8725-108">Possible Values</span></span>

<span data-ttu-id="c8725-109">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="c8725-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="c8725-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8725-110">Remarks</span></span>

<span data-ttu-id="c8725-111">Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="c8725-111">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="c8725-112">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c8725-112">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="c8725-113">Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c8725-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="c8725-114">**Windows Media Player 10 Mobile:** Gli attributi per un elemento multimediale sono disponibili solo durante la riproduzione, a meno che non vengano recuperati dall'elemento tramite la raccolta di supporti.</span><span class="sxs-lookup"><span data-stu-id="c8725-114">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="examples"></a><span data-ttu-id="c8725-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="c8725-115">Examples</span></span>

<span data-ttu-id="c8725-116">Nell'esempio JScript seguente viene usato il *supporto*. **attributeCount** per determinare il numero di attributi disponibili nell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="c8725-116">The following JScript example uses *Media*.**attributeCount** to determine the number of attributes available in the current media item.</span></span> <span data-ttu-id="c8725-117">Il codice usa tale valore per stampare un elenco di nomi e valori di attributi in un'area di testo HTML, denominata testo.</span><span class="sxs-lookup"><span data-stu-id="c8725-117">The code uses that value to print a list of attribute names and values in an HTML text area, named myText.</span></span> <span data-ttu-id="c8725-118">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="c8725-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Create arrays to hold each attribute name and value.
var atNames = new Array();
var atValues = new Array();

// Loop through the attribute list.   
for(var i = 0; i < cm.attributeCount; i++){

   // Fill the arrays with the attribute info.
   atNames[i] = cm.getAttributeName(i);
   atValues[i] = cm.getItemInfo(atNames[i]);

   // Print the attribute information to the text area.
   myText.value += atNames[i] + ": " + atValues[i];
   myText.value += "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="c8725-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8725-119">Requirements</span></span>



| <span data-ttu-id="c8725-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8725-120">Requirement</span></span> | <span data-ttu-id="c8725-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c8725-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c8725-122">Versione</span><span class="sxs-lookup"><span data-stu-id="c8725-122">Version</span></span><br/> | <span data-ttu-id="c8725-123">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="c8725-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c8725-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c8725-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="c8725-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8725-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8725-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8725-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8725-127">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="c8725-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="c8725-128">**Media. GetAttribute**</span><span class="sxs-lookup"><span data-stu-id="c8725-128">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="c8725-129">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="c8725-129">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="c8725-130">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="c8725-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="c8725-131">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="c8725-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





