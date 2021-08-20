---
title: Controller di dominio e strutture di gestione della replica
description: Il controller di dominio e le funzioni di gestione della replica usano le strutture seguenti.
ms.assetid: 42b20d3b-1799-4f5f-b74e-fe9284dd8ac3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4e7ddd37001b3b349159a21137fc1ae7b488c3a4997ac5f406677e3d421969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118018253"
---
# <a name="domain-controller-and-replication-management-structures"></a>Controller di dominio e strutture di gestione della replica

Le funzioni di gestione del controller di dominio e della replica usano le strutture seguenti:

-   [**INFORMAZIONI SUL \_ CONTROLLER DI \_ DOMINIO DS \_ \_ 1**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a)
-   [**INFORMAZIONI SUL \_ CONTROLLER DI \_ DOMINIO DS \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_2a)
-   [**INFORMAZIONI SUL CONTROLLER DI DOMINIO DS \_ \_ \_ \_ 3**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_3a)
-   [**RISULTATO DEL \_ NOME DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_resulta)
-   [**ELEMENTO RISULTATO NOME DS \_ \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_result_itema)
-   [**METADATI \_ \_ DELL'ATTR REPL \_ DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data)
-   [**DS \_ REPL \_ ATTR \_ META DATA \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_2)
-   [**BLOB DI METADATI ATTR DI DS \_ REPL \_ \_ \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_blob)
-   [**METADATI DEL VALORE ATTR DI DS \_ REPL \_ \_ \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data)
-   [**DS \_ REPL \_ ATTR \_ VALUE META \_ \_ DATA \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_2)
-   [**DS \_ REPL \_ ATTR \_ VALUE \_ META \_ DATA \_ EXT**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_ext)
-   [**CURSORE REPL DS \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
-   [**CURSORE \_ REPL \_ \_ DS 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_2)
-   [**CURSORE \_ REPL \_ \_ DS 3**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_3w)
-   [**BLOB DEL \_ \_ CURSORE REPL \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_blob)
-   [**\_CURSORI REPL \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)
-   [**CURSORI \_ REPL \_ DS \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_2)
-   [**CURSORI \_ REPL \_ DS \_ 3**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_3w)
-   [**ERRORE DS \_ REPL \_ KCC \_ DSA \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew)
-   [**ERRORI DS \_ REPL \_ KCC \_ DSA \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failuresw)
-   [**DS \_ REPL \_ KCC \_ DSA \_ FAILUREW \_ BLOB**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew_blob)
-   [**DS \_ REPL \_ NEIGHBOR**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw)
-   [**DS \_ REPL \_ NEIGHBORS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborsw)
-   [**DS \_ REPL \_ NEIGHBORW \_ BLOB**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw_blob)
-   [**METADATI \_ \_ OBJ DI \_ DS REPL \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data)
-   [**DS \_ REPL \_ OBJ \_ META DATA \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data_2)
-   [**DS \_ REPL \_ OP**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw)
-   [**BLOB DI DS \_ REPL \_ OPW \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw_blob)
-   [**DS \_ REPL \_ PENDING \_ OPS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_pending_opsw)
-   [**STATISTICHE CODA \_ REPL \_ DSW \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_queue_statisticsw)
-   [**DS \_ REPL \_ QUEUE \_ STATISTICSW \_ BLOB**](/previous-versions/windows/desktop/legacy/ms676274(v=vs.85))
-   [**METADATI DEL VALORE REPL DS \_ \_ \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data)
-   [**DS \_ REPL \_ VALUE META \_ DATA \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_2)
-   [**DS \_ REPL \_ VALUE \_ META \_ DATA \_ EXT**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_ext)
-   [**BLOB DI \_ METADATI DEL VALORE REPL DS \_ \_ \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob)
-   [**DS \_ REPL \_ VALUE \_ META \_ DATA \_ BLOB \_ EXT**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob_ext)
-   [**DS \_ REPSYNCALL \_ ERRINFO**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_errinfoa)
-   [**DS \_ REPSYNCALL \_ SYNC**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_synca)
-   [**DS \_ REPSYNCALL \_ UPDATE**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_updatea)
-   [**MAPPING GUID SCHEMA DS \_ \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_schema_guid_mapa)
-   [**INFORMAZIONI SUI COSTI \_ DEL \_ SITO DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_site_cost_info)
-   [**Programma**](/windows/desktop/api/Schedule/ns-schedule-schedule)
-   [**INTESTAZIONE \_ SCHEDULE**](/windows/desktop/api/Schedule/ns-schedule-schedule_header)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strutture in Active Directory Domain Services](structures-in-active-directory-domain-services.md)
</dt> </dl>

 

 