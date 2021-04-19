---
title: Controls. currentMarker
description: La proprietà currentMarker specifica o Recupera il numero di marcatore corrente.
ms.assetid: 4b4eacd4-3df0-4e11-8755-1ac326fad027
keywords:
- Media Player di Windows Controls. currentMarker
topic_type:
- apiref
api_name:
- Controls.currentMarker
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aae8af226b62550b3faae9389385d321bf10aad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330119"
---
# <a name="controlscurrentmarker"></a><span data-ttu-id="00d83-104">Controls. currentMarker</span><span class="sxs-lookup"><span data-stu-id="00d83-104">Controls.currentMarker</span></span>

<span data-ttu-id="00d83-105">La proprietà **currentMarker** specifica o Recupera il numero di marcatore corrente.</span><span class="sxs-lookup"><span data-stu-id="00d83-105">The **currentMarker** property specifies or retrieves the current marker number.</span></span>

``` syntax
player.controls.currentMarker
      
```

## <a name="possible-values"></a><span data-ttu-id="00d83-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="00d83-106">Possible Values</span></span>

<span data-ttu-id="00d83-107">Questa proprietà è un **numero** di lettura/scrittura (**Long**) il cui valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="00d83-107">This property is a read/write **Number** (**long**) with a default value of zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="00d83-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="00d83-108">Remarks</span></span>

<span data-ttu-id="00d83-109">L'impostazione di **currentMarker** fa sì che la riproduzione venga avviata dal marcatore specificato.</span><span class="sxs-lookup"><span data-stu-id="00d83-109">Setting **currentMarker** causes playback to start from the specified marker.</span></span> <span data-ttu-id="00d83-110">Prima di provare a impostare **currentMarker**, determinare se un file contiene marcatori e il numero di marcatori utilizzando **markerCount**.</span><span class="sxs-lookup"><span data-stu-id="00d83-110">Before attempting to set **currentMarker**, determine whether a file has markers and how many it has by using **markerCount**.</span></span> <span data-ttu-id="00d83-111">Se un file non ha marcatori, l'impostazione di **currentMarker** su qualsiasi elemento, ma con zero, genera un errore.</span><span class="sxs-lookup"><span data-stu-id="00d83-111">If a file has no markers, setting **currentMarker** to anything but zero results in an error.</span></span> <span data-ttu-id="00d83-112">L'impostazione di **currentMarker** su un numero maggiore di **markerCount** genera anche un errore.</span><span class="sxs-lookup"><span data-stu-id="00d83-112">Setting **currentMarker** to a number higher than **markerCount** also results in an error.</span></span>

<span data-ttu-id="00d83-113">La proprietà **currentMarker** restituisce sempre il marcatore corrente o ultimo, il che significa che la posizione effettiva del file può essere in corrispondenza del marcatore corrente o prima del marcatore successivo.</span><span class="sxs-lookup"><span data-stu-id="00d83-113">The **currentMarker** property always returns the current or last marker, which means the actual file position can be either at the current marker or before the next marker.</span></span> <span data-ttu-id="00d83-114">I marcatori sono numerati a partire da 1, pertanto se un file contiene marcatori, è possibile impostare **currentMarker** su zero per modificare la posizione del file su zero.</span><span class="sxs-lookup"><span data-stu-id="00d83-114">Markers are numbered beginning at 1, so if a file has markers, you can set **currentMarker** to zero to change the file position to zero.</span></span>

<span data-ttu-id="00d83-115">Fino a quando non viene impostato l'elemento multimediale corrente (utilizzando *Player*.**URL** o *lettore*. **currentMedia**), **currentMarker** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="00d83-115">Until the current media item is set (using *Player*.**URL** or *Player*.**currentMedia**), **currentMarker** returns zero.</span></span>

## <a name="examples"></a><span data-ttu-id="00d83-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="00d83-116">Examples</span></span>

<span data-ttu-id="00d83-117">Nell'esempio JScript seguente viene usato **currentMarker** per avviare la riproduzione video dal marcatore che corrisponde alla proprietà **SelectedIndex** di un elemento HTML SELECT.</span><span class="sxs-lookup"><span data-stu-id="00d83-117">The following JScript example uses **currentMarker** to start video playback from the marker that corresponds to the **selectedIndex** property of an HTML SELECT element.</span></span> <span data-ttu-id="00d83-118">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="00d83-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = "markers"  NAME = "markers"  LANGUAGE = "JScript"

    /* Seek to the marker number that corresponds to the SELECT element
       selectedIndex value when the list selection changes. */
    onChange = "Player.controls.currentMarker = markers.selectedIndex + 1;
">

    /* Fill the SELECT element with the marker identifiers. */
    <OPTION SELECTED>Sunrise
    <OPTION>Car chase 
    <OPTION>Happy ending
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="00d83-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00d83-119">Requirements</span></span>



| <span data-ttu-id="00d83-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="00d83-120">Requirement</span></span> | <span data-ttu-id="00d83-121">Valore</span><span class="sxs-lookup"><span data-stu-id="00d83-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="00d83-122">Versione</span><span class="sxs-lookup"><span data-stu-id="00d83-122">Version</span></span><br/> | <span data-ttu-id="00d83-123">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="00d83-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="00d83-124">DLL</span><span class="sxs-lookup"><span data-stu-id="00d83-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="00d83-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00d83-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00d83-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00d83-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00d83-127">**Oggetto Controls**</span><span class="sxs-lookup"><span data-stu-id="00d83-127">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="00d83-128">**Media. markerCount**</span><span class="sxs-lookup"><span data-stu-id="00d83-128">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="00d83-129">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="00d83-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="00d83-130">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="00d83-130">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





