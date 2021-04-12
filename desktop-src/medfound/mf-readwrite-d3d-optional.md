---
description: Specifica se l'applicazione richiede il supporto di Microsoft Direct3D nel lettore di origine o del sink.
ms.assetid: 3844ED7B-E1E5-4CD7-B080-FE7EC7B28AC5
title: Attributo MF_READWRITE_D3D_OPTIONAL (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8c78295dd12e5d187c9be380305dc225d7e8e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233743"
---
# <a name="mf_readwrite_d3d_optional-attribute"></a>\_Attributo facoltativo di MF ReadWrite \_ D3D \_

Specifica se l'applicazione richiede il supporto di Microsoft Direct3D nel [lettore di origine](source-reader.md) o del [sink](sink-writer.md).

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Questo attributo si applica solo se l'applicazione Abilita il supporto Direct3D usando l'attributo gestione [ \_ D3D del lettore di origine \_ \_ \_ MF](mf-source-reader-d3d-manager.md) o il [ \_ \_ \_ \_ gestore D3D sink writer](mf-sink-writer-d3d-manager.md) .

Se l'applicazione Abilita il supporto Direct3D, il writer di origine e di sink tenterà di allocare le superfici Direct3D per i video. Se l'operazione ha esito negativo e l' \_ \_ \_ attributo facoltativo ReadWrite D3D è **true**, il writer di lettura/sink di origine eseguirà il fallback per l'allocazione di superfici video nella memoria di sistema. In caso contrario, se non è possibile allocare le superfici Direct3D e \_ \_ l'opzione MF ReadWrite D3D \_ optional è **false**, si verifica un errore durante l'elaborazione.

Se l'applicazione non Abilita il supporto Direct3D, il writer di lettura/sink di origine utilizza la memoria di sistema e ignora il valore di MF \_ ReadWrite \_ D3D \_ Optional.

Questo attributo è facoltativo. Il valore predefinito è **false**. Impostare l'attributo quando si crea il Reader di origine o il writer del sink.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del writer di sink](sink-writer-attributes.md)
</dt> <dt>

[Attributi lettore di origine](source-reader-attributes.md)
</dt> </dl>

 

 




