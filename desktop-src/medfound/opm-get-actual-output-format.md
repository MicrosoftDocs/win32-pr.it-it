---
description: Restituisce una descrizione del segnale video trasmesso sul connettore.
ms.assetid: 8464470f-49db-4559-80b2-02cfc473e30e
title: OPM_GET_ACTUAL_OUTPUT_FORMAT (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eeca9bcf8fde670447afe4268a86ffa31b6a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344421"
---
# <a name="opm_get_actual_output_format"></a>\_formato di \_ \_ output effettivo \_ per OPM Get

Restituisce una descrizione del segnale video trasmesso sul connettore.



| Requisito | Valore |
|--------------|------------------------------------------------------------------------------|
| GUID richiesta | \_formato di \_ \_ output effettivo \_ per OPM Get                                             |
| Dati di input   | nessuno                                                                         |
| Restituisce i dati  | Struttura [**del \_ \_ \_ formato di output effettivo di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format) |



 

## <a name="remarks"></a>Commenti

Il segnale video trasmesso sul connettore non ha necessariamente lo stesso formato della modalità di visualizzazione del desktop. La modalità di visualizzazione desktop, ad esempio, potrebbe essere 1024 x 768 pixel a 85 Hz, mentre il connettore potrebbe essere un connettore S-video che trasmette un segnale video a 720 x 480 pixel, 60/1.01 Hz interlacciato. In tal caso, il driver restituirà la risoluzione del segnale S-video, non la risoluzione del desktop.

Questa query equivale alla \_ query DXVA COPPQueryDisplayData utilizzata in Certified Output Protocol (Copp).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Richieste di stato di OPM](opm-status-requests.md)
</dt> </dl>

 

 




