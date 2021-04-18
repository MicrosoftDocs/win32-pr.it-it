---
title: Media. imageSourceWidth
description: La proprietà imageSourceWidth recupera la larghezza dell'elemento multimediale corrente in pixel.
ms.assetid: 6559bd51-cec2-4fc6-aab8-f2fdd1d59bae
keywords:
- Media Player Windows Media. imageSourceWidth
topic_type:
- apiref
api_name:
- Media.imageSourceWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2a3fef7b74a3d033b058f0afd1f6eece007bd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329921"
---
# <a name="mediaimagesourcewidth"></a><span data-ttu-id="ce0ed-104">Media. imageSourceWidth</span><span class="sxs-lookup"><span data-stu-id="ce0ed-104">Media.imageSourceWidth</span></span>

<span data-ttu-id="ce0ed-105">La proprietà **imageSourceWidth** recupera la larghezza dell'elemento multimediale corrente in pixel.</span><span class="sxs-lookup"><span data-stu-id="ce0ed-105">The **imageSourceWidth** property retrieves the width of the current media item in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce0ed-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce0ed-106">Syntax</span></span>

<span data-ttu-id="ce0ed-107">*Player*. *currentMedia*. **imageSourceWidth**</span><span class="sxs-lookup"><span data-stu-id="ce0ed-107">*player*.*currentMedia*.**imageSourceWidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="ce0ed-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="ce0ed-108">Possible Values</span></span>

<span data-ttu-id="ce0ed-109">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="ce0ed-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="ce0ed-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce0ed-110">Remarks</span></span>

<span data-ttu-id="ce0ed-111">Se l'elemento multimediale non è quello corrente, questa proprietà restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="ce0ed-111">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="ce0ed-112">Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="ce0ed-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="ce0ed-113">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ce0ed-113">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ce0ed-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="ce0ed-114">Examples</span></span>

<span data-ttu-id="ce0ed-115">Nell'esempio JScript seguente viene usato il *supporto*. **imageSourceWidth** per visualizzare la dimensione dell'immagine, in pixel, dell' **elemento multimediale corrente. Le informazioni vengono stampate in un elemento TEXTAREA HTML denominato VideoSize. L'oggetto Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="ce0ed-115">The following JScript example uses *Media*.**imageSourceWidth** to display the image size, in pixels, of the **current media item. The information is printed to an HTML TEXTAREA element named VideoSize. The Player** object was created with ID = "player".</span></span>


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player"  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Store the height and width of the new media item.
   var Height = Player.currentMedia.imageSourceHeight;
   var Width =  Player.currentMedia.imageSourceWidth;

   // Erase the information in the text area.
   VideoSize.value = "";

   // Test whether an image is visible.
   if (Height != 0 && Width != 0)

      // Display the image size information.
      VideoSize.value = Width + " x " + Height;
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="ce0ed-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce0ed-116">Requirements</span></span>



| <span data-ttu-id="ce0ed-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce0ed-117">Requirement</span></span> | <span data-ttu-id="ce0ed-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ce0ed-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ce0ed-119">Versione</span><span class="sxs-lookup"><span data-stu-id="ce0ed-119">Version</span></span><br/> | <span data-ttu-id="ce0ed-120">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="ce0ed-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ce0ed-121">DLL</span><span class="sxs-lookup"><span data-stu-id="ce0ed-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="ce0ed-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce0ed-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce0ed-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce0ed-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce0ed-124">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="ce0ed-124">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="ce0ed-125">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="ce0ed-125">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="ce0ed-126">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ce0ed-126">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="ce0ed-127">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ce0ed-127">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





