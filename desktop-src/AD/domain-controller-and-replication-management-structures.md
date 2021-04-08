---
title: Controller di dominio e strutture di gestione della replica
description: Il controller di dominio e le funzioni di gestione della replica utilizzano le seguenti strutture.
ms.assetid: 42b20d3b-1799-4f5f-b74e-fe9284dd8ac3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4afe084e4285f4851457f9a519e747952e3bbd67
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872317"
---
# <a name="domain-controller-and-replication-management-structures"></a>Controller di dominio e strutture di gestione della replica

Il controller di dominio e le funzioni di gestione della replica utilizzano le strutture seguenti:

-   [**\_Informazioni sul controller di dominio DS \_ \_ \_ 1**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a)
-   [**\_Informazioni sul controller di dominio DS \_ \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_2a)
-   [**\_Informazioni sul controller di dominio DS \_ \_ \_ 3**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_3a)
-   [**\_risultato nome \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_resulta)
-   [**\_elemento di \_ risultato \_ nome DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_result_itema)
-   [**\_ \_ \_ meta data di DS REPL attr \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data)
-   [**DS \_ REPL \_ attr \_ meta \_ data \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_2)
-   [**\_BLOB di \_ \_ meta \_ data \_ di DS REPL attr**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_blob)
-   [**metadati del valore di DS \_ REPL \_ attr \_ \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data)
-   [**DS \_ REPL \_ attr \_ value \_ meta \_ data \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_2)
-   [**DS \_ REPL \_ attr \_ valore \_ meta \_ data \_ ext**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_ext)
-   [**\_cursore REPL \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
-   [**\_Cursore REPL \_ DS \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_2)
-   [**\_Cursore REPL \_ DS \_ 3**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_3w)
-   [**\_ \_ BLOB cursore REPL \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_blob)
-   [**\_ \_ cursori REPL DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)
-   [**\_ \_ Cursori REPL DS \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_2)
-   [**\_ \_ Cursori REPL DS \_ 3**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_3w)
-   [**\_ \_ \_ errore DSA KCC di DS REPL \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew)
-   [**\_ \_ \_ errori DSA KCC di DS REPL \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failuresw)
-   [**\_ \_ \_ BLOB FAILUREW KCC DSA \_ REPL \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew_blob)
-   [**DS \_ REPL \_ Neighbor**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw)
-   [**\_REPL \_ vicini DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborsw)
-   [**\_ \_ BLOB NEIGHBORW di DS REPL \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw_blob)
-   [**\_ \_ \_ meta dati di DS REPL obj \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data)
-   [**DS \_ REPL \_ obj \_ meta \_ data \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data_2)
-   [**\_op REPL \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw)
-   [**\_ \_ BLOB OPW di DS REPL \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw_blob)
-   [**\_ \_ operazioni in sospeso DS \_ repl**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_pending_opsw)
-   [**\_ \_ STATISTICSW coda DS \_ repl**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_queue_statisticsw)
-   [**\_ \_ \_ BLOB STATISTICSW coda REPL \_ DS**](/previous-versions/windows/desktop/legacy/ms676274(v=vs.85))
-   [**\_metadati del \_ valore \_ REPL \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data)
-   [**DS \_ REPL \_ valore \_ meta \_ data \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_2)
-   [**DS \_ REPL \_ valore \_ meta \_ dati \_ ext**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_ext)
-   [**\_ \_ \_ \_ BLOB dei metadati del valore REPL DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob)
-   [**DS \_ REPL \_ valore \_ meta \_ dati \_ BLOB \_ ext**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob_ext)
-   [**DS \_ REPSYNCALL \_ ERRINFO**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_errinfoa)
-   [**sincronizzazione di DS \_ REPSYNCALL \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_synca)
-   [**aggiornamento di DS \_ REPSYNCALL \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_updatea)
-   [**\_mappa GUID dello schema DS \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_schema_guid_mapa)
-   [**\_informazioni sui \_ costi del sito DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_site_cost_info)
-   [**PIANIFICAZIONE**](/windows/desktop/api/Schedule/ns-schedule-schedule)
-   [**\_intestazione pianificazione**](/windows/desktop/api/Schedule/ns-schedule-schedule_header)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strutture in Active Directory Domain Services](structures-in-active-directory-domain-services.md)
</dt> </dl>

 

 