---
title: Ottenere funzionalità di formato tramite IWMDMDevice3
description: Recupero delle funzionalità di formato nei dispositivi che supportano IWMDMDevice3
ms.assetid: a431c3cb-e722-4d68-a82d-385fff067ea6
keywords:
- Windows Gestione dispositivi multimediali, funzionalità del dispositivo
- Gestione dispositivi, funzionalità del dispositivo
- guida per programmatori, funzionalità del dispositivo
- applicazioni desktop, funzionalità dei dispositivi
- creazione Windows applicazioni di Gestione dispositivi multimediali, funzionalità del dispositivo
- scrittura di file nei dispositivi, funzionalità del dispositivo
- Metodo IWMDMDevice3
- Windows Media Device Manager,Metodo IWMDMDevice3
- Gestione dispositivi, metodo IWMDMDevice3
- Guida per programmatori,metodo IWMDMDevice3
- applicazioni desktop,metodo IWMDMDevice3
- creazione Windows applicazioni di Gestione dispositivi multimediali,metodo IWMDMDevice3
- scrittura di file nei dispositivi, metodo IWMDMDevice3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eadde80f957573563468375ea06cd64b95cf83815491a3f21775fb1ebcefc7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957527"
---
# <a name="getting-format-capabilities-through-iwmdmdevice3"></a>Ottenere funzionalità di formato tramite IWMDMDevice3

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) è il metodo preferito per chiedere a un dispositivo quali formati supporta. La procedura seguente illustra come usare questo metodo per eseguire query su un dispositivo per le relative funzionalità di formato:

1.  L'applicazione deve determinare i formati supportati da un dispositivo e quali sono di interesse. A tale scopo, l'applicazione può richiedere un elenco di formati supportati dal dispositivo chiamando [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty).
2.  L'applicazione esegue un ciclo in tutti i formati supportati e richiede le funzionalità di formato di un dispositivo per un formato specifico ,ad esempio WMA o WMV, chiamando **IWMDMDevice3::GetFormatCapability** e specificando un formato usando [**l'enumerazione \_ WMDM FORMATCODE.**](wmdm-formatcode.md) Questo metodo recupera una [**struttura WMDM \_ FORMAT \_ CAPABILITY.**](wmdm-format-capability.md)
3.  Scorrere tutte le [**strutture WMDM \_ PROP \_ CONFIG**](wmdm-prop-config.md) nella struttura **WMDM \_ FORMAT \_ CAPABILITY** recuperata. Ogni **struttura WMDM \_ PROP \_ CONFIG** contiene un gruppo di proprietà con valori supportati, che rappresentano una configurazione per tale formato. Ogni configurazione ha un numero di preferenza, in cui un numero inferiore indica una preferenza maggiore da parte del dispositivo.
4.  Eseguire un ciclo tra tutte [**le strutture \_ \_ DESC WMDM PROP**](wmdm-prop-desc.md) nel file DI CONFIGURAZIONE PROP **WMDM \_ \_ recuperato.** Ogni **WMDM \_ PROP \_ DESC** contiene un elenco di coppie proprietà/valore supportate.
5.  Recuperare i nomi e i valori delle proprietà dalla **struttura \_ WMDM PROP \_ DESC.** Le proprietà includono velocità in bit, codec e dimensioni dei fotogrammi. I nomi delle proprietà sono definiti nel file di intestazione mswmdm.h. Un elenco della maggior parte di queste costanti è disponibile in [Costanti dei metadati](metadata-constants.md). Sono possibili tre tipi di valori di proprietà:
    -   Valore singolo, WMDM ENUM PROP VALID VALUES ANY, che indica il supporto per \_ tutti i valori per questa \_ \_ \_ \_ proprietà.
    -   Intervallo di valori, definito da un valore massimo, un valore minimo e un intervallo.
    -   Elenco di valori discreti.
6.  Cancellare i valori archiviati. La memoria per questi valori viene allocata Windows Gestione dispositivi multimediali. il dispositivo è responsabile della liberazione della memoria. Come eseguire questa operazione è descritto alla fine di questo argomento.

Quando risponde a **GetFormatCapability,** un dispositivo può segnalare WMDM \_ ENUM \_ PROP VALID VALUES ANY per \_ \_ \_ **WMDM \_ FORMAT \_ CAPABILITY. WMDM \_ PROP \_ CONFIG. WMDM \_ PROP \_ DESC. ValidValuesForm per** richiedere il supporto per qualsiasi valore per velocità in bit, canali e così via. Tuttavia, è consigliabile considerare questa attestazione con cautela, perché i dispositivi talvolta possono segnalare il supporto per qualsiasi valore quando in realtà non supportano tutte le velocità in bit o le dimensioni delle immagini. È possibile che l'applicazione trascodifica file di dimensioni estremamente grandi o a velocità in bit elevata in versioni più piccole o versioni meno a elevato utilizzo di memoria e utilizzo elevato di CPU quando li invia a dispositivi destinati a riprodurre questi file.

La funzione C++ seguente illustra come richiedere il supporto del formato del dispositivo per un formato specifico.


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

Dopo il recupero delle funzionalità di formato da un dispositivo, l'applicazione deve liberare la memoria allocata per contenere la descrizione. [**GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) e [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) hanno matrici di strutture semplici che possono essere cancellate semplicemente chiamando **CoTaskMemFree** con la matrice. Tuttavia, **GetFormatCapability** ha una struttura di dati più complessa con memoria allocata dinamicamente che deve essere cancellata scorrendo tutti gli elementi e liberandoli singolarmente.

Il codice C++ seguente illustra come un'applicazione può liberare la memoria allocata per una **struttura WMDM \_ FORMAT \_ CAPABILITY.**


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

In genere, un'applicazione esegue una query su un dispositivo per un formato specifico, perché è interessata a inviare un file specifico al dispositivo. Tuttavia, se si vuole eseguire una query su un'applicazione per tutti i formati supportati, è possibile chiamare [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) e passare g \_ wszWMDMFormatsSupported per recuperare un elenco completo.

Se un dispositivo restituisce un solo elemento, WMDM FORMATCODE UNDEFINED, questo significa in genere che il \_ dispositivo non supporta i codici di \_ formato. La **chiamata di GetFormatCapability** con WMDM FORMATCODE UNDEFINED potrebbe recuperare funzionalità, ma queste proprietà potrebbero essere piuttosto generiche, ad esempio nome, dimensioni del file, data dell'ultima modifica e \_ \_ così via.

La procedura seguente illustra come eseguire una query per un elenco di tutti i formati supportati:

1.  Richiedere un elenco di tutti i codici di formato supportati chiamando **IWMDMDevice3::GetProperty** e passando g \_ wszWMDMFormatsSupported. Viene restituito **un elemento PROPVARIANT** contenente **un SAFEARRAY** di formati supportati.
2.  Scorrere gli elementi chiamando **SafeArrayGetElement**. Ogni elemento è **un'enumerazione \_ FORMATCODE WMDM.**
3.  Richiedere le funzionalità per ogni formato, liberando la memoria per ogni elemento **\_ WMDM FORMAT \_ CAPABILITY** al termine dell'operazione.
4.  Cancellare **l'oggetto PROPVARIANT** recuperato nel passaggio 1 chiamando **PropVariantClear**.

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

 

 




