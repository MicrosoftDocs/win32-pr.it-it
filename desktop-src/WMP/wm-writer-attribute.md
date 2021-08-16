---
title: Attributo WM/Writer
description: L'attributo WM/Writer è il nome dello scrittore che ha scritto le parole del contenuto.
ms.assetid: e2035cf7-29f4-4642-9388-4cd7cb08149e
keywords:
- Attributi WM/Writer Windows Media Player
topic_type:
- apiref
api_name:
- WM/Writer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a239fd83c936a0712459307fbf08b01c4bfcc4f6fd4c6d32cddc12d8092f2b2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332056"
---
# <a name="wmwriter-attribute"></a>Attributo WM/Writer

**L'attributo WM/Writer** è il nome dello scrittore che ha scritto le parole del contenuto.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Attributi dei Windows file multimediali comunemente usati](commonly-used-windows-media-file-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.

Questo attributo può avere più valori. Per recuperare tutti i valori per un attributo multivalore, è necessario usare il metodo **Media.getItemInfoByType,** non il **metodo Media.getItemInfo.**

**Writer** è un alias per questo attributo.

La Windows Media Format SDK per questo attributo è g \_ wszWMWriter.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento su attributi**](attribute-reference.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





