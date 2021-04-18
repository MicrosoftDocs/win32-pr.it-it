---
description: Archivia il puntatore IUnknown della classe che implementa l'interfaccia IMFSSLCertificateManager.
ms.assetid: 13e05bda-96c2-4095-a266-74185760f33a
title: Proprietà MFNETSOURCE_SSLCERTIFICATE_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf6e21962e3d521e8c5781d59b2e0fe6fed04aa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305366"
---
# <a name="mfnetsource_sslcertificate_manager-property"></a>Proprietà di MFNETSOURCE \_ SSLCERTIFICATE \_ Manager

Archivia il puntatore **IUnknown** della classe che implementa l'interfaccia [**IMFSSLCertificateManager**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) . L'implementazione client fornisce metodi per ottenere il certificato SSL del client quando viene richiesto dal server.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**Puntatore IUnknown**

VT \_ sconosciuto

**punkVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ SSLCERTIFICATE \_ Manager** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero. Per impostare questa proprietà nell'origine di rete, passare un puntatore **IPropertyStore** al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




