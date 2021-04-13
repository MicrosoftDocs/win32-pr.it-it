---
title: Esempio della finestra di dialogo Apri
description: L'esempio di forme utilizzato è stato piuttosto escogitato. Passiamo a un oggetto COM che è possibile usare in un programma Windows reale la finestra di dialogo Apri.
ms.assetid: f426cf83-ed24-4eeb-bc28-b5871b824525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d896c5928c5bcf5e7dae7835d011ddf0f1fbd6e6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398990"
---
# <a name="example-the-open-dialog-box"></a><span data-ttu-id="42060-104">Esempio: finestra di dialogo Apri</span><span class="sxs-lookup"><span data-stu-id="42060-104">Example: The Open Dialog Box</span></span>

<span data-ttu-id="42060-105">L' `Shapes` esempio che è stato usato è piuttosto escogitato.</span><span class="sxs-lookup"><span data-stu-id="42060-105">The `Shapes` example that we have been using is somewhat contrived.</span></span> <span data-ttu-id="42060-106">Passiamo a un oggetto COM che è possibile usare in un programma Windows reale: la finestra di dialogo **Apri** .</span><span class="sxs-lookup"><span data-stu-id="42060-106">Let's turn to a COM object that you might use in a real Windows program: the **Open** dialog box.</span></span>

![screenshot che mostra la finestra di dialogo Apri](images/fileopen01.png)

<span data-ttu-id="42060-108">Per visualizzare la finestra di dialogo **Apri** , un programma può utilizzare un oggetto com denominato oggetto finestra di dialogo elemento comune.</span><span class="sxs-lookup"><span data-stu-id="42060-108">To show the **Open** dialog box, a program can use a COM object called the Common Item Dialog object.</span></span> <span data-ttu-id="42060-109">La finestra di dialogo elemento comune implementa un'interfaccia denominata [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), dichiarata nel file di intestazione ShObjIdl. h.</span><span class="sxs-lookup"><span data-stu-id="42060-109">The Common Item Dialog implements an interface named [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), which is declared in the header file Shobjidl.h.</span></span>

<span data-ttu-id="42060-110">Ecco un programma che Visualizza l'utente nella finestra di dialogo **Apri** .</span><span class="sxs-lookup"><span data-stu-id="42060-110">Here is a program that displays the **Open** dialog box to the user.</span></span> <span data-ttu-id="42060-111">Se l'utente seleziona un file, il programma visualizza una finestra di dialogo contenente il nome del file.</span><span class="sxs-lookup"><span data-stu-id="42060-111">If the user selects a file, the program shows a dialog box that contains the file name.</span></span>


```C++
#include <windows.h>
#include <shobjidl.h> 

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        IFileOpenDialog *pFileOpen;

        // Create the FileOpenDialog object.
        hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
                IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                IShellItem *pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBoxW(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                    pItem->Release();
                }
            }
            pFileOpen->Release();
        }
        CoUninitialize();
    }
    return 0;
}
```



<span data-ttu-id="42060-112">Questo codice usa alcuni concetti che verranno descritti più avanti nel modulo, quindi non è necessario preoccuparsi se non si conoscono tutti i concetti.</span><span class="sxs-lookup"><span data-stu-id="42060-112">This code uses some concepts that will be described later in the module, so don't worry if you do not understand everything here.</span></span> <span data-ttu-id="42060-113">Ecco una struttura di base del codice:</span><span class="sxs-lookup"><span data-stu-id="42060-113">Here is a basic outline of the code:</span></span>

1.  <span data-ttu-id="42060-114">Chiamare [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) per inizializzare la libreria com.</span><span class="sxs-lookup"><span data-stu-id="42060-114">Call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="42060-115">Chiamare [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare l'oggetto finestra di dialogo elemento comune e ottenere un puntatore all'interfaccia [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="42060-115">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Common Item Dialog object and get a pointer to the object's [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) interface.</span></span>
3.  <span data-ttu-id="42060-116">Chiamare il metodo **show** dell'oggetto, che mostra la finestra di dialogo all'utente.</span><span class="sxs-lookup"><span data-stu-id="42060-116">Call the object's **Show** method, which shows the dialog box to the user.</span></span> <span data-ttu-id="42060-117">Questo metodo si blocca fino a quando l'utente non dimentica la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="42060-117">This method blocks until the user dismisses the dialog box.</span></span>
4.  <span data-ttu-id="42060-118">Chiamare il metodo [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="42060-118">Call the object's [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) method.</span></span> <span data-ttu-id="42060-119">Questo metodo restituisce un puntatore a un secondo oggetto COM, denominato oggetto *elemento della shell* .</span><span class="sxs-lookup"><span data-stu-id="42060-119">This method returns a pointer to a second COM object, called a *Shell item* object.</span></span> <span data-ttu-id="42060-120">L'elemento della shell, che implementa l'interfaccia [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) , rappresenta il file selezionato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="42060-120">The Shell item, which implements the [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) interface, represents the file that the user selected.</span></span>
5.  <span data-ttu-id="42060-121">Chiamare il metodo [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) dell'elemento della shell.</span><span class="sxs-lookup"><span data-stu-id="42060-121">Call the Shell item's [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) method.</span></span> <span data-ttu-id="42060-122">Questo metodo ottiene il percorso del file sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="42060-122">This method gets the file path, in the form of a string.</span></span>
6.  <span data-ttu-id="42060-123">Visualizza una finestra di messaggio in cui viene visualizzato il percorso del file.</span><span class="sxs-lookup"><span data-stu-id="42060-123">Show a message box that displays the file path.</span></span>
7.  <span data-ttu-id="42060-124">Chiamare [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) per annullare l'inizializzazione della libreria com.</span><span class="sxs-lookup"><span data-stu-id="42060-124">Call [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) to uninitialize the COM library.</span></span>

<span data-ttu-id="42060-125">Passaggi 1, 2 e 7 funzioni di chiamata definite dalla libreria COM.</span><span class="sxs-lookup"><span data-stu-id="42060-125">Steps 1, 2, and 7 call functions that are defined by the COM library.</span></span> <span data-ttu-id="42060-126">Si tratta di funzioni COM generiche.</span><span class="sxs-lookup"><span data-stu-id="42060-126">These are generic COM functions.</span></span> <span data-ttu-id="42060-127">I passaggi da 3 a 5 chiamano i metodi definiti dall'oggetto finestra di dialogo elemento comune.</span><span class="sxs-lookup"><span data-stu-id="42060-127">Steps 3–5 call methods that are defined by the Common Item Dialog object.</span></span>

<span data-ttu-id="42060-128">In questo esempio vengono illustrate entrambe le varietà di creazione di oggetti: la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) generica e un metodo ([**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)) specifico per l'oggetto finestra di dialogo elemento comune.</span><span class="sxs-lookup"><span data-stu-id="42060-128">This example shows both varieties of object creation: The generic [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, and a method ([**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)) that is specific to the Common Item Dialog object.</span></span>

## <a name="next"></a><span data-ttu-id="42060-129">Prossima</span><span class="sxs-lookup"><span data-stu-id="42060-129">Next</span></span>

[<span data-ttu-id="42060-130">Gestione della durata di un oggetto</span><span class="sxs-lookup"><span data-stu-id="42060-130">Managing the Lifetime of an Object</span></span>](managing-the-lifetime-of-an-object.md)

## <a name="related-topics"></a><span data-ttu-id="42060-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="42060-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42060-132">Apri esempio di finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="42060-132">Open Dialog Box Sample</span></span>](open-dialog-box-sample.md)
</dt> </dl>

 

 