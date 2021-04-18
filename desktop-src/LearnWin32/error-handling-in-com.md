---
title: Gestione degli errori in COM (introduzione a Win32 e C++)
description: .
ms.assetid: 022ca652-59d2-4513-9d73-1c6d8688c478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505f8cfe6867db07da77616e6a94fdc257e32f3e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300747"
---
# <a name="error-handling-in-com-get-started-with-win32-and-c"></a>Gestione degli errori in COM (introduzione a Win32 e C++)

COM utilizza valori **HRESULT** per indicare l'esito positivo o negativo di un metodo o di una chiamata di funzione. Varie intestazioni SDK definiscono varie costanti **HRESULT** . In WinError. h è definito un set comune di codici a livello di sistema. Nella tabella seguente vengono illustrati alcuni dei codici restituiti a livello di sistema.



| Costante            | Valore numerico | Descrizione                                          |
|---------------------|---------------|------------------------------------------------------|
| **E \_ AccessDenied** | 0x80070005    | Accesso negato.                                       |
| **E \_ non riescono**         | 0x80004005    | Errore non specificato.                                   |
| **E \_ INVALIDARG**   | 0x80070057    | Valore di parametro non valido.                             |
| **E \_ OutOfMemory**  | 0x8007000E    | Memoria insufficiente.                                       |
| **\_puntatore E**      | 0x80004003    | **Null** è stato passato erroneamente per un valore di puntatore. |
| **E \_ imprevisto**   | 0x8000FFFF    | Condizione imprevista.                                |
| **\_OK**           | 0x0           | Esito positivo.                                             |
| **S \_ false**        | 0x1           | Esito positivo.                                             |



 

Tutte le costanti con prefisso "E \_ " sono codici di errore. Le costanti **s \_ OK** e **s \_ false** sono entrambi codici di esito positivo. Probabilmente il 99% di metodi COM restituiscono **S \_ OK** quando hanno esito positivo, ma non consentono di ingannare l'utente. Un metodo può restituire altri codici di esito positivo, quindi testare sempre gli errori usando la macro [**succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded) o [**failed**](/windows/desktop/api/winerror/nf-winerror-failed) . Nell'esempio di codice seguente viene illustrato il modo errato e il modo giusto per verificare l'esito positivo di una chiamata di funzione.


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



Il codice di esito positivo **è \_ false** merita menzione. Alcuni metodi usano **\_ false** per indicare approssimativamente una condizione negativa che non è un errore. Può anche indicare una "no-op", il metodo ha avuto esito positivo, ma non ha avuto alcun effetto. Ad esempio, la funzione [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) restituisce **\_ false** se viene chiamata una seconda volta dallo stesso thread. Se è necessario distinguere tra **s \_ OK** e **s \_ false** nel codice, è necessario testare direttamente il valore, ma usare comunque [**failed**](/windows/desktop/api/winerror/nf-winerror-failed) o [**succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded) per gestire i casi rimanenti, come illustrato nel codice di esempio seguente.


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



Alcuni valori **HRESULT** sono specifici di una particolare funzionalità o sottosistema di Windows. Ad esempio, l'API di grafica Direct2D definisce il codice di errore **D2DERR \_ \_ \_ formato pixel non supportato**, il che significa che il programma ha usato un formato pixel non supportato. La documentazione di MSDN fornisce spesso un elenco di codici di errore specifici che possono essere restituiti da un metodo. Tuttavia, questi elenchi non devono essere considerati definitivi. Un metodo può sempre restituire un valore **HRESULT** non elencato nella documentazione. Utilizzare di nuovo le macro [**succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded) e [**failed**](/windows/desktop/api/winerror/nf-winerror-failed) . Se si verifica un codice di errore specifico, includere anche un case predefinito.


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

In questa sezione vengono esaminati alcuni modelli per la gestione degli errori COM in modo strutturato. Ogni modello presenta vantaggi e svantaggi. In una certa misura, la scelta è un argomento di gusto. Se si lavora su un progetto esistente, è possibile che siano già presenti linee guida per la codifica che proscrivano uno stile specifico. Indipendentemente dal modello adottato, il codice affidabile rispetta le regole seguenti.

-   Per ogni metodo o funzione che restituisce un valore **HRESULT**, controllare il valore restituito prima di procedere.
-   Rilasciare le risorse dopo che sono state usate.
-   Non tentare di accedere a risorse non valide o non inizializzate, ad esempio puntatori **null** .
-   Non tentare di usare una risorsa dopo averla rilasciata.

Tenendo presenti queste regole, di seguito sono illustrati quattro modelli per la gestione degli errori.

-   [IFS annidato](#nested-ifs)
-   [IFS a catena](#cascading-ifs)
-   [Errore di salto](#jump-on-fail)
-   [Genera in errore](#throw-on-fail)

### <a name="nested-ifs"></a>IFS annidato

Dopo ogni chiamata che restituisce un valore **HRESULT**, utilizzare un'istruzione **if** per verificare l'esito positivo. Quindi, inserire la chiamata al metodo successiva nell'ambito dell'istruzione **if** . Più istruzioni **if** possono essere annidate nel modo più approfondito necessario. Gli esempi di codice precedenti in questo modulo hanno usato questo modello, ma qui è di nuovo:


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

-   Le variabili possono essere dichiarate con ambito minimo. Ad esempio, *pItem* non viene dichiarato fino a quando non viene utilizzato.
-   All'interno di ogni istruzione **if** sono soddisfatte determinate invarianti: tutte le chiamate precedenti sono state completate e tutte le risorse acquisite sono ancora valide. Nell'esempio precedente, quando il programma raggiunge l'istruzione **if** più interna, *pItem* e *pFileOpen* sono noti come validi.
-   È chiaro quando rilasciare i puntatori all'interfaccia e altre risorse. Si rilascia una risorsa alla fine dell'istruzione **if** che segue immediatamente la chiamata che ha acquisito la risorsa.

Svantaggi

-   Alcuni utenti trovano molto difficile da leggere.
-   La gestione degli errori è combinata con altre istruzioni di branching e ciclo. Questo può rendere la logica di programma complessiva più difficile da seguire.

### <a name="cascading-ifs"></a>IFS a catena

Dopo ogni chiamata al metodo, utilizzare un'istruzione **if** per verificare l'esito positivo. Se il metodo ha esito positivo, inserire la chiamata al metodo successiva all'interno del blocco **if** . Anziché annidare ulteriori istruzioni **if** , inserire ogni successivo test [**completato**](/windows/desktop/api/winerror/nf-winerror-succeeded) dopo il blocco **if** precedente. Se un metodo ha esito negativo, tutti i test **riusciti** rimanenti hanno esito negativo solo fino a quando non viene raggiunta la fine della funzione.


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



In questo modello le risorse vengono rilasciate alla fine della funzione. Se si verifica un errore, alcuni puntatori potrebbero non essere validi quando la funzione viene chiusa. La chiamata della [**versione**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su un puntatore non valido arresterà in modo anomalo il programma (o peggiori), quindi è necessario inizializzare tutti i puntatori su **null** e verificare se sono **null** prima di rilasciarli. In questo esempio viene utilizzata la `SafeRelease` funzione. i puntatori intelligenti sono anche una scelta ottimale.

Se si usa questo modello, è necessario prestare attenzione ai costrutti di ciclo. All'interno di un ciclo, interrompere il ciclo se una chiamata ha esito negativo.

Vantaggi

-   Questo modello crea meno annidamento rispetto al modello "IFS annidato".
-   Il flusso di controllo generale è più facile da vedere.
-   Le risorse vengono rilasciate in un punto del codice.

Svantaggi

-   Tutte le variabili devono essere dichiarate e inizializzate all'inizio della funzione.
-   Se una chiamata ha esito negativo, la funzione esegue più verifiche degli errori non necessarie, anziché uscire immediatamente dalla funzione.
-   Poiché il flusso di controllo continua con la funzione dopo un errore, è necessario prestare attenzione nel corpo della funzione in modo da non accedere a risorse non valide.
-   Gli errori all'interno di un ciclo richiedono un caso speciale.

### <a name="jump-on-fail"></a>Errore di salto

Dopo ogni chiamata al metodo, verificare la presenza di errori (operazione non riuscita). In caso di errore, passare a un'etichetta accanto alla parte inferiore della funzione. Dopo l'etichetta, ma prima di uscire dalla funzione, rilasciare le risorse.


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

-   Il flusso di controllo generale è facile da vedere.
-   In ogni punto del codice dopo un controllo con [**esito negativo**](/windows/desktop/api/winerror/nf-winerror-failed) , se non è stato eseguito il salto all'etichetta, si garantisce che tutte le chiamate precedenti abbiano avuto esito positivo.
-   Le risorse vengono rilasciate in un'unica posizione nel codice.

Svantaggi

-   Tutte le variabili devono essere dichiarate e inizializzate all'inizio della funzione.
-   Alcuni programmatori non vogliono usare **goto** nel codice. Si noti, tuttavia, che l'uso di **goto** è altamente strutturato. il codice non viene mai saltato all'esterno della chiamata di funzione corrente.
-   le istruzioni **goto** ignorano gli inizializzatori.

### <a name="throw-on-fail"></a>Genera in errore

Anziché passare a un'etichetta, è possibile generare un'eccezione quando un metodo ha esito negativo. Questo può produrre uno stile più linguistico di C++ se si è abituati a scrivere codice indipendente dalle eccezioni.


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



Si noti che in questo esempio viene usata la classe **CComPtr** per gestire i puntatori di interfaccia. In genere, se il codice genera eccezioni, è necessario seguire il modello di RAII (acquisizione di risorse è l'inizializzazione). Ovvero ogni risorsa deve essere gestita da un oggetto il cui distruttore garantisce che la risorsa venga rilasciata correttamente. Se viene generata un'eccezione, è garantita la chiamata al distruttore. In caso contrario, il programma potrebbe perdere risorse.

Vantaggi

-   Compatibile con il codice esistente che usa la gestione delle eccezioni.
-   Compatibile con le librerie C++ che generano eccezioni, ad esempio la libreria STL (Standard Template Library).

Svantaggi

-   Richiede oggetti C++ per gestire risorse quali gli handle di memoria o di file.
-   Richiede una conoscenza corretta della scrittura di codice indipendente dalle eccezioni.

## <a name="next"></a>Prossima

[Modulo 3. Grafica di Windows](module-3---windows-graphics.md)

 

 
