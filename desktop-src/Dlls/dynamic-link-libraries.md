---
description: Una libreria a collegamento dinamico (DLL) è un modulo che contiene funzioni e dati che possono essere usati da un altro modulo (applicazione o DLL).
ms.assetid: 09e35b46-86a1-44ed-ab6d-207857b2605c
title: Dynamic-Link librerie (librerie a collegamento dinamico)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369091464aad63ea78ea9f24a84fb4eb49eb810a1faff14571fc67e2e39bb0fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815900"
---
# <a name="dynamic-link-libraries-dynamic-link-libraries"></a>Dynamic-Link librerie (librerie a collegamento dinamico)

Una *libreria a collegamento dinamico* (DLL) è un modulo che contiene funzioni e dati che possono essere usati da un altro modulo (applicazione o DLL).

Una DLL può definire due tipi di funzioni: esportata e interna. Le funzioni esportate devono essere chiamate da altri moduli, nonché dall'interno della DLL in cui sono definite. Le funzioni interne sono in genere destinate a essere chiamate solo dall'interno della DLL in cui sono definite. Anche se una DLL può esportare dati, i relativi dati vengono in genere usati solo dalle relative funzioni. Tuttavia, non c'è nulla per impedire a un altro modulo di leggere o scrivere tale indirizzo.

Le DLL consentono di modularizzare le applicazioni in modo che le relative funzionalità possano essere aggiornate e riutilizzate più facilmente. Le DLL consentono anche di ridurre l'overhead di memoria quando più applicazioni usano la stessa funzionalità contemporaneamente, perché anche se ogni applicazione riceve una propria copia dei dati DLL, le applicazioni condividono il codice DLL.

La Windows API (Application Programming Interface) viene implementata come set di DLL, pertanto qualsiasi processo che usa l'API Windows usa il collegamento dinamico.

-   [Informazioni Dynamic-Link librerie](about-dynamic-link-libraries.md)
-   [Uso Dynamic-Link librerie](using-dynamic-link-libraries.md)
-   [Informazioni di riferimento sulla libreria a collegamento dinamico](dynamic-link-library-reference.md)

> [!Note]  
> Se un utente riscontra difficoltà con una DLL nel computer, è necessario contattare il supporto tecnico del fornitore del software che pubblica la DLL. Se si ha bisogno di supporto per un prodotto Microsoft (incluso Windows), visitare il sito del supporto tecnico [all'indirizzo support.microsoft.com](https://support.microsoft.com).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DLL (Visual C++)](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
