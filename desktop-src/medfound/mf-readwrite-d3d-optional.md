---
description: Specifica se l'applicazione richiede il supporto Microsoft Direct3D nel lettore di origine o nel sink writer.
ms.assetid: 3844ED7B-E1E5-4CD7-B080-FE7EC7B28AC5
title: MF_READWRITE_D3D_OPTIONAL attributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cebc24991e5c2bfb90b7153f3a90a2e7447c2daef987b2956680e89f162223ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664111"
---
# <a name="mf_readwrite_d3d_optional-attribute"></a>Attributo \_ FACOLTATIVO MF READWRITE \_ D3D \_

Specifica se l'applicazione richiede il supporto Microsoft Direct3D nel lettore [di](source-reader.md) origine o nel [writer di sink.](sink-writer.md)

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica solo se l'applicazione abilita il supporto Direct3D usando l'attributo [MF \_ SOURCE READER \_ \_ D3D \_ MANAGER](mf-source-reader-d3d-manager.md) o [MF SINK WRITER \_ \_ \_ D3D \_ MANAGER.](mf-sink-writer-d3d-manager.md)

Se l'applicazione abilita il supporto Direct3D, il lettore di origine e sink writer tenteranno entrambi di allocare le superfici Direct3D per il video. Se l'operazione non riesce e l'attributo \_ MF READWRITE D3D OPTIONAL è TRUE, il writer di sink/lettore di origine verrà eseguito il fall back all'allocazione delle superfici \_ video nella memoria di \_ sistema.  In caso contrario, se non è possibile allocare superfici Direct3D e MF \_ READWRITE D3D OPTIONAL è FALSE, si \_ verifica un errore durante \_ l'elaborazione. 

Se l'applicazione non abilita il supporto Direct3D, il writer di lettura/sink di origine usa la memoria di sistema e ignora il valore di MF \_ READWRITE \_ D3D \_ OPTIONAL.

Questo attributo è facoltativo. Il valore predefinito è **FALSE.** Impostare l'attributo quando si crea il lettore di origine o il writer di sink.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del writer di sink](sink-writer-attributes.md)
</dt> <dt>

[Attributi del lettore di origine](source-reader-attributes.md)
</dt> </dl>

 

 




