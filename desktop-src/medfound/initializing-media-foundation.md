---
description: Inizializzazione di Media Foundation
ms.assetid: e4db81d3-7a9e-47d7-8611-6dac8026259c
title: Inizializzazione di Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb876ec3493d6c4fac1c2f6d6757ef647c511a98
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320753"
---
# <a name="initializing-media-foundation"></a>Inizializzazione di Media Foundation

Prima di usare oggetti o interfacce di Microsoft Media Foundation, è necessario chiamare la funzione [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) . Passare la costante **MF \_ Version**.


```C++
    hr = MFStartup(MF_VERSION);
```



La funzione [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) Inizializza la piattaforma Media Foundation. Se **MFStartup** restituisce la \_ versione MF E \_ Bad \_ Startup \_ , significa che l'applicazione è stata compilata utilizzando una versione delle intestazioni Media Foundation che non corrispondono alle dll Media Foundation nel sistema.

Per ogni chiamata a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup), l'applicazione deve chiamare [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).


```C++
MFShutdown();
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Architettura di Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[API della piattaforma Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 



