---
description: Le strutture seguenti vengono usate con Output Protection Manager (OPM).
ms.assetid: 676a60ca-393e-4b5d-89d3-50cf4b771492
title: Strutture OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35d72c5a5301dbc07b990aa4076f14fc221a1fde6af9c81e1f4a37fb424e24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737648"
---
# <a name="opm-structures"></a>Strutture OPM

Le strutture seguenti vengono usate con [Output Protection Manager](output-protection-manager.md) (OPM).



| Struttura                                                                                              | Descrizione                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INTESTAZIONE \_ GRL**](grl-header.md)                                                                      | Contiene l'intestazione dell'elenco di revoche globale( GRL).                                                                                                          |
| [**FIRMA \_ MF**](mf-signature.md)                                                                  | Contiene una firma dell'elenco di revoche globale( GRL).                                                                                                         |
| [**SEGNALAZIONE \_ OPM ACP \_ E \_ CGMSA \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling)                                 | Contiene il risultato di una query [**OPM \_ GET \_ ACP \_ E \_ CGMSA \_ SIGNALING.**](opm-get-acp-and-cgmsa-signaling.md)                                         |
| [**FORMATO \_ DI \_ OUTPUT EFFETTIVO \_ OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format)                                        | Contiene il risultato di una query [**OPM \_ GET ACTUAL OUTPUT \_ \_ \_ FORMAT**](opm-get-actual-output-format.md) in Output Protection Manager (OPM).               |
| [**PARAMETRI DI CONFIGURAZIONE DI \_ \_ OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters)                                         | Contiene un comando OPM o Certified Output Protection Manager (COPP).                                                                                     |
| [**INFORMAZIONI SUL \_ DISPOSITIVO \_ HDCP \_ CONNESSO OPM \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information)             | Contiene il risultato di una query [**OPM \_ GET CONNECTED \_ \_ HDCP DEVICE \_ \_ INFORMATION.**](opm-get-connected-hdcp-device-information.md)                     |
| [**PARAMETRI GET INFO COMPATIBILI CON \_ OPM COPP \_ \_ \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_copp_compatible_get_info_parameters)        | Contiene i parametri per il metodo [**IOPMVideoOutput::COPPCompatibleGetInformation.**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) |
| [**PARAMETRI DI \_ INIZIALIZZAZIONE CRITTOGRAFATI \_ \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters)          | Contiene i parametri di inizializzazione per una sessione OPM.                                                                                                     |
| [**OPM \_ GET CODEC INFO INFORMATION \_ (OTTENERE INFORMAZIONI SUL \_ \_ CODEC)**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information)                           | Contiene il risultato di una query [**OPM \_ GET CODEC \_ \_ INFO.**](opm-get-codec-info.md)                                                                     |
| [**OPM \_ GET \_ CODEC \_ INFO \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)                             | Contiene informazioni per il [**comando OPM \_ GET CODEC \_ \_ INFO.**](opm-get-codec-info.md)                                                                  |
| [**PARAMETRI OPM \_ GET \_ INFO \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)                                          | Contiene i parametri per il metodo [**IOPMVideoOutput::GetInformation.**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)                             |
| [**VETTORE DI \_ SELEZIONE DELLA CHIAVE HDCP OPM \_ \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_hdcp_key_selection_vector)                             | Contiene il vettore di selezione delle chiavi (KSV) per un ricevitore High-Bandwidth digital protezione del contenuto (HDCP).                                                   |
| [**OPM \_ OMAC**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_omac)                                                                          | Contiene un Message Authentication Code (MAC) per un messaggio OPM.                                                                                           |
| [**DATI ID \_ \_ OUTPUT \_ OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data)                                                    | Contiene il risultato di una richiesta [**di stato \_ OPM GET OUTPUT \_ \_ ID.**](opm-get-output-id.md)                                                              |
| [**NUMERO \_ CASUALE \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_random_number)                                                       | Contiene un numero casuale a 128 bit da usare con OPM.                                                                                                         |
| [**INFORMAZIONI RICHIESTE \_ \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)                                       | Contiene il risultato di una richiesta di stato OPM.                                                                                                              |
| [**OPM \_ IMPOSTA I PARAMETRI DI \_ SEGNALAZIONE ACP \_ E \_ CGMSA \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) | Contiene informazioni per il [**comando OPM \_ SET \_ ACP E \_ \_ CGMSA \_ SIGNALING**](opm-set-acp-and-cgmsa-signaling.md) in OPM.                               |
| [**OPM \_ SET \_ HDCP \_ SRM \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)                                 | Contiene i parametri per il [**comando OPM \_ SET \_ HDCP \_ SRM.**](opm-set-hdcp-srm.md)                                                                       |
| [**PARAMETRI DEL LIVELLO \_ DI PROTEZIONE OPM SET \_ \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)                 | Contiene i dati per il [comando OPM \_ SET PROTECTION \_ \_ LEVEL](opm-set-protection-level.md) in OPM.                                                          |
| [**INFORMAZIONI \_ STANDARD \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                         | Contiene il risultato di una richiesta di stato OPM.                                                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulla programmazione OPM](opm-programming-reference.md)
</dt> <dt>

[Output Protection Manager](output-protection-manager.md)
</dt> </dl>

 

 



