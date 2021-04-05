---
title: ESEGUIRE strutture e unioni
description: Le interfacce di ottimizzazione recapito utilizzano le seguenti strutture.
ms.assetid: 58A5361E-871A-4911-85BD-83F18CB9A2F5
ms.topic: article
ms.date: 07/03/2019
ms.openlocfilehash: 860672e72e1e5f134382fd46cd9b36d1d411361e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118127"
---
# <a name="do-structures-and-unions"></a>ESEGUIRE strutture e unioni

Le [interfacce](do-interfaces.md) di ottimizzazione recapito utilizzano le seguenti strutture.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**BG_FILE_PROGRESS**](bg-file-progress.md) | La struttura **BG_FILE_PROGRESS** fornisce informazioni sullo stato di avanzamento correlate ai file, ad esempio il numero di byte trasferiti. |
| [**BG_FILE_RANGE**](bg-file-range.md) | La struttura **BG_FILE_RANGE** identifica un intervallo di byte da scaricare da un file. |
| [**BG_JOB_PROGRESS**](bg-job-progress.md) | La struttura **BG_JOB_PROGRESS** fornisce informazioni sullo stato di avanzamento correlate al processo, ad esempio il numero di byte e i file trasferiti. Per i processi di caricamento, lo stato di avanzamento si applica al file di caricamento, non al file di risposta.  |
| [**BG_JOB_TIMES**](bg-job-times.md) | La struttura **BG_JOB_TIMES** fornisce timestamp relativi ai processi. |
| [**BITS_FILE_PROPERTY_VALUE**](bits-file-property-value.md) | Il **BITS_FILE_PROPERTY_VALUE** Unione fornisce il valore della proprietà del file do in base a un valore dell'enumerazione [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) . |
| [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) | Il **BITS_JOB_PROPERTY_VALUE** Unione fornisce il valore della proprietà del processo do in base al valore dell'enumerazione [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) . |
| [**DO_DOWNLOAD_ENUM_CATEGORY**](./do/ns-do-do_download_enum_category.md) | Usato da **IDOManager:: EnumDownloads** per filtrare l'enumerazione downloads in base al valore della proprietà specifica. |
| [**DO_DOWNLOAD_RANGE**](./deliveryoptimizationdownloadtypes/ns-deliveryoptimizationdownloadtypes-do_download_range.md) | Identifica un singolo intervallo di byte da scaricare da un file. |
| [**DO_DOWNLOAD_RANGE_INFO**](./do/ns-do-do_download_range_info.md) | Identifica una matrice di intervalli di byte da scaricare da un file. |
| [**DO_DOWNLOAD_STATUS**](./do/ns-do-do_download_status.md) | Utilizzato per ottenere lo stato di un download specifico. |
| [**DOSwarmStats**](doswarmstats.md) | Contiene i campi per scaricare e caricare le statistiche per un file. |