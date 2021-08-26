---
title: Marshalling dell'interfaccia
description: Marshalling dell'interfaccia
ms.assetid: 71069bd3-5f90-406a-be78-bb1af9b1c1c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cdee8762fb9ef69507fb5b2c4295531dd87a98d5174ab4e10f05a66cab718d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029871"
---
# <a name="interface-marshaling"></a>Marshalling dell'interfaccia

A meno che non si sappia oltre ogni dubbio che l'interfaccia non verrà mai usata oltre i limiti di apartment, thread o processo, è necessario decidere come fornire il supporto del marshalling per le interfacce. Esistono tre modi per fornire il supporto del marshalling:

-   Scrivere codice proxy/stub personalizzato che chiama il canale COM, che a sua volta chiama le librerie di runtime RPC. In teoria, è possibile eseguire questa operazione, ma in pratica è quasi impossibile senza un notevole sforzo.
-   Descrivere le interfacce in un file IDL (Interface Definition Language) e usare il compilatore MIDL per generare una DLL proxy/stub. Questo metodo offre le migliori prestazioni e la massima flessibilità in termini di tipi di dati accettabili. Usando gli stub proxy generati da MIDL, è possibile controllare non solo la gestione della memoria, ma anche il marshalling e l'unmarsshaling di tipi di dati complessi su piattaforme diverse.
-   Usare MIDL per generare una libreria dei tipi utilizzata dal sistema per fornire supporto per il marshalling in fase di esecuzione. Questo è il modo più semplice per implementare il supporto del marshalling. È necessario solo generare una libreria dei tipi e registrarla. Le interfacce devono essere compatibili con l'automazione [**(oleautomation**](/windows/desktop/Midl/oleautomation) o [**dual),**](/windows/desktop/Midl/dual)che pone alcune restrizioni sui tipi di dati che è possibile usare come parametri del metodo. Tuttavia, nella maggior parte dei casi, il vantaggio di avere le interfacce accessibili ai programmi scritti in altri linguaggi, ad esempio Microsoft Visual Basic e Java, supera le limitazioni relative ai tipi di dati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Comunicazione tra oggetti](inter-object-communication.md)
</dt> </dl>

 

 