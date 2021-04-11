---
description: Aggiorna il messaggio di rinnovabilità del sistema (SRM) per High-Bandwidth Digital protezione del contenuto (HDCP).
ms.assetid: ea18baba-0e03-4471-af0e-a588773c98d2
title: OPM_SET_HDCP_SRM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9283c493598f22a1715f687eccea985a27e0e6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226516"
---
# <a name="opm_set_hdcp_srm"></a>\_set OPM \_ HDCP \_ SRM

Aggiorna il messaggio di rinnovabilità del sistema (SRM) per High-Bandwidth Digital protezione del contenuto (HDCP).



| Requisito | Valore |
|--------------|-------------------------------------------------------------------------------------|
| GUID comando | \_set OPM \_ HDCP \_ SRM                                                                 |
| Dati di input   | Struttura di parametri di un [**set di OPM \_ \_ \_ SRM \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) |



 

Il parametro *pbAdditionalParameters* di [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) deve puntare a un buffer che contiene SRM. Il formato di un SRM SRM è documentato nella specifica HDCP. Impostare il parametro *ulAdditionalParametersSize* in modo che corrisponda alla dimensione del buffer, in byte.

## <a name="remarks"></a>Commenti

SRM vengono usati per aggiornare l'elenco dei dispositivi HDCP revocati. SRM vengono forniti con il contenuto video.

Questo comando Aggiorna l'SRM corrente dell'output del video. Se la funzionalità HDCP è abilitata al momento del comando, l'output del video usa il nuovo SRM per verificare se uno dei dispositivi HDCP connessi viene revocato. Se l'output del video rileva un dispositivo revocato, smette di visualizzare il video. Se si invia questo comando mentre HDCP è disabilitato, l'output del video convalida l'SRM e lo archivia. In seguito, se l'applicazione Abilita HDCP, l'output del video usa il nuovo SRM per verificare lo stato di revoca del dispositivo.

Questo comando può causare la restituzione da parte del metodo **Configure** dei codici di errore seguenti.



| Codice restituito                                            | Descrizione                             |
|--------------------------------------------------------|-----------------------------------------|
| ERRORE della \_ grafica \_ OPM \_ non valido \_ SRM                     | SRM non è valido.                   |
| ERRORE \_ l' \_ output OPM della grafica non \_ \_ \_ \_ supporta \_ HDCP | L'output del video non supporta la HDCP. |



 

Questo comando non è supportato quando l'interfaccia **IOPMVideoOutput** emula il protocollo COPP (Certified Output Protection). Quando si usano la semantica COPP, l'applicazione è responsabile dell'analisi di SRM e del controllo dello stato di revoca del dispositivo HDCP. Usare la richiesta di stato delle [ \_ \_ \_ \_ \_ informazioni sul dispositivo HDCP Get Connected](opm-get-connected-hdcp-device-information.md) per ottenere il vettore di selezione chiavi del dispositivo (KSV), necessario per controllare lo stato di revoca. Per altre informazioni su SRM, vedere la specifica HDCP.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[Comandi di OPM](opm-commands.md)
</dt> </dl>

 

 




