---
title: Esempio di implementazione di render
description: Esempio di implementazione di render
ms.assetid: 5791f6ea-ddad-49e6-8c6f-8093592895d4
keywords:
- Visualizzazioni, esempio Glow
- Visualizzazioni personalizzate, esempio Glow
- Guida per programmatori, visualizzazioni
- esempi, visualizzazione bagliore
- Esempio di visualizzazione bagliore
- Visualizzazioni, funzione render
- Visualizzazioni personalizzate, funzione render
- Funzione render, esempio Glow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dabc816283113a82c1d5d677dfc0ca8e8887d344
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517331"
---
# <a name="implementing-render-sample"></a><span data-ttu-id="55a79-111">Esempio di implementazione di render</span><span class="sxs-lookup"><span data-stu-id="55a79-111">Implementing Render Sample</span></span>

<span data-ttu-id="55a79-112">Il codice seguente viene usato per implementare la funzione **Render** :</span><span class="sxs-lookup"><span data-stu-id="55a79-112">The following code is used to implement the **Render** function:</span></span>


```C++
STDMETHODIMP CGlow::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    COLORREF mycolor;
    int mylevel = pLevels->waveform[0][0];
    
    switch (m_nPreset)
    {
    case PRESET_RED:
        {
        mycolor = RGB( mylevel, 0, 0);    
        }
        break;
    case PRESET_GREEN:
        {
        mycolor = RGB( 0, mylevel, 0);        
        }
        break;
    case PRESET_BLUE:
        {
        mycolor = RGB( 0, 0, mylevel);        
        }
        break;
    }

     HBRUSH hNewBrush = ::CreateSolidBrush( mycolor );
    ::FillRect( hdc, prc, hNewBrush );

    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }

    return S_OK;
}

```



<span data-ttu-id="55a79-113">Ecco una spiegazione del codice:</span><span class="sxs-lookup"><span data-stu-id="55a79-113">Here is an explanation of the code:</span></span>

<span data-ttu-id="55a79-114">Una variabile denominata *colori* viene utilizzata per il colore del bagliore ed è dichiarata con **COLORREF**.</span><span class="sxs-lookup"><span data-stu-id="55a79-114">A variable named *mycolor* is used for the color of the glow and is declared with **COLORREF**.</span></span> <span data-ttu-id="55a79-115">Tutti i colori devono usare il tipo di dati **COLORREF** .</span><span class="sxs-lookup"><span data-stu-id="55a79-115">All colors should use the **COLORREF** data type.</span></span>

<span data-ttu-id="55a79-116">Una variabile denominata " *livello* " viene usata per lo snapshot del livello di forma d'onda audio.</span><span class="sxs-lookup"><span data-stu-id="55a79-116">A variable named *mylevel* is used for the audio waveform level snapshot.</span></span> <span data-ttu-id="55a79-117">Questo valore dipenderà dal livello di potenza effettivo al momento dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="55a79-117">This value will depend on the actual power level at the moment of the snapshot.</span></span>

<span data-ttu-id="55a79-118">L'istruzione **Switch** viene impostata dal set di impostazioni scelto dall'utente in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="55a79-118">The **switch** statement is set by the preset that the user has chosen on Windows Media Player.</span></span> <span data-ttu-id="55a79-119">La scelta imposterà *colore* sul colore desiderato (rosso, verde o blu).</span><span class="sxs-lookup"><span data-stu-id="55a79-119">The choice will set *mycolor* to the desired color (red, green, or blue).</span></span> <span data-ttu-id="55a79-120">Tuttavia, il colore esatto sarà determinato dal livello di alimentazione audio.</span><span class="sxs-lookup"><span data-stu-id="55a79-120">However, the exact color will be determined by the audio power level.</span></span> <span data-ttu-id="55a79-121">Se, ad esempio, si sceglie il set di impostazioni rosso, il colore sarà un rosso tinta unita, ma sarà più chiaro o più scuro a seconda della forma d'onda audio al momento dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="55a79-121">For example, if the red preset is chosen, the color will be a solid red, but it will be lighter or darker depending on the audio waveform at the moment of the snapshot.</span></span> <span data-ttu-id="55a79-122">Assicurarsi di usare la macro **RBG** per creare il colore.</span><span class="sxs-lookup"><span data-stu-id="55a79-122">Be sure to use the **RBG** macro to create your color.</span></span>

<span data-ttu-id="55a79-123">Viene creato un pennello denominato *hNewBrush* che viene utilizzato per riempire il rettangolo *PRC* fornito da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="55a79-123">A brush is created called *hNewBrush*, and it is used to fill the *prc* rectangle provided by Windows Media Player.</span></span> <span data-ttu-id="55a79-124">La superficie di disegno è il contesto di dispositivo *HDC* fornito da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="55a79-124">The drawing surface is the *hdc* device context provided by Windows Media Player.</span></span>

<span data-ttu-id="55a79-125">Il pennello viene eliminato da **DeleteObject**.</span><span class="sxs-lookup"><span data-stu-id="55a79-125">The brush is deleted by **DeleteObject**.</span></span> <span data-ttu-id="55a79-126">Assicurarsi sempre di eliminare le penne o i pennelli creati.</span><span class="sxs-lookup"><span data-stu-id="55a79-126">Always be sure to delete any pens or brushes you create.</span></span>

<span data-ttu-id="55a79-127">Al termine del codice di **rendering** , Windows Media Player visualizzerà la grafica *HDC* in una finestra determinata dall'interfaccia usata.</span><span class="sxs-lookup"><span data-stu-id="55a79-127">Once the **Render** code is finished, Windows Media Player will display the *hdc* graphics in a window determined by the skin being used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55a79-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="55a79-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55a79-129">**Esempio Glow**</span><span class="sxs-lookup"><span data-stu-id="55a79-129">**The Glow Sample**</span></span>](the-glow-sample.md)
</dt> </dl>

 

 




