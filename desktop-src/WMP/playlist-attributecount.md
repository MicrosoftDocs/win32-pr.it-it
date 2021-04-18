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
# <a name="playlistattributecount"></a>Playlist. attributeCount

La proprietà **attributeCount** Recupera il numero di attributi associati alla playlist.

## <a name="syntax"></a>Sintassi

*Player*. *currentPlaylist*. **attributeCount**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**).

## <a name="remarks"></a>Commenti

Poiché le playlist possono provenire da molte origini diverse, possono avere diversi set di proprietà. Questo metodo recupera il numero totale di proprietà disponibili, in modo che gli altri metodi dell'oggetto **playlist** possano accedervi.

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.

## <a name="examples"></a>Esempio

Nell'esempio JScript riportato di seguito viene illustrato il modo in cui vengono utilizzate le varie proprietà e i metodi della **playlist** e degli oggetti **multimediali** .


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto playlist**](playlist-object.md)
</dt> <dt>

[**Playlist. AttributeName**](playlist-attributename.md)
</dt> <dt>

[**Playlist. getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Playlist. setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





