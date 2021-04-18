---
title: Attributo WM/ProtectionType
description: L'attributo WM/ProtectionType è il tipo di protezione utilizzato per il contenuto.
ms.assetid: aab36b57-5b4e-4a3f-80cf-872ec8369c49
keywords:
- Media Player Windows per gli attributi WM/ProtectionType
topic_type:
- apiref
api_name:
- WM/ProtectionType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bf2b9c4700cb45ca5daf2c7d9290456beefbf1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330452"
---
# <a name="wmprotectiontype-attribute"></a>Attributo WM/ProtectionType

L'attributo **WM/ProtectionType** è il tipo di protezione utilizzato per il contenuto.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Attributi di file di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.

**ProtectionType** è un alias per questo attributo.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMProtectionType.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





