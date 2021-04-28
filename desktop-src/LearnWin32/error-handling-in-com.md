---
title: Gestione degli errori in COM (Introduzione a Win32 e C++)
description: Gestione degli errori in COM (Introduzione a Win32 e C++)
ms.assetid: 022ca652-59d2-4513-9d73-1c6d8688c478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69cf89170087469fa6ef8587fb5377e6374f6a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103919"
---
# <a name="error-handling-in-com-get-started-with-win32-and-c"></a>Gestione degli errori in COM (Introduzione a Win32 e C++)

COM usa **i valori HRESULT** per indicare l'esito positivo o negativo di una chiamata di metodo o funzione. Varie intestazioni SDK definiscono diverse **costanti HRESULT.** Un set comune di codici a livello di sistema è definito in WinError.h. La tabella seguente illustra alcuni di questi codici restituiti a livello di sistema.



| Costante            | Valore numerico | Descrizione                                          |
|---------------------|---------------|------------------------------------------------------|
| **E \_ ACCESSO NEGATO** | 0x80070005    | Accesso negato.                                       |
| **E \_ FAIL**         | 0x80004005    | Errore non specificato.                                   |
| **E \_ INVALIDARG**   | 0x80070057    | Valore del parametro non valido.                             |
| **E \_ OUTOFMEMORY**  | 0x8007000E    | Memoria insufficiente.                                       |
| **PUNTATORE \_ E**      | 0x80004003    | **Null è** stato passato in modo non corretto per un valore del puntatore. |
| **E \_ UNEXPECTED**   | 0x8000FFFF    | Condizione imprevista.                                |
| **S \_ OK**           | 0x0           | Operazione completata.                                             |
| **S \_ FALSE**        | 0x1           | Operazione completata.                                             |



 

Tutte le costanti con il prefisso \_ "E" sono codici di errore. Le costanti **S \_ OK e** S **\_ FALSE** sono entrambe codici di esito positivo. Probabilmente il 99% dei metodi COM restituisce **S \_ OK** quando hanno esito positivo, ma non lasciare che questo fatto sia un errore. Un metodo potrebbe restituire altri codici di esito positivo, quindi verificare sempre la presenza di errori usando la macro [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) [**o FAILED.**](/windows/desktop/api/winerror/nf-winerror-failed) Il codice di esempio seguente illustra il modo errato e il modo corretto per testare l'esito positivo di una chiamata di funzione.


```C++
// Wrong.
HRESULT hr = SomeFunction();
if (hr != S_OK)
{
    printf("Error!\n"); // Bad. hr might be another success code.
}

// Right.
HRESULT hr = SomeFunction();
if (FAILED(hr))
{
    printf("Error!\n"); 
}
```



Il codice di **esito positivo S \_ FALSE** merita menzione. Alcuni metodi usano **S \_ FALSE** per indicare approssimativamente una condizione negativa che non è un errore. Può anche indicare una "no-op", ovvero il metodo ha avuto esito positivo, ma non ha avuto alcun effetto. Ad esempio, la [**funzione CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) restituisce **S \_ FALSE** se viene chiamata una seconda volta dallo stesso thread. Se è necessario distinguere **tra S \_ OK** e **S \_ FALSE** nel codice, è necessario testare direttamente il valore, ma usare [**ANCORA FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) o [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) per gestire i case rimanenti, come illustrato nel codice di esempio seguente.


```C++
if (hr == S_FALSE)
{
    // Handle special case.
}
else if (SUCCEEDED(hr))
{
    // Handle general success case.
}
else
{
    // Handle errors.
    printf("Error!\n"); 
}
```



Alcuni **valori HRESULT** sono specifici di una particolare funzionalità o sottosistema di Windows. Ad esempio, l'API grafica Direct2D definisce il codice di errore **D2DERR \_ UNSUPPORTED \_ PIXEL \_ FORMAT**, il che significa che il programma ha usato un formato pixel non supportato. La documentazione MSDN fornisce spesso un elenco di codici di errore specifici che un metodo potrebbe restituire. Tuttavia, non è consigliabile considerare questi elenchi come definitivi. Un metodo può sempre restituire un **valore HRESULT** non elencato nella documentazione. Anche in questo caso, usare le macro [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) [**e FAILED.**](/windows/desktop/api/winerror/nf-winerror-failed) Se si verifica un codice di errore specifico, includere anche un case predefinito.


```C++
if (hr == D2DERR_UNSUPPORTED_PIXEL_FORMAT)
{
    // Handle the specific case of an unsupported pixel format.
}
else if (FAILED(hr))
{
    // Handle other errors.
}
```



## <a name="patterns-for-error-handling"></a>Modelli per la gestione degli errori

Questa sezione esamina alcuni modelli per la gestione degli errori COM in modo strutturato. Ogni modello presenta vantaggi e svantaggi. In una certa misura, la scelta è una questione di assaggio. Se si lavora a un progetto esistente, è possibile che le linee guida per la scrittura del codice procrivano uno stile specifico. Indipendentemente dal modello adottato, un codice affidabile rispetta le regole seguenti.

-   Per ogni metodo o funzione che restituisce **un HRESULT,** controllare il valore restituito prima di procedere.
-   Rilasciare le risorse dopo che sono state usate.
-   Non tentare di accedere a risorse non valide o non inizializzate, ad esempio **puntatori NULL.**
-   Non provare a usare una risorsa dopo il rilascio.

Tenere presenti queste regole, ecco quattro modelli per la gestione degli errori.

-   [If annidati](#nested-ifs)
-   [If a catena](#cascading-ifs)
-   [Jump on Fail](#jump-on-fail)
-   [Genera in caso di errore](#throw-on-fail)

### <a name="nested-ifs"></a>If annidati

Dopo ogni chiamata che restituisce un **valore HRESULT,** usare un'istruzione **if** per verificare l'esito positivo. Inserire quindi la chiamata al metodo successiva nell'ambito **dell'istruzione if.** Più **istruzioni if** possono essere annidate in base alle esigenze. Gli esempi di codice precedenti in questo modulo hanno usato tutti questo modello, ma eccolo di nuovo:


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                // Use pItem (not shown). 
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    return hr;
}
```



Vantaggi

-   Le variabili possono essere dichiarate con ambito minimo. Ad esempio, *pItem non* viene dichiarato fino a quando non viene usato.
-   All'interno di ogni istruzione **if,** alcune invarianti sono vere: tutte le chiamate precedenti hanno avuto esito positivo e tutte le risorse acquisite sono ancora valide. Nell'esempio precedente, quando il programma raggiunge l'istruzione **if** più interna, sia *pItem* che *pFileOpen* sono noti come validi.
-   È chiaro quando rilasciare puntatori a interfaccia e altre risorse. Si rilascia una risorsa alla fine dell'istruzione **if** che segue immediatamente la chiamata che ha acquisito la risorsa.

Svantaggi

-   Alcuni utenti trovano difficile leggere l'annidamento profondo.
-   La gestione degli errori è mista ad altre istruzioni di diramazione e ciclo. Ciò può rendere la logica complessiva del programma più difficile da seguire.

### <a name="cascading-ifs"></a>If a catena

Dopo ogni chiamata al metodo, usare **un'istruzione if** per verificare l'esito positivo. Se il metodo ha esito positivo, inserire la chiamata al metodo successiva all'interno del **blocco if.** Invece di annidare ulteriormente le **istruzioni if,** inserire ogni test [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) successivo dopo il blocco **if** precedente. Se un metodo ha esito negativo, tutti i test **SUCCEEDED** rimanenti hanno semplicemente esito negativo fino a quando non viene raggiunta la parte inferiore della funzione.


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->GetResult(&pItem);
    }
    if (SUCCEEDED(hr))
    {
        // Use pItem (not shown).
    }

    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



In questo modello le risorse vengono rilasciate alla fine della funzione. Se si verifica un errore, alcuni puntatori potrebbero non essere validi quando la funzione viene chiusa. La [**chiamata di Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su un puntatore non valido arresterà il programma in modo anomalo (o peggiore), quindi è necessario inizializzare tutti i puntatori su **NULL** e verificare se sono **NULL** prima di rilasciarli. In questo esempio viene utilizzata la funzione . Anche i puntatori intelligenti `SafeRelease` sono una buona scelta.

Se si usa questo modello, è necessario prestare attenzione ai costrutti di ciclo. All'interno di un ciclo interrompere il ciclo se una chiamata ha esito negativo.

Vantaggi

-   Questo modello crea meno annidamento rispetto al modello "ifs annidato".
-   Il flusso di controllo complessivo è più facile da visualizzare.
-   Le risorse vengono rilasciate in un punto del codice.

Svantaggi

-   Tutte le variabili devono essere dichiarate e inizializzate all'inizio della funzione.
-   Se una chiamata non riesce, la funzione esegue più controlli degli errori non necessario, invece di uscire immediatamente dalla funzione.
-   Poiché il flusso di controllo continua attraverso la funzione dopo un errore, è necessario prestare attenzione in tutto il corpo della funzione a non accedere alle risorse non valide.
-   Gli errori all'interno di un ciclo richiedono un caso speciale.

### <a name="jump-on-fail"></a>Jump on Fail

Dopo ogni chiamata al metodo, verificare l'esito negativo (operazione non riuscita). In caso di errore, passare a un'etichetta nella parte inferiore della funzione. Dopo l'etichetta, ma prima di uscire dalla funzione, rilasciare le risorse.


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->Show(NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->GetResult(&pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use pItem (not shown).

done:
    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



Vantaggi

-   Il flusso di controllo complessivo è facile da vedere.
-   In ogni punto del codice dopo un controllo [**FAILED,**](/windows/desktop/api/winerror/nf-winerror-failed) se non è stato possibile passare all'etichetta, è garantito che tutte le chiamate precedenti hanno avuto esito positivo.
-   Le risorse vengono rilasciate in un'unica posizione nel codice.

Svantaggi

-   Tutte le variabili devono essere dichiarate e inizializzate all'inizio della funzione.
-   Alcuni programmatori non desiderano usare **goto** nel codice. Si noti tuttavia che questo uso di **goto** è altamente strutturato. Il codice non passa mai al di fuori della chiamata di funzione corrente.
-   **Le istruzioni goto** ignorano gli inizializzatori.

### <a name="throw-on-fail"></a>Genera in caso di errore

Anziché passare a un'etichetta, è possibile generare un'eccezione quando un metodo ha esito negativo. Questo può produrre uno stile più idiomatico di C++ se si è usati per scrivere codice indipendente da eccezioni.


```C++
#include <comdef.h>  // Declares _com_error

inline void throw_if_fail(HRESULT hr)
{
    if (FAILED(hr))
    {
        throw _com_error(hr);
    }
}

void ShowDialog()
{
    try
    {
        CComPtr<IFileOpenDialog> pFileOpen;
        throw_if_fail(CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen)));

        throw_if_fail(pFileOpen->Show(NULL));

        CComPtr<IShellItem> pItem;
        throw_if_fail(pFileOpen->GetResult(&pItem));

        // Use pItem (not shown).
    }
    catch (_com_error err)
    {
        // Handle error.
    }
}
```



Si noti che questo esempio usa la **classe CComPtr** per gestire i puntatori a interfaccia. In genere, se il codice genera eccezioni, è necessario seguire il modello RAII (Resource Acquisition is Initialization). Ciò significa che ogni risorsa deve essere gestita da un oggetto il cui distruttore garantisce che la risorsa venga rilasciata correttamente. Se viene generata un'eccezione, viene garantito che il distruttore sia richiamato. In caso contrario, il programma potrebbe perdere risorse.

Vantaggi

-   Compatibile con il codice esistente che usa la gestione delle eccezioni.
-   Compatibile con le librerie C++ che generano eccezioni, ad esempio la libreria STL (Standard Template Library).

Svantaggi

-   Richiede oggetti C++ per gestire risorse come la memoria o gli handle di file.
-   Richiede una buona conoscenza di come scrivere codice indipendente da eccezioni.

## <a name="next"></a>Prossima

[Modulo 3. Grafica Di Windows](module-3---windows-graphics.md)

 

 
