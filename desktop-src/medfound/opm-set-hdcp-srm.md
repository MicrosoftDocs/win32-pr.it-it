---
description: Aggiorna il messaggio di rinnovo del sistema (SRM) per High-Bandwidth Digital protezione del contenuto (HDCP).
ms.assetid: ea18baba-0e03-4471-af0e-a588773c98d2
title: OPM_SET_HDCP_SRM (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23601386353e0a18ed95238cee7a11ba9c39a84fbf1855b839bde0fd841ccd17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118058727"
---
# <a name="opm_set_hdcp_srm"></a>OPM \_ SET \_ HDCP \_ SRM

Aggiorna il messaggio di rinnovo del sistema (SRM) per High-Bandwidth Digital protezione del contenuto (HDCP).



| Requisito | Valore |
|--------------|-------------------------------------------------------------------------------------|
| GUID del comando | OPM \_ SET \_ HDCP \_ SRM                                                                 |
| Dati di input   | Struttura [**OPM \_ SET \_ HDCP \_ SRM \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) |



 

Il *parametro pbAdditionalParameters* di [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) deve puntare a un buffer che contiene SRM. Il formato di un SRM HDCP è documentato nella specifica HDCP. Impostare il *parametro ulAdditionalParametersSize* sulla dimensione del buffer, in byte.

## <a name="remarks"></a>Commenti

Gli SPM vengono usati per aggiornare l'elenco dei dispositivi HDCP revocati. Gli SPM vengono recapitati con il contenuto video.

Questo comando aggiorna la SRM corrente dell'output video. Se HDCP è abilitato al momento del comando, l'output video usa il nuovo SRM per verificare se uno dei dispositivi HDCP connessi viene revocato. Se l'output video rileva un dispositivo revocato, smette di visualizzare il video. Se si invia questo comando mentre HDCP è disabilitato, l'output video convalida sRM e lo archivia. In seguito, se l'applicazione abilita HDCP, l'output video usa il nuovo SRM per controllare lo stato di revoca del dispositivo.

Questo comando può causare la restituzione **di uno** dei codici di errore seguenti da parte del metodo Configure.



| Codice restituito                                            | Descrizione                             |
|--------------------------------------------------------|-----------------------------------------|
| ERRORE \_ GRAFICO \_ OPM \_ SRM NON \_ VALIDO                     | SRM non valido.                   |
| L'OUTPUT OPM DI GRAFICA \_ DEGLI ERRORI NON SUPPORTA \_ \_ \_ \_ \_ \_ HDCP | L'output video non supporta HDCP. |



 

Questo comando non è supportato quando **l'interfaccia IOPMVideoOutput** emula Il protocollo COPP (Certified Output Protection Protocol). Quando si usa la semantica COPP, l'applicazione è responsabile dell'analisi delle macchine virtuali e del controllo dello stato di revoca del dispositivo HDCP. Usare la richiesta di stato [OPM \_ GET CONNECTED \_ \_ HDCP DEVICE \_ \_ INFORMATION](opm-get-connected-hdcp-device-information.md) per ottenere il vettore di selezione delle chiavi (KSV) del dispositivo, necessario per controllare lo stato di revoca. Per altre informazioni sulle macchine virtuali, vedere la specifica HDCP.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[Comandi OPM](opm-commands.md)
</dt> </dl>

 

 




