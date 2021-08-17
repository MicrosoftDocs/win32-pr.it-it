---
description: Funzionamento di IUnknown
ms.assetid: 926778a5-e941-4424-8bc0-b50c925fd08b
title: Funzionamento di IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1523a8de5d9b99df60ebaff540d4bf9468799e3be1361a4be111f15a142bbea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015589"
---
# <a name="how-iunknown-works"></a>Funzionamento di IUnknown

I metodi in **IUnknown consentono** a un'applicazione di eseguire una query per le interfacce sul componente e di gestire il conteggio dei riferimenti del componente.

**Conteggio dei riferimenti**

Il conteggio dei riferimenti è una variabile interna, incrementata nel **metodo AddRef** e decrementata nel **metodo Release.** Le classi di base gestiscono il conteggio dei riferimenti e sincronizzano l'accesso al conteggio dei riferimenti tra più thread.

**Query di interfaccia**

Anche l'esecuzione di query per un'interfaccia è semplice. Il chiamante passa due parametri: un identificatore di interfaccia (IID) e l'indirizzo di un puntatore. Se il componente supporta l'interfaccia richiesta, imposta il puntatore all'interfaccia, incrementa il conteggio dei riferimenti e restituisce S \_ OK. In caso contrario, imposta il puntatore **su NULL** e restituisce E \_ NOINTERFACE. Lo pseudocodice seguente illustra la struttura generale del **metodo QueryInterface.** L'aggregazione dei componenti, descritta nella sezione successiva, introduce alcune complessità aggiuntive.


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



L'unica differenza tra il **metodo QueryInterface** di un componente e il metodo **QueryInterface** di un altro è l'elenco di ID che ogni componente testa. Per ogni interfaccia che il componente supporta, il componente deve testare l'IID di tale interfaccia.

**Aggregazione e delega**

L'aggregazione dei componenti deve essere trasparente per il chiamante. Pertanto, l'aggregazione deve esporre una singola **interfaccia IUnknown,** con il componente aggregato che rinvia l'implementazione del componente esterno. In caso contrario, il chiamante visualizza due interfacce **IUnknown** diverse nella stessa aggregazione. Se il componente non è aggregato, usa la propria implementazione.

Per supportare questo comportamento, il componente deve aggiungere un livello di riferimento indiretto. Un *oggetto IUnknown* delega il lavoro alla posizione appropriata: al componente esterno, se presente, o alla versione interna del componente. Un *IUnknown non recapitante* esegue il lavoro, come descritto nella sezione precedente.

La versione delegata è pubblica e mantiene il **nome IUnknown**. La versione non recapitante viene rinominata [**INonDelegatingUnknown**](inondelegatingunknown.md). Questo nome non fa parte della specifica COM, perché non è un'interfaccia pubblica.

Quando il client crea un'istanza del componente, chiama il **metodo IClassFactory::CreateInstance.** Un parametro è un puntatore all'interfaccia **IUnknown** del componente di aggregazione oppure **NULL** se la nuova istanza non è aggregata. Il componente usa questo parametro per archiviare una variabile membro che indica quale **interfaccia IUnknown** usare, come illustrato nell'esempio seguente:


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



Ogni metodo in **IUnknown delegante** chiama la controparte non delegante, come illustrato nell'esempio seguente:


```C++
HRESULT QueryInterface(REFIID iid, void **ppv) 
{
    return m_pUnknown->QueryInterface(iid, ppv);
}
```



Per natura della delega, i metodi di delega hanno un aspetto identico in ogni componente. Cambiano solo le versioni non di consegna.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come implementare IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 



