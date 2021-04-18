---
description: Vengono effettuate le provisioning per estendere costanti e strutture in modo indipendente dal dispositivo e in un modo specifico del dispositivo (specifico del fornitore).
ms.assetid: d30f80c3-3535-4d78-b0a1-c9a7389f8fd4
title: Estensibilità della struttura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b00fcf80b1ecfb7cc4d31b9ff040b101707ae236
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318930"
---
# <a name="structure-extensibility"></a>Estensibilità della struttura

Vengono effettuate le provisioning per estendere costanti e strutture in modo indipendente dal dispositivo e in un modo specifico del dispositivo (specifico del fornitore).

Nelle costanti che sono enumerazioni scalari, un intervallo di valori è riservato per le estensioni comuni future. Il resto dei valori viene identificato come specifico del dispositivo. Un fornitore può in alcun modo definire significati per questi valori. L'interpretazione di questi valori viene digitata nell' *identificatore di estensione* fornito tramite la struttura dei dati [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps) . Per le costanti definite come flag di bit, viene riservato un intervallo di bit di ordine inferiore, in cui i bit di ordine superiore possono essere specifici dell'estensione. È consigliabile che i valori estesi e le matrici di bit usino i bit dal valore massimo o dal bit di ordine superiore. In questo modo si lascia l'opzione per spostare il bordo tra la parte comune e la parte di estensione, se necessario in futuro. Alle estensioni per le strutture di dati viene assegnato un campo di dimensioni variabilmente con dimensioni/offset che fanno parte della parte fissa. TSPI descrive per ogni struttura di dati le estensioni specifiche del dispositivo consentite.

Oltre a riconoscere un identificatore di estensione specifico, TAPI (operante per conto di un'applicazione) deve negoziare il numero di versione dell'estensione con cui opera l'applicazione e il provider di servizi. Questa operazione viene eseguita usando le funzioni [**TSPI \_ LineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) e [**TSPI \_ phoneNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiateextversion) .

Un identificatore di estensione è un identificatore univoco globale. Non esiste alcun registro centrale per gli identificatori di estensione. Vengono invece generati localmente dal produttore da un'utilità disponibile con il Toolkit. Il numero è costituito da parti, ad esempio un indirizzo LAN (univoco), un'ora del giorno e un numero casuale, per garantire l'univocità globale. Gli identificatori univoci globali sono progettati per essere distinguibili dagli identificatori universalmente univoci di HP/DEC e sono quindi completamente compatibili con essi.

 

 
