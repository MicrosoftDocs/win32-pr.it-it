---
description: Restituisce il numero di versione del messaggio di rinnovabilità del sistema (SRM) attualmente utilizzato dall'output del video.
ms.assetid: 65d4b98b-369f-4863-a28c-f9e3b4c2b55d
title: OPM_GET_CURRENT_HDCP_SRM_VERSION (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e05ad53ae58e2141c63179c84a90f90cea86fb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309058"
---
# <a name="opm_get_current_hdcp_srm_version"></a>OPM \_ ottenere \_ la \_ versione corrente di HDCP \_ SRM \_

Restituisce il numero di versione del messaggio di rinnovabilità del sistema (SRM) attualmente utilizzato dall'output del video.



| Requisito | Valore |
|--------------|-----------------------------------------------------------------------------|
| GUID richiesta | OPM \_ ottenere \_ la \_ versione corrente di HDCP \_ SRM \_                                       |
| Dati di input   | nessuno                                                                        |
| Restituisce i dati  | Struttura [**di \_ \_ informazioni standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Commenti

Se la query ha esito positivo, il membro **ulInformation** della struttura di [**\_ \_ informazioni standard di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contiene il numero di versione SRM, in formato little-endian.

SRM vengono usati per aggiornare l'elenco dei dispositivi High-Bandwidth Digital protezione del contenuto (HDCP) revocati. SRM vengono forniti con il contenuto video. Per impostare SRM, inviare il comando [**OPM \_ set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) .

Questa query può causare il metodo [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) per restituire uno dei codici di errore seguenti.



| Codice restituito                                            | Descrizione                             |
|--------------------------------------------------------|-----------------------------------------|
| ERRORE \_ grafica \_ OPM \_ HDCP \_ SRM \_ mai \_ impostato            | L'applicazione non ha impostato un SRM.     |
| ERRORE \_ l' \_ output OPM della grafica non \_ \_ \_ \_ supporta \_ HDCP | L'output del video non supporta la HDCP. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Richieste di stato di OPM](opm-status-requests.md)
</dt> </dl>

 

 




