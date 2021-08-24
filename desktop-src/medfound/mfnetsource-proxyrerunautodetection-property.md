---
description: Specifica se il localizzatore proxy predefinito deve forzare il rilevamento automatico del proxy.
ms.assetid: ab547a92-94a2-482e-b7ac-aeb3fdfb6b91
title: MFNETSOURCE_PROXYRERUNAUTODETECTION proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3351766302952390bbe67ea2d86cd76e93b9267328fe2c07e2656a38b3fd2906
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713991"
---
# <a name="mfnetsource_proxyrerunautodetection-property"></a>MFNETSOURCE \_ PROXYRERUNAUTODETECTION - proprietà

Specifica se il localizzatore proxy predefinito deve forzare il rilevamento automatico del proxy.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

Boolean (**LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ PROXYSETTINGS** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare il localizzatore proxy durante la creazione dell'oggetto localizzatore proxy. Per impostare la proprietà, passare un **puntatore IPropertyStore** nel *parametro pProxyConfig* della [**funzione MFCreateProxyLocator.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) In modalità di rilevamento automatico, il localizzatore proxy usa il meccanismo di rilevamento proxy WinInet. Per forzare il rilevamento automatico, impostare il valore su 0.

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

 

 




