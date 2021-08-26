---
title: Matrici e puntatori
description: Rpc (Remote Procedure Call) è progettato per essere principalmente trasparente per gli sviluppatori.
ms.assetid: 5ad5a51d-a821-44a5-bbc3-14409cb42cb4
keywords:
- Chiamata di procedura remota RPC , descritto, matrici e puntatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26cc588d4db7cb222ec0fb2689bf645a2a7ed0e12b632392264d480c26777531
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073501"
---
# <a name="arrays-and-pointers"></a>Matrici e puntatori

Rpc (Remote Procedure Call) è progettato per essere principalmente trasparente per gli sviluppatori. Per ottenere questa trasparenza, lo stub client trasmette al server sia il puntatore che l'oggetto dati a cui punta. Se la procedura remota modifica i dati, il server deve trasmettere i nuovi dati al client in modo che il client possa copiare i nuovi dati sui dati originali.

In generale, una chiamata di procedura remota si comporta esattamente come una chiamata di procedura locale. In altri modi, quando un puntatore è un parametro, la procedura remota può accedere all'oggetto dati a cui fa riferimento il puntatore nello stesso modo possibile per una routine locale.

Poiché i programmi client e server vengono eseguiti in spazi di indirizzi diversi, gli sviluppatori devono usare gli attributi di Microsoft Interface Definition Language (MIDL) per descrivere la modalità di trasmissione dei dati di matrice e puntatore tra il client e il server. Questa sezione presenta una panoramica dell'uso di matrici e puntatori nelle applicazioni distribuite, negli argomenti seguenti:

-   [Matrici e RPC](arrays-and-rpc.md)
-   [Puntatori e RPC](pointers-and-rpc.md)
-   [Uso di matrici, stringhe e puntatori](using-arrays-strings-and-pointers.md)

 

 




