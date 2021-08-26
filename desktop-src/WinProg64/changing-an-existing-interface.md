---
title: Modifica di un'interfaccia esistente
description: Quando possibile, implementare una nuova interfaccia per l'applicazione, anziché apportare modifiche a una esistente.
ms.assetid: 29845cf5-445c-403d-b298-d4e07c3536b7
keywords:
- modifica delle interfacce esistenti a 64 bit Windows programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782587471de5616750501552445599a94571ff2275d080347937c595e2cd7668
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899071"
---
# <a name="changing-an-existing-interface"></a>Modifica di un'interfaccia esistente

Quando possibile, implementare una nuova interfaccia per l'applicazione, anziché apportare modifiche a una esistente. Se non è possibile evitare di modificare un'interfaccia esistente, usare nuovi tipi di dati solo nei nuovi metodi. L'introduzione di un nuovo tipo di dati o la modifica di un tipo esistente è l'origine più comune di problemi di incompatibilità. Il modello di run-time RPC presuppone che l'applicazione ricevente sia a conoscenza dei tipi di dati ricevuti, quindi i dati vengono messi in transito senza una descrizione generica dei dati. Quando il destinatario prevede un tipo di dati diverso da quello che il mittente ha inserito in transito, lo stub genera un'eccezione (o la trasmissione non riesce in un altro modo meno corretto).

Un'interfaccia RPC è definita dal relativo UUID e dai relativi numeri di versione principale e secondario. Quando si modifica un'interfaccia esistente, è necessario aggiungere i nuovi metodi alla fine dell'interfaccia e modificare il numero di versione secondaria. Se si aggiungono metodi in qualsiasi altro punto o si apportano altre modifiche all'interfaccia, sarà necessario modificare anche il numero di versione principale.

Realisticamente, in alcuni casi non è possibile modificare anche il numero di versione secondaria, perché un nuovo client non sarà in grado di comunicare con un server precedente e non sarà possibile aggiornare il server. Il tempo di esecuzione RPC genera un'eccezione, RPC S PROCNUM OUT OF RANGE, quando un client chiama un metodo oltre a quelli specificati per la relativa interfaccia \_ \_ con il \_ \_ \_ server. La soluzione alternativa consiste nel lasciare invariati i numeri di versione e scrivere il codice client per gestire correttamente questa eccezione, ad esempio con un peggioramento delle prestazioni del client o con qualsiasi mezzo appropriato per l'applicazione.

Esiste una soluzione alternativa simile per un caso speciale di modifica di un tipo di dati in un metodo esistente. Se si [](/windows/desktop/Midl/union) dispone di un'unione i cui rami sono puntatori e che non dispone di un ramo predefinito per i tipi non riconosciuti, è possibile aggiungere un nuovo ramo che usa il nuovo tipo di dati. In questo modo le dimensioni della struttura dei dati non verranno modificate. Quando il client parla con un nuovo server, può usare il nuovo tipo di dati. Tuttavia, quando il client parla con un server precedente, il tempo di esecuzione genererà l'eccezione RPC \_ S \_ INVALID \_ TAG. Anche in questo caso, sarà necessario scrivere il codice client per gestire questa eccezione in modo appropriato.

Un'interfaccia DCOM è identificata dal relativo GUID. In DCOM le interfacce sono considerate non modificabili ed è possibile apportare modifiche solo creando una nuova interfaccia che eredita da quella precedente. Queste regole garantiscono che i client e i server rimangano compatibili.

 

 