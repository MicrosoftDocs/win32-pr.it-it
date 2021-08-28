---
description: Specifica un elenco delimitato da punto e virgola di server multimediali in grado di accettare connessioni da applicazioni client senza utilizzare un server proxy.
ms.assetid: 218883c5-9a26-4733-8308-1827cf1f2cd7
title: MFNETSOURCE_PROXYEXCEPTIONLIST proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e87c07068d31cdd5e9762dab14e2a61edbe9c8f90f8750acc1b23c851ad47c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113491"
---
# <a name="mfnetsource_proxyexceptionlist-property"></a>MFNETSOURCE \_ PROXYEXCEPTIONLIST - proprietà

Specifica un elenco delimitato da punto e virgola di server multimediali in grado di accettare connessioni da applicazioni client senza utilizzare un server proxy.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

Stringa di caratteri wide (**WCHAR** \* )

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ PROXYEXCEPTIONLIST** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare il localizzatore proxy durante la creazione dell'oggetto localizzatore proxy. Per impostare la proprietà, passare un **puntatore IPropertyStore** nel *parametro pProxyConfig* della [**funzione MFCreateProxyLocator.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) Il localizzatore proxy non esegue il rilevamento proxy per questi indirizzi.

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

 

 




