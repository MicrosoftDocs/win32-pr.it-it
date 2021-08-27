---
title: Attributo WM/Language
description: L'attributo WM/Language è la lingua dell'elemento.
ms.assetid: aebfb518-61ca-4b75-875a-ce2127a74b67
keywords:
- Attributi WM/Language Windows Media Player
topic_type:
- apiref
api_name:
- WM/Language
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8902d36ebe9e8227d22f55273e8351d7ed09c592953b44a31e45c06b838f9871
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122651"
---
# <a name="wmlanguage-attribute"></a>Attributo WM/Language

**L'attributo WM/Language** è la lingua dell'elemento.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Attributi dei Windows file multimediali comunemente usati](commonly-used-windows-media-file-attributes.md)
-   [Elementi radio](radio-item-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.

Questo attributo può avere più valori. Per recuperare tutti i valori per un attributo multivalore, è necessario usare il metodo **Media.getItemInfoByType,** non il **metodo Media.getItemInfo.**

**Language** è un alias per questo attributo.

La Windows Media Format SDK per questo attributo è g \_ wszWMLanguage.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successiva (l'elemento radio è supportato solo in Windows Media Player serie 9)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento su attributi**](attribute-reference.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





