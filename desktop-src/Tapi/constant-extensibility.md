---
description: Vengono effettuate le provisioning per estendere costanti e strutture in modo indipendente dal dispositivo e in un modo specifico del dispositivo (specifico del fornitore).
ms.assetid: 78430503-3e1f-49ab-be9c-d48bd21a840e
title: Estendibilità costante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a470ccb52af1bdc92596ac42bbafb74d4821db1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308306"
---
# <a name="constant-extensibility"></a>Estendibilità costante

Vengono effettuate le provisioning per estendere costanti e strutture in modo indipendente dal dispositivo e in un modo specifico del dispositivo (specifico del fornitore).

Nelle costanti che sono enumerazioni scalari, un intervallo di valori è riservato per le estensioni comuni future. Il resto dei valori viene identificato come specifico del dispositivo. Un fornitore può definire significati per questi valori nel modo desiderato. L'interpretazione di questi valori è chiave per l'ID estensione fornito tramite la struttura dei dati [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps) . Per le costanti definite come flag di bit, viene riservato un intervallo di bit di ordine inferiore, in cui i bit di ordine superiore possono essere specifici dell'estensione. È consigliabile che i valori estesi e le matrici di bit usino i bit dal valore massimo o dal bit di ordine superiore. In questo modo si lascia l'opzione per spostare il bordo tra la parte comune e la parte di estensione, se necessario, in futuro. Alle estensioni per le strutture di dati viene assegnato un campo di dimensioni variabilmente con dimensioni/offset che fanno parte della parte fissa. TSPI descrive le estensioni specifiche del dispositivo consentite per ogni struttura dei dati. Per ulteriori informazioni, vedere l'argomento [allocazione di memoria](./memory-allocation.md) .

Oltre a riconoscere un identificatore di estensione specifico, TAPI (operante per conto di un'applicazione) deve negoziare il numero di versione dell'estensione che l'applicazione e il provider di servizi utilizzeranno. Questa operazione viene eseguita usando le funzioni [**TSPI \_ LineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) e [**TSPI \_ phoneNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiateextversion) .

Un identificatore di estensione è un identificatore univoco globale. Non esiste alcun registro centrale per gli identificatori di estensione. Vengono invece generati localmente dal produttore da un'utilità disponibile con il Toolkit. Per garantire l'univocità globale, il numero è costituito da parti quali un indirizzo LAN (univoco), un'ora del giorno e un numero casuale. Gli identificatori univoci globali sono progettati per essere distinguibili dagli identificatori universalmente univoci di HP/DEC e sono quindi completamente compatibili con essi.

 

 
