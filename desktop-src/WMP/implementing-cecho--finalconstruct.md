---
title: Implementazione di CEcho FinalConstruct
description: Implementazione di CEcho FinalConstruct
ms.assetid: 149e99c5-9f57-4447-b520-39a6dd39fc86
keywords:
- Windows Media Player plug-in, pagine delle proprietà di esempio Echo
- plug-in, pagine delle proprietà di esempio Echo
- plug-in di elaborazione del segnale digitale, pagine delle proprietà di esempio Echo
- Plug-in DSP, pagine delle proprietà di esempio Echo
- Esempio di plug-in Echo DSP, pagine delle proprietà
- Esempio di plug-in Echo DSP, metodo CEcho FinalConstruct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbeceeb9c0a7622ada62e98000ad4bfbc2e3faf08c22439039160810771cde8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748146"
---
# <a name="implementing-cechofinalconstruct"></a>Implementazione di CEcho::FinalConstruct

Il metodo CEcho::FinalConstruct viene implementato in Echo.cpp. Contiene il codice per leggere i valori delle proprietà dal Registro di sistema quando Windows Media Player crea un'istanza dell'oggetto plug-in DSP. Questo è importante perché consente di mantenere le impostazioni utente tra istanze dell'oggetto e tra sessioni. Il codice di esempio della procedura guidata plug-in fornisce l'implementazione per leggere una singola proprietà dal Registro di sistema. È possibile modificare questo codice per gestire la proprietà delay time e quindi aggiungere codice per leggere il valore della proprietà wet mix.

Il codice di esempio seguente legge ogni valore della proprietà dal Registro di sistema e li archivia nella variabile membro corretta:


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



Si noti che il valore DWORD per la combinazione wet viene convertito in un valore a virgola mobile. Si noti anche che il codice calcola il valore corretto per m \_ fDryMix.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Modifica della pagina delle proprietà Echo Sample**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




