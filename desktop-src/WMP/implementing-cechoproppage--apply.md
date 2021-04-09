---
title: Implementazione di CEchoPropPage Apply
description: Implementazione di CEchoPropPage Apply
ms.assetid: e887b851-e623-4ec4-8d8b-165e4b21e116
keywords:
- Plug-in di Windows Media Player, pagine delle proprietà di esempio Echo
- plug-in, pagine delle proprietà di esempio Echo
- plug-in di elaborazione dei segnali digitali, pagine delle proprietà di esempio Echo
- Plug-in DSP, pagine delle proprietà di esempio Echo
- Esempio di plug-in Echo DSP, pagine delle proprietà
- Esempio di plug-in Echo DSP, metodo CEchoPropPage Apply
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bdca8a771d3e3e26923567f25bf7d19e968595e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856314"
---
# <a name="implementing-cechoproppageapply"></a>Implementazione di CEchoPropPage:: Apply

Il metodo CEchoPropPage:: Apply è implementato in EchoPropPage. cpp. Viene eseguito quando l'utente fa clic su **applica** nella finestra di dialogo della pagina delle proprietà di Windows Media Player. Il codice di esempio della procedura guidata plug-in fornisce un'implementazione di per gestire una singola proprietà. È possibile modificare questo codice per una delle proprietà di esempio Echo, quindi aggiungere il codice per archiviare l'altro valore della proprietà.

## <a name="declaring-the-apply-method-variables"></a>Dichiarazione delle variabili del metodo Apply

In primo luogo, è necessario rimuovere la dichiarazione di fScaleFactor. Aggiungere quindi le dichiarazioni di variabili necessarie. Nell'esempio seguente vengono illustrate le dichiarazioni di variabile completate:


```
TCHAR   szStr[MAXSTRING] = { 0 };
DWORD   dwDelayTime = 1000;  // Initialize the delay time.
DWORD   dwWetmix = 50;       // Initialize a DWORD for effect level.
double  fWetmix = 0.50;      // Initialize a double for effect level.
```



## <a name="retrieving-the-values-from-the-property-page"></a>Recupero dei valori dalla pagina delle proprietà

È necessario implementare il codice per recuperare e convalidare l'input dell'utente. L'esempio di codice seguente recupera il valore di tempo di ritardo dalla \_ casella di modifica IDC DELAYTIME, quindi verifica che il valore si trovi all'interno di un intervallo specificato:


```
// Get the delay time value from the dialog box.
GetDlgItemText(IDC_DELAYTIME, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwDelayTime = atoi(szStr);

// Make sure delay time is valid.
if ((dwDelayTime < 10) || (dwDelayTime > 2000))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_DELAYRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



Se l'input dell'utente non è compreso nell'intervallo specificato, il codice visualizza una finestra di messaggio. Si noti l'uso della risorsa di stringa creata in precedenza per il messaggio di errore.

Nell'esempio seguente viene recuperato il livello di effetto dalla \_ casella di modifica IDC WETMIX, quindi viene verificato che il valore si trovi all'interno di un intervallo specificato:


```
// Get the effects level value from the dialog box.
GetDlgItemText(IDC_WETMIX, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwWetmix = atoi(szStr);

// Make sure wet mix value is valid.
if ((dwWetmix < 0) || (dwWetmix > 100))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_MIXRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



## <a name="storing-the-property-values-in-the-registry"></a>Archiviazione dei valori delle proprietà nel registro di sistema

Successivamente, il codice deve salvare i nuovi valori delle proprietà nel registro di sistema. Il codice seguente archivia entrambi i valori delle proprietà:


```
// update the registry
CRegKey key;
LONG    lResult;

// Write the delay time value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwDelayTime , kszPrefsDelayTime );
}

// Write the wet mix value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwWetmix , kszPrefsWetmix );
}
```



## <a name="updating-the-echo-plug-in-property-values"></a>Aggiornamento dei valori delle proprietà del plug-in Echo

Il metodo **Apply** deve informare il plug-in echo che i valori della proprietà sono stati modificati. Il codice seguente chiama il metodo Put della proprietà per ogni proprietà usando il puntatore a interfaccia recuperato in CEchoPropPage:: setpropertys:


```
// update the plug-in
if (m_spEcho)
{
    m_spEcho->put_delay(dwDelayTime);

    // Convert the wet mix value from DWORD to double.
    fWetmix = (double)dwWetmix / 100;
    m_spEcho->put_wetmix(fWetmix);
}
```



Si noti che il valore Wet Mix viene convertito in virgola mobile prima del passaggio al plug-in.

## <a name="disabling-the-apply-button"></a>Disabilitazione del pulsante applica

Come passaggio finale, il codice deve disabilitare applica nella finestra di dialogo della pagina delle proprietà come segnale all'utente che i valori sono stati aggiornati correttamente. Questa operazione richiede la riga di codice seguente:


```
m_bDirty = FALSE; // Tell the property page to disable Apply.
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Modifica della pagina delle proprietà di esempio Echo**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




