---
description: Una libreria di collegamento dinamico (DLL) è un modulo che contiene funzioni e dati che possono essere usati da un altro modulo (applicazione o DLL).
ms.assetid: 09e35b46-86a1-44ed-ab6d-207857b2605c
title: Librerie di Dynamic-Link (librerie a collegamento dinamico)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8068cd0b8f1d5431c5638a10350d9a1ae7060aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753783"
---
# <a name="dynamic-link-libraries-dynamic-link-libraries"></a>Librerie di Dynamic-Link (librerie a collegamento dinamico)

Una *libreria di collegamento dinamico* (dll) è un modulo che contiene funzioni e dati che possono essere usati da un altro modulo (applicazione o dll).

Una DLL può definire due tipi di funzioni: esportate e interne. Le funzioni esportate sono progettate per essere chiamate da altri moduli, nonché dall'interno della DLL in cui sono definite. Le funzioni interne sono in genere destinate a essere chiamate solo dall'interno della DLL in cui sono definite. Sebbene una DLL possa esportare dati, i relativi dati vengono in genere utilizzati solo dalle relative funzioni. Tuttavia, non c'è nulla da impedire a un altro modulo di leggere o scrivere tale indirizzo.

Le DLL consentono di modularizzare le applicazioni in modo che le relative funzionalità possano essere aggiornate e riutilizzate più facilmente. Le DLL consentono inoltre di ridurre il sovraccarico della memoria quando più applicazioni utilizzano la stessa funzionalità allo stesso tempo, perché anche se ogni applicazione riceve una copia dei dati DLL, le applicazioni condividono il codice DLL.

Windows Application Programming Interface (API) viene implementato come un set di dll, pertanto qualsiasi processo che utilizza l'API Windows utilizza il collegamento dinamico.

-   [Informazioni sulle librerie Dynamic-Link](about-dynamic-link-libraries.md)
-   [Uso di librerie Dynamic-Link](using-dynamic-link-libraries.md)
-   [Riferimenti alla libreria a collegamento dinamico](dynamic-link-library-reference.md)

> [!Note]  
> Se si riscontrano problemi con una DLL nel computer, è necessario contattare il supporto tecnico per il fornitore del software che pubblica la DLL. Se si ritiene che sia necessario il supporto per un prodotto Microsoft (incluso Windows), visitare il sito del supporto tecnico all'indirizzo [support.Microsoft.com](https://support.microsoft.com).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dll (Visual C++)](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
