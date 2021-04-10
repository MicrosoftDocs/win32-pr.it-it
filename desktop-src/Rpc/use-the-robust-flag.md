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
# <a name="use-the-robust-flag"></a>Usare il flag/robust

Compilare sempre i file con estensione IDL utilizzando l'opzione [**/robust**](/windows/desktop/Midl/-robust) . L'utilizzo dell'opzione **/robust** genera informazioni aggiuntive che consentono al motore di rappresentazione dei dati di rete (NDR) di eseguire il controllo degli errori di run-time sugli argomenti correlati in matrici dinamiche, unioni e puntatori di interfaccia in uscita nelle applicazioni com e RPC. Se il software non riesce a eseguire la compilazione con questo flag, il software viene esposto agli attacchi che non possono essere protetti da nessun'altra area.

 

 