---
title: Implementazione di Client-Side pipe
description: Implementazione della pipe lato client in RPC (Remote Procedure Call).
ms.assetid: d790f859-47a9-4b6c-a218-8cbe05db21b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5666656f1f7296c252395255c17902a91cb32a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856685"
---
# <a name="client-side-pipe-implementation"></a>Implementazione di Client-Side pipe

L'applicazione client deve implementare le seguenti procedure, che lo stub client chiamerà durante il trasferimento dei dati:

-   Procedura pull (per una pipe di input)
-   Procedura push (per una pipe di output)
-   Una procedura di allocazione per l'allocazione di un buffer per i dati di trasferimento

Tutte queste procedure devono usare gli argomenti specificati dal file di intestazione generato da MIDL. Inoltre, l'applicazione client deve avere una variabile di stato per identificare dove individuare o inserire i dati.

La procedura di allocazione può anche essere semplice o complessa se necessario. Ad esempio, può restituire un puntatore allo stesso buffer ogni volta che lo stub chiama la funzione oppure può allocare una quantità di memoria diversa ogni volta. Se i dati sono già nel formato corretto, ad esempio una matrice di elementi pipe, è possibile coordinare la procedura di allocazione con la procedura pull per allocare un buffer che contiene già i dati. In tal caso, la procedura pull potrebbe essere una routine vuota.

L'allocazione del buffer deve essere in byte. Le procedure push e pull, d'altra parte, modificano gli elementi, le cui dimensioni in byte dipendono da come sono state definite.

In questa sezione viene illustrata l'implementazione client dei pipe di input e di output nelle seguenti sezioni:

-   [Implementazione di pipe di input nel client](implementing-input-pipes-on-the-client.md)
-   [Implementazione di pipe di output nel client](implementing-output-pipes-on-the-client.md)

 

 




