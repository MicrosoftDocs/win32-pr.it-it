---
title: Aggiunta della proprietà Wet Mix
description: Aggiunta della proprietà Wet Mix
ms.assetid: 4605d893-8ac0-42fd-a1ac-51430561f174
keywords:
- Plug-in di Windows Media Player, proprietà di esempio Echo
- plug-in, proprietà di esempio Echo
- plug-in di elaborazione dei segnali digitali, proprietà di esempio Echo
- Plug-in DSP, proprietà di esempio Echo
- Esempio di plug-in Echo DSP, proprietà
- Esempio di plug-in Echo DSP, proprietà Wet Mix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6af8e7b4857ccbf6b725044575d1b8524aaf50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330095"
---
# <a name="adding-the-wet-mix-property"></a>Aggiunta della proprietà Wet Mix

È necessario aggiungere il codice per fornire la proprietà aggiuntiva per il livello di effetto.

Nella sezione [aggiunta di proprietà al plug-in audio DSP di esempio](adding-properties-to-the-sample-audio-dsp-plug-in.md) vengono fornite informazioni dettagliate su come aggiungere una nuova proprietà utilizzando Visual C++. Questa sezione illustra come aggiungere il codice manualmente. Questa operazione comporta l'aggiunta di codice nelle stesse tre posizioni in cui è stato modificato il codice per la proprietà tempo di ritardo.

Aggiungere i prototipi per i \_ metodi Get WETMIX e put \_ WETMIX immediatamente dopo gli altri prototipi di metodo di proprietà in Echo. h. Usare la sintassi seguente:


```C++
STDMETHOD(get_wetmix)(double *pVal);
STDMETHOD(put_wetmix)(double newVal);

```



A questo punto, aggiungere l'implementazione per ogni metodo immediatamente dopo le altre implementazioni di proprietà in Echo. cpp. Nell'esempio seguente viene illustrato il codice per entrambi i metodi:


```C++
// Property get to retrieve the wet mix value by using the public interface.
STDMETHODIMP CEcho::get_wetmix(double *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_fWetMix;

    return S_OK;
}

// Property put to store the wet mix value by using the public interface.
STDMETHODIMP CEcho::put_wetmix(double newVal)
{
    m_fWetMix = newVal;

    // Calculate m_fDryMix
    m_fDryMix = 1.0 - m_fWetMix;
    
    return S_OK;
}

```



Si noti che l'implementazione di put \_ WETMIX include il codice per calcolare il valore corretto per m \_ fDryMix. Ogni volta che viene specificato un nuovo valore per m \_ fWetMix, questo calcolo è obbligatorio.

Aggiungere il codice seguente nella definizione dell'interfaccia subito dopo il codice per i metodi Delay in Echo. idl:


```C++
HRESULT get_wetmix([out] double *pVal);
HRESULT put_wetmix([in] double newVal);

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Proprietà di esempio Echo**](echo-sample-properties.md)
</dt> </dl>

 

 




