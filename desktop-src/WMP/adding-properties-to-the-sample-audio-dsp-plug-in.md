---
title: Aggiunta di proprietà al plug-in DSP audio di esempio
description: Aggiunta di proprietà al plug-in DSP audio di esempio
ms.assetid: 9c6c2a34-4844-476b-8814-a95a236e75bb
keywords:
- Windows Media Player plug-in audio, DSP audio
- plug-in, DSP audio
- plug-in di elaborazione del segnale digitale, proprietà audio
- Plug-in DSP, proprietà audio
- plug-in audio DSP,proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b87c650ed66bbb3da0886eb02157804ca10005a47053def841996019917ceed8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031501"
---
# <a name="adding-properties-to-the-sample-audio-dsp-plug-in"></a>Aggiunta di proprietà al plug-in DSP audio di esempio

Il codice di esempio DSP audio generato dalla Windows Media Player plug-in audio usa una singola proprietà che rappresenta il fattore di scala per il volume audio. Il plug-in potrebbe richiedere più di una proprietà. È possibile aggiungere facilmente proprietà al plug-in DSP in Visual Studio seguendo questa procedura:

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

 

 




