---
description: Implementazione della conversione da un oggetto input penna di testo (tInk) a input penna.
ms.assetid: 9365da4c-3667-49f0-838f-f099d28dab44
title: Conversione di un oggetto input penna di testo in input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef543fda3ed53123e99ee042aed67af9cedfef3533ae47bc40d8dd284a73675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941161"
---
# <a name="converting-a-text-ink-object-to-ink"></a>Conversione di un oggetto input penna di testo in input penna

Implementazione della conversione da un oggetto input penna di testo (tInk) a input penna.

## <a name="to-convert-from-a-text-ink-object-to-ink"></a>Per eseguire la conversione da un oggetto input penna di testo a input penna

1.  Usare [l'interfaccia IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) per scrivere il contenuto dell'oggetto input penna di testo in un flusso. L'oggetto input penna di testo usa il formato serializzato dell'input penna per scrivere nel flusso.
2.  Leggere il contenuto del flusso in una matrice BYTE.
3.  Usare il [**metodo Load**](inkdisp-class.md) dell'oggetto [**InkDisp**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) per caricare il contenuto del flusso nell'oggetto **InkDisp.**

## <a name="text-ink-object-to-ink-object-example"></a>Esempio di oggetto Input penna di testo nell'oggetto Ink

Il frammento di codice seguente converte un oggetto input penna di testo in input penna.

In primo luogo, il codice ottiene un oggetto input penna di testo.


```C++
/* Create a variable to hold the text ink object */
CComPtr<IInkObject *> spITextInk;

/* Obtain the text ink object */
```



Il codice crea quindi un puntatore per il flusso che contiene il contenuto dell'oggetto input penna di testo.


```C++
// Create a Stream pointer to hold the saved object
CComPtr<IStream *> spStream = NULL; 
```



Il codice ottiene quindi [l'interfaccia IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) dall'oggetto input penna di testo.


```C++
// Declare the IPersistStream to be used for retrieving the saved data from the text ink
CComPtr<IPersistStream *> spIPersistStream = NULL;
// Get the actual IPersistStream interface off of the TextInk
HRESULT hr = pITextInk->QueryInterface(IID_IPersistStream, (void **)&spIPersistStream);
ASSERT(SUCCEEDED(hr) && spIPersistStream);
```



Il codice usa quindi [l'interfaccia IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) per salvare il contenuto dell'oggetto input penna di testo nel flusso.


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



Il codice crea quindi un [**oggetto InkCollector,**](inkcollector-class.md) crea un oggetto [**InkDisp**](inkdisp-class.md) per **InkCollector,** associa **InkCollector** alla finestra dell'applicazione e abilita la raccolta di input penna **in InkCollector.**


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



Il codice recupera quindi le dimensioni del flusso e crea una matrice sicura per contenere il contenuto del flusso.


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



Infine, il codice accede alla matrice sicura e usa il metodo [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) dell'oggetto [**InkDisp**](inkdisp-class.md) per caricare l'input penna dalla matrice.


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



 

 
