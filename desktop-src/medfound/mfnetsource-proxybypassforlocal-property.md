---
description: Specifica se il localizzatore proxy deve utilizzare un server proxy per gli indirizzi locali.
ms.assetid: 384343f5-5919-44da-b8ea-0c994b4743a8
title: MFNETSOURCE_PROXYBYPASSFORLOCAL proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1de60371ac71e570b9c11abcbc255e20efe1793884ebb0746834d32a34353006
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954791"
---
# <a name="mfnetsource_proxybypassforlocal-property"></a>MFNETSOURCE \_ PROXYBYPASSFORLOCAL - proprietà

Specifica se il localizzatore proxy deve utilizzare un server proxy per gli indirizzi locali.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

Boolean (**LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ PROXYBYPASSFORLOCAL** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare il localizzatore proxy durante la creazione dell'oggetto localizzatore proxy. Per impostare la proprietà, passare un **puntatore IPropertyStore** nel *parametro pProxyConfig* della [**funzione MFCreateProxyLocator.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) Il valore deve essere impostato su 0 se il server proxy deve essere usato per gli indirizzi locali. In caso contrario, un valore diverso da zero configura il localizzatore proxy predefinito per ignorare il server proxy per gli indirizzi locali.

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

 

 




