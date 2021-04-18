---
description: Le strutture seguenti vengono utilizzate per la creazione e la gestione di file e directory segnaposto.
ms.assetid: 50CCA8F5-7118-48E8-ADBF-337798FAF549
title: Strutture di filtro cloud
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebe6623ad3d9d348d624f8ab8da3427416d4742
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305339"
---
# <a name="cloud-filter-structures"></a>Strutture di filtro cloud

Le strutture seguenti vengono utilizzate per la creazione e la gestione di file e directory segnaposto.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                   | Descrizione                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_informazioni callback \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_info)<br/>                          | Contiene informazioni di callback comuni.<br/>                                                                                          |
| [**\_parametri di callback CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_parameters)<br/>              | Contiene parametri specifici del callback, ad esempio offset del file, lunghezza, flag e così via.<br/>                                                 |
| [**\_registrazione di callback CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_registration)<br/>          | Callback che devono essere registrati dal provider di sincronizzazione.<br/>                                                                           |
| [**\_intervallo di file CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_file_range)<br/>                                | Specifica un intervallo di dati in un file segnaposto.<br/>                                                                               |
| [**\_ \_ buffer intervallo di file CF \_**](/previous-versions/windows/desktop/legacy/mt844616(v=vs.85))<br/>                | Struttura per descrivere la posizione e l'intervallo di dati in un file.<br/>                                                              |
| [**\_metadati CF FS \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_fs_metadata)<br/>                              | Metadati di file o directory segnaposto.<br/>                                                                                        |
| [**\_criteri di idratazione CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_hydration_policy)<br/>                    | Specifica i criteri di idratazione primari e il relativo modificatore.<br/>                                                                       |
| [**\_informazioni sulle operazioni di CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info)<br/>                        | Informazioni su un'operazione su un file o una cartella segnaposto.<br/>                                                                |
| [**\_parametri dell'operazione CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_parameters)<br/>            | Parametri di un'operazione su un file o una cartella segnaposto.<br/>                                                                    |
| [**\_informazioni di \_ base SEGNAPOSTo CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_basic_info)<br/>       | Informazioni di base sul segnaposto.<br/>                                                                                                 |
| [**\_informazioni di \_ creazione SEGNAPOSTo CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_create_info)<br/>     | Contiene informazioni segnaposto per la creazione di nuovi file o directory segnaposto. <br/>                                           |
| [**\_informazioni standard segnaposto CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_standard_info)<br/> | Informazioni segnaposto standard.<br/>                                                                                              |
| [**\_informazioni piattaforma \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_platform_info)<br/>                          | Restituisce informazioni per la piattaforma di file cloud. Questa operazione è destinata ai provider di sincronizzazione in esecuzione su più versioni di Windows.<br/> |
| [**\_criteri di popolazione CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_population_policy)<br/>                  | Specifica i criteri di popolamento primario e il relativo modificatore.<br/>                                                                      |
| [**\_informazioni sul processo CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_process_info)<br/>                            | Contiene informazioni su un processo utente.<br/>                                                                                     |
| [**\_criteri di sincronizzazione CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_policies)<br/>                          | Definisce i criteri di sincronizzazione utilizzati da una radice di sincronizzazione.<br/>                                                                                 |
| [**\_registrazione della sincronizzazione CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_registration)<br/>                  | Dettagli del provider di sincronizzazione e della radice di sincronizzazione da registrare.<br/>                                                               |
| [**\_informazioni di \_ base sulla radice di sincronizzazione CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_basic_info)<br/>          | Informazioni radice di sincronizzazione di base.<br/>                                                                                                   |
| [**\_informazioni sul \_ \_ provider radice di sincronizzazione \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_provider_info)<br/>    | Informazioni sul provider radice di sincronizzazione.<br/>                                                                                                |
| [**\_ \_ \_ informazioni standard radice sincronizzazione \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_standard_info)<br/>    | Informazioni radice di sincronizzazione standard.<br/>                                                                                                |
| [**\_stato di sincronizzazione CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_status)<br/>                              | Utilizzato in una struttura di [**\_ \_ informazioni sulle operazioni di CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info) per descrivere lo stato di una radice di sincronizzazione specificata.<br/>     |



 

 

