---
title: Attributo WM/ProviderRating
description: L'attributo WM/ProviderRating è la classificazione dell'elemento assegnato dal provider dei valori dell'attributo.
ms.assetid: a1a76560-a8d9-486a-badc-56d7bf488c10
keywords:
- Media Player Windows per gli attributi WM/ProviderRating
topic_type:
- apiref
api_name:
- WM/ProviderRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc0f71985d948e59b8c0f98d50445a48263d67cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326998"
---
# <a name="wmproviderrating-attribute"></a>Attributo WM/ProviderRating

L'attributo **WM/ProviderRating** è la classificazione dell'elemento assegnato dal provider dei valori dell'attributo.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Playlist CD](cd-playlist-attributes.md)
-   [Tracce CD](cd-track-attributes.md)
-   [Attributi di file di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)
-   [DVD](dvd-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato nella libreria o nella cache e nel file multimediale digitale.

**Rating** è un alias per questo attributo.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMProviderRating.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





