---
title: Implementazione di CEcho FinalConstruct
description: Implementazione di CEcho FinalConstruct
ms.assetid: 149e99c5-9f57-4447-b520-39a6dd39fc86
keywords:
- Plug-in di Windows Media Player, pagine delle proprietà di esempio Echo
- plug-in, pagine delle proprietà di esempio Echo
- plug-in di elaborazione dei segnali digitali, pagine delle proprietà di esempio Echo
- Plug-in DSP, pagine delle proprietà di esempio Echo
- Esempio di plug-in Echo DSP, pagine delle proprietà
- Esempio di plug-in Echo DSP, metodo CEcho FinalConstruct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876db9f2479644800c42354a041ad3b1909b526b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116805"
---
# <a name="implementing-cechofinalconstruct"></a>Implementazione di CEcho:: FinalConstruct

Il metodo CEcho:: FinalConstruct è implementato in Echo. cpp. Contiene il codice per leggere i valori delle proprietà dal registro di sistema quando Windows Media Player crea un'istanza dell'oggetto plug-in DSP. Si tratta di un aspetto importante perché consente alle impostazioni utente di mantenersi tra le istanze dell'oggetto, nonché tra le sessioni. Il codice di esempio della procedura guidata plug-in fornisce l'implementazione di per leggere una singola proprietà dal registro di sistema. È possibile modificare questo codice per gestire la proprietà tempo di ritardo, quindi aggiungere il codice per leggere il valore della proprietà Wet Mix.

Il codice di esempio seguente legge ogni valore di proprietà dal registro di sistema e li archivia nella variabile membro corretta:


```CSharp
CRegKey key;
LONG    lResult;
DWORD   dwValue;

lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
if (ERROR_SUCCESS == lResult)
{
    // Read the delay time from the registry. 
    lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
    if (ERROR_SUCCESS == lResult)
    {
        m_dwDelayTime = dwValue;
    }

    // Read the wet mix value from the registry. 
    lResult = key.QueryValue(dwValue, kszPrefsWetmix );
    if (ERROR_SUCCESS == lResult)
    {
        // Convert the DWORD to a double.
        m_fWetMix = (double)dwValue / 100;
        // Calculate the dry mix value.
        m_fDryMix = 1.0 - m_fWetMix;
    }

}

return S_OK;
```



Si noti che il valore DWORD per la combinazione Wet viene convertito in un valore a virgola mobile. Si noti anche che il codice calcola il valore corretto per m \_ fDryMix.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Modifica della pagina delle proprietà di esempio Echo**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




