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
# <a name="implementing-cechoproppageoninitdialog"></a><span data-ttu-id="63fbf-109">Implementazione di CEchoPropPage:: OnInitDialog</span><span class="sxs-lookup"><span data-stu-id="63fbf-109">Implementing CEchoPropPage::OnInitDialog</span></span>

<span data-ttu-id="63fbf-110">Il metodo **CEchoPropPage:: OnInitDialog** è implementato in EchoPropPage. cpp.</span><span class="sxs-lookup"><span data-stu-id="63fbf-110">The **CEchoPropPage::OnInitDialog** method is implemented in EchoPropPage.cpp.</span></span> <span data-ttu-id="63fbf-111">Viene eseguito quando viene richiamata la finestra di dialogo della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="63fbf-111">It executes when the property page dialog box is invoked.</span></span> <span data-ttu-id="63fbf-112">Il codice in questo metodo deve recuperare i valori correnti della proprietà e visualizzarli nella casella di modifica corretta.</span><span class="sxs-lookup"><span data-stu-id="63fbf-112">The code in this method needs to retrieve the current property values and display them in the correct edit box.</span></span> <span data-ttu-id="63fbf-113">Il codice di esempio della procedura guidata plug-in fornisce un'implementazione per una singola proprietà.</span><span class="sxs-lookup"><span data-stu-id="63fbf-113">The plug-in wizard sample code provides an implementation for a single property.</span></span> <span data-ttu-id="63fbf-114">È possibile modificare questo codice per una delle proprietà di esempio Echo, quindi aggiungere il codice per recuperare il secondo valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="63fbf-114">You can modify this code for one of the Echo sample properties, and then add code to retrieve the second property value.</span></span>

## <a name="declaring-the-oninitdialog-method-variables"></a><span data-ttu-id="63fbf-115">Dichiarazione delle variabili del metodo OnInitDialog</span><span class="sxs-lookup"><span data-stu-id="63fbf-115">Declaring the OnInitDialog Method Variables</span></span>

<span data-ttu-id="63fbf-116">Prima di tutto, è necessario rimuovere la dichiarazione di fScaleFactor e sostituirla con le seguenti dichiarazioni di variabili:</span><span class="sxs-lookup"><span data-stu-id="63fbf-116">First, you must remove the declaration of fScaleFactor and replace it with the following variable declarations:</span></span>


```
DWORD  dwDelayTime = 1000;    // Default delay time.
DWORD  dwWetmix = 50;         // Default wet mix DWORD.
double fWetmix =  0.50;       // Default wet mix double.
```



## <a name="retrieving-the-current-values-from-the-plug-in"></a><span data-ttu-id="63fbf-117">Recupero dei valori correnti dal plug-in</span><span class="sxs-lookup"><span data-stu-id="63fbf-117">Retrieving the Current Values from the Plug-in</span></span>

<span data-ttu-id="63fbf-118">Il codice deve tentare di recuperare i valori correnti della proprietà dal plug-in Echo.</span><span class="sxs-lookup"><span data-stu-id="63fbf-118">The code should next attempt to retrieve the current property values from the Echo plug-in.</span></span> <span data-ttu-id="63fbf-119">Nell'esempio seguente viene eseguito un tentativo di recupero di ogni proprietà:</span><span class="sxs-lookup"><span data-stu-id="63fbf-119">The following example attempts to retrieve each property:</span></span>


```
if (m_spEcho)
{
    m_spEcho->get_delay(&dwDelayTime);
    m_spEcho->get_wetmix(&fWetmix);
    // Convert wet mix from double to DWORD.
    dwWetmix = (DWORD)(fWetmix * 100);
}
```



<span data-ttu-id="63fbf-120">Nella finestra di dialogo viene visualizzato il valore del livello effetti all'utente come intero, ma il plug-in archivia il valore come numero a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="63fbf-120">The dialog box displays the effects level value to the user as an integer, but the plug-in stores the value as a floating-point number.</span></span> <span data-ttu-id="63fbf-121">Pertanto, il codice converte il valore a virgola mobile in un valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="63fbf-121">Therefore, the code converts the floating-point value to a **DWORD** value.</span></span>

## <a name="retrieving-the-current-values-from-the-registry"></a><span data-ttu-id="63fbf-122">Recupero dei valori correnti dal registro di sistema</span><span class="sxs-lookup"><span data-stu-id="63fbf-122">Retrieving the Current Values from the Registry</span></span>

<span data-ttu-id="63fbf-123">Se la pagina delle proprietà non è in grado di recuperare i valori correnti dal plug-in, è necessario tentarne la lettura dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="63fbf-123">If the property page cannot retrieve the current values from the plug-in, it must attempt to read them from the registry.</span></span> <span data-ttu-id="63fbf-124">Il codice seguente legge ogni valore di proprietà:</span><span class="sxs-lookup"><span data-stu-id="63fbf-124">The following code reads each property value:</span></span>


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



<span data-ttu-id="63fbf-125">Si noti l'uso delle costanti del registro di sistema create in precedenza.</span><span class="sxs-lookup"><span data-stu-id="63fbf-125">Notice the use of the registry constants you created previously.</span></span>

## <a name="displaying-the-values-to-the-user"></a><span data-ttu-id="63fbf-126">Visualizzazione dei valori all'utente</span><span class="sxs-lookup"><span data-stu-id="63fbf-126">Displaying the Values to the User</span></span>

<span data-ttu-id="63fbf-127">Infine, la pagina delle proprietà deve visualizzare i valori nei controlli corretti della casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="63fbf-127">Finally, the property page must display the values in the correct edit box controls.</span></span> <span data-ttu-id="63fbf-128">Nell'esempio di codice seguente viene illustrato quanto segue:</span><span class="sxs-lookup"><span data-stu-id="63fbf-128">The following example code demonstrates this:</span></span>


```
 TCHAR   szStr[MAXSTRING];

// Display the delay time.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwDelayTime);
SetDlgItemText(IDC_DELAYTIME, szStr);

// Display the effect level.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwWetmix);
SetDlgItemText(IDC_WETMIX, szStr);
```



## <a name="related-topics"></a><span data-ttu-id="63fbf-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="63fbf-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63fbf-130">**Modifica della pagina delle proprietà di esempio Echo**</span><span class="sxs-lookup"><span data-stu-id="63fbf-130">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




