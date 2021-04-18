---
title: Attributo WM/InitialKey
description: L'attributo WM/InitialKey è la chiave iniziale del brano musicale.
ms.assetid: 1458f1a2-3d46-4491-8b89-731276d7c024
keywords:
- Media Player Windows per gli attributi WM/InitialKey
topic_type:
- apiref
api_name:
- WM/InitialKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dd4daeabe2971615518b0a3cf37223a4c623c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327013"
---
# <a name="wminitialkey-attribute"></a>Attributo WM/InitialKey

L'attributo **WM/InitialKey** è la chiave iniziale del brano musicale.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Attributi di file di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMInitialKey.

**InitialKey** è un alias per questo attributo.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





