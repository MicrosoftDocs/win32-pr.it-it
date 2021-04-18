---
title: Attributo WM/MediaClassSecondaryID
description: L'attributo WM/MediaClassSecondaryID è un GUID che specifica la classe multimediale secondaria, che è una sottoclasse della classe multimediale primaria.
ms.assetid: 8112513a-b73a-497a-9c24-24ccef31cffc
keywords:
- Media Player Windows per gli attributi WM/MediaClassSecondaryID
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb88ea03e565df649088366e13b20332256b374d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327003"
---
# <a name="wmmediaclasssecondaryid-attribute"></a>Attributo WM/MediaClassSecondaryID

L'attributo **WM/MediaClassSecondaryID** è un GUID che specifica la classe multimediale secondaria, che è una sottoclasse della classe multimediale primaria.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Attributi di file di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)
-   [Altri elementi](other-item-attributes.md)
-   [Elementi foto](photo-item-attributes.md)
-   [Playlist](playlist-attributes-ref.md)
-   [Elementi radio](radio-item-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.

La tabella seguente elenca i GUID supportati e le relative descrizioni.



| GUID                                 | Descrizione                                    |
|--------------------------------------|------------------------------------------------|
| D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC | L'oggetto multimediale rappresenta una playlist statica. |
| EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D | L'oggetto multimediale rappresenta una playlist automatica.  |



 

**MediaClassSecondaryID** è un alias per questo attributo.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMMediaClassSecondaryID.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | L'elemento Photo è supportato solo in Windows Media Player 10 o versioni successive l'elemento radio è supportato solo in Windows Media Player 9 Series tutti gli altri elementi sono supportati in Windows Media Player 9 Series e versioni successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





