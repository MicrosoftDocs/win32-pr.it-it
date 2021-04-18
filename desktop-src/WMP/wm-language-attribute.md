---
title: Attributo WM/Language
description: L'attributo WM/Language è la lingua dell'elemento.
ms.assetid: aebfb518-61ca-4b75-875a-ce2127a74b67
keywords:
- Finestra degli attributi WM/Language Media Player
topic_type:
- apiref
api_name:
- WM/Language
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172cc8498bf5360e29822a484bcc2ddacd70b8b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327011"
---
# <a name="wmlanguage-attribute"></a>Attributo WM/Language

L'attributo **WM/Language** è la lingua dell'elemento.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Attributi di file di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)
-   [Elementi radio](radio-item-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.

Questo attributo può avere più valori. Per recuperare tutti i valori per un attributo multivalore, è necessario usare il metodo **Media. getItemInfoByType** , non il metodo **Media. GetItemInfo** .

**Language** è un alias per questo attributo.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMLanguage.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 Series o versione successiva (l'elemento radio è supportato solo nella serie Windows Media Player 9)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





