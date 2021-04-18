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
# <a name="adding-properties-to-the-sample-audio-dsp-plug-in"></a>Aggiunta di proprietà al plug-in audio DSP di esempio

Il codice di esempio dell'audio DSP generato dalla procedura guidata per il plug-in di Windows Media Player usa una singola proprietà che rappresenta il fattore di scala per il volume audio. Il plug-in potrebbe richiedere più di una proprietà. È possibile aggiungere facilmente le proprietà al plug-in DSP in Visual Studio attenendosi alla procedura seguente:

-   Definire i metodi nel codice di definizione dell'interfaccia nel file IDL che fa parte del progetto proxy-stub.
    -   Aggiungere le implementazioni del metodo al file CPP principale del progetto:

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

    

Infine, per rendere le proprietà accessibili all'utente, è necessario apportare modifiche all'implementazione della pagina delle proprietà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di un plug-in DSP audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




