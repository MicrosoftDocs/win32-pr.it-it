---
title: Attributo WM/ContentGroupDescription
description: L'attributo WM/ContentGroupDescription è la descrizione del gruppo di contenuto, ovvero una raccolta di elementi multimediali, ad esempio un set di CD boxed.
ms.assetid: b2615f78-2d45-45f0-89f7-f1e8e083be9b
keywords:
- Media Player Windows per gli attributi WM/ContentGroupDescription
topic_type:
- apiref
api_name:
- WM/ContentGroupDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4690e52f2745fa2761252fdba4ad4df31b18619
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327023"
---
# <a name="wmcontentgroupdescription-attribute"></a>Attributo WM/ContentGroupDescription

L'attributo **WM/ContentGroupDescription** è la descrizione del gruppo di contenuto, ovvero una raccolta di elementi multimediali, ad esempio un set di CD boxed.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Attributi di file di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.

**ContentGroupDescription** è un alias per questo attributo.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMContentGroupDistribution.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





