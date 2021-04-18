---
description: Intervallo di porte UDP valide che l'origine di rete può usare per ricevere contenuti in streaming.
ms.assetid: 97fe2d11-70f7-4baa-b49f-513d90146591
title: Proprietà MFNETSOURCE_UDP_PORT_RANGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04db8c450bd20adc8c03ec3b964b543f1500aa51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307956"
---
# <a name="mfnetsource_udp_port_range-property"></a>MFNETSOURCE \_ \_ \_ Proprietà intervallo porte UDP

Intervallo di porte UDP valide che l'origine di rete può usare per ricevere contenuti in streaming. Il valore di questa proprietà è una stringa nel formato " *m*–*n* " dove *m* e *n* sono numeri di porta.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

Stringa di caratteri wide (**WCHAR** \* )

\_LPWSTR VT

**pwszVal**



## <a name="remarks"></a>Commenti

L' **intervallo di \_ \_ porte UDP \_ MFNETSOURCE** costante definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare l'origine di rete. Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

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

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




