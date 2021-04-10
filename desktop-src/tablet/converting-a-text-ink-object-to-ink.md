---
description: Implementazione della conversione da un oggetto input penna (tInk) a input penna.
ms.assetid: 9365da4c-3667-49f0-838f-f099d28dab44
title: Conversione di un oggetto input penna in input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b8c7fe4a7847834fffda2df9c4ab94293756cee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225794"
---
# <a name="converting-a-text-ink-object-to-ink"></a><span data-ttu-id="e273d-103">Conversione di un oggetto input penna in input penna</span><span class="sxs-lookup"><span data-stu-id="e273d-103">Converting a Text Ink Object to Ink</span></span>

<span data-ttu-id="e273d-104">Implementazione della conversione da un oggetto input penna (tInk) a input penna.</span><span class="sxs-lookup"><span data-stu-id="e273d-104">Implementation of converting from a text ink object (tInk) to ink.</span></span>

## <a name="to-convert-from-a-text-ink-object-to-ink"></a><span data-ttu-id="e273d-105">Per eseguire la conversione da un oggetto input penna di testo a input penna</span><span class="sxs-lookup"><span data-stu-id="e273d-105">To convert from a text ink object to ink</span></span>

1.  <span data-ttu-id="e273d-106">Usare l'interfaccia [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) per scrivere il contenuto dell'oggetto Ink di testo in un flusso.</span><span class="sxs-lookup"><span data-stu-id="e273d-106">Use the [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface to write the contents of the text ink object out to a stream.</span></span> <span data-ttu-id="e273d-107">L'oggetto Ink text usa il formato serializzato con input penna per scrivere nel flusso di vapore.</span><span class="sxs-lookup"><span data-stu-id="e273d-107">The text ink object uses ink serialized format to write to the steam.</span></span>
2.  <span data-ttu-id="e273d-108">Leggere il contenuto del flusso in una matrice di BYTE.</span><span class="sxs-lookup"><span data-stu-id="e273d-108">Read the contents of the stream into a BYTE array.</span></span>
3.  <span data-ttu-id="e273d-109">Usare il metodo [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) dell'oggetto [**InkDisp**](inkdisp-class.md) per caricare il contenuto del flusso nell'oggetto **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="e273d-109">Use the [**InkDisp**](inkdisp-class.md) object's [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) method to load the contents of the stream into the **InkDisp** object.</span></span>

## <a name="text-ink-object-to-ink-object-example"></a><span data-ttu-id="e273d-110">Esempio di oggetto input penna testo in oggetto Ink</span><span class="sxs-lookup"><span data-stu-id="e273d-110">Text Ink Object to Ink Object Example</span></span>

<span data-ttu-id="e273d-111">Il frammento di codice seguente converte un oggetto input penna in input penna.</span><span class="sxs-lookup"><span data-stu-id="e273d-111">The following code fragment converts a text ink object to ink.</span></span>

<span data-ttu-id="e273d-112">In primo luogo, il codice ottiene un oggetto input penna.</span><span class="sxs-lookup"><span data-stu-id="e273d-112">First, the code obtains a text ink object.</span></span>


```C++
/* Create a variable to hold the text ink object */
CComPtr<IInkObject *> spITextInk;

/* Obtain the text ink object */
```



<span data-ttu-id="e273d-113">Quindi, il codice crea un puntatore per il flusso che contiene il contenuto dell'oggetto input penna di testo.</span><span class="sxs-lookup"><span data-stu-id="e273d-113">Then, the code creates a pointer for the stream that holds the contents of the text ink object.</span></span>


```C++
// Create a Stream pointer to hold the saved object
CComPtr<IStream *> spStream = NULL; 
```



<span data-ttu-id="e273d-114">Quindi, il codice ottiene l'interfaccia [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) dall'oggetto input penna di testo.</span><span class="sxs-lookup"><span data-stu-id="e273d-114">Then, the code obtains the [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface from the text ink object.</span></span>


```C++
// Declare the IPersistStream to be used for retrieving the saved data from the text ink
CComPtr<IPersistStream *> spIPersistStream = NULL;
// Get the actual IPersistStream interface off of the TextInk
HRESULT hr = pITextInk->QueryInterface(IID_IPersistStream, (void **)&spIPersistStream);
ASSERT(SUCCEEDED(hr) && spIPersistStream);
```



<span data-ttu-id="e273d-115">Il codice usa quindi l'interfaccia [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) per salvare il contenuto dell'oggetto Ink di testo nel flusso.</span><span class="sxs-lookup"><span data-stu-id="e273d-115">Then, the code uses the [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface to save the contents of the text ink object to the stream.</span></span>


```C++
if( SUCCEEDED(hr) && pIPersistStream )
{
    // Create the stream 
    if( SUCCEEDED(hr=CreateStreamOnHGlobal(NULL, TRUE, &spStream)) && spStream )
    {
        // Save the TextInk through IPersistStream Interface to the IStream
        hr = spIPersistStream->Save(spStream, FALSE);
    }
}
```



<span data-ttu-id="e273d-116">Quindi, tramite il codice viene creato un oggetto [**InkCollector**](inkcollector-class.md) , viene creato un oggetto [**InkDisp**](inkdisp-class.md) per l'oggetto **InkCollector**, viene collegato l'oggetto **InkCollector** alla finestra dell'applicazione e viene abilitata la raccolta di input penna in **InkCollector**.</span><span class="sxs-lookup"><span data-stu-id="e273d-116">Then, the code creates an [**InkCollector**](inkcollector-class.md) object, creates an [**InkDisp**](inkdisp-class.md) object for the **InkCollector**, attaches the **InkCollector** to the application window, and enables ink collection on the **InkCollector**.</span></span>


```C++
// Now create an InkCollector object along with InkDisp Object
if( SUCCEEDED(hr) && spStream)
{
    CComPtr<IInkCollector *> spIInkCollector;
    CComPtr<IInkDisp *> spIInkDisp = NULL;

    // Create the InkCollector object.
    hr = CoCreateInstance(CLSID_InkCollector, 
        NULL, CLSCTX_INPROC_SERVER, 
        IID_IInkCollector, 
        (void **) &spIInkCollector);
    if (FAILED(hr)) 
        return -1;

    // Get a pointer to the Ink object
    hr = spIInkCollector->get_Ink(&spIInkDisp);
    if (FAILED(hr)) 
        return -1;

    // Tell InkCollector the window to collect ink in
    hr = spIInkCollector->put_hWnd((long)hwnd);
    if (FAILED(hr)) 
        return -1;

    // Enable ink input in the window
    hr = spIInkCollector->put_Enabled(VARIANT_TRUE);
    if (FAILED(hr)) 
        return -1;
```



<span data-ttu-id="e273d-117">Il codice recupera quindi le dimensioni del flusso e crea una matrice sicura per conservare il contenuto del flusso.</span><span class="sxs-lookup"><span data-stu-id="e273d-117">Then, the code retrieves the size of the stream and creates a safe array to hold the contents of the stream.</span></span>


```C++
    // Now create a variant data type based on the IStream data
    const LARGE_INTEGER li0 = {0, 0};
    ULARGE_INTEGER uli = {0,0};

    // Find the size of the stream
    hr = spStream->Seek(li0, STREAM_SEEK_END, &uli);
    ASSERT(0 == uli.HighPart);
    DWORD dwSize = uli.LowPart;

    // Set uli to point to the beginning of the stream.
    hr=spStream->Seek(li0, STREAM_SEEK_SET, &uli);
    ASSERT(SUCCEEDED(hr));

    // Create a safe array to hold the stream contents
    if( SUCCEEDED(hr) )
    {
        VARIANT vtData;
        VariantInit(&vtData);
        vtData.vt = VT_ARRAY | VT_UI1;

        vtData.parray = ::SafeArrayCreateVector(VT_UI1, 0, dwSize);
        if (vtData.parray)
        {
```



<span data-ttu-id="e273d-118">Infine, il codice accede alla matrice sicura e usa il metodo [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) dell'oggetto [**InkDisp**](inkdisp-class.md) per caricare l'input penna dalla matrice.</span><span class="sxs-lookup"><span data-stu-id="e273d-118">Finally, the code accesses the safe array and uses the [**InkDisp**](inkdisp-class.md) object's [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) method to load the ink from the array.</span></span>


```C++
            DWORD dwRead = 0;
            LPBYTE pbData = NULL; 

            if (SUCCEEDED(::SafeArrayAccessData(vtData.parray, (void**)&pbData)))
            {
                // Read the data from the stream to the varian data and load that into an InkDisp object
                if (TRUE == spStream->Read(pbData, uli.LowPart, &dwRead)
                    && SUCCEEDED(spIInkDisp->Load(vtData)))
                {
                    hr = S_OK;
                }
                ::SafeArrayUnaccessData(vtData.parray);
            }
            ::SafeArrayDestroy(vtData.parray);
        }
    }
}
```



 

 
