---
title: Modifica dei set di impostazioni
description: Modifica dei set di impostazioni
ms.assetid: f8a5565d-676b-4679-a4cb-4bd7551cf41c
keywords:
- visualizzazioni,Esempio di alone
- visualizzazioni personalizzate,Esempio di alone
- guida alla programmazione, visualizzazioni
- esempi, visualizzazione Alone
- Esempio di visualizzazione alone
- visualizzazioni, set di impostazioni
- visualizzazioni personalizzate, set di impostazioni
- set di impostazioni nelle visualizzazioni,Esempio di alone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03828614093836c5f9a3b422167b62f11b8f2489eb30556d42a2d80495935ec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863911"
---
# <a name="changing-presets"></a>Modifica dei set di impostazioni

Le sezioni di codice predefinite seguenti sono state modificate per consentire tre set di impostazioni:

## <a name="getpresettitle"></a>GetPresetTitle

Questo codice è stato inserito al posto del codice predefinito generato:


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

L'enumerazione seguente in Alone.h è stata modificata per consentire tre set di impostazioni:


```C++
enum {
    PRESET_RED = 0,
    PRESET_GREEN,
    PRESET_BLUE,
    PRESET_COUNT
};

```



## <a name="resource-header"></a>Intestazione della risorsa

Le risorse seguenti sono state definite in Resource.h per consentire tre set di impostazioni:


```C++
#define IDS_REDPRESETNAME               102
#define IDS_GREENPRESETNAME             103
#define IDS_BLUEPRESETNAME              104

```



Si noti che è anche necessario modificare il numero di **\_ risorsa piattaforma di strumenti analitici NEXT \_ \_ SYMED \_ VALUE** in 106.

## <a name="resource-file"></a>File di risorse

Le stringhe seguenti devono essere modificate nel file Alonedll.rc per consentire tre set di impostazioni e assegnare loro i nomi:


```C++
    IDS_REDPRESETNAME       "Glow Red"
    IDS_GREENPRESETNAME     "Glow Green"
    IDS_BLUEPRESETNAME      "Glow Blue"

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempio di alone**](the-glow-sample.md)
</dt> </dl>

 

 




