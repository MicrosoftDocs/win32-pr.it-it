---
title: Implementazione di CEchoPropPage Apply
description: Implementazione di CEchoPropPage Apply
ms.assetid: e887b851-e623-4ec4-8d8b-165e4b21e116
keywords:
- Windows Media Player plug-in, pagine delle proprietà di esempio Echo
- plug-in, pagine delle proprietà di esempio Echo
- plug-in di elaborazione del segnale digitale,pagine delle proprietà di esempio Echo
- Plug-in DSP, pagine delle proprietà di esempio Echo
- Esempio di plug-in Echo DSP, pagine delle proprietà
- Esempio di plug-in Echo DSP, metodo Apply CEchoPropPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a53d05bee90908f766034c300c99bcfa8d529b06e6713c803bd99bcf042b579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135624"
---
# <a name="implementing-cechoproppageapply"></a>Implementazione di CEchoPropPage::Apply

Il metodo CEchoPropPage::Apply viene implementato in EchoPropPage.cpp. Viene eseguito quando l'utente fa clic **su Applica** nella finestra di dialogo della pagina delle proprietà Windows Media Player. Il codice di esempio della procedura guidata plug-in fornisce un'implementazione per gestire una singola proprietà. È possibile modificare questo codice per una delle proprietà di esempio Echo e quindi aggiungere codice per archiviare l'altro valore della proprietà.

## <a name="declaring-the-apply-method-variables"></a>Dichiarazione delle variabili del metodo Apply

Prima di tutto, è necessario rimuovere la dichiarazione di fScaleFactor. Aggiungere quindi le dichiarazioni di variabile necessarie. L'esempio seguente illustra le dichiarazioni di variabili completate:


```
TCHAR   szStr[MAXSTRING] = { 0 };
DWORD   dwDelayTime = 1000;  // Initialize the delay time.
DWORD   dwWetmix = 50;       // Initialize a DWORD for effect level.
double  fWetmix = 0.50;      // Initialize a double for effect level.
```



## <a name="retrieving-the-values-from-the-property-page"></a>Recupero dei valori dalla pagina delle proprietà

È necessario implementare il codice per recuperare e convalidare l'input dell'utente. L'esempio di codice seguente recupera il valore del tempo di ritardo dalla casella di modifica IDC DELAYTIME e quindi verifica che il valore sia compreso \_ in un intervallo specificato:


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



Se l'input dell'utente non è compreso nell'intervallo specificato, nel codice viene visualizzata una finestra di messaggio. Si noti l'uso della risorsa stringa creata in precedenza per il messaggio di errore.

L'esempio seguente recupera il livello di effetto dalla casella di modifica IDC WETMIX e quindi verifica che il valore sia compreso \_ in un intervallo specificato:


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



## <a name="storing-the-property-values-in-the-registry"></a>Archiviazione dei valori delle proprietà nel Registro di sistema

Successivamente, il codice deve rendere persistenti i nuovi valori delle proprietà nel Registro di sistema. Il codice seguente archivia entrambi i valori delle proprietà:


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

Il **metodo Apply** deve informare il plug-in Echo che i valori delle proprietà sono stati modificati. Il codice seguente chiama il metodo property put per ogni proprietà usando il puntatore a interfaccia recuperato in CEchoPropPage::SetObjects:


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



Si noti che il valore della combinazione di umidità viene convertito in virgola mobile prima di essere passato al plug-in.

## <a name="disabling-the-apply-button"></a>Disabilitazione del pulsante Applica

Come passaggio finale, il codice deve disabilitare Applica nella finestra di dialogo della pagina delle proprietà come segnale all'utente che i valori sono stati aggiornati correttamente. Questa operazione richiede la singola riga di codice seguente:


```
m_bDirty = FALSE; // Tell the property page to disable Apply.
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Modifica della pagina delle proprietà Echo Sample**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




