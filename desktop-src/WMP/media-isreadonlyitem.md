---
title: Media. isReadOnlyItem, metodo
description: Il metodo isReadOnlyItem restituisce un valore che indica se l'attributo specificato dell'elemento multimediale può essere modificato.
ms.assetid: 5e398e76-f64a-45b5-9b4f-679c65e5a0d1
keywords:
- Metodo isReadOnlyItem Windows Media Player
- Metodo isReadOnlyItem Windows Media Player, classe media
- Media class Media Player Windows, metodo isReadOnlyItem
topic_type:
- apiref
api_name:
- Media.isReadOnlyItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ac5bb8d445c3ba6418be4ee5c0c5e7a96f507d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323907"
---
# <a name="mediaisreadonlyitem-method"></a><span data-ttu-id="2b21f-106">Media. isReadOnlyItem, metodo</span><span class="sxs-lookup"><span data-stu-id="2b21f-106">Media.isReadOnlyItem method</span></span>

<span data-ttu-id="2b21f-107">Il metodo **isReadOnlyItem** restituisce un valore che indica se l'attributo specificato dell'elemento multimediale può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="2b21f-107">The **isReadOnlyItem** method returns a value indicating whether the specified attribute of the media item can be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b21f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b21f-108">Syntax</span></span>


```JScript
bRetVal = Media.isReadOnlyItem(
  attribute
)
```



## <a name="parameters"></a><span data-ttu-id="2b21f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b21f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b21f-110">*attributo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b21f-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b21f-111">**Stringa** che indica il nome dell'attributo da testare.</span><span class="sxs-lookup"><span data-stu-id="2b21f-111">**String** indicating the name of the attribute to test.</span></span> <span data-ttu-id="2b21f-112">Per informazioni sugli attributi supportati da Windows Media Player, vedere le informazioni di [riferimento sull'attributo](attribute-reference.md)Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="2b21f-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b21f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b21f-113">Return value</span></span>

<span data-ttu-id="2b21f-114">Questo metodo restituisce un **valore booleano**.</span><span class="sxs-lookup"><span data-stu-id="2b21f-114">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b21f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b21f-115">Remarks</span></span>

<span data-ttu-id="2b21f-116">Se un attributo è di sola lettura, non può essere impostato con il metodo **setItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="2b21f-116">If an attribute is read-only, then it cannot be set with the **setItemInfo** method.</span></span> <span data-ttu-id="2b21f-117">Si noti che questo metodo può restituire valori diversi per un attributo specifico se usato con versioni diverse di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="2b21f-117">Note that this method may return different values for a particular attribute when used with different versions of Windows Media Player.</span></span>

<span data-ttu-id="2b21f-118">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="2b21f-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="2b21f-119">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2b21f-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="2b21f-120">**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="2b21f-120">**Windows Media Player 10 Mobile:** This property always returns **true**.</span></span>

## <a name="examples"></a><span data-ttu-id="2b21f-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="2b21f-121">Examples</span></span>

<span data-ttu-id="2b21f-122">Nell'esempio JScript seguente viene usato il *supporto*. **isReadOnlyItem** per inserire un elemento textarea HTML denominato rwText con le informazioni sull'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="2b21f-122">The following JScript example uses *Media*.**isReadOnlyItem** to fill an HTML TEXTAREA element named rwText with information about the current media item.</span></span> <span data-ttu-id="2b21f-123">Il codice restituisce ogni attributo dell'elemento multimediale corrente, insieme al testo che indica se l'attributo è di sola lettura o in lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2b21f-123">The code outputs each attribute of the current media item, along with text indicating whether the attribute is read-only or read/write.</span></span> <span data-ttu-id="2b21f-124">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="2b21f-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media item object.
var cm = Player.currentMedia;

// Create a variable to hold each attribute name.
var atName;

// Loop through the attribute list.
for(var i = 0; i < cm.attributeCount; i++){

   // Get the attribute name.
   atName = cm.getAttributeName(i);

   // Test whether the attribute is read-only.
   var test = ((cm.isReadOnlyItem(atName))?"Read-Only":"Read/Write");

// Print the attribute information to the text area.
   rwText.value += atName + " is " + test;
   rwText.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="2b21f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b21f-125">Requirements</span></span>



| <span data-ttu-id="2b21f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b21f-126">Requirement</span></span> | <span data-ttu-id="2b21f-127">Valore</span><span class="sxs-lookup"><span data-stu-id="2b21f-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2b21f-128">Versione</span><span class="sxs-lookup"><span data-stu-id="2b21f-128">Version</span></span><br/> | <span data-ttu-id="2b21f-129">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="2b21f-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2b21f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="2b21f-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="2b21f-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b21f-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b21f-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b21f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b21f-133">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="2b21f-133">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="2b21f-134">**Media. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="2b21f-134">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="2b21f-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2b21f-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="2b21f-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2b21f-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





