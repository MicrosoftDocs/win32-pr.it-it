---
title: Modifica di set di impostazioni
description: Modifica di set di impostazioni
ms.assetid: f8a5565d-676b-4679-a4cb-4bd7551cf41c
keywords:
- Visualizzazioni, esempio Glow
- Visualizzazioni personalizzate, esempio Glow
- Guida per programmatori, visualizzazioni
- esempi, visualizzazione bagliore
- Esempio di visualizzazione bagliore
- Visualizzazioni, set di impostazioni
- Visualizzazioni personalizzate, set di impostazioni
- impostazioni predefinite nelle visualizzazioni, esempio Glow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d24841c95c3fc1029aa0c405e90b329799fdbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298199"
---
# <a name="changing-presets"></a>Modifica di set di impostazioni

Le sezioni di codice del set di impostazioni seguenti sono state modificate per consentire tre set di impostazioni:

## <a name="getpresettitle"></a>GetPresetTitle

Questo codice è stato inserito al posto del codice del set di impostazioni generato:


```C++
    switch (nPreset)
    {
    case PRESET_RED:
        bstrTemp.LoadString(IDS_REDPRESETNAME); 
        break;

    case PRESET_GREEN:
        bstrTemp.LoadString(IDS_GREENPRESETNAME); 
        break;

    case PRESET_BLUE:
        bstrTemp.LoadString(IDS_BLUEPRESETNAME); 
        break;
    }

```



## <a name="enumerations"></a>Enumerazioni

L'enumerazione seguente in Glow. h è stata modificata in modo da consentire tre set di impostazioni:


```C++
enum {
    PRESET_RED = 0,
    PRESET_GREEN,
    PRESET_BLUE,
    PRESET_COUNT
};

```



## <a name="resource-header"></a>Intestazione della risorsa

Le risorse seguenti sono state definite in Resource. h per consentire tre set di impostazioni:


```C++
#define IDS_REDPRESETNAME               102
#define IDS_GREENPRESETNAME             103
#define IDS_BLUEPRESETNAME              104

```



Si noti che è necessario modificare anche il numero di risorsa del **\_ \_ \_ \_ valore SYMED successivo di APS** in 106.

## <a name="resource-file"></a>File di risorse

È necessario modificare le seguenti stringhe nel file Glowdll. RC per consentire tre set di impostazioni e assegnare loro i nomi:


```C++
    IDS_REDPRESETNAME       "Glow Red"
    IDS_GREENPRESETNAME     "Glow Green"
    IDS_BLUEPRESETNAME      "Glow Blue"

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempio Glow**](the-glow-sample.md)
</dt> </dl>

 

 




