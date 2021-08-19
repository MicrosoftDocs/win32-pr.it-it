---
title: Valori restituiti dalla funzione
description: I valori restituiti dalle funzioni sono simili ai parametri \ out\ -only perché i relativi dati non vengono forniti dall'applicazione client.
ms.assetid: 98d8d228-7222-49bf-9f29-7749a7a76d5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525c63422b058da5267003711efa612814907eb91ced353bd78ee78a820a7377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021001"
---
# <a name="function-return-values"></a>Valori restituiti dalla funzione

I valori restituiti dalle funzioni sono simili ai **\[ parametri out \]**-only perché i relativi dati non vengono forniti dall'applicazione client. Tuttavia, vengono gestite in modo diverso. A **\[ differenza dei \]** parametri out -only, non è necessario che siano puntatori. La procedura remota può restituire qualsiasi tipo di dati valido, ad eccezione dei puntatori di riferimento e delle unioni non incapsulate.

È tuttavia consigliabile usare **\[ un parametro out \]** anziché un valore restituito per i tipi di dati complessi. Durante la restituzione di tipi di dati complessi, il compilatore MIDL genererà uno stub in modalità /Os. Di conseguenza, tutte le informazioni recenti sul controllo degli errori fornite da /robust vengono perse.

I valori restituiti dalla funzione che sono tipi puntatore vengono allocati dallo stub client con una chiamata a [midl \_ user \_ allocate](/windows/desktop/Midl/midl-user-allocate-1). Di conseguenza, solo l'attributo del puntatore univoco o completo può essere applicato a un tipo restituito dalla funzione puntatore.

 

 