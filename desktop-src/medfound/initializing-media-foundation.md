---
description: Inizializzazione Media Foundation
ms.assetid: e4db81d3-7a9e-47d7-8611-6dac8026259c
title: Inizializzazione Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 202ab57db5821b252001a723eb8765493eb86362111da5c54e5e16e9fca4219a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268921"
---
# <a name="initializing-media-foundation"></a>Inizializzazione Media Foundation

Prima di usare Microsoft Media Foundation oggetti o interfacce, è necessario chiamare la [**funzione MFStartup.**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) Passare la costante **MF \_ VERSION**.


```C++
    hr = MFStartup(MF_VERSION);
```



La [**funzione MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) inizializza la Media Foundation piattaforma. Se **MFStartup** restituisce MF E BAD STARTUP VERSION, significa che l'applicazione è stata compilata usando una versione delle intestazioni Media Foundation che non corrisponde alle \_ DLL Media Foundation nel \_ \_ \_ sistema.

Per ogni chiamata a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup), l'applicazione deve chiamare [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).


```C++
MFShutdown();
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Architettura di Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[Media Foundation API della piattaforma](media-foundation-platform-apis.md)
</dt> </dl>

 

 



