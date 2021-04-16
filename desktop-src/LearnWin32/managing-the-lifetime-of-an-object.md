---
title: Gestione della durata di un oggetto
description: Informazioni su come gestire i metodi AddRef e Release per controllare la durata di un oggetto.
ms.assetid: 0e522ded-8976-4cdd-9a61-eae7834c896b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 495e657863150612e5b8efa21fff0b00c7a936b9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104557212"
---
# <a name="managing-the-lifetime-of-an-object"></a>Gestione della durata di un oggetto

Esiste una regola per le interfacce COM che non sono ancora state citate. Ogni interfaccia COM deve ereditare, direttamente o indirettamente, da un'interfaccia denominata [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown). Questa interfaccia fornisce alcune funzionalità di base che tutti gli oggetti COM devono supportare.

L'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) definisce tre metodi:

-   [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
-   [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)
-   [**Versione**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)

Il metodo [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) consente a un programma di eseguire query sulle funzionalità dell'oggetto in fase di esecuzione. Nell'argomento successivo verrà richiesto di aggiungere [un oggetto per un'interfaccia](asking-an-object-for-an-interface.md). I metodi [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) vengono usati per controllare la durata di un oggetto. Questo argomento è soggetto a questo argomento.

## <a name="reference-counting"></a>Conteggio dei riferimenti

Qualsiasi altra operazione eseguita da un programma, a un certo punto le risorse vengono allocate e gratuite. L'allocazione di una risorsa è facile. Sapere quando liberare la risorsa è difficile, soprattutto se la durata della risorsa si estende oltre l'ambito corrente. Questo problema non è univoco per COM. Qualsiasi programma che alloca memoria heap deve risolvere lo stesso problema. Ad esempio, C++ usa i distruttori automatici, mentre C# e Java usano Garbage Collection. COM usa un approccio denominato *conteggio dei riferimenti*.

Ogni oggetto COM mantiene un conteggio interno. Questa operazione è nota come conteggio dei riferimenti. Il conteggio dei riferimenti tiene traccia del numero di riferimenti all'oggetto attualmente attivi. Quando il numero di riferimenti scende a zero, l'oggetto viene eliminato automaticamente. L'ultima parte vale la pena di ripetere: l'oggetto Elimina se stesso. L'oggetto non viene mai eliminato in modo esplicito dal programma.

Di seguito sono riportate le regole per il conteggio dei riferimenti:

-   Quando l'oggetto viene creato per la prima volta, il conteggio dei riferimenti è 1. A questo punto, il programma ha un solo puntatore all'oggetto.
-   Il programma può creare un nuovo riferimento duplicando (copiando) il puntatore. Quando si copia il puntatore, è necessario chiamare il metodo [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) dell'oggetto. Questo metodo incrementa di uno il conteggio dei riferimenti.
-   Al termine dell'utilizzo di un puntatore all'oggetto, è necessario chiamare [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release). Il metodo di **rilascio** decrementa il conteggio dei riferimenti di uno. Invalida anche il puntatore. Non usare di nuovo il puntatore dopo la chiamata a **Release**. Se si dispone di altri puntatori allo stesso oggetto, è possibile continuare a usare tali puntatori.
-   Quando è stato chiamato [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) con ogni puntatore, il conteggio dei riferimenti all'oggetto dell'oggetto raggiunge zero e l'oggetto viene eliminato.

Il diagramma seguente mostra un caso semplice, ma tipico.

![Diagramma che mostra un caso semplice di conteggio dei riferimenti.](images/com04.png)

Il programma crea un oggetto e archivia un puntatore (*p*) all'oggetto. A questo punto, il conteggio dei riferimenti è 1. Al termine dell'uso del puntatore, il programma chiama [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release). Il conteggio dei riferimenti viene decrementato a zero e l'oggetto viene eliminato automaticamente. Ora *p* non è valido. Non è possibile utilizzare *p* per altre chiamate al metodo.

Il diagramma seguente mostra un esempio più complesso.

![illustrazione che mostra il conteggio dei riferimenti](images/com05.png)

In questo caso, il programma crea un oggetto e archivia il puntatore *p*, come prima. Successivamente, il programma copia *p* in una nuova variabile, *d*. A questo punto, il programma deve chiamare [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) per incrementare il conteggio dei riferimenti. Il conteggio dei riferimenti è ora 2 e sono presenti due puntatori validi per l'oggetto. Si supponga ora che il programma sia terminato con *p*. Il programma chiama il [**rilascio**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), il conteggio dei riferimenti va a 1 e *p* non è più valido. Tuttavia, *q* è ancora valido. Successivamente, il programma termina con *q*. Quindi chiama di nuovo **Release** . Il conteggio dei riferimenti va a zero e l'oggetto viene eliminato.

Ci si potrebbe chiedere perché il programma copia *p*. Esistono due motivi principali: prima di tutto, è consigliabile archiviare il puntatore in una struttura di dati, ad esempio un elenco. In secondo luogo, è consigliabile lasciare il puntatore oltre l'ambito corrente della variabile originale. Pertanto, è necessario copiarlo in una nuova variabile con ambito più ampio.

Un vantaggio del conteggio dei riferimenti è che è possibile condividere i puntatori in diverse sezioni di codice, senza che i vari percorsi di codice coordinano per eliminare l'oggetto. Al contrario, ogni percorso del codice chiama semplicemente [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) quando il percorso del codice viene eseguito utilizzando l'oggetto. L'oggetto gestisce l'eliminazione di se stesso all'ora corretta.

## <a name="example"></a>Esempio

Di seguito è riportato il codice dall'esempio di finestra di [dialogo Apri](example--the-open-dialog-box.md) .

```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    IFileOpenDialog *pFileOpen;

    hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL,
            IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                PWSTR pszFilePath;
                hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
                if (SUCCEEDED(hr))
                {
                    MessageBox(NULL, pszFilePath, L&quot;File Path&quot;, MB_OK);
                    CoTaskMemFree(pszFilePath);
                }
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    CoUninitialize();
}
````

Il conteggio dei riferimenti viene eseguito in due posizioni in questo codice. Innanzitutto, se il programma crea correttamente l'oggetto finestra di dialogo elemento comune, deve chiamare [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sul puntatore *pFileOpen* .

```C++
hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
        IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

if (SUCCEEDED(hr))
{
    // ...
    pFileOpen->Release();
}
```

In secondo luogo, quando il metodo [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) restituisce un puntatore all'interfaccia [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) , il programma deve chiamare [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sul puntatore *pItem* .

```C++
hr = pFileOpen->GetResult(&pItem);

if (SUCCEEDED(hr))
{
    // ...
    pItem->Release();
}
```

Si noti che in entrambi i casi, la chiamata di [**versione**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) è l'ultima cosa che si verifica prima che il puntatore esca dall'ambito. Si noti inoltre che la **versione** viene chiamata solo dopo aver testato **HRESULT** per l'esito positivo. Se, ad esempio, la chiamata a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ha esito negativo, il puntatore *pFileOpen* non è valido. Quindi, sarebbe un errore chiamare **Release** sul puntatore.

## <a name="next"></a>Prossima

[Richiesta di un oggetto per un'interfaccia](asking-an-object-for-an-interface.md)