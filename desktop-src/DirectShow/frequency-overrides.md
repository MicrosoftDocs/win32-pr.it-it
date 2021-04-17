---
description: Override della frequenza
ms.assetid: 0e45d0a6-3c3e-462c-a8dc-c4f25b614b85
title: Override della frequenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57177e4990cb40be271fc551718964faf1696d2d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520658"
---
# <a name="frequency-overrides"></a><span data-ttu-id="21ab4-103">Override della frequenza</span><span class="sxs-lookup"><span data-stu-id="21ab4-103">Frequency Overrides</span></span>

<span data-ttu-id="21ab4-104">È stata impiegata una quantità significativa di lavoro per garantire la correttezza delle frequenze di broadcast e delle assegnazioni standard dei colori per ogni paese/area geografica.</span><span class="sxs-lookup"><span data-stu-id="21ab4-104">A significant amount of effort was spent to ensure that the broadcast frequencies and color standard assignments are correct for each country/region.</span></span> <span data-ttu-id="21ab4-105">Anche in questo caso, si verificano situazioni in cui le tabelle di frequenza non sono sufficienti, contengono errori o diventano obsolete.</span><span class="sxs-lookup"><span data-stu-id="21ab4-105">Even so, there will be situations when the frequency tables are not sufficient, contain errors, or become obsolete.</span></span> <span data-ttu-id="21ab4-106">Per risolvere questo problema, le frequenze elencate nelle tabelle di frequenza del filtro del sintonizzatore TV possono essere sostituite selettivamente, usando la chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="21ab4-106">To address this problem, the frequencies listed in the TV Tuner filter's frequency tables may be selectively overridden, by using the following registry key:</span></span>

<span data-ttu-id="21ab4-107">**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **TV System Services** \\ **TVAutoTune** \\ **TS0-1**</span><span class="sxs-lookup"><span data-stu-id="21ab4-107">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**TV System Services**\\**TVAutoTune**\\**TS0-1**</span></span>

> [!Note]  
> <span data-ttu-id="21ab4-108">A partire da Windows 7, la chiave del registro di sistema reindirizzata seguente viene usata per le applicazioni x86 eseguite in versioni x64 di Windows:</span><span class="sxs-lookup"><span data-stu-id="21ab4-108">Starting in Windows 7, the following redirected registry key is used for x86 applications running on x64 versions of Windows:</span></span>

 

<span data-ttu-id="21ab4-109">**HKEY \_ \_Computer locale** \\ **software** \\ **Wow6432Node** \\ **Microsoft** \\ **TV System Services** \\ **TVAutoTune** \\ **TS0-1**</span><span class="sxs-lookup"><span data-stu-id="21ab4-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Wow6432Node**\\**Microsoft**\\**TV System Services**\\**TVAutoTune**\\**TS0-1**</span></span>

<span data-ttu-id="21ab4-110">Gli override di frequenza sono raggruppati in "spazi di ottimizzazione" definiti dall'applicazione, identificati da Number.</span><span class="sxs-lookup"><span data-stu-id="21ab4-110">Frequency overrides are grouped into application-defined "tuning spaces," which are identified by number.</span></span> <span data-ttu-id="21ab4-111">Nell'esempio seguente viene illustrato un override di esempio:</span><span class="sxs-lookup"><span data-stu-id="21ab4-111">The following example shows an example override:</span></span>

``` syntax
HKEY_LOCAL_MACHINE\Software\Microsoft\TV System Services\TVAutoTune\TS0-1
"12"=dword:04022750
```

<span data-ttu-id="21ab4-112">In questo caso, "TS0-1" indica lo spazio di ottimizzazione 0 per le frequenze dei cavi.</span><span class="sxs-lookup"><span data-stu-id="21ab4-112">In this case, "TS0-1" indicates Tuning Space 0 for cable frequencies.</span></span> <span data-ttu-id="21ab4-113">Il primo numero identifica lo spazio di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="21ab4-113">The first number identifies the tuning space.</span></span> <span data-ttu-id="21ab4-114">Il secondo numero è 0 per le frequenze di broadcast o 1 per le frequenze dei cavi.</span><span class="sxs-lookup"><span data-stu-id="21ab4-114">The second number is either 0 for broadcast frequencies or 1 for cable frequencies.</span></span>

<span data-ttu-id="21ab4-115">La sottochiave denominata "12" esegue l'override del valore Frequency per la frequenza in corrispondenza dell'indice 12 della tabella Frequency corrente.</span><span class="sxs-lookup"><span data-stu-id="21ab4-115">The subkey named "12" overrides the frequency value for the frequency at index 12 in the current frequency table.</span></span> <span data-ttu-id="21ab4-116">Il valore della sottochiave è un **DWORD** che specifica la frequenza in Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="21ab4-116">The value of the subkey is a **DWORD** that specifies the frequency in Hertz (Hz).</span></span> <span data-ttu-id="21ab4-117">In questo esempio, la frequenza è impostata su 67,25 MHz.</span><span class="sxs-lookup"><span data-stu-id="21ab4-117">In this example, the frequency is set to 67.25 MHz.</span></span> <span data-ttu-id="21ab4-118">È possibile definire le sostituzioni per qualsiasi numero di canale nell'intervallo compreso tra 1 e 999, inclusi.</span><span class="sxs-lookup"><span data-stu-id="21ab4-118">Overrides can be defined for any channel numbers in the range of 1 to 999, inclusive.</span></span> <span data-ttu-id="21ab4-119">Se l'hardware di ottimizzazione non supporta una determinata frequenza, la richiesta di ottimizzazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="21ab4-119">If the tuning hardware does not support a given frequency, the tune request will fail.</span></span>

<span data-ttu-id="21ab4-120">Questo meccanismo può essere utilizzato anche per creare nuovi numeri di canale al di fuori dell'intervallo esistente nella tabella Frequency.</span><span class="sxs-lookup"><span data-stu-id="21ab4-120">This mechanism can also be used to create new channel numbers outside the existing range in the frequency table.</span></span> <span data-ttu-id="21ab4-121">Il metodo [**IAMTuner:: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) restituirà l'intervallo di canali esteso.</span><span class="sxs-lookup"><span data-stu-id="21ab4-121">The [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) method will return the extended channel range.</span></span> <span data-ttu-id="21ab4-122">Se, ad esempio, l'intervallo di canali originale è compreso tra 1 e 158 e viene aggiunto un override del canale "200" al registro di sistema, il metodo **ChannelMinMax** restituirà 200 come canale massimo.</span><span class="sxs-lookup"><span data-stu-id="21ab4-122">For example, if the original channel range was 1 to 158, and a channel override of "200" is added to the registry, the **ChannelMinMax** method will return 200 as the maximum channel.</span></span> <span data-ttu-id="21ab4-123">In questo caso, ai numeri di canale compresi tra 159 e 199 non verrà assegnata alcuna frequenza, quindi le richieste di ottimizzazione in tale intervallo avranno automaticamente esito negativo.</span><span class="sxs-lookup"><span data-stu-id="21ab4-123">In this case, channel numbers in the range of 159 to 199 will have no frequencies assigned to them, so any tuning requests in that range will automatically fail.</span></span>

<span data-ttu-id="21ab4-124">Il metodo [**IAMTuner::p UT \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) consente all'applicazione di scegliere il set di sostituzioni e le informazioni di ottimizzazione da usare.</span><span class="sxs-lookup"><span data-stu-id="21ab4-124">The [**IAMTuner::put\_TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) method allows the application to choose which set of overrides and fine-tuning information to use.</span></span> <span data-ttu-id="21ab4-125">I numeri di spazio di ottimizzazione sono arbitrari.</span><span class="sxs-lookup"><span data-stu-id="21ab4-125">Tuning space numbers are arbitrary.</span></span> <span data-ttu-id="21ab4-126">È responsabilità dell'applicazione mantenere la relazione tra lo spazio di ottimizzazione e la tabella Frequency.</span><span class="sxs-lookup"><span data-stu-id="21ab4-126">It is the application's responsibility to maintain the relationship between the tuning space and the frequency table.</span></span> <span data-ttu-id="21ab4-127">L'approccio più semplice consiste nell'usare il codice paese/area geografica come numero di spazio di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="21ab4-127">The most straightforward approach is to use the country/region code as the tuning space number.</span></span> <span data-ttu-id="21ab4-128">Quindi, ogni volta che l'applicazione passa a un nuovo codice paese/area geografica, passa anche allo stesso spazio di ottimizzazione (in questo ordine).</span><span class="sxs-lookup"><span data-stu-id="21ab4-128">Then, every time the application switches to a new country/region code, it also switches to the same tuning space (in that order).</span></span>

## <a name="related-topics"></a><span data-ttu-id="21ab4-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="21ab4-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21ab4-130">Ottimizzazione della TV analoga internazionale</span><span class="sxs-lookup"><span data-stu-id="21ab4-130">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



