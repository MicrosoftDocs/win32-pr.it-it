---
title: Allocazione e deallocazione di nodi per nodo
description: L'allocazione nodo per nodo e la deallocazione di strutture di dati dagli Stub è il metodo predefinito di gestione della memoria per tutti i parametri nel client e nel server.
ms.assetid: 04752fd9-438c-4b52-830b-ce136f83b3b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cc6b3ff61d4db3ba716664a2ff854e94cb28fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473638"
---
# <a name="node-by-node-allocation-and-deallocation"></a>Allocazione e deallocazione di nodi per nodo

L'allocazione nodo per nodo e la deallocazione di strutture di dati dagli Stub è il metodo predefinito di gestione della memoria per tutti i parametri nel client e nel server. Sul lato client lo stub alloca ogni nodo con una chiamata separata a [MIDL \_ User \_ allocate](/windows/desktop/Midl/midl-user-allocate-1). Sul lato server, anziché chiamare **MIDL \_ User \_ allocate**, viene usata la memoria privata quando possibile. Se viene chiamato l' **\_ utente MIDL \_ allocate** , gli stub del server chiameranno l' **\_ utente MIDL \_ gratuitamente** per liberare i dati. Nella maggior parte dei casi, l'utilizzo dell'allocazione e della deallocazione di nodi anziché di **\[ allocare (tutti i \_ nodi) \]** comporterà un miglioramento delle prestazioni degli stub lato server.

 

 