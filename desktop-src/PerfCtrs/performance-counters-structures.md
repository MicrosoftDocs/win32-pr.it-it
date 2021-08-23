---
description: Quando si usano i dati sulle prestazioni, si usano le strutture seguenti.
ms.assetid: 97118b64-3a2f-49c0-92e7-324df08bdb12
title: Strutture dei contatori delle prestazioni
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 00e9a505a9fe74592f571f3db108af2247a6d44889bc3ddbc2e4dae0844600b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674751"
---
# <a name="performance-counters-structures"></a>Strutture dei contatori delle prestazioni

Quando si usano i dati sulle prestazioni, si usano le strutture seguenti.

Per informazioni sulle funzioni disponibili per l'utilizzo dei contatori delle prestazioni, vedere [Funzioni dei contatori delle prestazioni.](performance-counters-functions.md)

## <a name="performance-data-helper-pdh-structures"></a>Strutture PDH (Performance Data Helper)

I consumer che usano [le funzioni dell'helper dati delle prestazioni (PDH)](using-the-pdh-functions-to-consume-counter-data.md) usano le strutture seguenti:

- [**PDH \_ BROWSE \_ DLG \_ CONFIG**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a)
- [**PDH \_ BROWSE \_ DLG \_ CONFIG \_ H**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_ha)
- [**PDH \_ COUNTER \_ INFO**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_info_a)
- [**ELEMENTI DEL PERCORSO DEL \_ \_ CONTATORE \_ PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a)
- [**ELEMENTI DEL PERCORSO \_ DELL'ELEMENTO \_ DATI \_ \_ PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_data_item_path_elements_a)
- [**PDH \_ FMT \_ COUNTERVALUE**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue)
- [**PDH \_ FMT \_ COUNTERVALUE \_ ITEM**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue_item_a)
- [**PDH \_ RAW \_ COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)
- [**ELEMENTO DEL \_ CONTATORE NON ELABORATO \_ PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter_item_a)
- [**RECORD DI LOG NON ELABORATO PDH \_ \_ \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_log_record)
- [**STATISTICHE \_ PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics)
- [**PDH \_ TIME \_ INFO**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info)

## <a name="perflib-v2-consumer-structures"></a>Strutture del consumer PerfLib V2

I consumer che usano [le funzioni PerfLib V2 Consumer](using-the-perflib-functions-to-consume-counter-data.md) usano le strutture seguenti:

- [**DATI DEI \_ CONTATORI DELLE \_ PRESTAZIONI**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_data)
- [**INTESTAZIONE DEL \_ CONTATORE DELLE PRESTAZIONI \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_header)
- [**IDENTIFICATORE DEL \_ CONTATORE \_ DELLE PRESTAZIONI**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identifier)
- [**INFORMAZIONI REG DEL \_ \_ CONTATORE DELLE PRESTAZIONI \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_reg_info)
- [**PERF \_ COUNTERSET \_ REG \_ INFO**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_reg_info)
- [**INTESTAZIONE \_ DATI PERF \_**](/windows/desktop/api/Perflib/ns-perflib-perf_data_header)
- [**INTESTAZIONE \_ DELL'ISTANZA DI \_ PERF**](/windows/desktop/api/Perflib/ns-perflib-perf_instance_header)
- [**CONTATORI \_ PERF \_ MULTI**](/windows/desktop/api/Perflib/ns-perflib-perf_multi_counters)
- [**ISTANZE MULTIPLE DI PERF \_ \_**](/windows/desktop/api/Perflib/ns-perflib-perf_multi_instances)
- [**INTESTAZIONE BUFFER STRINGA PERF \_ \_ \_**](/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header)
- [**INTESTAZIONE DEL \_ CONTATORE PERF STRING \_ \_**](/windows/win32/api/perflib/ns-perflib-perf_string_counter_header)

## <a name="perflib-v2-provider-structures"></a>Strutture del provider PerfLib V2

[I provider di dati delle prestazioni V2](providing-counter-data-using-version-2-0.md) usano le strutture seguenti:

- [**IDENTITÀ DEL \_ CONTATORE DELLE PRESTAZIONI \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [**INFORMAZIONI SUL \_ CONTATORE \_ DELLE PRESTAZIONI**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [**INFORMAZIONI \_ SULL'INSIEME DI \_ CONTATORI DELLE PRESTAZIONI**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [**ISTANZA \_ COUNTERSET PERF \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)
- [**CONTESTO DEL \_ PROVIDER PERF \_**](/windows/win32/api/perflib/ns-perflib-perf_provider_context)

## <a name="performance-dll-structures"></a>Strutture delle DLL delle prestazioni

[I provider DLL e i consumer](providing-counter-data-using-a-performance-dll.md) delle estensioni delle prestazioni che usano le funzioni del Registro di sistema per utilizzare i dati dei [contatori](using-the-registry-functions-to-consume-counter-data.md) usano le strutture seguenti:

- [**BLOCCO \_ CONTATORE PRESTAZIONI \_**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block)
- [**DEFINIZIONE DEL \_ CONTATORE DELLE PRESTAZIONI \_**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition)
- [**BLOCCO DI DATI \_ PERF \_**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block)
- [**DEFINIZIONE \_ DELL'ISTANZA DI PERF \_**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition)
- [**TIPO DI \_ OGGETTO \_ PERF**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type)
