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
# <a name="getting-format-capabilities-through-iwmdmdevice3"></a><span data-ttu-id="af00a-116">Ottenere le funzionalità di formattazione tramite IWMDMDevice3</span><span class="sxs-lookup"><span data-stu-id="af00a-116">Getting format capabilities through IWMDMDevice3</span></span>

<span data-ttu-id="af00a-117">[**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) è il metodo preferito per chiedere a un dispositivo quali formati sono supportati.</span><span class="sxs-lookup"><span data-stu-id="af00a-117">[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) is the preferred method for asking a device what formats it supports.</span></span> <span data-ttu-id="af00a-118">I passaggi seguenti illustrano come usare questo metodo per eseguire una query su un dispositivo per le funzionalità di formato:</span><span class="sxs-lookup"><span data-stu-id="af00a-118">The following steps show how to use this method to query a device for its format capabilities:</span></span>

1.  <span data-ttu-id="af00a-119">L'applicazione deve determinare quali formati sono supportati da un dispositivo e quali sono di interesse.</span><span class="sxs-lookup"><span data-stu-id="af00a-119">The application must determine which formats a device supports and which are of interest.</span></span> <span data-ttu-id="af00a-120">A tale scopo, l'applicazione può richiedere un elenco di formati supportati dal dispositivo chiamando [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty).</span><span class="sxs-lookup"><span data-stu-id="af00a-120">To do this, the application can request a list of formats supported by the device by calling [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty).</span></span>
2.  <span data-ttu-id="af00a-121">L'applicazione esegue il ciclo di tutti i formati supportati e richiede le funzionalità di formattazione di un dispositivo per un formato specifico, ad esempio WMA o WMV, chiamando **IWMDMDevice3:: GetFormatCapability** e specificando un formato usando l'enumerazione [**WMDM \_ FORMATCODE**](wmdm-formatcode.md) .</span><span class="sxs-lookup"><span data-stu-id="af00a-121">The application loops through all of the supported formats and requests a device's format capabilities for a specific format (such as WMA or WMV) by calling **IWMDMDevice3::GetFormatCapability** and specifying a format using the [**WMDM\_FORMATCODE**](wmdm-formatcode.md) enumeration.</span></span> <span data-ttu-id="af00a-122">Questo metodo recupera una struttura di [**\_ \_ funzionalità del formato WMDM**](wmdm-format-capability.md) .</span><span class="sxs-lookup"><span data-stu-id="af00a-122">This method retrieves a [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md) structure.</span></span>
3.  <span data-ttu-id="af00a-123">Scorrere in ciclo tutte le strutture di [**\_ \_ configurazione della prop WMDM**](wmdm-prop-config.md) nella struttura della **\_ \_ funzionalità del formato WMDM** recuperato.</span><span class="sxs-lookup"><span data-stu-id="af00a-123">Loop through all the [**WMDM\_PROP\_CONFIG**](wmdm-prop-config.md) structures in the retrieved **WMDM\_FORMAT\_CAPABILITY** structure.</span></span> <span data-ttu-id="af00a-124">Ogni struttura di **\_ \_ configurazione di WMDM prop** include un gruppo di proprietà con valori supportati, che rappresentano una configurazione per tale formato.</span><span class="sxs-lookup"><span data-stu-id="af00a-124">Each **WMDM\_PROP\_CONFIG** structure holds a group of properties with supported values, representing one configuration for that format.</span></span> <span data-ttu-id="af00a-125">Ogni configurazione ha un numero di preferenza, dove un numero inferiore indica una preferenza maggiore da parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af00a-125">Each configuration has a preference number, where a lower number indicates a greater preference by the device.</span></span>
4.  <span data-ttu-id="af00a-126">Eseguire il ciclo di tutte le strutture [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md) nella **\_ \_ configurazione di WMDM prop** recuperata.</span><span class="sxs-lookup"><span data-stu-id="af00a-126">Loop through all the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures in the retrieved **WMDM\_PROP\_CONFIG**.</span></span> <span data-ttu-id="af00a-127">Ogni **WMDM \_ prop \_ desc** contiene un elenco di coppie proprietà/valore supportate.</span><span class="sxs-lookup"><span data-stu-id="af00a-127">Each **WMDM\_PROP\_DESC** contains a list of supported property/value pairs.</span></span>
5.  <span data-ttu-id="af00a-128">Recuperare i nomi e i valori delle proprietà dalla struttura **WMDM \_ prop \_ desc** .</span><span class="sxs-lookup"><span data-stu-id="af00a-128">Retrieve the property names and values from the **WMDM\_PROP\_DESC** structure.</span></span> <span data-ttu-id="af00a-129">Le proprietà includono velocità in bit, codec e dimensioni del frame.</span><span class="sxs-lookup"><span data-stu-id="af00a-129">Properties include bit rate, codec, and frame size.</span></span> <span data-ttu-id="af00a-130">I nomi delle proprietà vengono definiti nel file di intestazione mswmdm. h; un elenco della maggior parte di queste costanti viene specificato nelle [costanti dei metadati](metadata-constants.md).</span><span class="sxs-lookup"><span data-stu-id="af00a-130">Property names are defined in the mswmdm.h header file; a list of most of these constants is given in [Metadata Constants](metadata-constants.md).</span></span> <span data-ttu-id="af00a-131">Sono possibili tre tipi di valori di proprietà:</span><span class="sxs-lookup"><span data-stu-id="af00a-131">Three types of property values are possible:</span></span>
    -   <span data-ttu-id="af00a-132">Un singolo valore, WMDM \_ enum \_ prop \_ valid \_ Values \_ any, che indica il supporto per qualsiasi valore per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="af00a-132">A single value, WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY, indicating support for any values for this property.</span></span>
    -   <span data-ttu-id="af00a-133">Intervallo di valori, definito da un valore massimo, da un valore minimo e da un intervallo.</span><span class="sxs-lookup"><span data-stu-id="af00a-133">A range of values, defined by a maximum value, minimum value, and interval.</span></span>
    -   <span data-ttu-id="af00a-134">Elenco di valori discreti.</span><span class="sxs-lookup"><span data-stu-id="af00a-134">A list of discrete values.</span></span>
6.  <span data-ttu-id="af00a-135">Cancellare i valori archiviati.</span><span class="sxs-lookup"><span data-stu-id="af00a-135">Clear the stored values.</span></span> <span data-ttu-id="af00a-136">La memoria per questi valori viene allocata da Windows Media Gestione dispositivi; il dispositivo è responsabile della liberazione della memoria.</span><span class="sxs-lookup"><span data-stu-id="af00a-136">Memory for these values is allocated by Windows Media Device Manager; your device is responsible for freeing the memory.</span></span> <span data-ttu-id="af00a-137">Questa procedura è descritta alla fine di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="af00a-137">How to do this is described at the end of this topic.</span></span>

<span data-ttu-id="af00a-138">Quando si risponde a **GetFormatCapability**, un dispositivo può segnalare \_ \_ i valori validi di WMDM enum Prop \_ \_ \_ any per la **funzionalità di \_ formato WMDM \_ . \_configurazione della prop WMDM \_ . WMDM \_ prop \_ desc. ValidValuesForm** per richiedere il supporto per qualsiasi valore per la velocità in bit, i canali e così via.</span><span class="sxs-lookup"><span data-stu-id="af00a-138">When responding to **GetFormatCapability**, a device can report WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY for **WMDM\_FORMAT\_CAPABILITY.WMDM\_PROP\_CONFIG.WMDM\_PROP\_DESC.ValidValuesForm** to claim support for any values for bit rate, channels, and so on.</span></span> <span data-ttu-id="af00a-139">Tuttavia, è consigliabile considerare questa richiesta con cautela, perché i dispositivi possono a volte segnalare il supporto per qualsiasi valore quando in realtà non supportano tutte le velocità in bit o le dimensioni delle immagini.</span><span class="sxs-lookup"><span data-stu-id="af00a-139">However, you should treat this claim with caution, because devices can sometimes report support for any values when in fact they do not support all bit rates or image sizes.</span></span> <span data-ttu-id="af00a-140">Si può prendere in considerazione la possibilità di eseguire la transcodifica di file di grandi dimensioni o a velocità elevata in un'applicazione a versioni più piccole o con un numero minore di versioni con utilizzo intensivo di memoria e CPU durante l'invio ai dispositivi destinati a riprodurre questi file.</span><span class="sxs-lookup"><span data-stu-id="af00a-140">You might consider having your application transcode extremely large or high-bit-rate files to smaller versions or less memory-intensive and CPU-intensive versions when sending them to devices that are intended to play these files.</span></span>

<span data-ttu-id="af00a-141">La seguente funzione C++ Mostra come richiedere il supporto del formato del dispositivo per un formato specifico.</span><span class="sxs-lookup"><span data-stu-id="af00a-141">The following C++ function shows how to request device format support for a specific format.</span></span>


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



<span data-ttu-id="af00a-142">**Cancellazione della memoria allocata**</span><span class="sxs-lookup"><span data-stu-id="af00a-142">**Clearing allocated memory**</span></span>

<span data-ttu-id="af00a-143">Dopo aver recuperato le funzionalità di formato da un dispositivo, l'applicazione deve liberare la memoria allocata per la descrizione.</span><span class="sxs-lookup"><span data-stu-id="af00a-143">After retrieving format capabilities from a device, the application must free the memory allocated to hold the description.</span></span> <span data-ttu-id="af00a-144">[**GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) e [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) hanno matrici di strutture semplici che possono essere cancellate semplicemente chiamando **CoTaskMemFree** con la matrice.</span><span class="sxs-lookup"><span data-stu-id="af00a-144">[**GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) and [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) have arrays of simple structures that can be cleared by simply calling **CoTaskMemFree** with the array.</span></span> <span data-ttu-id="af00a-145">Tuttavia, **GetFormatCapability** dispone di una struttura di dati più complessa con la memoria allocata in modo dinamico che deve essere cancellata mediante il ciclo di tutti gli elementi e la loro liberazione singolarmente.</span><span class="sxs-lookup"><span data-stu-id="af00a-145">However, **GetFormatCapability** has a more complex data structure with dynamically allocated memory that must be cleared by looping through all the elements and freeing them individually.</span></span>

<span data-ttu-id="af00a-146">Nel codice C++ riportato di seguito viene illustrato come un'applicazione può liberare la memoria allocata per una struttura di **\_ \_ funzionalità del formato WMDM** .</span><span class="sxs-lookup"><span data-stu-id="af00a-146">The following C++ code shows how an application can free the memory allocated for a **WMDM\_FORMAT\_CAPABILITY** structure.</span></span>


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



<span data-ttu-id="af00a-147">**Esecuzione di query per tutti i formati supportati**</span><span class="sxs-lookup"><span data-stu-id="af00a-147">**Querying for all supported formats**</span></span>

<span data-ttu-id="af00a-148">In genere, un'applicazione esegue una query su un dispositivo per un formato specifico, perché è interessato all'invio di un file specifico al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af00a-148">Typically, an application queries a device for a specific format, because it is interested in sending a specific file to the device.</span></span> <span data-ttu-id="af00a-149">Tuttavia, se si desidera eseguire una query su un'applicazione per tutti i formati supportati, è possibile chiamare [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) e passare g \_ wszWMDMFormatsSupported per recuperare un elenco completo.</span><span class="sxs-lookup"><span data-stu-id="af00a-149">However, if you want to query an application for all its supported formats, you can call [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) and pass in g\_wszWMDMFormatsSupported to retrieve a full list.</span></span>

<span data-ttu-id="af00a-150">Se un dispositivo restituisce solo un elemento, WMDM \_ FORMATCODE \_ undefined, significa che il dispositivo non supporta i codici di formato.</span><span class="sxs-lookup"><span data-stu-id="af00a-150">If a device only returns one element, WMDM\_FORMATCODE\_UNDEFINED, this usually means that the device does not support format codes.</span></span> <span data-ttu-id="af00a-151">La chiamata di **GetFormatCapability** con WMDM \_ FORMATCODE \_ non definita potrebbe recuperare le funzionalità, ma queste proprietà potrebbero essere piuttosto generiche, ad esempio nome, dimensioni del file, data dell'Ultima modifica e così via.</span><span class="sxs-lookup"><span data-stu-id="af00a-151">Calling **GetFormatCapability** with WMDM\_FORMATCODE\_UNDEFINED might retrieve capabilities, but these properties might be fairly generic (such as name, file size, last modified date, and so on).</span></span>

<span data-ttu-id="af00a-152">Nei passaggi seguenti viene illustrato come eseguire una query per un elenco di tutti i formati supportati:</span><span class="sxs-lookup"><span data-stu-id="af00a-152">The following steps show how to query for a list of all supported formats:</span></span>

1.  <span data-ttu-id="af00a-153">Richiedere un elenco di tutti i codici di formato supportati chiamando **IWMDMDevice3:: GetProperty** e passando g \_ wszWMDMFormatsSupported.</span><span class="sxs-lookup"><span data-stu-id="af00a-153">Request a list of all format codes supported by calling **IWMDMDevice3::GetProperty** and passing in g\_wszWMDMFormatsSupported.</span></span> <span data-ttu-id="af00a-154">Restituisce un **PROPVARIANT** contenente un **SAFEARRAY** di formati supportati.</span><span class="sxs-lookup"><span data-stu-id="af00a-154">This returns a **PROPVARIANT** containing a **SAFEARRAY** of supported formats.</span></span>
2.  <span data-ttu-id="af00a-155">Eseguire il ciclo degli elementi chiamando **SafeArrayGetElement**.</span><span class="sxs-lookup"><span data-stu-id="af00a-155">Loop through the elements by calling **SafeArrayGetElement**.</span></span> <span data-ttu-id="af00a-156">Ogni elemento è un'enumerazione **WMDM \_ FORMATCODE** .</span><span class="sxs-lookup"><span data-stu-id="af00a-156">Each element is a **WMDM\_FORMATCODE** enumeration.</span></span>
3.  <span data-ttu-id="af00a-157">Richiedere le funzionalità per ogni formato, liberando la memoria per ogni elemento di **\_ \_ capacità del formato WMDM** , una volta completata.</span><span class="sxs-lookup"><span data-stu-id="af00a-157">Request the capabilities for each format, freeing the memory for each **WMDM\_FORMAT\_CAPABILITY** element once done with it.</span></span>
4.  <span data-ttu-id="af00a-158">Cancellare il **PROPVARIANT** recuperato nel passaggio 1 chiamando **PropVariantClear**.</span><span class="sxs-lookup"><span data-stu-id="af00a-158">Clear the **PROPVARIANT** retrieved in step 1 by calling **PropVariantClear**.</span></span>

<span data-ttu-id="af00a-159">Il codice di esempio C++ seguente recupera un elenco di formati supportati per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af00a-159">The following C++ example code retrieves a list of supported formats for a device.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="af00a-160">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af00a-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af00a-161">**Individuazione delle funzionalità del formato del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="af00a-161">**Discovering Device Format Capabilities**</span></span>](discovering-device-format-capabilities.md)
</dt> </dl>

 

 




