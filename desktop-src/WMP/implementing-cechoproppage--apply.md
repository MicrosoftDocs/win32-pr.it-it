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
# <a name="implementing-cechoproppageapply"></a><span data-ttu-id="6aff6-109">Implementazione di CEchoPropPage:: Apply</span><span class="sxs-lookup"><span data-stu-id="6aff6-109">Implementing CEchoPropPage::Apply</span></span>

<span data-ttu-id="6aff6-110">Il metodo CEchoPropPage:: Apply è implementato in EchoPropPage. cpp.</span><span class="sxs-lookup"><span data-stu-id="6aff6-110">The CEchoPropPage::Apply method is implemented in EchoPropPage.cpp.</span></span> <span data-ttu-id="6aff6-111">Viene eseguito quando l'utente fa clic su **applica** nella finestra di dialogo della pagina delle proprietà di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6aff6-111">It executes when the user clicks **Apply** in the property page dialog box in Windows Media Player.</span></span> <span data-ttu-id="6aff6-112">Il codice di esempio della procedura guidata plug-in fornisce un'implementazione di per gestire una singola proprietà.</span><span class="sxs-lookup"><span data-stu-id="6aff6-112">The plug-in wizard sample code provides an implementation to handle a single property.</span></span> <span data-ttu-id="6aff6-113">È possibile modificare questo codice per una delle proprietà di esempio Echo, quindi aggiungere il codice per archiviare l'altro valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="6aff6-113">You can modify this code for one of the Echo sample properties, and then add code to store the other property value.</span></span>

## <a name="declaring-the-apply-method-variables"></a><span data-ttu-id="6aff6-114">Dichiarazione delle variabili del metodo Apply</span><span class="sxs-lookup"><span data-stu-id="6aff6-114">Declaring the Apply Method Variables</span></span>

<span data-ttu-id="6aff6-115">In primo luogo, è necessario rimuovere la dichiarazione di fScaleFactor.</span><span class="sxs-lookup"><span data-stu-id="6aff6-115">First, you must remove the declaration of fScaleFactor.</span></span> <span data-ttu-id="6aff6-116">Aggiungere quindi le dichiarazioni di variabili necessarie.</span><span class="sxs-lookup"><span data-stu-id="6aff6-116">Then, add variable declarations that you will need.</span></span> <span data-ttu-id="6aff6-117">Nell'esempio seguente vengono illustrate le dichiarazioni di variabile completate:</span><span class="sxs-lookup"><span data-stu-id="6aff6-117">The following example shows the completed variable declarations:</span></span>


```
TCHAR   szStr[MAXSTRING] = { 0 };
DWORD   dwDelayTime = 1000;  // Initialize the delay time.
DWORD   dwWetmix = 50;       // Initialize a DWORD for effect level.
double  fWetmix = 0.50;      // Initialize a double for effect level.
```



## <a name="retrieving-the-values-from-the-property-page"></a><span data-ttu-id="6aff6-118">Recupero dei valori dalla pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="6aff6-118">Retrieving the Values from the Property Page</span></span>

<span data-ttu-id="6aff6-119">È necessario implementare il codice per recuperare e convalidare l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6aff6-119">You must implement code to retrieve and validate the user input.</span></span> <span data-ttu-id="6aff6-120">L'esempio di codice seguente recupera il valore di tempo di ritardo dalla \_ casella di modifica IDC DELAYTIME, quindi verifica che il valore si trovi all'interno di un intervallo specificato:</span><span class="sxs-lookup"><span data-stu-id="6aff6-120">The following code example retrieves the delay time value from the IDC\_DELAYTIME edit box, and then verifies that the value is within a specified range:</span></span>


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



<span data-ttu-id="6aff6-121">Se l'input dell'utente non è compreso nell'intervallo specificato, il codice visualizza una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="6aff6-121">If the user input is not in the specified range, the code displays a message box.</span></span> <span data-ttu-id="6aff6-122">Si noti l'uso della risorsa di stringa creata in precedenza per il messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="6aff6-122">Notice the use of the string resource you created earlier for the error message.</span></span>

<span data-ttu-id="6aff6-123">Nell'esempio seguente viene recuperato il livello di effetto dalla \_ casella di modifica IDC WETMIX, quindi viene verificato che il valore si trovi all'interno di un intervallo specificato:</span><span class="sxs-lookup"><span data-stu-id="6aff6-123">The following example retrieves the effect level from the IDC\_WETMIX edit box and then verifies that the value is within a specified range:</span></span>


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



## <a name="storing-the-property-values-in-the-registry"></a><span data-ttu-id="6aff6-124">Archiviazione dei valori delle proprietà nel registro di sistema</span><span class="sxs-lookup"><span data-stu-id="6aff6-124">Storing the Property Values in the Registry</span></span>

<span data-ttu-id="6aff6-125">Successivamente, il codice deve salvare i nuovi valori delle proprietà nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="6aff6-125">Next, your code must persist the new property values to the registry.</span></span> <span data-ttu-id="6aff6-126">Il codice seguente archivia entrambi i valori delle proprietà:</span><span class="sxs-lookup"><span data-stu-id="6aff6-126">The following code stores both property values:</span></span>


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



## <a name="updating-the-echo-plug-in-property-values"></a><span data-ttu-id="6aff6-127">Aggiornamento dei valori delle proprietà del plug-in Echo</span><span class="sxs-lookup"><span data-stu-id="6aff6-127">Updating the Echo Plug-in Property Values</span></span>

<span data-ttu-id="6aff6-128">Il metodo **Apply** deve informare il plug-in echo che i valori della proprietà sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="6aff6-128">The **Apply** method must inform the Echo plug-in that the property values have changed.</span></span> <span data-ttu-id="6aff6-129">Il codice seguente chiama il metodo Put della proprietà per ogni proprietà usando il puntatore a interfaccia recuperato in CEchoPropPage:: setpropertys:</span><span class="sxs-lookup"><span data-stu-id="6aff6-129">The following code calls the property put method for each property using the interface pointer retrieved in CEchoPropPage::SetObjects:</span></span>


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



<span data-ttu-id="6aff6-130">Si noti che il valore Wet Mix viene convertito in virgola mobile prima del passaggio al plug-in.</span><span class="sxs-lookup"><span data-stu-id="6aff6-130">Notice that the wet mix value is converted to floating point before being passed to the plug-in.</span></span>

## <a name="disabling-the-apply-button"></a><span data-ttu-id="6aff6-131">Disabilitazione del pulsante applica</span><span class="sxs-lookup"><span data-stu-id="6aff6-131">Disabling the Apply Button</span></span>

<span data-ttu-id="6aff6-132">Come passaggio finale, il codice deve disabilitare applica nella finestra di dialogo della pagina delle proprietà come segnale all'utente che i valori sono stati aggiornati correttamente.</span><span class="sxs-lookup"><span data-stu-id="6aff6-132">As a final step, your code should disable Apply in the property page dialog box as a signal to the user that the values have been successfully updated.</span></span> <span data-ttu-id="6aff6-133">Questa operazione richiede la riga di codice seguente:</span><span class="sxs-lookup"><span data-stu-id="6aff6-133">This requires the following single line of code:</span></span>


```
m_bDirty = FALSE; // Tell the property page to disable Apply.
```



## <a name="related-topics"></a><span data-ttu-id="6aff6-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6aff6-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6aff6-135">**Modifica della pagina delle proprietà di esempio Echo**</span><span class="sxs-lookup"><span data-stu-id="6aff6-135">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




