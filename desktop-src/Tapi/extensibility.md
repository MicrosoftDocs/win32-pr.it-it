---
description: Vengono effettuate le provisioning per estendere costanti e strutture in modo indipendente dal dispositivo e in un modo specifico del dispositivo (specifico del fornitore).
ms.assetid: bc0a18f3-1f58-4a24-8afb-c31f3b561375
title: Estensibilità (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ca446a03a9bdbe6d906e7accf261645401cd937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227487"
---
# <a name="extensibility"></a>Estendibilità

Vengono effettuate le provisioning per estendere costanti e strutture in modo indipendente dal dispositivo e in un modo specifico del dispositivo (specifico del fornitore). Nelle costanti che sono enumerazioni scalari, un intervallo di valori è riservato per le estensioni comuni future. Il resto dei valori viene identificato come specifico del dispositivo. Un fornitore può definire significati per questi valori nel modo desiderato. La loro interpretazione viene digitata nell' *identificatore di estensione* fornito nella struttura di dati [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps) . Per le costanti definite come flag di bit, viene riservato un intervallo di bit di ordine inferiore, in cui i bit di ordine superiore possono essere specifici dell'estensione. È consigliabile che i valori estesi e le matrici di bit usino i bit dal valore massimo o dal bit di ordine superiore. In questo modo si lascia l'opzione per spostare il bordo tra la parte comune e la parte di estensione se è necessario eseguire questa operazione in futuro. Alle estensioni per le strutture di dati viene assegnato un campo di dimensioni variabilmente con dimensioni/offset che fanno parte della parte fissa. TAPI descrive per ogni struttura di dati le estensioni specifiche del dispositivo consentite.

Oltre a riconoscere un identificatore di estensione specifico, l'applicazione deve negoziare il numero di versione dell'estensione con cui opera l'applicazione e il provider di servizi. Questa operazione viene eseguita nella seconda fase di negoziazione della versione della funzione [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) .

Un identificatore di estensione è un identificatore univoco globale. Non esiste alcun registro centrale per gli identificatori di estensione. Vengono invece generati localmente dal produttore da un'utilità disponibile con il Toolkit. Il numero è costituito da parti, ad esempio un indirizzo LAN univoco, un'ora del giorno e un numero casuale, per garantire l'univocità globale. Gli identificatori univoci globali sono progettati per essere distinguibili dagli identificatori universalmente univoci di HP/DEC e sono quindi completamente compatibili con essi.

 

 
