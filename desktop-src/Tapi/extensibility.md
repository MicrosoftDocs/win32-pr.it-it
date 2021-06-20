---
description: Informazioni sull'estendibilità. Il provisioning viene effettuato per estendere costanti e strutture sia in modo indipendente dal dispositivo che in modo specifico del dispositivo.
ms.assetid: bc0a18f3-1f58-4a24-8afb-c31f3b561375
title: Estendibilità (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f29ad34b5156bdd652ab6b6f8901be7a2341bdc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406564"
---
# <a name="extensibility"></a>Estendibilità

Il provisioning viene effettuato per estendere costanti e strutture in modo indipendente dal dispositivo e in modo specifico del dispositivo (specifico del fornitore). Nelle costanti che sono enumerazioni scalari, un intervallo di valori è riservato per le future estensioni comuni. Il resto dei valori viene identificato come specifico del dispositivo. Un fornitore può definire significati per questi valori nel modo desiderato. La loro interpretazione è impostata *sull'identificatore di estensione* fornito nella struttura dei dati [**LINEDEVCAPS.**](/windows/win32/api/tapi/ns-tapi-linedevcaps) Per le costanti definite come flag di bit, viene riservato un intervallo di bit meno elevati, in cui i bit più elevati possono essere specifici dell'estensione. È consigliabile che i valori estesi e le matrici di bit usino bit dal valore più alto o dal bit più alto in basso. In questo modo si lascia l'opzione per spostare il bordo tra la parte comune e la parte di estensione se è necessario farlo in futuro. Alle estensioni per le strutture di dati viene assegnato un campo di dimensioni variabili con dimensioni/offset che fanno parte della parte fissa. TAPI descrive per ogni struttura di dati quali estensioni specifiche del dispositivo sono consentite.

Oltre a riconoscere un identificatore di estensione specifico, l'applicazione deve negoziare il numero di versione dell'estensione con cui operano l'applicazione e il provider di servizi. Questa operazione viene eseguita nella seconda fase di negoziazione della versione [**della funzione lineGetDevCaps.**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)

Un identificatore di estensione è un identificatore univoco globale. Non è disponibile alcun registro centrale per gli identificatori di estensione. Vengono invece generati in locale dal produttore da un'utilità disponibile con il toolkit. Il numero è costituito da parti, ad esempio un indirizzo LAN univoco, l'ora del giorno e un numero casuale, per garantire l'univocità globale. Gli identificatori univoci globali sono progettati per essere distinguibili dagli identificatori univoci universali HP/DEC e sono pertanto completamente compatibili con essi.

 

 
