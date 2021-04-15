---
title: Modifica di un'interfaccia esistente
description: Quando possibile, implementare una nuova interfaccia per l'applicazione, invece di apportare modifiche a un oggetto esistente.
ms.assetid: 29845cf5-445c-403d-b298-d4e07c3536b7
keywords:
- modifica della programmazione Windows a 64 bit delle interfacce esistenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a656ee768dcc2e88725d2cff0ddc5604fd771f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516918"
---
# <a name="changing-an-existing-interface"></a>Modifica di un'interfaccia esistente

Quando possibile, implementare una nuova interfaccia per l'applicazione, invece di apportare modifiche a un oggetto esistente. Se non è possibile modificare un'interfaccia esistente, utilizzare i nuovi tipi di dati solo nei nuovi metodi. L'introduzione di un nuovo tipo di dati o la modifica di un tipo esistente è l'origine più comune di problemi di incompatibilità. Il modello di runtime RPC presuppone che l'applicazione ricevente conosca i tipi di dati ricevuti, quindi i dati vengono inseriti in rete senza una descrizione dei dati generici. Quando il destinatario prevede un tipo di dati diverso rispetto a quello che il mittente ha messo in rete, lo stub genera un'eccezione (o la trasmissione ha esito negativo in un altro modo meno appropriato).

Un'interfaccia RPC è definita dal rispettivo UUID e dai numeri di versione principale e secondaria. Quando si modifica un'interfaccia esistente, è necessario aggiungere i nuovi metodi alla fine dell'interfaccia e modificare il numero della versione secondaria. Se si aggiungono metodi altrove o si apportano altre modifiche all'interfaccia, sarà necessario modificare anche il numero di versione principale.

Realisticamente, in alcuni casi non è possibile modificare anche il numero di versione secondario, perché un nuovo client non sarà in grado di comunicare con un server precedente e non sarà possibile aggiornare il server. Il tempo di esecuzione RPC genera un'eccezione, \_ \_ PROCNUM RPC \_ fuori \_ \_ intervallo, quando un client chiama un metodo oltre quelli specificati per la relativa interfaccia con il server. La soluzione alternativa consiste nel lasciare invariati i numeri di versione e scrivere il codice client per gestire correttamente questa eccezione, ovvero dal client, ad esempio, o con qualsiasi mezzo, appropriato per l'applicazione.

Esiste una soluzione alternativa simile per un caso speciale di modifica di un tipo di dati in un metodo esistente. Se si dispone di un' [**Unione**](/windows/desktop/Midl/union) i cui rami sono puntatori e che non dispone di un ramo predefinito per i tipi non riconosciuti, è possibile aggiungere un nuovo ramo che utilizza il nuovo tipo di dati. In questo modo non si modificano le dimensioni della struttura dei dati. Quando il client comunica con un nuovo server, può utilizzare il nuovo tipo di dati. Tuttavia, quando il client comunica con un vecchio server, il tempo di esecuzione genera il \_ \_ tag non valido per la RPC di eccezione \_ . Anche in questo caso, sarà necessario scrivere il codice client per gestire questa eccezione.

Un'interfaccia DCOM è identificata dal relativo GUID. In DCOM le interfacce sono considerate non modificabili ed è possibile apportare modifiche solo creando una nuova interfaccia che eredita da quella precedente. Queste regole assicurano che client e server rimangano compatibili.

 

 