---
title: Matrici e puntatori
description: Remote Procedure Call (RPC) è progettato per essere perlopiù trasparente per gli sviluppatori.
ms.assetid: 5ad5a51d-a821-44a5-bbc3-14409cb42cb4
keywords:
- RPC, descrizione, matrici e puntatori di RPC (Remote Procedure Call)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb6bc3f4a2ec4af85156bf15160b0ce7d1efc33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711335"
---
# <a name="arrays-and-pointers"></a>Matrici e puntatori

Remote Procedure Call (RPC) è progettato per essere perlopiù trasparente per gli sviluppatori. Per ottenere questa trasparenza, lo stub del client trasmette al server sia il puntatore che l'oggetto dati a cui punta. Se la procedura remota modifica i dati, il server deve trasmettere nuovamente i nuovi dati al client, in modo che il client possa copiare i nuovi dati sui dati originali.

In generale, una chiamata di procedura remota si comporta esattamente come una chiamata di procedura locale. Ovvero, quando un puntatore è un parametro, la procedura remota può accedere all'oggetto dati a cui fa riferimento il puntatore in modo analogo a una procedura locale.

Poiché i programmi client e server vengono eseguiti in spazi di indirizzi diversi, gli sviluppatori devono usare gli attributi Microsoft Interface Definition Language (MIDL) per descrivere il modo in cui i dati della matrice e del puntatore vengono trasmessi tra il client e il server. In questa sezione viene presentata una panoramica sull'utilizzo di matrici e puntatori nelle applicazioni distribuite negli argomenti seguenti:

-   [Matrici e RPC](arrays-and-rpc.md)
-   [Puntatori e RPC](pointers-and-rpc.md)
-   [Utilizzo di matrici, stringhe e puntatori](using-arrays-strings-and-pointers.md)

 

 




