---
description: Richieste di stato di OPM
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: Richieste di stato di OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd994d7cb8d43db23fe59352dba830e741b74b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753914"
---
# <a name="opm-status-requests"></a>Richieste di stato di OPM

In questa sezione sono elencate le richieste di stato disponibili per l' [Output Protection Manager](output-protection-manager.md) (OPM). Per inviare una richiesta di stato di OPM, chiamare [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation). Per ogni richiesta sono elencate le informazioni seguenti.



|              |                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID richiesta | Identifica la richiesta. Impostare il membro **guidSetting** della struttura [**OPM \_ get \_ info \_ Parameters**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) uguale a questo valore. |
| Dati di input   | Specifica come interpretare la matrice **abParameters** nella struttura [**del \_ \_ \_ parametro OPM Get Info**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) .                      |
| Dati di output  | Specifica come interpretare la matrice **abRequestedInformation** nella struttura [**di \_ \_ informazioni richiesta da OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) .         |



 

Sono definite le seguenti richieste di stato:



| Richiesta di stato                                                                                      | Descrizione                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_per la \_ \_ segnalazione di ACP e \_ CGMSA \_**](opm-get-acp-and-cgmsa-signaling.md)                     | Restituisce le informazioni seguenti su un output video:                                                                                               |
| [**\_formato di \_ \_ output effettivo \_ per OPM Get**](opm-get-actual-output-format.md)                            | Restituisce una descrizione del segnale video trasmesso sul connettore.                                                               |
| [**OPM \_ ottenere \_ il \_ livello di protezione effettivo \_**](opm-get-actual-protection-level.md)                      | Restituisce il livello di protezione globale per un meccanismo di protezione specificato.                                                                             |
| [**\_tipo di \_ bus di adapter \_ \_ per OPM Get**](opm-get-adapter-bus-type.md)                                    | Restituisce il tipo di bus di I/O usato dall'output del video.                                                                                                 |
| [**\_informazioni sul \_ codec di Get di OPM \_**](opm-get-codec-info.md)                                                 | Ottiene il valore di Merit di un codec hardware.                                                                                                             |
| [**\_ \_ \_ \_ informazioni sul dispositivo HDCP connesso \_ ad OPM**](opm-get-connected-hdcp-device-information.md) | Ottiene informazioni su un dispositivo High-Bandwidth Digital protezione del contenuto (HDCP) collegato all'output del video. Vengono restituite le seguenti informazioni: |
| [**\_tipo di \_ connettore OPM Get \_**](opm-get-connector-type.md)                                         | Restituisce il tipo di connettore fisico dell'output del video.                                                                                              |
| [**OPM \_ ottenere \_ la \_ versione corrente di HDCP \_ SRM \_**](opm-get-current-hdcp-srm-version.md)                   | Restituisce il numero di versione del messaggio di rinnovabilità del sistema (SRM) attualmente utilizzato dall'output del video.                                               |
| [**\_caratteristiche di Get \_ DVI \_ per OPM**](opm-get-dvi-characteristics.md)                               | Esegue una query se un connettore DVI (Digital Video Interface) supporta la versione DVI 1,1 o successiva.                                                          |
| [**\_ID di \_ output \_ Get di OPM**](opm-get-output-id.md)                                                   | Restituisce l'identificatore univoco del monitoraggio associato a questo output del video.                                                                       |
| [**OPM \_ ottenere \_ i \_ tipi di protezione supportati \_**](opm-get-supported-protection-types.md)                | Restituisce l'elenco dei meccanismi di protezione supportati dal connettore.                                                                        |
| [**\_livello di \_ \_ protezione virtuale \_ di OPM Get**](opm-get-virtual-protection-level.md)                    | Restituisce il livello di protezione virtuale per un meccanismo di protezione specificato.                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla programmazione di OPM](opm-programming-reference.md)
</dt> <dt>

[Gestione protezione output](output-protection-manager.md)
</dt> </dl>

 

 



