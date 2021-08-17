---
description: 'Windows fornisce funzioni che eseguono le attività seguenti:'
ms.assetid: 437419c7-d6c5-4cae-b5d0-d552c75d4448
title: Interfaccia dell'oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3db15a60d88b8258f5959d2bf4cf447496cbe97ae906bdf087fe316f449b276
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763990"
---
# <a name="object-interface"></a>Interfaccia dell'oggetto

Windows fornisce funzioni che eseguono le attività seguenti:

-   Creare un oggetto
-   Ottenere un handle di oggetto
-   Ottenere informazioni sull'oggetto
-   Impostare le informazioni sull'oggetto
-   Chiudere l'handle dell'oggetto
-   Eliminare l'oggetto

Alcune di queste attività non sono necessarie per ogni oggetto. Alcune di queste attività vengono combinate per determinati oggetti. Ad esempio, un'applicazione può creare un oggetto evento. Altre applicazioni possono aprire l'evento per ottenere un handle univoco per questo oggetto evento. Quando ogni applicazione termina di usare l'evento , chiude l'handle all'oggetto . Quando non sono presenti handle aperti rimanenti per l'oggetto evento, il sistema elimina l'oggetto evento. Al contrario, un'applicazione può ottenere un handle per un oggetto finestra esistente. Quando l'oggetto finestra non è più necessario, l'applicazione deve eliminare l'oggetto, invalidando l'handle della finestra.

In alcuni casi, un oggetto rimane in memoria dopo la chiusura di tutti gli handle di oggetto. Ad esempio, un thread può creare un oggetto evento e attendere l'handle dell'evento. Mentre il thread è in attesa, un altro thread potrebbe chiudere lo stesso handle dell'oggetto evento. L'oggetto evento rimane in memoria, senza alcun handle di oggetto evento, finché l'oggetto evento non viene impostato sullo stato segnalato e l'operazione di attesa non viene completata. Al momento, il sistema rimuove l'oggetto dalla memoria.

Gli handle e gli oggetti utilizzano la memoria. Pertanto, per mantenere le prestazioni del sistema, è necessario chiudere gli handle ed eliminare gli oggetti non appena non sono più necessari. Se non si esegue questa operazione, l'applicazione può danneggiare le prestazioni del sistema, a causa dell'uso eccessivo del file di paging.

Al termine di un processo, il sistema chiude automaticamente gli handle ed elimina gli oggetti creati dal processo. Tuttavia, quando un thread termina, il sistema in genere non chiude gli handle o elimina gli oggetti. Le uniche eccezioni sono finestra, hook, posizione della finestra e oggetti di conversazione DDE (Dynamic Data Exchange). Questi oggetti vengono distrutti quando il thread di creazione termina.

 

 



