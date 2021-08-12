---
description: Archivia il puntatore IUnknown della classe che implementa l'interfaccia IMFSSLCertificateManager.
ms.assetid: 13e05bda-96c2-4095-a266-74185760f33a
title: MFNETSOURCE_SSLCERTIFICATE_MANAGER proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d6f853ae3fe44a9c4508386df4096e4adac36f3cec8a8cf199eb91cb87e1fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243295"
---
# <a name="mfnetsource_sslcertificate_manager-property"></a>MFNETSOURCE \_ SSLCERTIFICATE \_ MANAGER - proprietà

Archivia il **puntatore IUnknown** della classe che implementa l'interfaccia [**IMFSSLCertificateManager.**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) L'implementazione client fornisce metodi per ottenere il certificato SSL client quando viene richiesto dal server.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**Puntatore IUnknown**

VT \_ UNKNOWN

**valvalore**



## <a name="remarks"></a>Commenti

La **costante MFNETSOURCE \_ SSLCERTIFICATE \_ MANAGER** definisce il GUID per la chiave di proprietà. L'identificatore di proprietà (PID) è zero. Per impostare questa proprietà nell'origine di rete, passare un **puntatore IPropertyStore** al resolver di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale.](configuring-a-media-source.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




