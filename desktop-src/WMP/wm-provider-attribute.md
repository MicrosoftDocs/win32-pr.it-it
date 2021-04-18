---
title: WM/attributo provider
description: L'attributo WM/provider è il nome del provider dei valori di attributo.
ms.assetid: 358651d3-5bcd-4a03-a9aa-a33745d0323a
keywords:
- Windows Media Player attributo WM/provider
topic_type:
- apiref
api_name:
- WM/Provider
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d7c2c1c796edf28a567f72708c60c7976f718bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327000"
---
# <a name="wmprovider-attribute"></a>WM/attributo provider

L'attributo **WM/provider** è il nome del provider dei valori di attributo.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Playlist CD](cd-playlist-attributes.md)
-   [Tracce CD](cd-track-attributes.md)
-   [Attributi di file di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)
-   [Elementi radio](radio-item-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato nella libreria o nella cache e nel file multimediale digitale.

**Metadatasource** è un alias per questo attributo.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMProvider.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 Series o versione successiva (l'elemento Photo è supportato solo in Windows Media Player 10 o versione successiva)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





