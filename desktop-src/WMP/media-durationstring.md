---
title: Media. durationString
description: La proprietà durationString recupera un valore stringa che indica la durata dell'elemento multimediale corrente nel formato HH MM SS.
ms.assetid: dfcb4c2e-c62c-4c3e-a9f4-fd147fb5b28c
keywords:
- Media Player Windows Media. durationString
topic_type:
- apiref
api_name:
- Media.durationString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1bbb89716ab1d06b176754396611ab22980659
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331384"
---
# <a name="mediadurationstring"></a><span data-ttu-id="5c673-104">Media. durationString</span><span class="sxs-lookup"><span data-stu-id="5c673-104">Media.durationString</span></span>

<span data-ttu-id="5c673-105">La proprietà **durationstring** recupera un valore **stringa** che indica la durata dell'elemento multimediale corrente nel formato HH: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="5c673-105">The **durationString** property retrieves a **String** value indicating the duration of the current media item in HH:MM:SS format.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c673-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c673-106">Syntax</span></span>

<span data-ttu-id="5c673-107">*Player*. *currentMedia*. **durationstring**</span><span class="sxs-lookup"><span data-stu-id="5c673-107">*player*.*currentMedia*.**durationString**</span></span>

## <a name="possible-values"></a><span data-ttu-id="5c673-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="5c673-108">Possible Values</span></span>

<span data-ttu-id="5c673-109">Questa proprietà è una **stringa** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="5c673-109">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c673-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c673-110">Remarks</span></span>

<span data-ttu-id="5c673-111">Se questa proprietà viene utilizzata con un elemento multimediale diverso da quello specificato in *Player*. **currentMedia**, non può contenere un valore valido.</span><span class="sxs-lookup"><span data-stu-id="5c673-111">If this property is used with a media item other than the one specified in *Player*.**currentMedia**, it may not contain a valid value.</span></span> <span data-ttu-id="5c673-112">Se la lunghezza dell'elemento multimediale è inferiore a un'ora, la parte HH: del valore restituito viene omessa.</span><span class="sxs-lookup"><span data-stu-id="5c673-112">If the media item is less than an hour long, the HH: portion of the return value is omitted.</span></span>

<span data-ttu-id="5c673-113">Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="5c673-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="5c673-114">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5c673-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5c673-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="5c673-115">Examples</span></span>

<span data-ttu-id="5c673-116">Nell'esempio JScript seguente viene usato il *supporto*. **durationstring** per visualizzare la durata dell'elemento multimediale corrente come testo formattato.</span><span class="sxs-lookup"><span data-stu-id="5c673-116">The following JScript example uses *Media*.**durationString** to display the duration of the current media item as formatted text.</span></span> <span data-ttu-id="5c673-117">Un elemento DIV HTML denominato MediaInfo Visualizza le informazioni sulla durata.</span><span class="sxs-lookup"><span data-stu-id="5c673-117">An HTML DIV element named MediaInfo displays the duration information.</span></span> <span data-ttu-id="5c673-118">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="5c673-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler to update the display when
 the current media item changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Write the formatted duration string to the DIV region.
   MediaInfo.innerHTML = "Duration: " + Player.currentMedia.durationString;
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="5c673-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c673-119">Requirements</span></span>



| <span data-ttu-id="5c673-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c673-120">Requirement</span></span> | <span data-ttu-id="5c673-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5c673-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5c673-122">Versione</span><span class="sxs-lookup"><span data-stu-id="5c673-122">Version</span></span><br/> | <span data-ttu-id="5c673-123">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="5c673-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5c673-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5c673-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="5c673-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c673-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c673-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c673-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c673-127">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="5c673-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="5c673-128">**Media. durata**</span><span class="sxs-lookup"><span data-stu-id="5c673-128">**Media.duration**</span></span>](media-duration.md)
</dt> <dt>

[<span data-ttu-id="5c673-129">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="5c673-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="5c673-130">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5c673-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="5c673-131">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5c673-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





