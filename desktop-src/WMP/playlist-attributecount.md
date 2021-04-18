---
title: Playlist. attributeCount
description: La proprietà attributeCount Recupera il numero di attributi associati alla playlist.
ms.assetid: 92063131-0118-4458-9122-0539628a9821
keywords:
- Playlist. attributeCount Windows Media Player
topic_type:
- apiref
api_name:
- Playlist.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e42d72e029f232bb6dabc074b412406a1bb64c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329437"
---
# <a name="playlistattributecount"></a><span data-ttu-id="0a9d2-104">Playlist. attributeCount</span><span class="sxs-lookup"><span data-stu-id="0a9d2-104">Playlist.attributeCount</span></span>

<span data-ttu-id="0a9d2-105">La proprietà **attributeCount** Recupera il numero di attributi associati alla playlist.</span><span class="sxs-lookup"><span data-stu-id="0a9d2-105">The **attributeCount** property retrieves the number of attributes associated with the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a9d2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a9d2-106">Syntax</span></span>

<span data-ttu-id="0a9d2-107">*Player*. *currentPlaylist*. **attributeCount**</span><span class="sxs-lookup"><span data-stu-id="0a9d2-107">*player*.*currentPlaylist*.**attributeCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="0a9d2-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="0a9d2-108">Possible Values</span></span>

<span data-ttu-id="0a9d2-109">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="0a9d2-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="0a9d2-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a9d2-110">Remarks</span></span>

<span data-ttu-id="0a9d2-111">Poiché le playlist possono provenire da molte origini diverse, possono avere diversi set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="0a9d2-111">Because playlists can come from many different sources, they can have several different sets of properties.</span></span> <span data-ttu-id="0a9d2-112">Questo metodo recupera il numero totale di proprietà disponibili, in modo che gli altri metodi dell'oggetto **playlist** possano accedervi.</span><span class="sxs-lookup"><span data-stu-id="0a9d2-112">This method retrieves the total number of properties available so that the other methods of the **Playlist** object can access them.</span></span>

<span data-ttu-id="0a9d2-113">Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="0a9d2-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="0a9d2-114">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="0a9d2-114">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="0a9d2-115">Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0a9d2-115">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0a9d2-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="0a9d2-116">Examples</span></span>

<span data-ttu-id="0a9d2-117">Nell'esempio JScript riportato di seguito viene illustrato il modo in cui vengono utilizzate le varie proprietà e i metodi della **playlist** e degli oggetti **multimediali** .</span><span class="sxs-lookup"><span data-stu-id="0a9d2-117">The following JScript example illustrates how various properties and methods of the **Playlist** and **Media** objects are used.</span></span>


```JScript
function onLoad() {
    var display;
    var pl = player.currentPlaylist;

    pl.setItemInfo("custom playlist attribute", "changed");
    pl.item(0).setItemInfo("new custom attribute", "5");

    display = pl.attributeCount + " Playlist Attributes:\r\r";

    for (var i = 0; i < pl.attributeCount; ++i) {
        display = display + pl.attributeName(i) + ": ";
        display = display + pl.getItemInfo(pl.attributeName(i)) + "\r";
    }

    for (var j = 0; j < pl.count; ++j) {
        display = display + "\rTrack " + j + "\r"
        display = display + pl.item(j).attributeCount + " Attributes:\r\r";

        for (var k = 0; k < pl.item(j).attributeCount; ++k) {
            var it = pl.item(j);  // Media object
            display = display + it.getAttributeName(k) + ": ";
            display = display + it.getItemInfo(it.getAttributeName(k)) + "\r";
        }
    }

    myText.value = display;
}

```



## <a name="requirements"></a><span data-ttu-id="0a9d2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a9d2-118">Requirements</span></span>



| <span data-ttu-id="0a9d2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a9d2-119">Requirement</span></span> | <span data-ttu-id="0a9d2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0a9d2-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0a9d2-121">Versione</span><span class="sxs-lookup"><span data-stu-id="0a9d2-121">Version</span></span><br/> | <span data-ttu-id="0a9d2-122">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="0a9d2-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0a9d2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0a9d2-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="0a9d2-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a9d2-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a9d2-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a9d2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a9d2-126">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="0a9d2-126">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="0a9d2-127">**Playlist. AttributeName**</span><span class="sxs-lookup"><span data-stu-id="0a9d2-127">**Playlist.attributeName**</span></span>](playlist-attributename.md)
</dt> <dt>

[<span data-ttu-id="0a9d2-128">**Playlist. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="0a9d2-128">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="0a9d2-129">**Playlist. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="0a9d2-129">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="0a9d2-130">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="0a9d2-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="0a9d2-131">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="0a9d2-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





