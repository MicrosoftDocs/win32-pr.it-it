---
description: Specifica il nome host del server proxy.
ms.assetid: e53c86e9-c326-41c9-aa86-c80a750b9ce3
title: MFNETSOURCE_PROXYHOSTNAME proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82746763c937bdca388782cb0882b536c0b9e93b660e0f8e0a04426e5b48a61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663671"
---
# <a name="mfnetsource_proxyhostname-property"></a>Proprietà MFNETSOURCE \_ PROXYHOSTNAME

Specifica il nome host del server proxy.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

Stringa di caratteri wide (**WCHAR** \* )

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ PROXYHOSTNAME** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare il localizzatore proxy predefinito durante la creazione dell'oggetto localizzatore proxy. Per impostare la proprietà, passare un **puntatore IPropertyStore** nel *parametro pProxyConfig* della [**funzione MFCreateProxyLocator.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) Questa proprietà deve essere impostata dall'applicazione quando il localizzatore proxy è configurato per funzionare in modalità manuale.

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

 

 




