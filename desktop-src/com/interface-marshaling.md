---
title: Marshalling dell'interfaccia
description: Marshalling dell'interfaccia
ms.assetid: 71069bd3-5f90-406a-be78-bb1af9b1c1c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5112b67e643fb95e1025fd4ed297043f81f576e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300498"
---
# <a name="interface-marshaling"></a>Marshalling dell'interfaccia

A meno che non si conoscano tutti i dubbi che l'interfaccia non verrà mai usata tra i limiti di Apartment, thread o processo, è necessario decidere come fornire supporto per il marshalling per le interfacce. Sono disponibili tre modi per fornire supporto per il marshalling:

-   Scrivere il proprio codice proxy/stub che chiama il canale COM, che a sua volta chiama le librerie di runtime RPC. In teoria, è possibile eseguire questa operazione, ma in pratica è quasi impossibile eseguire senza una notevole quantità di lavoro.
-   Descrivere le interfacce in un file IDL (Interface Definition Language) e usare il compilatore MIDL per generare una DLL proxy/stub. Questo metodo offre le migliori prestazioni e la massima flessibilità in termini di tipi di dati accettabili. Usando stub proxy generati da MIDL, è possibile controllare non solo la gestione della memoria, ma anche il marshalling e l'unmarshalling di tipi di dati complessi su piattaforme diverse.
-   Utilizzare MIDL per generare una libreria dei tipi utilizzata dal sistema per fornire supporto per il marshalling in fase di esecuzione. Questo è il modo più semplice per implementare il supporto del marshalling. È sufficiente generare una libreria di tipi e registrarla. Le interfacce devono essere compatibili con l'automazione ( [**oleautomation**](/windows/desktop/Midl/oleautomation) o [**Dual**](/windows/desktop/Midl/dual)), che pone alcune restrizioni sui tipi di dati che è possibile usare come parametri del metodo. Tuttavia, nella maggior parte dei casi, il vantaggio di avere le interfacce accessibili ai programmi scritti in altri linguaggi, ad esempio Microsoft Visual Basic e Java, supera le limitazioni dei tipi di dati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Comunicazione tra oggetti](inter-object-communication.md)
</dt> </dl>

 

 