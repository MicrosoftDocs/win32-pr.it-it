---
title: Usare il flag/robust
description: Compilare sempre i file con estensione IDL utilizzando l'opzione/robust.
ms.assetid: bb2fd026-3ad8-4bb5-b05e-4835b874882f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db395841842331d9297a782fdcd8ea7573139f9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963222"
---
# <a name="use-the-robust-flag"></a><span data-ttu-id="030b3-103">Usare il flag/robust</span><span class="sxs-lookup"><span data-stu-id="030b3-103">Use the /robust Flag</span></span>

<span data-ttu-id="030b3-104">Compilare sempre i file con estensione IDL utilizzando l'opzione [**/robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="030b3-104">Always compile .idl files using the [**/robust**](/windows/desktop/Midl/-robust) switch.</span></span> <span data-ttu-id="030b3-105">L'utilizzo dell'opzione **/robust** genera informazioni aggiuntive che consentono al motore di rappresentazione dei dati di rete (NDR) di eseguire il controllo degli errori di run-time sugli argomenti correlati in matrici dinamiche, unioni e puntatori di interfaccia in uscita nelle applicazioni com e RPC.</span><span class="sxs-lookup"><span data-stu-id="030b3-105">Using the **/robust** switch generates additional information that enables the Network Data Representation (NDR) engine to perform run-time error checking on correlated arguments in dynamic arrays, unions, and in out interface pointers in COM and RPC applications.</span></span> <span data-ttu-id="030b3-106">Se il software non riesce a eseguire la compilazione con questo flag, il software viene esposto agli attacchi che non possono essere protetti da nessun'altra area.</span><span class="sxs-lookup"><span data-stu-id="030b3-106">If software fails to compile with this flag, the software is so exposed to attacks that no efforts in any other area can protect it.</span></span>

 

 