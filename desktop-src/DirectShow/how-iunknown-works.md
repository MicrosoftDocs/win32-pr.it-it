---
description: Funzionamento di IUnknown
ms.assetid: 926778a5-e941-4424-8bc0-b50c925fd08b
title: Funzionamento di IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7549ce892e9c0dd3c82f1229a2440f1b930190
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123456"
---
# <a name="how-iunknown-works"></a>Funzionamento di IUnknown

I metodi in **IUnknown** consentono a un'applicazione di eseguire una query per le interfacce del componente e di gestire il conteggio dei riferimenti del componente.

**Conteggio riferimenti**

Il conteggio dei riferimenti è una variabile interna, incrementata nel metodo **AddRef** e decrementata nel metodo di **rilascio** . Le classi base gestiscono il conteggio dei riferimenti e sincronizzano l'accesso al conteggio dei riferimenti tra più thread.

**Query di interfaccia**

Anche l'esecuzione di query per un'interfaccia è semplice. Il chiamante passa due parametri: un identificatore di interfaccia (IID) e l'indirizzo di un puntatore. Se il componente supporta l'interfaccia richiesta, imposta il puntatore sull'interfaccia, incrementa il proprio conteggio dei riferimenti e restituisce S \_ OK. In caso contrario, imposta il puntatore su **null** E restituisce e \_ nointerface. Nello pseudocodice seguente viene illustrato il contorno generale del metodo **QueryInterface** . L'aggregazione di componenti, descritta nella sezione successiva, introduce alcune complessità aggiuntive.


```C++
if (IID == IID_IUnknown)
    set pointer to (IUnknown *)this
    AddRef
    return S_OK

else if (IID == IID_ISomeInterface)
    set pointer to (ISomeInterface *)this
    AddRef
    return S_OK

else if ... 

else
    set pointer to NULL
    return E_NOINTERFACE
```



L'unica differenza tra il metodo **QueryInterface** di un componente e il metodo **QueryInterface** di un altro è l'elenco di IID testati da ogni componente. Per ogni interfaccia supportata dal componente, il componente deve verificare l'IID di tale interfaccia.

**Aggregazione e delega**

L'aggregazione del componente deve essere trasparente per il chiamante. L'aggregazione deve pertanto esporre una singola interfaccia **IUnknown** , con il componente aggregato che fa riferimento all'implementazione del componente esterno. In caso contrario, il chiamante vedrà due interfacce **IUnknown** diverse nella stessa aggregazione. Se il componente non è aggregato, viene utilizzata una propria implementazione.

Per supportare questo comportamento, il componente deve aggiungere un livello di riferimento indiretto. Un *IUnknown* delegante delega il lavoro al posto appropriato: al componente esterno, se presente, o alla versione interna del componente. Un *IUnknown non delegante* esegue l'operazione, come descritto nella sezione precedente.

La versione di delega è Public e mantiene il nome **IUnknown**. La versione non delegante viene rinominata [**INonDelegatingUnknown**](inondelegatingunknown.md). Questo nome non fa parte della specifica COM, perché non è un'interfaccia pubblica.

Quando il client crea un'istanza del componente, chiama il metodo **IClassFactory:: CreateInstance** . Un parametro è un puntatore all'interfaccia **IUnknown** del componente di aggregazione o **null** se la nuova istanza non è aggregata. Il componente usa questo parametro per archiviare una variabile membro che indica l'interfaccia **IUnknown** da usare, come illustrato nell'esempio seguente:


```C++
CMyComponent::CMyComponent(IUnknown *pOuterUnkown)
{
    if (pOuterUnknown == NULL)
        m_pUnknown = (IUnknown *)(INonDelegatingUnknown *)this;
    else
        m_pUnknown = pOuterUnknown;

    [ ... more constructor code ... ]
}
```



Ogni metodo nell' **IUnknown** delegante chiama la rispettiva controparte non delegante, come illustrato nell'esempio seguente:


```C++
HRESULT QueryInterface(REFIID iid, void **ppv) 
{
    return m_pUnknown->QueryInterface(iid, ppv);
}
```



Per la natura della delega, i metodi di delega hanno un aspetto identico in ogni componente. Vengono modificate solo le versioni non deleganti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come implementare IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 



