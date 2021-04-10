---
description: Durata massima del flusso accelerato, in millisecondi, quando l'origine di rete utilizza il trasporto UDP.
ms.assetid: d5f3064a-b222-4f72-b889-cd88c14a239c
title: Proprietà MFNETSOURCE_MAXUDPACCELERATEDSTREAMINGDURATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2621e01203ba81b54e565f86953df64304c9bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058209"
---
# <a name="mfnetsource_maxudpacceleratedstreamingduration-property"></a>\_Proprietà MAXUDPACCELERATEDSTREAMINGDURATION di MFNETSOURCE

Durata massima del flusso accelerato, in millisecondi, quando l'origine di rete utilizza il trasporto UDP.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**DWORD** (archiviato come **Long**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ MAXUDPACCELERATEDSTREAMINGDURATION** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero.

Per il trasporto UDP, questa proprietà esegue l'override della proprietà [**MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) se il valore di questa proprietà è inferiore.

Le applicazioni possono usare questa proprietà per configurare l'origine di rete. Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

Il valore predefinito di questa proprietà è 8.000 millisecondi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Funzionalità di origine della rete](network-source-features.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




