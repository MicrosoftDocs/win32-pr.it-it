---
title: Orfana della memoria
description: Se l'applicazione distribuita usa un parametro del puntatore \ in, out, unique\ o \ in, out, ptr\, il lato server dell'applicazione può modificare il valore del parametro pointer su Null.
ms.assetid: 65588b4d-6bf4-44f7-994c-29a5b185c6b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64b3a560eb1daecf3cd10bc18c62057cd2d09c1321c272f4e8fe73a65305832
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019829"
---
# <a name="memory-orphaning"></a>Orfana della memoria

Se l'applicazione distribuita usa un parametro del puntatore \[ [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl), [unique](/windows/desktop/Midl/unique) o \] \[ **in**, **out**, [ptr](/windows/desktop/Midl/ptr) , il lato server dell'applicazione può modificare il valore del parametro \] pointer su Null. Quando il server restituisce successivamente il valore Null al client, la memoria a cui fa riferimento il puntatore prima della chiamata di procedura remota è ancora presente sul lato client, ma non è più accessibile da tale puntatore (tranne nel caso di un puntatore completo con alias). Si dice che questa memoria sia *orfana.* Si tratta anche di una perdita *di memoria.* La ripetizione dell'orfano della memoria nel client causa l'esinging delle risorse di memoria disponibili nel client.

La memoria può anche essere orfana ogni volta che il server modifica un puntatore incorporato a un valore Null. Ad esempio, se il parametro punta a una struttura di dati complessa, ad esempio un albero, il lato server dell'applicazione può eliminare nodi dell'albero e impostare i puntatori all'interno dell'albero su Null.

Un'altra situazione che può causare una perdita di memoria comporta matrici conformi, variabili e aperte contenenti puntatori. Quando l'applicazione server modifica il parametro che specifica le dimensioni della matrice o l'intervallo trasmesso in modo che rappresenti un valore più piccolo, gli stub usano i valori più piccoli per liberare memoria. Gli elementi della matrice con indici maggiori del parametro size sono orfani. L'applicazione deve liberare elementi al di fuori dell'intervallo trasmesso.

 

 