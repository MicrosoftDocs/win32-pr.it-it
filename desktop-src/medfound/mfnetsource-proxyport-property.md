---
description: Specifica il numero di porta del server proxy.
ms.assetid: cd84911b-3658-489f-b454-23eded0cbfa0
title: MFNETSOURCE_PROXYPORT proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ac286fdcce276a29f08fef9df536f9a92152729791ff04d63478246825a718f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874625"
---
# <a name="mfnetsource_proxyport-property"></a>MFNETSOURCE \_ - proprietà PROXYPORT

Specifica il numero di porta del server proxy.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**DWORD** (archiviato come **LONG)**

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ PROXYPORT** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare il localizzatore proxy durante la creazione dell'oggetto localizzatore proxy. Per impostare la proprietà, passare un **puntatore IPropertyStore** nel *parametro pProxyConfig* della [**funzione MFCreateProxyLocator.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) Se questa proprietà non è impostata per HTTP, per impostazione predefinita il localizzatore proxy usa il valore 80.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Supporto proxy per origini di rete](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




