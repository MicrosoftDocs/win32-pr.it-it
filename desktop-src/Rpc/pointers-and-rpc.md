---
title: Puntatori e RPC
description: È molto efficiente usare i puntatori come parametri della funzione C.
ms.assetid: 5792bd45-9c2a-4dd2-b050-17082fd0c929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a2ce934ed1440bc070fab1b59b76f87182419aada06acaf7699533ef9989697
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019183"
---
# <a name="pointers-and-rpc"></a>Puntatori e RPC

È molto efficiente usare i puntatori come parametri della funzione C. Il puntatore costa solo pochi byte e può essere usato per accedere a una grande quantità di memoria. In un'applicazione distribuita, tuttavia, le procedure client e server si trovano in spazi di indirizzi diversi, che possono trovarsi in computer diversi. Pertanto, il client e il server in genere non hanno accesso allo stesso spazio di memoria.

Quando uno dei parametri della procedura remota è un puntatore a un oggetto, il client deve trasmettere una copia di tale oggetto e il relativo puntatore al server. Se la procedura remota modifica l'oggetto tramite il relativo puntatore, il server restituisce il puntatore e la copia modificata.

MIDL offre attributi puntatore per ridurre al minimo la quantità di overhead richiesto e le dimensioni dell'applicazione. Questa sezione illustra lo scopo e gli usi degli attributi del puntatore MIDL. Presenta inoltre informazioni sulla gestione dei puntatori nelle applicazioni RPC. È suddiviso negli argomenti seguenti:

-   [Tipi di puntatori](kinds-of-pointers.md)
-   [Puntatori e allocazione di memoria](pointers-and-memory-allocation.md)
-   [Tipi di puntatore predefiniti](default-pointer-types.md)
-   [Ereditarietà del tipo pointer-attribute](pointer-attribute-type-inheritance.md)

 

 




