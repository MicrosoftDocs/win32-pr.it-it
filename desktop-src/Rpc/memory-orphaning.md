---
title: Memoria orfana
description: Se l'applicazione distribuita usa un parametro \ in, out, Unique \ o \ in, out, PTR \ Pointer, il lato server dell'applicazione può modificare il valore del parametro pointer in null.
ms.assetid: 65588b4d-6bf4-44f7-994c-29a5b185c6b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32042911695f377e0a628168e91387bfa25f0d79
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300328"
---
# <a name="memory-orphaning"></a>Memoria orfana

Se l'applicazione distribuita usa un \[ parametro puntatore [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl), [Unique](/windows/desktop/Midl/unique) \] o \[ **in**, **out**, [ptr](/windows/desktop/Midl/ptr) \] , il lato server dell'applicazione può modificare il valore del parametro pointer in null. Quando il server restituisce successivamente il valore null al client, la memoria a cui fa riferimento il puntatore prima della chiamata di procedura remota è ancora presente sul lato client, ma non è più accessibile da tale puntatore, tranne nel caso di un puntatore completo con alias. Questa memoria è detta *orfana*. Questa operazione è stata definita anche *perdita di memoria*. La memoria orfana ripetuta sul client causa l'esaurimento delle risorse di memoria disponibili da parte del client.

La memoria può anche essere orfana ogni volta che il server modifica un puntatore incorporato a un valore null. Se, ad esempio, il parametro punta a una struttura di dati complessa, ad esempio un albero, il lato server dell'applicazione può eliminare i nodi dell'albero e impostare i puntatori nell'albero su null.

Un'altra situazione che può causare una perdita di memoria comporta matrici conformi, variabili e aperte contenenti puntatori. Quando l'applicazione server modifica il parametro che specifica la dimensione della matrice o l'intervallo trasmesso in modo che rappresenti un valore più piccolo, gli stub utilizzano i valori più piccoli per liberare memoria. Gli elementi della matrice con indici di dimensioni superiori al parametro size sono orfani. L'applicazione deve liberare elementi al di fuori dell'intervallo trasmesso.

 

 