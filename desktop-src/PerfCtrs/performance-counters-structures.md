---
description: Utilizzare le strutture seguenti quando si utilizzano i dati sulle prestazioni.
ms.assetid: 97118b64-3a2f-49c0-92e7-324df08bdb12
title: Strutture dei contatori delle prestazioni
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 0629aa1763f08dfce9e2cc646bd1b5744d6591cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967501"
---
# <a name="performance-counters-structures"></a>Strutture dei contatori delle prestazioni

Utilizzare le strutture seguenti quando si utilizzano i dati sulle prestazioni.

Per informazioni sulle funzioni disponibili per l'utilizzo dei contatori delle prestazioni, vedere [funzioni dei contatori delle prestazioni](performance-counters-functions.md).

## <a name="performance-data-helper-pdh-structures"></a>Strutture PDH (Performance Data Helper)

I consumer che utilizzano le funzioni [PDH (Performance Data Helper)](using-the-pdh-functions-to-consume-counter-data.md) utilizzano le strutture seguenti:

- [**PDH \_ esplorare \_ la \_ configurazione DLG**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a)
- [**PDH \_ Browse \_ DLG \_ config \_ H**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_ha)
- [**\_info contatore \_ PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_info_a)
- [**\_elementi del \_ percorso del contatore PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a)
- [**\_elementi del \_ percorso dell'elemento di dati PDH \_ \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_data_item_path_elements_a)
- [**PDH \_ FMT \_ COUNTERVALUE**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue)
- [**\_ \_ elemento COUNTERVALUE di PDH FMT \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue_item_a)
- [**PDH \_ \_ contatore RAW**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)
- [**PDH \_ \_ elemento contatore non elaborato \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter_item_a)
- [**\_record del \_ log non elaborato PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_log_record)
- [**\_statistiche PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics)
- [**\_informazioni PDH tempo \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info)

## <a name="perflib-v2-consumer-structures"></a>Strutture consumer PerfLib V2

I consumer che usano le funzioni [consumer Perflib V2](using-the-perflib-functions-to-consume-counter-data.md) utilizzano le strutture seguenti:

- [**\_dati contatore \_ prestazioni**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_data)
- [**\_intestazione contatore \_ prestazioni**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_header)
- [**\_identificatore contatore \_ prestazioni**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identifier)
- [**\_ \_ informazioni reg contatore \_ prestazioni**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_reg_info)
- [**\_ \_ informazioni reg del contatore delle prestazioni \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_reg_info)
- [**\_intestazione dati \_ perf**](/windows/desktop/api/Perflib/ns-perflib-perf_data_header)
- [**\_intestazione dell'istanza Perf \_**](/windows/desktop/api/Perflib/ns-perflib-perf_instance_header)
- [**PRESTAZIONI \_ più \_ contatori**](/windows/desktop/api/Perflib/ns-perflib-perf_multi_counters)
- [**più \_ istanze di perf \_**](/windows/desktop/api/Perflib/ns-perflib-perf_multi_instances)
- [**\_ \_ intestazione buffer stringa \_ perf**](/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header)
- [**\_ \_ intestazione contatore della stringa Perf \_**](/windows/win32/api/perflib/ns-perflib-perf_string_counter_header)

## <a name="perflib-v2-provider-structures"></a>Strutture del provider PerfLib V2

[V2 i provider di dati sulle prestazioni](providing-counter-data-using-version-2-0.md) utilizzano le strutture seguenti:

- [**\_identità contatore \_ prestazioni**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [**\_informazioni contatore \_ prestazioni**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [**informazioni sul contatore delle prestazioni \_ \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [**istanza del contatore delle prestazioni \_ \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)
- [**\_contesto del provider Perf \_**](/windows/win32/api/perflib/ns-perflib-perf_provider_context)

## <a name="performance-dll-structures"></a>Strutture DLL di prestazioni

I [provider di dll dell'estensione](providing-counter-data-using-a-performance-dll.md) per le prestazioni e [gli utenti che utilizzano le funzioni del registro di sistema per](using-the-registry-functions-to-consume-counter-data.md) utilizzare i dati del contatore utilizzano le seguenti strutture

- [**\_blocco contatore \_ prestazioni**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block)
- [**\_definizione del contatore delle prestazioni \_**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition)
- [**\_blocco di dati Perf \_**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block)
- [**\_definizione dell'istanza di perf \_**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition)
- [**\_tipo di oggetto Perf \_**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type)
