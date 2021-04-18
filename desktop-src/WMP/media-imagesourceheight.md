---
title: Media. imageSourceHeight
description: La proprietà ImageSourceHeight recupera l'altezza in pixel dell'elemento multimediale corrente.
ms.assetid: fa98ec62-4c58-46ab-98f3-8017096d46d8
keywords:
- Media Player Windows Media. imageSourceHeight
topic_type:
- apiref
api_name:
- Media.imageSourceHeight
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de364243e71c6653085b4c9c9ff81f148dc299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329926"
---
# <a name="mediaimagesourceheight"></a><span data-ttu-id="b8c8f-104">Media. imageSourceHeight</span><span class="sxs-lookup"><span data-stu-id="b8c8f-104">Media.imageSourceHeight</span></span>

<span data-ttu-id="b8c8f-105">La proprietà **ImageSourceHeight** recupera l'altezza in pixel dell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="b8c8f-105">The **ImageSourceHeight** property retrieves the height of the current media item in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8c8f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8c8f-106">Syntax</span></span>

<span data-ttu-id="b8c8f-107">*Player*. *currentMedia*. **imageSourceHeight**</span><span class="sxs-lookup"><span data-stu-id="b8c8f-107">*player*.*currentMedia*.**imageSourceHeight**</span></span>

## <a name="possible-values"></a><span data-ttu-id="b8c8f-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="b8c8f-108">Possible Values</span></span>

<span data-ttu-id="b8c8f-109">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="b8c8f-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="b8c8f-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8c8f-110">Remarks</span></span>

<span data-ttu-id="b8c8f-111">Se l'elemento multimediale non è quello corrente, questa proprietà restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="b8c8f-111">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="b8c8f-112">Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="b8c8f-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="b8c8f-113">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b8c8f-113">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b8c8f-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="b8c8f-114">Examples</span></span>

<span data-ttu-id="b8c8f-115">Nell'esempio JScript seguente viene utilizzato *media*. imageSourceHeight per visualizzare la dimensione dell'immagine, in pixel, dell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="b8c8f-115">The following JScript example uses *Media*.imageSourceHeight to display the image size, in pixels, of the current media item.</span></span> <span data-ttu-id="b8c8f-116">Le informazioni vengono stampate in un elemento TEXTAREA HTML denominato VideoSize.</span><span class="sxs-lookup"><span data-stu-id="b8c8f-116">The information is printed to an HTML TEXTAREA element named VideoSize.</span></span> <span data-ttu-id="b8c8f-117">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="b8c8f-117">The **Player** object was created with ID = "player".</span></span>


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

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



## <a name="requirements"></a><span data-ttu-id="b8c8f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8c8f-118">Requirements</span></span>



| <span data-ttu-id="b8c8f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8c8f-119">Requirement</span></span> | <span data-ttu-id="b8c8f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c8f-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b8c8f-121">Versione</span><span class="sxs-lookup"><span data-stu-id="b8c8f-121">Version</span></span><br/> | <span data-ttu-id="b8c8f-122">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="b8c8f-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b8c8f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b8c8f-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="b8c8f-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8c8f-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8c8f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8c8f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8c8f-126">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="b8c8f-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="b8c8f-127">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="b8c8f-127">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="b8c8f-128">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b8c8f-128">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="b8c8f-129">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b8c8f-129">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





