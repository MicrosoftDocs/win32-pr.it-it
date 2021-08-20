---
title: Strutture e unioni DO
description: Le Ottimizzazione recapito (DO) usano le strutture seguenti.
ms.assetid: 58A5361E-871A-4911-85BD-83F18CB9A2F5
ms.topic: article
ms.date: 07/03/2019
ms.openlocfilehash: 4bb78e2efa11dd067abf53a4fc7453aadb6c9a4844b4302701a466eec13806a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101754"
---
# <a name="do-structures-and-unions"></a>Strutture e unioni DO

Le Ottimizzazione recapito (DO) [](do-interfaces.md) usano le strutture seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**BG_FILE_PROGRESS**](bg-file-progress.md) | La **BG_FILE_PROGRESS** fornisce informazioni sullo stato di avanzamento relative ai file, ad esempio il numero di byte trasferiti. |
| [**BG_FILE_RANGE**](bg-file-range.md) | La **BG_FILE_RANGE** identifica un intervallo di byte da scaricare da un file. |
| [**BG_JOB_PROGRESS**](bg-job-progress.md) | La **BG_JOB_PROGRESS** fornisce informazioni sullo stato di avanzamento relative ai processi, ad esempio il numero di byte e file trasferiti. Per i processi di caricamento, lo stato di avanzamento si applica al file di caricamento, non al file di risposta.  |
| [**BG_JOB_TIMES**](bg-job-times.md) | La **BG_JOB_TIMES** fornisce timestamp correlati al processo. |
| [**BITS_FILE_PROPERTY_VALUE**](bits-file-property-value.md) | **L BITS_FILE_PROPERTY_VALUE** union fornisce il valore della proprietà del file DO in base a un valore dell'enumerazione [**BITS_FILE_PROPERTY_ID.**](bits-file-property-id-.md) |
| [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) | **L BITS_JOB_PROPERTY_VALUE** union fornisce il valore della proprietà del processo DO in base al valore dell'enumerazione [**BITS_JOB_PROPERTY_ID.**](bits-job-property-id.md) |
| [**DO_DOWNLOAD_ENUM_CATEGORY**](./do/ns-do-do_download_enum_category.md) | Usato da **IDOManager::EnumDownloads** per filtrare l'enumerazione downloads in base al valore della proprietà specifica. |
| [**DO_DOWNLOAD_RANGE**](./deliveryoptimizationdownloadtypes/ns-deliveryoptimizationdownloadtypes-do_download_range.md) | Identifica un singolo intervallo di byte da scaricare da un file. |
| [**DO_DOWNLOAD_RANGE_INFO**](./do/ns-do-do_download_range_info.md) | Identifica una matrice di intervalli di byte da scaricare da un file. |
| [**DO_DOWNLOAD_STATUS**](./do/ns-do-do_download_status.md) | Usato per ottenere lo stato di un download specifico. |
| [**DOSwarmStats**](doswarmstats.md) | Contiene i campi per scaricare e caricare le statistiche per un file. |