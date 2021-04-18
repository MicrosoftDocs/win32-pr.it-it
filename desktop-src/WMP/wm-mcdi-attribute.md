---
title: Attributo WM/MCDI
description: L'attributo WM/MCDI è l'identificatore del CD musicale del CD da cui è stato copiato il file o la traccia.
ms.assetid: f0bec14d-416c-477f-98df-dece0bf85ea4
keywords:
- Media Player Windows per gli attributi WM/MCDI
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aec51c306f94e25acb94155c4d87f1f1a8b95866
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327007"
---
# <a name="wmmcdi-attribute"></a>Attributo WM/MCDI

L'attributo **WM/MCDI** è l'identificatore del CD musicale del CD da cui è stato copiato il file o la traccia.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Tracce CD](cd-track-attributes.md)
-   [Attributi di file di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato nella libreria o nella cache e nel file multimediale digitale.

**TOC** è un alias per questo attributo.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMMCDI.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





