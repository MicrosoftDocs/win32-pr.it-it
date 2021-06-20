---
description: Informazioni sull'estendibilità costante. Il provisioning viene effettuato per estendere costanti e strutture sia in modo indipendente dal dispositivo che in modo specifico del dispositivo.
ms.assetid: 78430503-3e1f-49ab-be9c-d48bd21a840e
title: Estensibilità costante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975d2901dcc3f7e574ffdacdabbcf457821ef932
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409974"
---
# <a name="constant-extensibility"></a>Estensibilità costante

Il provisioning viene effettuato per estendere costanti e strutture in modo indipendente dal dispositivo e in modo specifico del dispositivo (specifico del fornitore).

Nelle costanti che sono enumerazioni scalari, un intervallo di valori è riservato per le future estensioni comuni. Il resto dei valori viene identificato come specifico del dispositivo. Un fornitore può definire significati per questi valori nel modo desiderato. L'interpretazione di questi valori viene impostata sull'ID di estensione fornito tramite la [**struttura dei dati LINEDEVCAPS.**](/windows/win32/api/tapi/ns-tapi-linedevcaps) Per le costanti definite come flag di bit, viene riservato un intervallo di bit meno elevati, in cui i bit più elevati possono essere specifici dell'estensione. È consigliabile che i valori estesi e le matrici di bit usino bit dal valore più alto o dal bit più alto in basso. In questo modo si lascia l'opzione per spostare il bordo tra la parte comune e la parte di estensione, se necessario in futuro. Alle estensioni per le strutture di dati viene assegnato un campo di dimensioni variabili con dimensioni/offset che fanno parte della parte fissa. TSPI descrive le estensioni specifiche del dispositivo consentite per ogni struttura di dati. Per altre informazioni, vedere l'argomento [relativo all'allocazione di](./memory-allocation.md) memoria.

Oltre a riconoscere un identificatore di estensione specifico, TAPI (che opera per conto di un'applicazione) deve negoziare il numero di versione dell'estensione con cui l'applicazione e il provider di servizi funzioneranno. Questa operazione viene eseguita usando [**le funzioni \_ lineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) e [**TSPI \_ phoneNegotiateExtVersion.**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiateextversion)

Un identificatore di estensione è un identificatore univoco globale. Non è disponibile alcun registro centrale per gli identificatori di estensione. Vengono invece generati in locale dal produttore da un'utilità disponibile con il toolkit. Per garantire l'univocità globale, il numero è costituito da parti quali un indirizzo LAN (univoco), l'ora del giorno e un numero casuale. Gli identificatori univoci globali sono progettati per essere distinguibili dagli identificatori univoci universali HP/DEC e sono pertanto completamente compatibili con essi.

 

 
