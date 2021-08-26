---
title: Pipe asincrone
description: L'uso di parametri pipe con RPC asincrono consente di trasmettere i dati in modo incrementale, non appena disponibili, senza creare connessioni tra client e server.
ms.assetid: e5c466b8-c0b0-4fa8-8867-d0715fd614b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0957b1ddc381d2a91b77033842b2807ed8a9dd34718d0148d6853083229d408d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023791"
---
# <a name="asynchronous-pipes"></a>Pipe asincrone

[L'uso](/windows/desktop/Midl/pipe) di parametri pipe con RPC asincrono consente di trasmettere i dati in modo incrementale, non appena disponibili, senza creare connessioni tra client e server. Ciò è particolarmente utile quando si dispone di una grande quantità di dati da trasferire, combinati con un client lento, un server lento o una rete lenta. Se si usa una pipe in una chiamata di funzione asincrona, si tratta, per definizione, di una pipe asincrona. Le pipe sincrone non sono supportate insieme alle funzioni asincrone.

A differenza delle pipe convenzionali (sincrone), in cui il server gestisce tutti i dettagli dell'invio e della ricezione dei dati della pipe, le pipe asincrone sono simmetriche. In altri casi, sia il client che il server possono eseguire il push e il pull dei dati attraverso la pipe.

> [!Note]  
> I parametri della pipe possono essere passati solo per riferimento. Anche se il file IDL mostra che i parametri [della pipe](/windows/desktop/Midl/pipe) vengono passati per valore, gli stub generati accetteranno i parametri della pipe solo per riferimento.

 

Nella discussione seguente sulle pipe asincrone si presuppone la familiarità con il costruttore del tipo di pipe. Per altre informazioni sulle procedure di pipe descritte in questi argomenti, vedere [Pipe .](pipes.md)

 

 