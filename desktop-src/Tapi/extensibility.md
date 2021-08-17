---
description: Informazioni sull'estendibilità. Vengono effettuate le disposizioni per estendere costanti e strutture sia in modo indipendente dal dispositivo che in modo specifico del dispositivo.
ms.assetid: bc0a18f3-1f58-4a24-8afb-c31f3b561375
title: Estendibilità (API Di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b9b130c27ffb01131181ad0b765d6a41b3eae0bbfc84cc2ab325c3a13230a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140674"
---
# <a name="extensibility"></a>Estendibilità

Vengono effettuate le disposizioni per estendere costanti e strutture sia in modo indipendente dal dispositivo che in modo specifico del dispositivo (specifico del fornitore). Nelle costanti che sono enumerazioni scalari, un intervallo di valori è riservato per le estensioni comuni future. Il resto dei valori viene identificato come specifico del dispositivo. Un fornitore può definire significati per questi valori nel modo desiderato. La loro interpretazione è impostata *sull'identificatore di estensione* fornito nella struttura di dati [**LINEDEVCAPS.**](/windows/win32/api/tapi/ns-tapi-linedevcaps) Per le costanti definite come flag di bit, viene riservato un intervallo di bit di ordine basso, in cui i bit più elevati possono essere specifici dell'estensione. È consigliabile che i valori estesi e le matrici di bit usino bit dal valore più alto o dal bit più alto verso il basso. In questo modo viene lasciato l'opzione per spostare il bordo tra la parte comune e la parte di estensione se è necessario farlo in futuro. Alle estensioni per le strutture di dati viene assegnato un campo di dimensioni variabili con dimensioni/offset che fanno parte della parte fissa. TAPI descrive per ogni struttura di dati quali estensioni specifiche del dispositivo sono consentite.

Oltre a riconoscere un identificatore di estensione specifico, l'applicazione deve negoziare il numero di versione dell'estensione con cui operano l'applicazione e il provider di servizi. Questa operazione viene eseguita nella seconda fase di negoziazione della versione della [**funzione lineGetDevCaps.**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)

Un identificatore di estensione è un identificatore univoco globale. Non è disponibile alcun registro centrale per gli identificatori di estensione. Vengono invece generati in locale dal produttore da un'utilità disponibile con il toolkit. Il numero è costituito da parti, ad esempio un indirizzo LAN univoco, l'ora del giorno e un numero casuale, per garantire l'univocità globale. Gli identificatori univoci globali sono progettati per essere distinguibili dagli identificatori univoci universalmente HP/DEC e sono quindi completamente compatibili con essi.

 

 
