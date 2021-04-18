---
title: Implementazione di CEchoPropPage OnInitDialog
description: Implementazione di CEchoPropPage OnInitDialog
ms.assetid: 568989b0-bc07-480f-8b5c-41bbada713f8
keywords:
- Plug-in di Windows Media Player, pagine delle proprietà di esempio Echo
- plug-in, pagine delle proprietà di esempio Echo
- plug-in di elaborazione dei segnali digitali, pagine delle proprietà di esempio Echo
- Plug-in DSP, pagine delle proprietà di esempio Echo
- Esempio di plug-in Echo DSP, pagine delle proprietà
- Esempio di plug-in Echo DSP, metodo CEchoPropPage OnInitDialog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0874c750914b5caecf86ffa61a0c42d38bb1c02e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297963"
---
# <a name="implementing-cechoproppageoninitdialog"></a>Implementazione di CEchoPropPage:: OnInitDialog

Il metodo **CEchoPropPage:: OnInitDialog** è implementato in EchoPropPage. cpp. Viene eseguito quando viene richiamata la finestra di dialogo della pagina delle proprietà. Il codice in questo metodo deve recuperare i valori correnti della proprietà e visualizzarli nella casella di modifica corretta. Il codice di esempio della procedura guidata plug-in fornisce un'implementazione per una singola proprietà. È possibile modificare questo codice per una delle proprietà di esempio Echo, quindi aggiungere il codice per recuperare il secondo valore della proprietà.

## <a name="declaring-the-oninitdialog-method-variables"></a>Dichiarazione delle variabili del metodo OnInitDialog

Prima di tutto, è necessario rimuovere la dichiarazione di fScaleFactor e sostituirla con le seguenti dichiarazioni di variabili:


```
DWORD  dwDelayTime = 1000;    // Default delay time.
DWORD  dwWetmix = 50;         // Default wet mix DWORD.
double fWetmix =  0.50;       // Default wet mix double.
```



## <a name="retrieving-the-current-values-from-the-plug-in"></a>Recupero dei valori correnti dal plug-in

Il codice deve tentare di recuperare i valori correnti della proprietà dal plug-in Echo. Nell'esempio seguente viene eseguito un tentativo di recupero di ogni proprietà:


```
if (m_spEcho)
{
    m_spEcho->get_delay(&dwDelayTime);
    m_spEcho->get_wetmix(&fWetmix);
    // Convert wet mix from double to DWORD.
    dwWetmix = (DWORD)(fWetmix * 100);
}
```



Nella finestra di dialogo viene visualizzato il valore del livello effetti all'utente come intero, ma il plug-in archivia il valore come numero a virgola mobile. Pertanto, il codice converte il valore a virgola mobile in un valore **DWORD** .

## <a name="retrieving-the-current-values-from-the-registry"></a>Recupero dei valori correnti dal registro di sistema

Se la pagina delle proprietà non è in grado di recuperare i valori correnti dal plug-in, è necessario tentarne la lettura dal registro di sistema. Il codice seguente legge ogni valore di proprietà:


```
else // Otherwise, read values from registry
{
    CRegKey key;
    LONG    lResult;

    lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
    if (ERROR_SUCCESS == lResult)
    {
        DWORD   dwValue = 0;

        // Read the delay time.
        lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
        if (ERROR_SUCCESS == lResult)
        {
            dwDelayTime = dwValue;
        }

        // Read the wet mix value.
        lResult = key.QueryValue(dwValue, kszPrefsWetmix );
        if (ERROR_SUCCESS == lResult)
        {
            dwWetmix = dwValue;
        }
    }
}
```



Si noti l'uso delle costanti del registro di sistema create in precedenza.

## <a name="displaying-the-values-to-the-user"></a>Visualizzazione dei valori all'utente

Infine, la pagina delle proprietà deve visualizzare i valori nei controlli corretti della casella di modifica. Nell'esempio di codice seguente viene illustrato quanto segue:


```
 TCHAR   szStr[MAXSTRING];

// Display the delay time.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwDelayTime);
SetDlgItemText(IDC_DELAYTIME, szStr);

// Display the effect level.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwWetmix);
SetDlgItemText(IDC_WETMIX, szStr);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Modifica della pagina delle proprietà di esempio Echo**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




