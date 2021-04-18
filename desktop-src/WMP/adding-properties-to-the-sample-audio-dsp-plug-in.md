---
title: Aggiunta di proprietà al plug-in audio DSP di esempio
description: Aggiunta di proprietà al plug-in audio DSP di esempio
ms.assetid: 9c6c2a34-4844-476b-8814-a95a236e75bb
keywords:
- Plug-in di Windows Media Player, DSP audio
- plug-in, audio DSP
- plug-in di elaborazione dei segnali digitali, proprietà audio
- Plug-in DSP, proprietà audio
- plug-in DSP audio, proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d180ab1054631b09997ac986529a641e6ff05ec3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298222"
---
# <a name="adding-properties-to-the-sample-audio-dsp-plug-in"></a><span data-ttu-id="51a95-108">Aggiunta di proprietà al plug-in audio DSP di esempio</span><span class="sxs-lookup"><span data-stu-id="51a95-108">Adding Properties to the Sample Audio DSP Plug-in</span></span>

<span data-ttu-id="51a95-109">Il codice di esempio dell'audio DSP generato dalla procedura guidata per il plug-in di Windows Media Player usa una singola proprietà che rappresenta il fattore di scala per il volume audio.</span><span class="sxs-lookup"><span data-stu-id="51a95-109">The audio DSP sample code that the Windows Media Player Plug-in Wizard generates uses a single property that represents the scale factor for the audio volume.</span></span> <span data-ttu-id="51a95-110">Il plug-in potrebbe richiedere più di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="51a95-110">Your plug-in may require more than one property.</span></span> <span data-ttu-id="51a95-111">È possibile aggiungere facilmente le proprietà al plug-in DSP in Visual Studio attenendosi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="51a95-111">You can easily add properties to your DSP plug-in in Visual Studio using the following steps:</span></span>

-   <span data-ttu-id="51a95-112">Definire i metodi nel codice di definizione dell'interfaccia nel file IDL che fa parte del progetto proxy-stub.</span><span class="sxs-lookup"><span data-stu-id="51a95-112">Define the methods in the interface definition code in the IDL file that is part of the proxy-stub project.</span></span>
    -   <span data-ttu-id="51a95-113">Aggiungere le implementazioni del metodo al file CPP principale del progetto:</span><span class="sxs-lookup"><span data-stu-id="51a95-113">Add the method implementations to the project's main CPP file:</span></span>

    ```C++
    STDMETHODIMP CYourProject::get_color(COLORREF *pColor)
    {
        if ( NULL == pColor )
        {
            return E_POINTER;
        }

        *pColor = m_Color;

        return S_OK;
    }

    STDMETHODIMP CYourProject::put_color(COLORREF newColor)
    {
        m_Color = newColor;
        
        return S_OK;
    }
    
    ```

    

<span data-ttu-id="51a95-114">Infine, per rendere le proprietà accessibili all'utente, è necessario apportare modifiche all'implementazione della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="51a95-114">Finally, to make the properties accessible to the user, you'll want to make changes to the property page implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51a95-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="51a95-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51a95-116">**Implementazione di un plug-in DSP audio**</span><span class="sxs-lookup"><span data-stu-id="51a95-116">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




