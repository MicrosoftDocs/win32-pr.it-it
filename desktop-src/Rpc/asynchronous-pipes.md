---
title: Pipe asincrone
description: L'utilizzo di parametri pipe con RPC asincrono consente di trasmettere i dati in modo incrementale, così come diventano disponibili, senza vincolare il client e il server.
ms.assetid: e5c466b8-c0b0-4fa8-8867-d0715fd614b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be9d6dd5a3e8de7d5c4ad233a577187a49d04ed8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729431"
---
# <a name="asynchronous-pipes"></a>Pipe asincrone

L'utilizzo di parametri [pipe](/windows/desktop/Midl/pipe) con RPC asincrono consente di trasmettere i dati in modo incrementale, così come diventano disponibili, senza vincolare il client e il server. Questa operazione è particolarmente utile quando si dispone di una grande quantità di dati da trasferire, combinati con un client lento, un server lento o una rete lenta. Se si usa una pipe in una chiamata di funzione asincrona, è, per definizione, una pipe asincrona. Le pipe sincrone non sono supportate insieme alle funzioni asincrone.

Diversamente dalle pipe convenzionali (sincrone), in cui il server gestisce tutti i dettagli relativi all'invio e alla ricezione dei dati della pipe, le pipe asincrone sono simmetriche. Ovvero sia il client che il server possono eseguire il push e il pull dei dati attraverso la pipe.

> [!Note]  
> I parametri pipe possono essere passati solo per riferimento. Anche se il file IDL Mostra i parametri della [pipe](/windows/desktop/Midl/pipe) passati per valore, gli stub generati accetteranno parametri pipe solo per riferimento.

 

Nella discussione seguente sulle pipe asincrone si presuppone una certa familiarità con il costruttore del tipo di pipe. Per ulteriori informazioni sulle procedure di pipe descritte in questi argomenti, vedere [pipe](pipes.md).

 

 