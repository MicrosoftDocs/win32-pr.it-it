---
description: È possibile utilizzare le firme digitali per distribuire un messaggio in formato testo non crittografato quando i destinatari devono identificare e verificare il mittente del messaggio.
ms.assetid: 10c33787-72d3-4e5d-b4dd-633b3fd29903
title: Firme digitali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299d84d1a1c71b6b6d709dbe67b4fa2c81f4b54e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128790"
---
# <a name="digital-signatures"></a>Firme digitali

È possibile utilizzare le [*firme digitali*](../secgloss/d-gly.md) per distribuire un messaggio in formato [*testo non crittografato*](../secgloss/p-gly.md) quando i destinatari devono identificare e verificare il mittente del messaggio. La firma di un messaggio non comporta la modifica del messaggio. genera semplicemente una stringa di firma digitale che è possibile aggregare con il messaggio o trasmettere separatamente. Una firma digitale è un breve frammento di dati crittografato con la [*chiave privata*](../secgloss/p-gly.md)del mittente. La decrittografia dei dati della firma tramite la [*chiave pubblica*](../secgloss/p-gly.md) del mittente dimostra che i dati sono stati crittografati dal mittente o da un utente che ha accesso alla chiave privata del mittente.

Le firme digitali vengono generate usando gli algoritmi di firma a [*chiave pubblica*](../secgloss/p-gly.md) . Una [*chiave privata*](../secgloss/p-gly.md) genera la firma ed è necessario utilizzare la chiave pubblica corrispondente per convalidare la firma. Questo processo è illustrato nella figura seguente.

![generazione di una firma digitale](images/capi02.png)

Per la creazione di una firma digitale da un messaggio sono necessari due passaggi. Il primo passaggio prevede la creazione di un valore [*hash*](../secgloss/h-gly.md) (noto anche come [*digest del messaggio*](../secgloss/m-gly.md)) dal messaggio. Questo valore hash viene quindi firmato usando la chiave privata del firmatario. Di seguito sono illustrati i passaggi necessari per la creazione di una firma digitale.

![creazione di una firma digitale da un messaggio](images/capi06.png)

Per verificare una firma, il messaggio e la firma sono obbligatori. Per prima cosa, è necessario creare un valore hash dal messaggio nello stesso modo in cui è stata creata la firma. Questo valore hash viene quindi verificato sulla base della firma usando la chiave pubblica del firmatario. Se il valore hash e la firma corrispondono, si può essere certi che il messaggio sia effettivamente quello che il firmatario ha firmato originariamente e che non è stato manomesso. Il diagramma seguente illustra il processo richiesto per la verifica di una firma digitale.

![Verifica di una firma digitale](images/capi07.png)

Un valore hash è costituito da una piccola quantità di dati binari, in genere circa 160 bit. Questa operazione viene prodotta usando un [*algoritmo di hash*](../secgloss/h-gly.md). Alcuni di questi algoritmi sono elencati più avanti in questa sezione.

Tutti i valori hash condividono le seguenti proprietà, indipendentemente dall'algoritmo utilizzato:

-   La lunghezza del valore hash è determinata dal tipo di algoritmo utilizzato e la lunghezza non varia in base alla dimensione del messaggio. Le lunghezze dei valori hash più comuni sono 128 o 160 bit.
-   Ogni coppia di messaggi non identici si traduce in un valore hash completamente diverso, anche se i due messaggi differiscono solo per un singolo bit. Grazie alla tecnologia odierna, non è possibile individuare una coppia di messaggi che si traduce nello stesso valore hash senza suddividere l'algoritmo hash.
-   Ogni volta che viene eseguito l'hashing di un messaggio specifico con lo stesso algoritmo, viene generato lo stesso valore hash.
-   Tutti gli algoritmi di hashing sono unidirezionali. Dato un valore hash, non è possibile recuperare il messaggio originale. In realtà, non è possibile determinare nessuna delle proprietà del messaggio originale dato il valore hash da solo.

 

 
