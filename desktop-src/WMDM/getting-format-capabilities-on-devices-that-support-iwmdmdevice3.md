---
title: Ottenere le funzionalità di formattazione tramite IWMDMDevice3
description: Ottenere le funzionalità di formato nei dispositivi che supportano IWMDMDevice3
ms.assetid: a431c3cb-e722-4d68-a82d-385fff067ea6
keywords:
- Windows Media Gestione dispositivi, funzionalità del dispositivo
- Gestione dispositivi, funzionalità del dispositivo
- Guida per programmatori, funzionalità del dispositivo
- applicazioni desktop, funzionalità del dispositivo
- creazione di applicazioni Windows Media Gestione dispositivi, funzionalità del dispositivo
- scrittura di file nei dispositivi, funzionalità del dispositivo
- Metodo IWMDMDevice3
- Windows Media Gestione dispositivi, metodo IWMDMDevice3
- Gestione dispositivi, metodo IWMDMDevice3
- Guida per programmatori, metodo IWMDMDevice3
- applicazioni desktop, metodo IWMDMDevice3
- creazione di applicazioni Windows Media Gestione dispositivi, metodo IWMDMDevice3
- scrittura di file nei dispositivi, metodo IWMDMDevice3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734f674a5fc54aaec0df10d4db613fa067f9b505
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/27/2019
ms.locfileid: "104046158"
---
# <a name="getting-format-capabilities-through-iwmdmdevice3"></a>Ottenere le funzionalità di formattazione tramite IWMDMDevice3

[**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) è il metodo preferito per chiedere a un dispositivo quali formati sono supportati. I passaggi seguenti illustrano come usare questo metodo per eseguire una query su un dispositivo per le funzionalità di formato:

1.  L'applicazione deve determinare quali formati sono supportati da un dispositivo e quali sono di interesse. A tale scopo, l'applicazione può richiedere un elenco di formati supportati dal dispositivo chiamando [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty).
2.  L'applicazione esegue il ciclo di tutti i formati supportati e richiede le funzionalità di formattazione di un dispositivo per un formato specifico, ad esempio WMA o WMV, chiamando **IWMDMDevice3:: GetFormatCapability** e specificando un formato usando l'enumerazione [**WMDM \_ FORMATCODE**](wmdm-formatcode.md) . Questo metodo recupera una struttura di [**\_ \_ funzionalità del formato WMDM**](wmdm-format-capability.md) .
3.  Scorrere in ciclo tutte le strutture di [**\_ \_ configurazione della prop WMDM**](wmdm-prop-config.md) nella struttura della **\_ \_ funzionalità del formato WMDM** recuperato. Ogni struttura di **\_ \_ configurazione di WMDM prop** include un gruppo di proprietà con valori supportati, che rappresentano una configurazione per tale formato. Ogni configurazione ha un numero di preferenza, dove un numero inferiore indica una preferenza maggiore da parte del dispositivo.
4.  Eseguire il ciclo di tutte le strutture [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md) nella **\_ \_ configurazione di WMDM prop** recuperata. Ogni **WMDM \_ prop \_ desc** contiene un elenco di coppie proprietà/valore supportate.
5.  Recuperare i nomi e i valori delle proprietà dalla struttura **WMDM \_ prop \_ desc** . Le proprietà includono velocità in bit, codec e dimensioni del frame. I nomi delle proprietà vengono definiti nel file di intestazione mswmdm. h; un elenco della maggior parte di queste costanti viene specificato nelle [costanti dei metadati](metadata-constants.md). Sono possibili tre tipi di valori di proprietà:
    -   Un singolo valore, WMDM \_ enum \_ prop \_ valid \_ Values \_ any, che indica il supporto per qualsiasi valore per questa proprietà.
    -   Intervallo di valori, definito da un valore massimo, da un valore minimo e da un intervallo.
    -   Elenco di valori discreti.
6.  Cancellare i valori archiviati. La memoria per questi valori viene allocata da Windows Media Gestione dispositivi; il dispositivo è responsabile della liberazione della memoria. Questa procedura è descritta alla fine di questo argomento.

Quando si risponde a **GetFormatCapability**, un dispositivo può segnalare \_ \_ i valori validi di WMDM enum Prop \_ \_ \_ any per la **funzionalità di \_ formato WMDM \_ . \_configurazione della prop WMDM \_ . WMDM \_ prop \_ desc. ValidValuesForm** per richiedere il supporto per qualsiasi valore per la velocità in bit, i canali e così via. Tuttavia, è consigliabile considerare questa richiesta con cautela, perché i dispositivi possono a volte segnalare il supporto per qualsiasi valore quando in realtà non supportano tutte le velocità in bit o le dimensioni delle immagini. Si può prendere in considerazione la possibilità di eseguire la transcodifica di file di grandi dimensioni o a velocità elevata in un'applicazione a versioni più piccole o con un numero minore di versioni con utilizzo intensivo di memoria e CPU durante l'invio ai dispositivi destinati a riprodurre questi file.

La seguente funzione C++ Mostra come richiedere il supporto del formato del dispositivo per un formato specifico.


```C++
HRESULT GetFormatCaps(WMDM_FORMATCODE formatCode, IWMDMDevice3* pDevice)
{
    HRESULT hr = S_OK;

    // Get a list of supported configurations for the format.
    WMDM_FORMAT_CAPABILITY formatCapList;
    hr = pDevice->GetFormatCapability(formatCode, &formatCapList);
    if (FAILED(hr)) return E_FAIL;

    // TODO: Display the format name.
    // Loop through the configurations and examine each one.
    for (UINT iConfig = 0; iConfig < formatCapList.nPropConfig; iConfig++)
    {
        WMDM_PROP_CONFIG formatConfig = formatCapList.pConfigs[iConfig];

        // Preference level for this configuration (lower number means more preferred).
        // TODO: Display the preference level for this format configuration.

        // Loop through all properties for this configuration and get supported
        // values for the property. Values can be a single value, a range, 
        // or a list of enumerated values.
        for (UINT iDesc = 0; iDesc < formatConfig.nPropDesc; iDesc++)
        {
            WMDM_PROP_DESC propDesc = formatConfig.pPropDesc[iDesc];
            // TODO: Display the property name.

            // Three ways a value can be represented: any, a range, or a list.
            switch (propDesc.ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // TODO: Display a message indicating that all values are valid.
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    {
                        // List these in the docs as the propvariants set.
                        WMDM_PROP_VALUES_RANGE rng = 
                            propDesc.ValidValues.ValidValuesRange;
                        // TODO: Display the min, max, and step values.
                    }
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    {
                        // TODO: Display a banner for the list of valid values.
                        WMDM_PROP_VALUES_ENUM list = propDesc.ValidValues.EnumeratedValidValues;
                        PROPVARIANT pVal;
                        for (UINT iValue = 0; iValue < list.cEnumValues; iValue++)
                        {
                            pVal = list.pValues[iValue];
                            // TODO: Display each valid value.
                            PropVariantClear(&pVal);
                            PropVariantInit(&pVal);
                        }
                    }

                    break;
                default:
                    return E_FAIL,
                    break;
            }
        }
    }
    // Now clear the memory used by WMDM_FORMAT_CAPABILITY.
    FreeFormatCapability(formatCapList);
    return hr;
}
```



**Cancellazione della memoria allocata**

Dopo aver recuperato le funzionalità di formato da un dispositivo, l'applicazione deve liberare la memoria allocata per la descrizione. [**GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) e [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) hanno matrici di strutture semplici che possono essere cancellate semplicemente chiamando **CoTaskMemFree** con la matrice. Tuttavia, **GetFormatCapability** dispone di una struttura di dati più complessa con la memoria allocata in modo dinamico che deve essere cancellata mediante il ciclo di tutti gli elementi e la loro liberazione singolarmente.

Nel codice C++ riportato di seguito viene illustrato come un'applicazione può liberare la memoria allocata per una struttura di **\_ \_ funzionalità del formato WMDM** .


```C++
void CWMDMController::FreeFormatCapability(WMDM_FORMAT_CAPABILITY formatCap)
{
    // Loop through all configurations.
    for (UINT i = 0; i < formatCap.nPropConfig; i++) 
    {
        // Loop through all descriptions of a configuration and delete
        // the values particular to that description type.
        for (UINT j=0; j < formatCap.pConfigs[i].nPropDesc; j++) 
        {
            switch (formatCap.pConfigs[i].pPropDesc[j].ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    for (UINT k=0; k < formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.cEnumValues; k++)
                    {
                        PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues[k]));
                    }
                    CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues);
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMin));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMax));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeStep));
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // No dynamically allocated memory for this value.
                default:
                    break;
            }

            // Free the memory for the description name.
            CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].pwszPropName);
        }
        // Free the memory holding the array of description items for this configuration.
        CoTaskMemFree(formatCap.pConfigs[i].pPropDesc);
    }

    // Free the memory pointing to the array of configurations.
    CoTaskMemFree(formatCap.pConfigs);
    formatCap.nPropConfig = 0;
}
```



**Esecuzione di query per tutti i formati supportati**

In genere, un'applicazione esegue una query su un dispositivo per un formato specifico, perché è interessato all'invio di un file specifico al dispositivo. Tuttavia, se si desidera eseguire una query su un'applicazione per tutti i formati supportati, è possibile chiamare [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) e passare g \_ wszWMDMFormatsSupported per recuperare un elenco completo.

Se un dispositivo restituisce solo un elemento, WMDM \_ FORMATCODE \_ undefined, significa che il dispositivo non supporta i codici di formato. La chiamata di **GetFormatCapability** con WMDM \_ FORMATCODE \_ non definita potrebbe recuperare le funzionalità, ma queste proprietà potrebbero essere piuttosto generiche, ad esempio nome, dimensioni del file, data dell'Ultima modifica e così via.

Nei passaggi seguenti viene illustrato come eseguire una query per un elenco di tutti i formati supportati:

1.  Richiedere un elenco di tutti i codici di formato supportati chiamando **IWMDMDevice3:: GetProperty** e passando g \_ wszWMDMFormatsSupported. Restituisce un **PROPVARIANT** contenente un **SAFEARRAY** di formati supportati.
2.  Eseguire il ciclo degli elementi chiamando **SafeArrayGetElement**. Ogni elemento è un'enumerazione **WMDM \_ FORMATCODE** .
3.  Richiedere le funzionalità per ogni formato, liberando la memoria per ogni elemento di **\_ \_ capacità del formato WMDM** , una volta completata.
4.  Cancellare il **PROPVARIANT** recuperato nel passaggio 1 chiamando **PropVariantClear**.

Il codice di esempio C++ seguente recupera un elenco di formati supportati per un dispositivo.


```C++
// Query a device for supported configurations for each media or format type. 
HRESULT CWMDMController::GetCaps(IWMDMDevice3* pDevice)
{
    HRESULT hr = S_OK;

    // Request the "formats supported" property to get a list of supported formats.
    PROPVARIANT pvFormatsSupported;
    PropVariantInit(&pvFormatsSupported);
    hr = pDevice->GetProperty(g_wszWMDMFormatsSupported, &pvFormatsSupported);
    HANDLE_HR(hr, "Got a property list in GetCaps", "Couldn't get a property list in GetCaps.");

    // Loop through the retrieved format list.
    // For each format, get a list of format configurations.
    SAFEARRAY* formatList = pvFormatsSupported.parray;
    WMDM_FORMATCODE formatCode = WMDM_FORMATCODE_NOTUSED;
    for (LONG iCap = 0; iCap < formatList->rgsabound[0].cElements; iCap++)
    { 
        // Get a format from the SAFEARRAY of retrieved formats.
        SafeArrayGetElement(formatList, &iCap, &formatCode);

        // Call a custom function to request the format capabilities.
        if (formatCode != WMDM_FORMATCODE_NOTUSED)
            myGetFormatCaps(formatCode, pDevice);
    }

e_Exit:
    // Clear out the memory we used.
    PropVariantClear(&pvFormatsSupported);
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Individuazione delle funzionalità del formato del dispositivo**](discovering-device-format-capabilities.md)
</dt> </dl>

 

 




