---
title: Procedure di scrittura del codice COM
description: In questo argomento vengono descritti i modi per rendere il codice COM più efficace e affidabile.
ms.assetid: 76aca556-b4d6-4e67-a2a3-4439900f0c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93febc4ee3dfd4f05f20fae8078bc2a5ebb7f9623a860f49ec9cd6ce4e69b95a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913890"
---
# <a name="com-coding-practices"></a>Procedure di scrittura del codice COM

In questo argomento vengono descritti i modi per rendere il codice COM più efficace e affidabile.

-   [Operatore \_ \_ uuidof](/windows)
-   [The IID \_ PPV \_ ARGS Macro](/windows)
-   [Modello SafeRelease](#the-saferelease-pattern)
-   [Puntatori intelligenti COM](#com-smart-pointers)

## <a name="the-__uuidof-operator"></a>Operatore \_ \_ uuidof

Quando si compila il programma, potrebbero verificarsi errori del linker simili ai seguenti:

`unresolved external symbol "struct _GUID const IID_IDrawable"`

Questo errore indica che una costante GUID è stata dichiarata con collegamento esterno (**extern**) e il linker non è stato in grado di trovare la definizione della costante. Il valore di una costante GUID viene in genere esportato da un file di libreria statica. Se si usa Microsoft Visual C++, è possibile evitare la necessità di collegare una libreria statica usando l'operatore **\_ \_ uuidof.** Questo operatore è un'estensione del linguaggio Microsoft. Restituisce un valore GUID da un'espressione. L'espressione può essere un nome di tipo di interfaccia, un nome di classe o un puntatore a interfaccia. Usando **\_ \_ uuidof**, è possibile creare l'oggetto Common Item Dialog come indicato di seguito:


```C++
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    __uuidof(pFileOpen), reinterpret_cast<void**>(&pFileOpen));
```



Il compilatore estrae il valore GUID dall'intestazione, quindi non è necessaria alcuna esportazione della libreria.

> [!Note]  
> Il valore GUID è associato al nome del tipo dichiarando `__declspec(uuid( ... ))` nell'intestazione . Per altre informazioni, vedere la documentazione per **\_ \_ declspec** nella documentazione Visual C++.

 

## <a name="the-iid_ppv_args-macro"></a>The IID \_ PPV \_ ARGS Macro

Si è visto che [**sia CoCreateInstance che**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) richiedono la coesistenza del parametro finale in un **tipo void. \* \*** Ciò crea il rischio di mancata corrispondenza del tipo. Si consideri il frammento di codice riportato di seguito.


```C++
// Wrong!

IFileOpenDialog *pFileOpen;

hr = CoCreateInstance(
    __uuidof(FileOpenDialog), 
    NULL, 
    CLSCTX_ALL, 
    __uuidof(IFileDialogCustomize),       // The IID does not match the pointer type!
    reinterpret_cast<void**>(&pFileOpen)  // Coerce to void**.
    );
```



Questo codice richiede [**l'interfaccia IFileDialogCustomize,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) ma passa un [**puntatore IFileOpenDialog.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) **\_ L'espressione reinterpret cast** aggira il sistema di tipi C++, quindi il compilatore non intercetterà questo errore. Nel migliore dei casi, se l'oggetto non implementa l'interfaccia richiesta, la chiamata ha semplicemente esito negativo. Nel peggiore dei casi, la funzione ha esito positivo ed è presente un puntatore non corrispondente. In altre parole, il tipo di puntatore non corrisponde all'effettiva vtable in memoria. Come si può immaginare, a questo punto non può accadere nulla di positivo.

> [!Note]  
> Una *tabella vtable* (tabella dei metodi virtuali) è una tabella di puntatori a funzione. Il vtable è il modo in cui COM associa una chiamata al metodo alla relativa implementazione in fase di esecuzione. Non a caso, le vtable sono il modo in cui la maggior parte dei compilatori C++ implementa i metodi virtuali.

 

La macro [**\_ IID PPV \_ ARGS**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) consente di evitare questa classe di errore. Per usare questa macro, sostituire il codice seguente:


```C++
__uuidof(IFileDialogCustomize), reinterpret_cast<void**>(&pFileOpen)
```



con il seguente:


```C++
IID_PPV_ARGS(&pFileOpen)
```



La macro inserisce automaticamente per l'identificatore di interfaccia, pertanto è garantito che `__uuidof(IFileOpenDialog)` corrisponda al tipo di puntatore. Ecco il codice modificato (e corretto):


```C++
// Right.
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    IID_PPV_ARGS(&pFileOpen));
```



È possibile usare la stessa macro con [**QueryInterface:**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))


```C++
IFileDialogCustomize *pCustom;
hr = pFileOpen->QueryInterface(IID_PPV_ARGS(&pCustom));
```



## <a name="the-saferelease-pattern"></a>Modello SafeRelease

Il conteggio dei riferimenti è uno di questi aspetti della programmazione che è fondamentalmente semplice, ma è anche noioso, il che rende più facile ottenere un errore. Gli errori tipici comprendono:

-   Non è possibile rilasciare un puntatore a interfaccia al termine dell'uso. Questa classe di bug causerà la perdita di memoria e di altre risorse da parte del programma, perché gli oggetti non vengono distrutti.
-   Chiamata [**di Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) con un puntatore non valido. Ad esempio, questo errore può verificarsi se l'oggetto non è mai stato creato. Questa categoria di bug causerà probabilmente l'arresto anomalo del programma.
-   Dereferenziazione di un puntatore a interfaccia dopo [**la chiamata**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) a Release. Questo bug può causare l'arresto anomalo del programma. La situazione peggiore potrebbe causare l'arresto anomalo del programma in un secondo momento casuale, rendendo difficile rilevare l'errore originale.

Un modo per evitare questi bug è chiamare [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) tramite una funzione che rilascia in modo sicuro il puntatore. Il codice seguente illustra una funzione che esegue questa operazione:


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



Questa funzione accetta un puntatore a interfaccia COM come parametro ed esegue le operazioni seguenti:

1.  Controlla se il puntatore è **NULL.**
2.  Chiama [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) se il puntatore non è **NULL.**
3.  Imposta il puntatore su **NULL.**

Di seguito è riportato un esempio di come usare `SafeRelease` :


```C++
void UseSafeRelease()
{
    IFileOpenDialog *pFileOpen = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        // Use the object.
    }
    SafeRelease(&pFileOpen);
}
```



Se [**CoCreateInstance ha**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) esito positivo, la chiamata a `SafeRelease` rilascia il puntatore . Se **CoCreateInstance ha** esito negativo, *pFileOpen* rimane **NULL.** La `SafeRelease` funzione verifica questa operazione e ignora la chiamata a [**Release.**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)

È anche possibile chiamare più volte sullo stesso `SafeRelease` puntatore, come illustrato di seguito:


```C++
// Redundant, but OK.
SafeRelease(&pFileOpen);
SafeRelease(&pFileOpen);
```



## <a name="com-smart-pointers"></a>Puntatori intelligenti COM

La `SafeRelease` funzione è utile, ma richiede di ricordare due elementi:

-   Inizializzare ogni puntatore di interfaccia **su NULL.**
-   Chiamare `SafeRelease` prima che ogni puntatore es esterno all'ambito.

I programmatori C++ probabilmente pensano di non doversi ricordare di nessuno di questi elementi. Dopo tutto, questo è il motivo per cui C++ include costruttori e distruttori. Sarebbe bene avere una classe che esegue il wrapping del puntatore a interfaccia sottostante e inizializza e rilascia automaticamente il puntatore. In altre parole, si vuole avere un aspetto simile al seguente:


```C++
// Warning: This example is not complete.

template <class T>
class SmartPointer
{
    T* ptr;

 public:
    SmartPointer(T *p) : ptr(p) { }
    ~SmartPointer()
    {
        if (ptr) { ptr->Release(); }
    }
};
```



La definizione di classe illustrata di seguito è incompleta e non può essere utilizzata come illustrato. Come minimo, è necessario definire un costruttore di copia, un operatore di assegnazione e un modo per accedere al puntatore COM sottostante. Fortunatamente, non è necessario eseguire nessuna di queste operazioni, perché Microsoft Visual Studio fornisce già una classe puntatore intelligente come parte del Active Template Library (ATL).

La classe di puntatore intelligente ATL è denominata **CComPtr.** È disponibile anche una **classe CComQIPtr,** che non viene illustrata qui. Di seguito è riportato [l'esempio open dialog box](example--the-open-dialog-box.md) riscritto per usare **CComPtr.**


```C++
#include <windows.h>
#include <shobjidl.h> 
#include <atlbase.h> // Contains the declaration of CComPtr.

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CComPtr<IFileOpenDialog> pFileOpen;

        // Create the FileOpenDialog object.
        hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                CComPtr<IShellItem> pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBox(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                }

                // pItem goes out of scope.
            }

            // pFileOpen goes out of scope.
        }
        CoUninitialize();
    }
    return 0;
}
```



La differenza principale tra questo codice e l'esempio originale è che questa versione non chiama in modo esplicito [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release). Quando **l'istanza di CComPtr** esce dall'ambito, il distruttore chiama **Release** sul puntatore sottostante.

**CComPtr è** un modello di classe. L'argomento di modello è il tipo di interfaccia COM. Internamente, **CComPtr contiene** un puntatore di quel tipo. **CComPtr esegue l'override** **di operator->()** e **dell'operatore&()** in modo che la classe agisca come il puntatore sottostante. Ad esempio, il codice seguente equivale a chiamare direttamente il metodo **IFileOpenDialog::Show:**


```C++
hr = pFileOpen->Show(NULL);
```



**CComPtr** definisce anche un metodo **CComPtr::CoCreateInstance,** che chiama la funzione [**COM CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con alcuni valori di parametro predefiniti. L'unico parametro obbligatorio è l'identificatore di classe, come illustrato nell'esempio seguente:


```C++
hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
```



Il **metodo CComPtr::CoCreateInstance** viene fornito esclusivamente per praticità. È comunque possibile chiamare la funzione [**COM CoCreateInstance,**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) se si preferisce.

## <a name="next"></a>Prossima

[Gestione degli errori in COM](error-handling-in-com.md)

 

 