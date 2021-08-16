---
description: Per ottenere un controllo più dettagliato sul comportamento del completamento automatico o per aggiungere un'origine personalizzata di stringhe di completamento automatico, è necessario gestire manualmente l'oggetto di completamento automatico.
ms.assetid: E1A7B1B0-2879-452E-9EBB-73F02B932200
title: Come abilitare il completamento automatico manualmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7df686e4c5a4a6e96b1faf82e4926dffc73398b360e3e6235d6a61451eae189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859708"
---
# <a name="how-to-enable-autocomplete-manually"></a>Come abilitare il completamento automatico manualmente

Per ottenere un controllo più dettagliato sul comportamento del completamento automatico o per aggiungere un'origine personalizzata di stringhe di completamento automatico, è necessario gestire manualmente l'oggetto di completamento automatico. È possibile abilitare il completamento automatico manualmente nei modi seguenti.

## <a name="instructions"></a>Istruzioni

### <a name="creating-a-simple-autocomplete-object"></a>Creazione di un oggetto di completamento automatico semplice

La procedura seguente illustra come creare e inizializzare un semplice oggetto di completamento automatico. Un semplice oggetto di completamento automatico completa le stringhe da una singola origine. In questo esempio il controllo degli errori è stato intenzionalmente omesso.

1.  Creare l'oggetto di completamento automatico.

    ```C++
    IAutoComplete *pac;

    HRESULT hr = CoCreateInstance(CLSID_AutoComplete, 
                                    NULL, 
                                  CLSCTX_INPROC_SERVER,
                                  IID_PPV_ARGS(&pac));
    ```

    

2.  Creare l'origine di completamento automatico. È possibile usare [un'origine predefinita di completamento automatico](ac-ovw.md) oppure scrivere un'origine personalizzata.

    Nel codice seguente viene utilizzata una delle origini predefinite di completamento automatico.

    ```C++
    IUnknown *punkSource;

    hr = CoCreateInstance(CLSID_ACListISF, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&punkSource));
    ```

    

    Il codice seguente usa un'origine di completamento automatico personalizzata. È possibile scrivere un'origine di completamento automatico personalizzata implementando un oggetto che espone [**l'interfaccia IEnumString.**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) L'oggetto può anche implementare facoltativamente [**le interfacce IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) e [**IACList2.**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)

    ```C++
    CCustomAutoCompleteSource *pcacs = new CCustomAutoCompleteSource();

    hr = pcacs->QueryInterface(IID_PPV_ARGS(&punkSource));
    if(SUCCEEDED(hr))
    {
        // ...
    }

    pcacs->Release();
    ```

    

3.  Impostare le opzioni nell'origine di completamento automatico (facoltativo).

    È possibile personalizzare il comportamento dell'origine di completamento automatico impostandone le opzioni se l'origine espone [**l'interfaccia IACList2.**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) Quando si usano le origini predefinite di completamento automatico, solo CLSID \_ ACListISF esporta **IACList2.** Per un elenco completo delle opzioni e dei relativi valori, vedere [**IACList2::SetOptions.**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions)

    ```C++
    IACList2 *pal2;

    hr = punkSource->QueryInterface(IID_PPV_ARGS(&pal2));
    if (SUCCEEDED(hr))
    {
        hr = pal2->SetOptions(ACLO_FILESYSONLY);
        pal2->Release();
    }
    ```

    

4.  Inizializzare l'oggetto di completamento automatico.

    In questo esempio **hwndEdit è** l'handle della finestra di controllo di modifica per la quale deve essere abilitato il completamento automatico. Per una descrizione dei due parametri inutilizzati finali, vedere [**IAutoComplete::Init.**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init)

    ```C++
    hr = pac->Init(hwndEdit, punkSource, NULL, NULL);
    ```

    

5.  Impostare le opzioni dell'oggetto di completamento automatico (facoltativo).

    È possibile personalizzare il comportamento dell'oggetto di completamento automatico impostandone le opzioni. Per un elenco completo delle opzioni e dei relativi valori, vedere la documentazione per [**IACList2::SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).

    ```C++
    IAutoComplete2 *pac2;

    hr = pac->QueryInterface(IID_PPV_ARGS(&pac2));

    if (SUCCEEDED(hr))
    {
        hr = pac2->SetOptions(ACO_AUTOSUGGEST);
        pac2->Release();
    }
    ```

    

6.  Rilasciare gli oggetti .

    > [!Note]  
    > L'oggetto di completamento automatico rimane associato al controllo di modifica anche dopo il rilascio. Se si prevede di dover accedere a questi oggetti in un secondo momento, ad esempio se si vogliono modificare le opzioni di completamento automatico in un secondo momento, non è necessario rilasciarli a questo punto.

     

    ```C++
    punkSource->Release();
    pac->Release();
    ```

    

### <a name="creating-a-compound-autocomplete-object"></a>Creazione di un oggetto di completamento automatico composto

Un oggetto di completamento automatico composto corrisponde a stringhe provenienti da più origini. Ad esempio, la barra Windows Internet Explorer indirizzo usa un oggetto di completamento automatico composto perché l'utente potrebbe iniziare a digitare il nome di un file o di un URL. La maggior parte dei passaggi necessari per la creazione di un oggetto di completamento automatico composto è identica alla procedura descritta in "Creazione di un oggetto di completamento automatico semplice". Questi passaggi sono indicati come tali.

1.  Creare l'oggetto di completamento automatico. Questo è lo stesso del passaggio 1 precedente.

2.  Creare il gestore di oggetti di origine composto di completamento automatico.

    L'oggetto di origine composto di completamento automatico consente di combinare più origini di completamento automatico in un'unica origine di completamento automatico.

    ```C++
    IObjMgr *pom;

    hr = CoCreateInstance(CLSID_ACLMulti, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pom));
    ```

    

3.  Creare e impostare opzioni per ognuna delle origini di completamento automatico. Ripetere i passaggi 2 e 3 precedenti per ogni origine.

4.  Collegare ogni origine di completamento automatico al gestore oggetti di origine.

    ```C++
    hr = pom->Append(punkSource1);
    hr = pom->Append(punkSource2);
    ```

    

5.  Inizializzare l'oggetto di completamento automatico.

    È uguale al passaggio 4 precedente, ad eccezione del fatto che invece di passare l'origine di completamento automatico semplice a [**IAutoComplete::Init,**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init)si passa il gestore di oggetti di origine composto.

    ```C++
    hr = pac->Init(hwndEdit, pom, NULL, NULL);
    ```

    

6.  Impostare le opzioni dell'oggetto di completamento automatico. Questo è lo stesso del passaggio 5 precedente.

7.  Rilasciare gli oggetti .

    Come nel caso semplice, è possibile rilasciare gli oggetti non appena si è terminato di usarli, ma è anche possibile conservarli per modificare le opzioni in un secondo momento.

    ```C++
    pac->Release();
    pom->Release();

    // Release each individual source.
    punkSource1->Release(); 
    punkSource2->Release();
    ```

    

 

 
