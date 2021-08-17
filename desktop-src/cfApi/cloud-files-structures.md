---
description: Le strutture seguenti vengono usate per la creazione e la gestione di file e directory segnaposto.
ms.assetid: 50CCA8F5-7118-48E8-ADBF-337798FAF549
title: Strutture di filtro cloud
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6da8cf5e512c6e65e88d17c5904fca264c28829dd0a0e842227da4b069aa82d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130223"
---
# <a name="cloud-filter-structures"></a>Strutture di filtro cloud

Le strutture seguenti vengono usate per la creazione e la gestione di file e directory segnaposto.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                   | Descrizione                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**INFORMAZIONI DI CALLBACK DI CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_info)<br/>                          | Contiene informazioni di callback comuni.<br/>                                                                                          |
| [**PARAMETRI DI CALLBACK CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_parameters)<br/>              | Contiene parametri specifici del callback, ad esempio offset di file, lunghezza, flag e così via.<br/>                                                 |
| [**REGISTRAZIONE CALLBACK CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_registration)<br/>          | Callback da registrare dal provider di sincronizzazione.<br/>                                                                           |
| [**CF \_ FILE \_ RANGE**](/windows/desktop/api/cfapi/ns-cfapi-cf_file_range)<br/>                                | Specifica un intervallo di dati in un file segnaposto.<br/>                                                                               |
| [**CF \_ FILE \_ RANGE \_ BUFFER**](/previous-versions/windows/desktop/legacy/mt844616(v=vs.85))<br/>                | Struttura che descrive la posizione e l'intervallo di dati in un file.<br/>                                                              |
| [**METADATI DI CF \_ \_ FS**](/windows/desktop/api/cfapi/ns-cfapi-cf_fs_metadata)<br/>                              | File segnaposto o metadati della directory.<br/>                                                                                        |
| [**CRITERI \_ DI IDRAZIONE CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_hydration_policy)<br/>                    | Specifica i criteri di idratazione primari e il relativo modificatore.<br/>                                                                       |
| [**INFORMAZIONI \_ SULL'OPERAZIONE \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info)<br/>                        | Informazioni su un'operazione su un file o una cartella segnaposto.<br/>                                                                |
| [**PARAMETRI \_ DELL'OPERAZIONE CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_parameters)<br/>            | Parametri di un'operazione su un file o una cartella segnaposto.<br/>                                                                    |
| [**INFORMAZIONI \_ DI BASE SUL \_ SEGNAPOSTO \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_basic_info)<br/>       | Informazioni di base sui segnaposto.<br/>                                                                                                 |
| [**INFO DI \_ CREAZIONE \_ SEGNAPOSTO CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_create_info)<br/>     | Contiene informazioni segnaposto per la creazione di nuovi file o directory segnaposto. <br/>                                           |
| [**INFO \_ \_ STANDARD SEGNAPOSTO CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_standard_info)<br/> | Informazioni segnaposto standard.<br/>                                                                                              |
| [**INFORMAZIONI \_ SULLA \_ PIATTAFORMA CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_platform_info)<br/>                          | Restituisce informazioni per la piattaforma di file cloud. È destinato ai provider di sincronizzazione in esecuzione in più versioni di Windows.<br/> |
| [**CRITERI DI \_ POPOLAMENTO CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_population_policy)<br/>                  | Specifica i criteri di popolamento primario e il relativo modificatore.<br/>                                                                      |
| [**CF \_ PROCESS \_ INFO**](/windows/desktop/api/cfapi/ns-cfapi-cf_process_info)<br/>                            | Contiene informazioni su un processo utente.<br/>                                                                                     |
| [**CRITERI DI \_ SINCRONIZZAZIONE CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_policies)<br/>                          | Definisce i criteri di sincronizzazione usati da una radice di sincronizzazione.<br/>                                                                                 |
| [**REGISTRAZIONE \_ DELLA SINCRONIZZAZIONE CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_registration)<br/>                  | Dettagli del provider di sincronizzazione e della radice di sincronizzazione da registrare.<br/>                                                               |
| [**INFORMAZIONI DI \_ BASE SULLA RADICE DI \_ \_ SINCRONIZZAZIONE \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_basic_info)<br/>          | Informazioni di base sulla radice di sincronizzazione.<br/>                                                                                                   |
| [**INFORMAZIONI SUL \_ \_ PROVIDER RADICE DI \_ SINCRONIZZAZIONE \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_provider_info)<br/>    | Sincronizzare le informazioni sul provider radice.<br/>                                                                                                |
| [**INFO \_ \_ STANDARD RADICE DI \_ SINCRONIZZAZIONE \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_standard_info)<br/>    | Informazioni radice di sincronizzazione standard.<br/>                                                                                                |
| [**STATO \_ SINCRONIZZAZIONE \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_status)<br/>                              | Usato in una [**struttura CF \_ OPERATION \_ INFO**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info) per descrivere lo stato di una radice di sincronizzazione specificata.<br/>     |



 

 

