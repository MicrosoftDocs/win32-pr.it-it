---
description: Restituisce una descrizione del segnale video trasmesso tramite il connettore.
ms.assetid: 8464470f-49db-4559-80b2-02cfc473e30e
title: OPM_GET_ACTUAL_OUTPUT_FORMAT (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37f35e9f3d64bd1a72bb6800011978ea1cf2f4c60f523a344594f949beb4f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102075"
---
# <a name="opm_get_actual_output_format"></a>OPM \_ GET \_ ACTUAL \_ OUTPUT \_ FORMAT

Restituisce una descrizione del segnale video trasmesso tramite il connettore.



| Requisito | Valore |
|--------------|------------------------------------------------------------------------------|
| GUID della richiesta | OPM \_ GET \_ ACTUAL \_ OUTPUT \_ FORMAT                                             |
| Dati di input   | Nessuno                                                                         |
| Restituisce i dati  | Struttura [**OPM \_ ACTUAL OUTPUT \_ \_ FORMAT**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format) |



 

## <a name="remarks"></a>Commenti

Il segnale video trasmesso tramite il connettore non ha necessariamente lo stesso formato della modalità di visualizzazione del desktop. Ad esempio, la modalità di visualizzazione desktop potrebbe essere di 1024 x 768 pixel a 85 Hz, mentre il connettore potrebbe essere un connettore S-Video che trasmette un segnale video a 720 x 480 pixel, interlacciato a 60/1,01 Hz. In tal caso, il driver restituirebbe la risoluzione del segnale S-Video, non la risoluzione desktop.

Questa query equivale alla query DXVA \_ COPPQueryDisplayData usata nel protocollo COPP (Certified Output Protection Protocol).

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

 

 




