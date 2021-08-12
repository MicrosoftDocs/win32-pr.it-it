---
title: Modifica della proprietà Scale
description: Modifica della proprietà Scale
ms.assetid: 32ebaa54-ed13-4b10-8876-bf8e188d7317
keywords:
- Windows Media Player plug-in, proprietà di esempio Echo
- plug-in, proprietà di esempio Echo
- plug-in di elaborazione del segnale digitale, proprietà dell'esempio Echo
- Plug-in DSP, proprietà di esempio Echo
- Esempio di plug-in Echo DSP, proprietà scale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10073e01213469dcb6a85ddffd378421fddb6ae8f2fd432b9822c3a5046fdd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574618"
---
# <a name="modifying-the-scale-property"></a>Modifica della proprietà Scale

L'implementazione predefinita della procedura guidata espone la proprietà scale. È invece possibile modificare l'implementazione esistente per esporre la proprietà delay time.

Usare prima di tutto l'esempio seguente per modificare i prototipi di funzione per ottenere \_ la scalabilità \_ e inserire la scala in Echo.h. Modificare il nome dei metodi e i tipi di dati per i parametri:


```C++
// IEcho methods
STDMETHOD(get_delay)(DWORD *pVal);
STDMETHOD(put_delay)(DWORD newVal);

```



Modificare quindi le implementazioni dei metodi get \_ scale e put scale in \_ Echo.cpp. Fare in modo che il codice corrisponda agli esempi seguenti:


```C++
// Formerly get_scale
STDMETHODIMP CEcho::get_delay(DWORD *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_dwDelayTime;

    return S_OK;
}

// Formerly put_scale
STDMETHODIMP CEcho::put_delay(DWORD newVal)
{
    m_dwDelayTime = newVal;

    return S_OK;
}

```



Il codice di esempio precedente modifica i nomi dei metodi e i tipi di dati dei parametri. Il nome della variabile membro deve essere stato modificato in precedenza. Ricordarsi di modificare anche i commenti che introducono ogni metodo.

Modificare ora la definizione dell'interfaccia. Il codice seguente sostituisce il codice nella dichiarazione dell'interfaccia IEcho in Echo.idl:


```C++
HRESULT get_delay([out] DWORD *pVal);
HRESULT put_delay([in] DWORD newVal);

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Proprietà dell'esempio Echo**](echo-sample-properties.md)
</dt> </dl>

 

 




