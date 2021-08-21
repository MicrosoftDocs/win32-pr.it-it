---
title: Attributo WM/WMContentID
description: L'attributo WM/WMContentID è un GUID che identifica il contenuto dell'elemento.
ms.assetid: 1e741286-cdd8-4c2f-8fef-5d91d81d6387
keywords:
- Attributo WM/WMContentID Windows Media Player
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f31a42a650d382597e2495d80541d667e229dde09a8181605d83cef65e39945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053759"
---
# <a name="wmwmcontentid-attribute"></a>Attributo WM/WMContentID

**L'attributo WM/WMContentID** è un GUID che identifica il contenuto dell'elemento.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Tracce CD](cd-track-attributes.md)
-   [Attributi dei Windows file multimediali comunemente usati](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria (o cache) che nel file multimediale digitale.

**WMContentID** è un alias per questo attributo.

La Windows Media Format SDK per questo attributo è g \_ wszWMContentID.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento su attributi**](attribute-reference.md)
</dt> </dl>

 

 





