---
title: Procedure di codifica COM
description: Questo argomento descrive i modi per rendere il codice COM più efficace e affidabile.
ms.assetid: 76aca556-b4d6-4e67-a2a3-4439900f0c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a26143e5049c3db7efcbcc9353e74890fe0009c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104118587"
---
# <a name="com-coding-practices"></a>Procedure di codifica COM

Questo argomento descrive i modi per rendere il codice COM più efficace e affidabile.

-   [\_ \_ Operatore uuidof](/windows)
-   [La macro degli argomenti di IID \_ PPV \_](/windows)
-   [Modello SafeRelease](#the-saferelease-pattern)
-   [Puntatori intelligenti COM](#com-smart-pointers)

## <a name="the-__uuidof-operator"></a>\_ \_ Operatore uuidof

Quando si compila il programma, è possibile che vengano visualizzati errori del linker simili ai seguenti:

`unresolved external symbol "struct _GUID const IID_IDrawable"`

Questo errore indica che è stata dichiarata una costante GUID con collegamento esterno (**extern**) e che il linker non è riuscito a trovare la definizione della costante. Il valore di una costante GUID viene in genere esportato da un file di libreria statica. Se si usa Microsoft Visual C++, è possibile evitare di dover collegare una libreria statica usando l'operatore **\_ \_ uuidof** . Questo operatore è un'estensione del linguaggio Microsoft. Restituisce un valore GUID da un'espressione. L'espressione può essere un nome di tipo interfaccia, un nome di classe o un puntatore di interfaccia. Utilizzando **\_ \_ uuidof**, è possibile creare l'oggetto finestra di dialogo elemento comune come segue:


```C++
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    __uuidof(pFileOpen), reinterpret_cast<void**>(&pFileOpen));
```



Il compilatore estrae il valore GUID dall'intestazione, pertanto non è necessaria alcuna esportazione della libreria.

> [!Note]  
> Il valore GUID è associato al nome del tipo dichiarando `__declspec(uuid( ... ))` nell'intestazione. Per ulteriori informazioni, vedere la documentazione relativa a **\_ \_ declspec** nella documentazione di Visual C++.

 

## <a name="the-iid_ppv_args-macro"></a>La macro degli argomenti di IID \_ PPV \_

È stato rilevato che per [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) e [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) è necessario assegnare il parametro finale a un tipo **void \* \*** . Ciò crea il rischio di mancata corrispondenza del tipo. Si consideri il frammento di codice riportato di seguito.


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



Questo codice richiede l'interfaccia [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) , ma passa un puntatore [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) . L'espressione **\_ cast reinterpretate** elude il sistema di tipi C++, pertanto il compilatore non rileverà questo errore. Nel migliore dei casi, se l'oggetto non implementa l'interfaccia richiesta, la chiamata ha semplicemente esito negativo. Nel peggiore dei casi, la funzione ha esito positivo e si dispone di un puntatore non corrispondente. In altre parole, il tipo di puntatore non corrisponde alla vtable effettiva in memoria. Come si può immaginare, a questo punto non è possibile che si verifichino elementi validi.

> [!Note]  
> Un oggetto *vtable* (tabella dei metodi virtuali) è una tabella di puntatori a funzione. Vtable è il modo in cui COM associa una chiamata al metodo alla relativa implementazione in fase di esecuzione. Per la maggior parte dei compilatori C++ implementano i metodi virtuali, vtable.

 

La macro [**IID \_ PPV \_ args**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) consente di evitare questa classe di errore. Per usare questa macro, sostituire il codice seguente:


```C++
__uuidof(IFileDialogCustomize), reinterpret_cast<void**>(&pFileOpen)
```



con il seguente:


```C++
IID_PPV_ARGS(&pFileOpen)
```



La macro inserisce automaticamente `__uuidof(IFileOpenDialog)` per l'identificatore di interfaccia, quindi è garantita la corrispondenza con il tipo di puntatore. Ecco il codice modificato (e corretto):


```C++
// Right.
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    IID_PPV_ARGS(&pFileOpen));
```



È possibile usare la stessa macro con [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):


```C++
IFileDialogCustomize *pCustom;
hr = pFileOpen->QueryInterface(IID_PPV_ARGS(&pCustom));
```



## <a name="the-saferelease-pattern"></a>Modello SafeRelease

Il conteggio dei riferimenti è uno degli elementi della programmazione che è sostanzialmente semplice, ma è anche noioso, il che rende più semplice l'errore. Gli errori tipici comprendono:

-   Errore di rilascio di un puntatore a interfaccia al termine dell'utilizzo. Questa classe di bug provocherà la perdita di memoria e di altre risorse da un programma, perché gli oggetti non vengono eliminati definitivamente.
-   Chiamata della [**versione**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) con un puntatore non valido. Questo errore può verificarsi, ad esempio, se l'oggetto non è mai stato creato. Questa categoria di bug provocherà probabilmente un arresto anomalo del programma.
-   Dereferenziazione di un puntatore a interfaccia dopo la chiamata di [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) . Questo bug può causare l'arresto anomalo del programma. Peggiori, potrebbe causare l'arresto anomalo del programma in un momento successivo, rendendo difficile l'individuazione dell'errore originale.

Un modo per evitare questi bug consiste nel chiamare il metodo [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) tramite una funzione che rilascia in modo sicuro il puntatore. Nel codice seguente viene illustrata una funzione che esegue questa operazione:


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

1.  Controlla se il puntatore è **null**.
2.  Chiama [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) se il puntatore non è **null**.
3.  Imposta il puntatore su **null**.

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



Se [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ha esito positivo, la chiamata a `SafeRelease` rilascia il puntatore. Se **CoCreateInstance** ha esito negativo, *pFileOpen* rimane **null**. La `SafeRelease` funzione verifica l'oggetto e ignora la chiamata a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).

È anche possibile chiamare `SafeRelease` più volte nello stesso puntatore, come illustrato di seguito:


```C++
// Redundant, but OK.
SafeRelease(&pFileOpen);
SafeRelease(&pFileOpen);
```



## <a name="com-smart-pointers"></a>Puntatori intelligenti COM

La `SafeRelease` funzione è utile, ma è necessario ricordare due elementi:

-   Inizializzare ogni puntatore di interfaccia su **null**.
-   Chiamare `SafeRelease` prima che ogni puntatore esca dall'ambito.

In qualità di programmatore C++, è probabile che si stia pensando di non dover ricordare uno di questi aspetti. Per questo motivo, C++ dispone di costruttori e distruttori. Sarebbe bello avere una classe che esegue il wrapping del puntatore a interfaccia sottostante e Inizializza e rilascia automaticamente il puntatore. In altre parole, è necessario avere un aspetto simile al seguente:


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



La definizione della classe riportata di seguito è incompleta e non è utilizzabile come illustrato. Come minimo, è necessario definire un costruttore di copia, un operatore di assegnazione e un modo per accedere al puntatore COM sottostante. Fortunatamente, non è necessario eseguire alcuna operazione, perché Microsoft Visual Studio fornisce già una classe di puntatore intelligente come parte del Active Template Library (ATL).

La classe del puntatore intelligente ATL è denominata **CComPtr**. (Esiste anche una classe **CComQIPtr** , che non viene discussa qui). Ecco l'esempio di finestra di [dialogo Apri](example--the-open-dialog-box.md) riscritta per usare **CComPtr**.


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



La differenza principale tra questo codice e l'esempio originale è che questa versione non chiama in modo esplicito [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release). Quando l'istanza di **CComPtr** esce dall'ambito, il distruttore chiama **Release** sul puntatore sottostante.

**CComPtr** è un modello di classe. L'argomento di modello è il tipo di interfaccia COM. Internamente, **CComPtr** include un puntatore di quel tipo. **CComPtr** esegue l'override di **operator-> ()** e dell' **operatore& ()** in modo che la classe funga da puntatore sottostante. Ad esempio, il codice seguente equivale a chiamare direttamente il metodo **IFileOpenDialog:: Show** :


```C++
hr = pFileOpen->Show(NULL);
```



**CComPtr** definisce anche un metodo **CComPtr:: CoCreateInstance** , che chiama la funzione com [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con alcuni valori di parametro predefiniti. L'unico parametro obbligatorio è l'identificatore della classe, come illustrato nell'esempio seguente:


```C++
hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
```



Il metodo **CComPtr:: CoCreateInstance** viene fornito esclusivamente come praticità. Se lo si preferisce, è comunque possibile chiamare la funzione COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .

## <a name="next"></a>Prossima

[Gestione degli errori in COM](error-handling-in-com.md)

 

 