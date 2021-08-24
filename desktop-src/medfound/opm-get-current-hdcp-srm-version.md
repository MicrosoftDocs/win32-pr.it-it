---
description: Restituisce il numero di versione del messaggio di rinnovo del sistema (SRM) attualmente usato dall'output video.
ms.assetid: 65d4b98b-369f-4863-a28c-f9e3b4c2b55d
title: OPM_GET_CURRENT_HDCP_SRM_VERSION (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee36516510d04fec067bbc692387e2e36b9da083db1a6daae0f51948a992cc83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887491"
---
# <a name="opm_get_current_hdcp_srm_version"></a>OPM \_ GET \_ CURRENT \_ HDCP \_ SRM \_ VERSION

Restituisce il numero di versione del messaggio di rinnovo del sistema (SRM) attualmente usato dall'output video.



| Requisito | Valore |
|--------------|-----------------------------------------------------------------------------|
| GUID della richiesta | OPM \_ GET \_ CURRENT \_ HDCP \_ SRM \_ VERSION                                       |
| Dati di input   | Nessuno                                                                        |
| Restituisce i dati  | Struttura [**OPM \_ STANDARD \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Commenti

Se la query ha esito positivo, il membro **ulInformation** della struttura [**OPM \_ STANDARD \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contiene il numero di versione SRM, in formato little-endian.

Le macchine virtuali vengono usate per aggiornare l'High-Bandwidth elenco dei dispositivi HDCP (Digital protezione del contenuto protezione del contenuto) revocati. Gli SPM vengono recapitati con il contenuto video. Per impostare SRM, inviare il [**comando OPM \_ SET \_ HDCP \_ SRM.**](opm-set-hdcp-srm.md)

Questa query può fare in modo che il metodo [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) restituirà uno dei codici di errore seguenti.



| Codice restituito                                            | Descrizione                             |
|--------------------------------------------------------|-----------------------------------------|
| ERRORE \_ GRAFICO \_ OPM \_ HDCP \_ SRM MAI \_ \_ IMPOSTATO            | L'applicazione non ha impostato un SRM.     |
| L'OUTPUT OPM DI GRAFICA \_ DEGLI ERRORI NON SUPPORTA \_ \_ \_ \_ \_ \_ HDCP | L'output video non supporta HDCP. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Richieste di stato OPM](opm-status-requests.md)
</dt> </dl>

 

 




