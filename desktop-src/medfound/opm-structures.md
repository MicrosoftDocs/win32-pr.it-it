---
description: Con l'output Protection Manager (OPM) vengono utilizzate le strutture seguenti.
ms.assetid: 676a60ca-393e-4b5d-89d3-50cf4b771492
title: Strutture OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b62bc7cbc13b987a2cfdda5d210cddd2fd05b8fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309047"
---
# <a name="opm-structures"></a>Strutture OPM

Con l' [Output Protection Manager](output-protection-manager.md) (OPM) vengono utilizzate le strutture seguenti.



| Struttura                                                                                              | Descrizione                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_intestazione GRL**](grl-header.md)                                                                      | Contiene l'intestazione dell'elenco di revoche globale (GRL).                                                                                                          |
| [**\_firma MF**](mf-signature.md)                                                                  | Contiene una firma dell'elenco di revoche globale (GRL).                                                                                                         |
| [**\_ \_ segnalazione di ACP e \_ CGMSA di \_ OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling)                                 | Contiene il risultato di una query di [**\_ \_ \_ \_ \_ segnalazione CGMSA di OPM e ACP**](opm-get-acp-and-cgmsa-signaling.md) .                                         |
| [**\_formato di \_ output \_ effettivo OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format)                                        | Contiene il risultato di una query del formato di output di un [**OPM \_ get \_ effettivo \_ \_**](opm-get-actual-output-format.md) in output Protection Manager (OPM).               |
| [**\_configurare i \_ parametri di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters)                                         | Contiene un comando OPM o Certified Output Protection Manager (COPP).                                                                                     |
| [**\_ \_ \_ informazioni sul dispositivo HDCP connesso a OPM \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information)             | Contiene il risultato di una query di [**\_ \_ \_ \_ \_ informazioni sul dispositivo HDCP connesso ad OPM**](opm-get-connected-hdcp-device-information.md) .                     |
| [**\_parametri di \_ \_ get \_ info \_ compatibili con copp di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_copp_compatible_get_info_parameters)        | Contiene i parametri per il metodo [**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) . |
| [**\_parametri di \_ inizializzazione crittografati di OPM \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters)          | Contiene i parametri di inizializzazione per una sessione di OPM.                                                                                                     |
| [**\_ \_ \_ \_ informazioni sulle informazioni sul codec di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information)                           | Contiene il risultato di una query per [**\_ ottenere \_ \_ informazioni sui codec di OPM**](opm-get-codec-info.md) .                                                                     |
| [**\_parametri di \_ \_ informazioni codec \_ di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)                             | Contiene informazioni per il comando [**OPM \_ get \_ codec \_ info**](opm-get-codec-info.md) .                                                                  |
| [**\_parametri di \_ informazioni \_ Get di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)                                          | Contiene i parametri per il metodo [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) .                             |
| [**\_vettore di \_ selezione delle chiavi \_ \_ di OPM HDCP**](/windows/desktop/api/opmapi/ns-opmapi-opm_hdcp_key_selection_vector)                             | Contiene il vettore di selezione della chiave (KSV) per un ricevitore High-Bandwidth Digital protezione del contenuto (HDCP).                                                   |
| [**\_OMAC OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_omac)                                                                          | Contiene un Message Authentication Code (MAC) per un messaggio OPM.                                                                                           |
| [**\_ \_ dati ID di output OPM \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data)                                                    | Contiene il risultato di una richiesta di stato dell' [**\_ \_ \_ ID di output dell'OPM**](opm-get-output-id.md) .                                                              |
| [**\_numero casuale \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_random_number)                                                       | Contiene un numero casuale a 128 bit da usare con OPM.                                                                                                         |
| [**\_informazioni richieste da OPM \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)                                       | Contiene il risultato di una richiesta di stato OPM.                                                                                                              |
| [**\_ \_ \_ parametri di segnalazione ACP e CGMSA di impostazione di \_ \_ \_ OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) | Contiene informazioni per il comando [**OPM \_ set \_ ACP \_ e \_ CGMSA \_ signaling**](opm-set-acp-and-cgmsa-signaling.md) in OPM.                               |
| [**\_imposta i \_ \_ parametri HDCP SRM \_ di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)                                 | Contiene i parametri per il comando [**OPM \_ set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) .                                                                       |
| [**\_parametri del \_ livello di protezione impostati \_ da OPM \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)                 | Contiene i dati per il comando [OPM \_ set \_ Protection \_ Level](opm-set-protection-level.md) in OPM.                                                          |
| [**\_informazioni standard \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                         | Contiene il risultato di una richiesta di stato OPM.                                                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla programmazione di OPM](opm-programming-reference.md)
</dt> <dt>

[Gestione protezione output](output-protection-manager.md)
</dt> </dl>

 

 



