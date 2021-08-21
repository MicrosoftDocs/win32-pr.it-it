---
description: Specifica l'impostazione di configurazione per il localizzatore proxy predefinito.
ms.assetid: 85f2bd02-8a2f-46b5-b765-1a0bc5b6ccc3
title: MFNETSOURCE_PROXYSETTINGS proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a6af82b593899eb504818ff041c6c6839c4cca1b18ea29218f7259c41b4df9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738676"
---
# <a name="mfnetsource_proxysettings-property"></a>Proprietà MFNETSOURCE \_ PROXYSETTINGS

Specifica l'impostazione di configurazione per il localizzatore proxy predefinito. Il valore di questa proprietà è un membro [**dell'enumerazione \_ MFNET PROXYSETTINGS.**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings)



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**LONG**

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ PROXYSETTINGS** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare il localizzatore proxy durante la creazione dell'oggetto localizzatore proxy predefinito. Per impostare la proprietà, passare un **puntatore IPropertyStore** nel *parametro pProxyConfig* della [**funzione MFCreateProxyLocator.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator)

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

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Supporto proxy per le origini di rete](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




