---
title: Puntatori e RPC
description: È molto efficiente usare i puntatori come parametri della funzione C.
ms.assetid: 5792bd45-9c2a-4dd2-b050-17082fd0c929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbacce89046e2808acad539d19bbdcfeb1bc99c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856637"
---
# <a name="pointers-and-rpc"></a>Puntatori e RPC

È molto efficiente usare i puntatori come parametri della funzione C. Il puntatore costa solo pochi byte e può essere usato per accedere a una grande quantità di memoria. Tuttavia, in un'applicazione distribuita, le procedure client e server si trovano in spazi di indirizzi diversi, ma possono trovarsi in computer diversi. Pertanto, il client e il server in genere non hanno accesso allo stesso spazio di memoria.

Quando uno dei parametri della procedura remota è un puntatore a un oggetto, il client deve trasmettere una copia di tale oggetto e il relativo puntatore al server. Se la procedura remota modifica l'oggetto tramite il puntatore, il server restituisce il puntatore e la copia modificata.

MIDL offre attributi puntatore per ridurre al minimo la quantità di overhead necessario e le dimensioni dell'applicazione. Questa sezione illustra lo scopo e gli usi degli attributi del puntatore MIDL. Vengono inoltre fornite informazioni sulla gestione dei puntatori nelle applicazioni RPC. È divisa negli argomenti seguenti:

-   [Tipi di puntatori](kinds-of-pointers.md)
-   [Puntatori e allocazione di memoria](pointers-and-memory-allocation.md)
-   [Tipi di puntatore predefiniti](default-pointer-types.md)
-   [Puntatore-ereditarietà del tipo di attributo](pointer-attribute-type-inheritance.md)

 

 




