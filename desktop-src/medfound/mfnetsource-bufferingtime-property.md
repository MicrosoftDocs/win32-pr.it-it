---
description: Numero di secondi di dati memorizzati nel buffer dell'origine di rete all'avvio.
ms.assetid: 186b55fc-d1b1-4187-a748-efaee114eca9
title: MFNETSOURCE_BUFFERINGTIME proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b6de79344913d77a30dc05dcad4e4f8dd3608e0d35009b1d8e5254e08790993
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243808"
---
# <a name="mfnetsource_bufferingtime-property"></a>MFNETSOURCE \_ BUFFERINGTIME - proprietà

Numero di secondi di dati memorizzati nel buffer dell'origine di rete all'avvio.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**DWORD** (archiviato come **LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ BUFFERINGTIME** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare l'origine di rete. Per impostare la proprietà, passare un **puntatore IPropertyStore** al sistema di risoluzione di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale](configuring-a-media-source.md).

Il valore predefinito di questa proprietà è 5 secondi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[Funzionalità dell'origine di rete](network-source-features.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




