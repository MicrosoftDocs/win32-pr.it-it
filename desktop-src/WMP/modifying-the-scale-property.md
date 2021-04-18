---
title: Modifica della proprietà scale
description: Modifica della proprietà scale
ms.assetid: 32ebaa54-ed13-4b10-8876-bf8e188d7317
keywords:
- Plug-in di Windows Media Player, proprietà di esempio Echo
- plug-in, proprietà di esempio Echo
- plug-in di elaborazione dei segnali digitali, proprietà di esempio Echo
- Plug-in DSP, proprietà di esempio Echo
- Esempio di plug-in Echo DSP, proprietà scale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd91e2315db9d0d1e14d2aec55f79a8b05c442ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298087"
---
# <a name="modifying-the-scale-property"></a>Modifica della proprietà scale

L'implementazione della procedura guidata predefinita espone la proprietà scale. È possibile modificare l'implementazione esistente per esporre la proprietà tempo di ritardo.

Per prima cosa, usare l'esempio seguente per modificare i prototipi di funzione per Get \_ scale e put \_ scale in Echo. h. Modificare il nome dei metodi e i tipi di dati per i parametri:


```C++
// IEcho methods
STDMETHOD(get_delay)(DWORD *pVal);
STDMETHOD(put_delay)(DWORD newVal);

```



Modificare quindi le implementazioni dei \_ metodi Get scale e put \_ scale in Echo. cpp. Fare in modo che il codice corrisponda agli esempi seguenti:


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



Il codice di esempio precedente modifica i nomi dei metodi e i tipi di dati dei parametri. Il nome della variabile membro deve essere stato modificato in precedenza. Ricordarsi di modificare i commenti che introducono anche ogni metodo.

A questo punto, modificare la definizione dell'interfaccia. Il codice seguente sostituisce il codice nella dichiarazione dell'interfaccia IEcho in Echo. idl:


```C++
HRESULT get_delay([out] DWORD *pVal);
HRESULT put_delay([in] DWORD newVal);

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Proprietà di esempio Echo**](echo-sample-properties.md)
</dt> </dl>

 

 




