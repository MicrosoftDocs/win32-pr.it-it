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
# <a name="implementing-cechofinalconstruct"></a><span data-ttu-id="e1aec-109">Implementazione di CEcho:: FinalConstruct</span><span class="sxs-lookup"><span data-stu-id="e1aec-109">Implementing CEcho::FinalConstruct</span></span>

<span data-ttu-id="e1aec-110">Il metodo CEcho:: FinalConstruct è implementato in Echo. cpp.</span><span class="sxs-lookup"><span data-stu-id="e1aec-110">The CEcho::FinalConstruct method is implemented in Echo.cpp.</span></span> <span data-ttu-id="e1aec-111">Contiene il codice per leggere i valori delle proprietà dal registro di sistema quando Windows Media Player crea un'istanza dell'oggetto plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="e1aec-111">It contains code to read the property values from the registry when Windows Media Player instantiates the DSP plug-in object.</span></span> <span data-ttu-id="e1aec-112">Si tratta di un aspetto importante perché consente alle impostazioni utente di mantenersi tra le istanze dell'oggetto, nonché tra le sessioni.</span><span class="sxs-lookup"><span data-stu-id="e1aec-112">This is important because it allows the user settings to persist between instances of the object, as well as between sessions.</span></span> <span data-ttu-id="e1aec-113">Il codice di esempio della procedura guidata plug-in fornisce l'implementazione di per leggere una singola proprietà dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e1aec-113">The plug-in wizard sample code provides implementation to read a single property from the registry.</span></span> <span data-ttu-id="e1aec-114">È possibile modificare questo codice per gestire la proprietà tempo di ritardo, quindi aggiungere il codice per leggere il valore della proprietà Wet Mix.</span><span class="sxs-lookup"><span data-stu-id="e1aec-114">You can modify this code to handle the delay time property, and then add code to read the wet mix property value.</span></span>

<span data-ttu-id="e1aec-115">Il codice di esempio seguente legge ogni valore di proprietà dal registro di sistema e li archivia nella variabile membro corretta:</span><span class="sxs-lookup"><span data-stu-id="e1aec-115">The following example code reads each property value from the registry and stores each in the correct member variable:</span></span>


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



<span data-ttu-id="e1aec-116">Si noti che il valore DWORD per la combinazione Wet viene convertito in un valore a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="e1aec-116">Notice that the DWORD value for the wet mix is converted to a floating-point value.</span></span> <span data-ttu-id="e1aec-117">Si noti anche che il codice calcola il valore corretto per m \_ fDryMix.</span><span class="sxs-lookup"><span data-stu-id="e1aec-117">Also note that the code calculates the correct value for m\_fDryMix.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1aec-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e1aec-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1aec-119">**Modifica della pagina delle proprietà di esempio Echo**</span><span class="sxs-lookup"><span data-stu-id="e1aec-119">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




