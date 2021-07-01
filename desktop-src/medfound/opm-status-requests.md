---
description: Richieste di stato OPM
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: Richieste di stato OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbf7338fe1309feb49fd191e3f4a1a22f3639b4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120176"
---
# <a name="opm-status-requests"></a>Richieste di stato OPM

Questa sezione elenca le richieste di stato disponibili per [Output Protection Manager](output-protection-manager.md) (OPM). Per inviare una richiesta di stato OPM, chiamare [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation). Per ogni richiesta sono elencate le informazioni seguenti.



| Valore             | Descrizione                                                                                                                                                           |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID della richiesta | Identifica la richiesta. Impostare il **membro guidSetting** della struttura [**OPM \_ GET INFO \_ \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) su questo valore. |
| Dati di input   | Specifica come interpretare la matrice **abParameters** nella [**struttura OPM \_ GET INFO \_ \_ PARAMETERS.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)                      |
| Dati di output  | Specifica come interpretare la matrice **abRequestedInformation** nella [**struttura OPM \_ REQUESTED \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)         |



 

Vengono definite le richieste di stato seguenti:



| Richiesta di stato                                                                                      | Descrizione                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OPM \_ GET \_ ACP E \_ \_ CGMSA \_ SIGNALING**](opm-get-acp-and-cgmsa-signaling.md)                     | Restituisce le informazioni seguenti su un output video:                                                                                               |
| [**OPM \_ GET \_ ACTUAL \_ OUTPUT \_ FORMAT**](opm-get-actual-output-format.md)                            | Restituisce una descrizione del segnale video trasmesso tramite il connettore.                                                               |
| [**OPM \_ OTTIENE IL LIVELLO DI PROTEZIONE \_ \_ \_ EFFETTIVO**](opm-get-actual-protection-level.md)                      | Restituisce il livello di protezione globale per un meccanismo di protezione specificato.                                                                             |
| [**TIPO DI \_ \_ BUS \_ DELL'ADAPTER \_ OPM GET**](opm-get-adapter-bus-type.md)                                    | Restituisce il tipo di bus di I/O utilizzato dall'output video.                                                                                                 |
| [**OPM \_ GET \_ CODEC \_ INFO**](opm-get-codec-info.md)                                                 | Ottiene il valore di merito di un codec hardware.                                                                                                             |
| [**OPM \_ GET \_ CONNECTED \_ HDCP \_ DEVICE \_ INFORMATION**](opm-get-connected-hdcp-device-information.md) | Ottiene informazioni su High-Bandwidth dispositivo HDCP (Digital protezione del contenuto) collegato all'output video. Vengono restituite le informazioni seguenti: |
| [**TIPO DI CONNETTORE OPM \_ GET \_ \_**](opm-get-connector-type.md)                                         | Restituisce il tipo di connettore fisico dell'output video.                                                                                              |
| [**OPM \_ GET \_ CURRENT \_ HDCP \_ SRM \_ VERSION**](opm-get-current-hdcp-srm-version.md)                   | Restituisce il numero di versione del messaggio di rinnovo del sistema (SRM) attualmente usato dall'output video.                                               |
| [**OPM \_ GET \_ DVI \_ CHARACTERISTICS**](opm-get-dvi-characteristics.md)                               | Verifica se un connettore DVI (Digital Video Interface) supporta DVI versione 1.1 o successiva.                                                          |
| [**OPM \_ GET \_ OUTPUT \_ ID**](opm-get-output-id.md)                                                   | Restituisce l'identificatore univoco del monitoraggio associato a questo output video.                                                                       |
| [**OPM \_ OTTIENE I TIPI DI PROTEZIONE \_ \_ \_ SUPPORTATI**](opm-get-supported-protection-types.md)                | Restituisce l'elenco dei meccanismi di protezione supportati dal connettore.                                                                        |
| [**OPM \_ GET \_ VIRTUAL \_ PROTECTION \_ LEVEL**](opm-get-virtual-protection-level.md)                    | Restituisce il livello di protezione virtuale per un meccanismo di protezione specificato.                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulla programmazione OPM](opm-programming-reference.md)
</dt> <dt>

[Output Protection Manager](output-protection-manager.md)
</dt> </dl>

 

 



