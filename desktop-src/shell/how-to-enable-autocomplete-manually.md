---
description: Per ottenere un controllo più dettagliato sul comportamento di completamento automatico o per aggiungere un'origine personalizzata di stringhe di completamento automatico, è necessario gestire manualmente l'oggetto di completamento automatico.
ms.assetid: E1A7B1B0-2879-452E-9EBB-73F02B932200
title: Come abilitare il completamento automatico manualmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee4b327c6ccdd62fd921c56cfb046edb8527bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979570"
---
# <a name="how-to-enable-autocomplete-manually"></a>Come abilitare il completamento automatico manualmente

Per ottenere un controllo più dettagliato sul comportamento di completamento automatico o per aggiungere un'origine personalizzata di stringhe di completamento automatico, è necessario gestire manualmente l'oggetto di completamento automatico. È possibile abilitare il completamento automatico manualmente nei modi seguenti.

## <a name="instructions"></a>Istruzioni

### <a name="creating-a-simple-autocomplete-object"></a>Creazione di un oggetto di completamento automatico semplice

Nei passaggi seguenti viene illustrato come creare e inizializzare un semplice oggetto di completamento automatico. Un oggetto di completamento automatico semplice completa le stringhe da un'unica origine. Il controllo degli errori è stato intenzionalmente omesso in questo esempio.

1.  Creare l'oggetto di completamento automatico.

    ```C++
    IAutoComplete *pac;

    HRESULT hr = CoCreateInstance(CLSID_AutoComplete, 
                                    NULL, 
                                  CLSCTX_INPROC_SERVER,
                                  IID_PPV_ARGS(&pac));
    ```

    

2.  Creare l'origine di completamento automatico. È possibile usare un' [origine di completamento automatico predefinita](ac-ovw.md) oppure è possibile scrivere un'origine personalizzata.

    Nel codice seguente viene utilizzata una delle origini di completamento automatico predefinite.

    ```C++
    IUnknown *punkSource;

    hr = CoCreateInstance(CLSID_ACListISF, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&punkSource));
    ```

    

    Il codice seguente usa un'origine di completamento automatico personalizzata. È possibile scrivere un'origine di completamento automatico personalizzata implementando un oggetto che espone l'interfaccia [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) . L'oggetto può inoltre implementare facoltativamente le interfacce [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) e [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) .

    ```C++
    CCustomAutoCompleteSource *pcacs = new CCustomAutoCompleteSource();

    hr = pcacs->QueryInterface(IID_PPV_ARGS(&punkSource));
    if(SUCCEEDED(hr))
    {
        // ...
    }

    pcacs->Release();
    ```

    

3.  Impostare le opzioni nell'origine completamento automatico (facoltativo).

    È possibile personalizzare il comportamento dell'origine AutoComplete impostando le opzioni se l'origine espone l'interfaccia [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) . Quando si usano le origini di completamento automatico predefinite, solo CLSID \_ ACListISF Esporta **IACList2**. Per un elenco completo delle opzioni e dei relativi valori, vedere [**IACList2:: SetOption**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).

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

    In questo esempio, **hwndEdit** è l'handle della finestra di controllo di modifica per la quale è necessario abilitare la funzionalità di completamento automatico. Per una descrizione degli ultimi due parametri inutilizzati, vedere [**IAutoComplete:: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) .

    ```C++
    hr = pac->Init(hwndEdit, punkSource, NULL, NULL);
    ```

    

5.  Impostare le opzioni dell'oggetto di completamento automatico (facoltativo).

    È possibile personalizzare il comportamento dell'oggetto di completamento automatico impostando le relative opzioni. Per un elenco completo delle opzioni e dei relativi valori, vedere la documentazione di [**IACList2:: SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).

    ```C++
    IAutoComplete2 *pac2;

    hr = pac->QueryInterface(IID_PPV_ARGS(&pac2));

    if (SUCCEEDED(hr))
    {
        hr = pac2->SetOptions(ACO_AUTOSUGGEST);
        pac2->Release();
    }
    ```

    

6.  Rilasciare gli oggetti.

    > [!Note]  
    > L'oggetto di completamento automatico rimane collegato al controllo di modifica anche dopo che è stato rilasciato. Se si prevede di dover accedere successivamente a questi oggetti, se si desidera modificare le opzioni di completamento automatico in un secondo momento, ad esempio, non è necessario rilasciarle a questo punto.

     

    ```C++
    punkSource->Release();
    pac->Release();
    ```

    

### <a name="creating-a-compound-autocomplete-object"></a>Creazione di un oggetto di completamento automatico composto

Un oggetto di completamento automatico composto corrisponde a stringhe da più origini. La barra degli indirizzi di Windows Internet Explorer, ad esempio, utilizza un oggetto di completamento automatico composto perché l'utente potrebbe iniziare a digitare il nome di un file o un URL. La maggior parte dei passaggi necessari per la creazione di un oggetto di completamento automatico composto è identica a quella descritta in "creazione di un oggetto di completamento automatico semplice". Questi passaggi sono indicati come tali.

1.  Creare l'oggetto di completamento automatico. Corrisponde al passaggio 1.

2.  Creare il gestore dell'oggetto di origine composto di completamento automatico.

    L'oggetto di origine composto di completamento automatico consente di combinare più origini di completamento automatico in un'unica origine di completamento automatico.

    ```C++
    IObjMgr *pom;

    hr = CoCreateInstance(CLSID_ACLMulti, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pom));
    ```

    

3.  Creare e impostare le opzioni per ognuna delle origini di completamento automatico. Ripetere i passaggi 2 e 3 sopra per ogni origine.

4.  Alleghi ogni origine di completamento automatico a gestione oggetti di origine.

    ```C++
    hr = pom->Append(punkSource1);
    hr = pom->Append(punkSource2);
    ```

    

5.  Inizializzare l'oggetto di completamento automatico.

    Questo è lo stesso del passaggio 4 precedente, ad eccezione del fatto che anziché passare la semplice origine di completamento automatico a [**IAutoComplete:: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init), si passa il gestore oggetti di origine composto.

    ```C++
    hr = pac->Init(hwndEdit, pom, NULL, NULL);
    ```

    

6.  Impostare le opzioni dell'oggetto di completamento automatico. Questo è lo stesso del passaggio 5 riportato sopra.

7.  Rilasciare gli oggetti.

    Come nel caso più semplice, è possibile rilasciare gli oggetti non appena ne è stata completata l'uso, ma è possibile conservarli anche per modificare le opzioni in un secondo momento.

    ```C++
    pac->Release();
    pom->Release();

    // Release each individual source.
    punkSource1->Release(); 
    punkSource2->Release();
    ```

    

 

 
