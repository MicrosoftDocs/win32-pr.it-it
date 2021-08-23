---
title: Aggiunta della proprietà Wet Mix
description: Aggiunta della proprietà Wet Mix
ms.assetid: 4605d893-8ac0-42fd-a1ac-51430561f174
keywords:
- Windows Media Player plug-in, proprietà di esempio Echo
- plug-in, proprietà di esempio Echo
- plug-in di elaborazione del segnale digitale, proprietà dell'esempio Echo
- Plug-in DSP, proprietà di esempio Echo
- Esempio di plug-in Echo DSP, proprietà
- Esempio di plug-in Echo DSP, proprietà della combinazione wet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f743cc25ce25aed1e7ff5695c022d65e30c1680eee4121eb3952698d6f0da94f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055419"
---
# <a name="adding-the-wet-mix-property"></a>Aggiunta della proprietà Wet Mix

È necessario aggiungere il codice per fornire la proprietà aggiuntiva per il livello di effetto.

La sezione [Aggiunta di proprietà al plug-in DSP audio](adding-properties-to-the-sample-audio-dsp-plug-in.md) di esempio fornisce informazioni dettagliate su come aggiungere una nuova proprietà usando Visual C++. Questa sezione illustra come aggiungere manualmente il codice. Ciò comporta l'aggiunta di codice nelle stesse tre posizioni in cui è stato modificato il codice per la proprietà delay time.

Aggiungere i prototipi per i metodi get wetmix e inserire i metodi wetmix immediatamente dopo gli altri prototipi di metodo di \_ \_ proprietà in Echo.h. Usare la sintassi seguente:


```C++
STDMETHOD(get_wetmix)(double *pVal);
STDMETHOD(put_wetmix)(double newVal);

```



Aggiungere ora l'implementazione per ogni metodo immediatamente dopo le altre implementazioni di proprietà in Echo.cpp. L'esempio seguente illustra il codice per entrambi i metodi:


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



Si noti che l'implementazione di put \_ wetmix include il codice per calcolare il valore corretto per m \_ fDryMix. Ogni volta che viene specificato un nuovo valore per m \_ fWetMix, questo calcolo è obbligatorio.

Aggiungere il codice seguente nella definizione dell'interfaccia subito dopo il codice per i metodi delay in Echo.idl:


```C++
HRESULT get_wetmix([out] double *pVal);
HRESULT put_wetmix([in] double newVal);

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Proprietà dell'esempio Echo**](echo-sample-properties.md)
</dt> </dl>

 

 




