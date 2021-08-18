---
description: 'Altre informazioni su: OPM_GET_ACP_AND_CGMSA_SIGNALING'
ms.assetid: d477fe3e-4498-450b-93b7-ce74ae9ed005
title: OPM_GET_ACP_AND_CGMSA_SIGNALING (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6c06da78ea9ae1a4f0ea58f0fb8770dffadff6a34d577fd2328816ffc100e4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102065"
---
# <a name="opm_get_acp_and_cgmsa_signaling"></a>OPM \_ GET \_ ACP E \_ \_ CGMSA \_ SIGNALING

Restituisce le informazioni seguenti su un output video:

-   Elenco di standard di protezione della tv supportati dal driver.
-   Standard attualmente attivo.
-   Proporzioni correnti o altri dati di segnalazione.



| Requisito | Valore |
|--------------|-------------------------------------------------------------------------------------|
| GUID della richiesta | OPM \_ GET \_ ACP E \_ \_ CGMSA \_ SIGNALING                                                |
| Dati di input   | Nessuno                                                                                |
| Restituisce i dati  | Struttura [**OPM \_ ACP \_ E \_ CGMSA \_ SIGNALING**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling) |



 

## <a name="remarks"></a>Commenti

Questa query equivale alla query DXVA \_ COPPQuerySignaling usata nel protocollo COPP (Certified Output Protection Protocol).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Richieste di stato OPM](opm-status-requests.md)
</dt> </dl>

 

 




