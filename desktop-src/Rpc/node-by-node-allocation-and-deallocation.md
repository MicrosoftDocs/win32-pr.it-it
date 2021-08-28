---
title: Allocazione e deallocazione nodo per nodo
description: L'allocazione nodo per nodo e la deallocazione delle strutture di dati da parte degli stub è il metodo predefinito di gestione della memoria per tutti i parametri sia nel client che nel server.
ms.assetid: 04752fd9-438c-4b52-830b-ce136f83b3b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52aea7c2e95615af8549c1f66476e1a105b91abd68dd31089db9cf23d8ec2af3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927840"
---
# <a name="node-by-node-allocation-and-deallocation"></a>Allocazione e deallocazione nodo per nodo

L'allocazione nodo per nodo e la deallocazione delle strutture di dati da parte degli stub è il metodo predefinito di gestione della memoria per tutti i parametri sia nel client che nel server. Sul lato client, lo stub alloca ogni nodo con una chiamata separata [all'utente midl \_ \_ allocare](/windows/desktop/Midl/midl-user-allocate-1). Sul lato server, anziché chiamare **midl \_ user \_ allocate,** la memoria privata viene usata quando possibile. Se **viene chiamato midl user \_ \_ allocate,** gli stub del server chiameranno **l'utente midl \_ \_ gratuito** per liberare i dati. Nella maggior parte dei casi, l'uso dell'allocazione e della deallocazione nodo per nodo anziché dell'allocazione (tutti i **\[ \_ nodi) \]** comporta un aumento delle prestazioni degli stub sul lato server.

 

 