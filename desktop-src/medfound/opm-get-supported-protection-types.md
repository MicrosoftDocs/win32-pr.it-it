---
description: Restituisce l'elenco dei meccanismi di protezione supportati dal connettore.
ms.assetid: dd4cdd3c-6bb5-4427-827d-f3e909e752e5
title: OPM_GET_SUPPORTED_PROTECTION_TYPES (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eddc6f4006f9692ec6152875cda412191b87d247e907d33b615aa6d4fb89748e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012541"
---
# <a name="opm_get_supported_protection_types"></a>OPM \_ OTTIENE I TIPI DI PROTEZIONE \_ \_ \_ SUPPORTATI

Restituisce l'elenco dei meccanismi di protezione supportati dal connettore.



| Requisito | Valore |
|--------------|-----------------------------------------------------------------------------|
| GUID richiesta | OPM \_ OTTIENE I TIPI DI PROTEZIONE \_ \_ \_ SUPPORTATI                                      |
| Dati di input   | Nessuno                                                                        |
| Restituisce i dati  | Struttura [**OPM \_ STANDARD \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Commenti

I meccanismi di protezione vengono restituiti nel **membro ulInformation** della [**struttura OPM STANDARD \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Il valore è **un'operazione OR** bit per bit [dei flag del tipo di protezione OPM](opm-protection-type-flags.md).

Questa query equivale alla \_ query DXVA COPPQueryProtectionType usata in Certified Output Protection Protocol (COPP).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Richieste di stato OPM](opm-status-requests.md)
</dt> </dl>

 

 




