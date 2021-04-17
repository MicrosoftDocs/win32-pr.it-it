---
description: 'Windows fornisce funzioni che eseguono le attività seguenti:'
ms.assetid: 437419c7-d6c5-4cae-b5d0-d552c75d4448
title: Interfaccia oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adc85eafdcfe4bb573d3e156b20f9b74dbf0652
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485245"
---
# <a name="object-interface"></a>Interfaccia oggetto

Windows fornisce funzioni che eseguono le attività seguenti:

-   Creare un oggetto
-   Ottenere un handle di oggetto
-   Ottenere informazioni sull'oggetto
-   Impostare le informazioni sull'oggetto
-   Chiudere l'handle dell'oggetto
-   Eliminare definitivamente l'oggetto

Alcune di queste attività non sono necessarie per ogni oggetto. Alcune di queste attività vengono combinate per determinati oggetti. Ad esempio, un'applicazione può creare un oggetto evento. Altre applicazioni possono aprire l'evento per ottenere un handle univoco per questo oggetto evento. Quando ogni applicazione termina utilizzando l'evento, chiude il relativo handle all'oggetto. Quando non sono presenti handle aperti rimanenti per l'oggetto evento, il sistema elimina l'oggetto evento. Un'applicazione può invece ottenere un handle per un oggetto finestra esistente. Quando l'oggetto finestra non è più necessario, l'applicazione deve eliminare definitivamente l'oggetto che invalida l'handle della finestra.

Occasionalmente, un oggetto rimane in memoria dopo la chiusura di tutti gli handle degli oggetti. Un thread, ad esempio, può creare un oggetto evento e attendere l'handle dell'evento. Mentre il thread è in attesa, è possibile che un altro thread chiuda lo stesso handle di oggetto evento. L'oggetto evento rimane in memoria, senza alcun handle di oggetto evento, fino a quando l'oggetto evento non viene impostato sullo stato segnalato e l'operazione di attesa viene completata. A questo punto, il sistema rimuove l'oggetto dalla memoria.

Handle e oggetti utilizzano la memoria. Pertanto, per mantenere le prestazioni del sistema, è necessario chiudere gli handle ed eliminare gli oggetti non appena non sono più necessari. In caso contrario, l'applicazione può influire negativamente sulle prestazioni del sistema, a causa dell'utilizzo eccessivo del file di paging.

Al termine di un processo, il sistema chiude automaticamente gli handle ed Elimina gli oggetti creati dal processo. Tuttavia, quando un thread termina, il sistema in genere non chiude gli handle o Elimina gli oggetti. Le uniche eccezioni sono finestra, Hook, posizione della finestra e oggetti di conversazione DDE (Dynamic Data Exchange); questi oggetti vengono eliminati definitivamente al termine del thread di creazione.

 

 



