---
description: Recupera il corpo dell'entità di risposta come IStream.
ms.assetid: e12a9338-5e0c-4672-bbc6-31375b872e94
title: 'Proprietà IWinHttpRequest:: ResponseStream'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseStream
- IWinHttpRequest.get_ResponseStream
- WinHttpRequest.ResponseStream
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: ec9f497e687c52735784a5e3edad01905ac7a6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232914"
---
# <a name="iwinhttprequestresponsestream-property"></a><span data-ttu-id="a0d6d-103">Proprietà IWinHttpRequest:: ResponseStream</span><span class="sxs-lookup"><span data-stu-id="a0d6d-103">IWinHttpRequest::ResponseStream property</span></span>

<span data-ttu-id="a0d6d-104">La proprietà **responseStream** Recupera il corpo dell'entità di risposta come [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="a0d6d-104">The **ResponseStream** property retrieves the response entity body as an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span>

<span data-ttu-id="a0d6d-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a0d6d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0d6d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0d6d-106">Syntax</span></span>


```C++
HRESULT get_ResponseStream(
  [out, retval] VARIANT *Body
);
```


```JScript

vtResponseStream = WinHttpRequest.ResponseStream
```





## <a name="property-value"></a><span data-ttu-id="a0d6d-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a0d6d-107">Property value</span></span>

<span data-ttu-id="a0d6d-108">**Variante** che riceve un puntatore a un'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) su cui è possibile eseguire query per un'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="a0d6d-108">A **Variant** that receives a pointer to an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface that can be queried for an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> <span data-ttu-id="a0d6d-109">Questo flusso restituisce i dati non elaborati ricevuti direttamente dal server.</span><span class="sxs-lookup"><span data-stu-id="a0d6d-109">This stream returns the raw data as received directly from the server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a0d6d-110">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a0d6d-110">Error codes</span></span>

<span data-ttu-id="a0d6d-111">Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="a0d6d-111">The return value is **S\_OK** on success or an error value otherwise.</span></span>

<span data-ttu-id="a0d6d-112">Se l'operazione di [**invio**](iwinhttprequest-send.md) precedente non è completa, sarà **e \_ in sospeso** .</span><span class="sxs-lookup"><span data-stu-id="a0d6d-112">It will be **E\_PENDING** if the previous [**Send**](iwinhttprequest-send.md) operation is not complete.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0d6d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0d6d-113">Remarks</span></span>

<span data-ttu-id="a0d6d-114">Chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul puntatore restituito per ottenere un puntatore a un'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="a0d6d-114">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the returned pointer to obtain a pointer to an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> <span data-ttu-id="a0d6d-115">Questa proprietà restituisce i dati di risposta come **IStream**.</span><span class="sxs-lookup"><span data-stu-id="a0d6d-115">This property returns the response data as an **IStream**.</span></span> <span data-ttu-id="a0d6d-116">Questa proprietà può essere richiamata solo dopo la chiamata del metodo [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="a0d6d-116">This property can only be invoked after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="a0d6d-117">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a0d6d-117">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="a0d6d-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="a0d6d-118">Examples</span></span>

<span data-ttu-id="a0d6d-119">Nell'esempio seguente viene illustrato come aprire una connessione HTTP, inviare una richiesta HTTP e leggere la risposta come [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="a0d6d-119">The following example shows how to open an HTTP connection, send an HTTP request, and read the response as an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span> <span data-ttu-id="a0d6d-120">I dati di **IStream** vengono scritti nel file Temp1.gif.</span><span class="sxs-lookup"><span data-stu-id="a0d6d-120">The data from the **IStream** is written to the file Temp1.gif.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <objbase.h>

#include "httprequest.h"

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "oleaut32.lib")

// IID for IWinHttpRequest.
const IID IID_IWinHttpRequest =
{
  0x06f29373,
  0x5c5a,
  0x4b54,
  {0xb0, 0x25, 0x6e, 0xf1, 0xbf, 0x8a, 0xbf, 0x0e}
};

#define Trace(_s) fprintf(stderr, _s) 
#define TraceErr(_s, _hr) fprintf(stderr, _s, _hr) 
#define Check(_hr,_s) if (FAILED(_hr)) { fprintf(stderr, _s ## " 0x%08lx\n", _hr); return -1; }

int main(int argc, char* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    
    // Variable for return value.
    HRESULT    hr;

    // Initialize COM.
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varFalse;
    VARIANT         varEmpty;
    VARIANT            varResponse;

    VariantInit(&varResponse);
    
    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IWinHttpRequest, 
                              (void **)&pIWinHttpRequest);
    }

    // ==== Get binary (.gif) file and write it to disk. =========
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest for synchronous access.
        BSTR bstrMethod = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(
            L"https://www.microsoft.com/library/homepage/images/ms-banner.gif");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get response body.
        hr = pIWinHttpRequest->get_ResponseBody(&varResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to file temp1.gif.
        long UpperBounds;
        long LowerBounds;
        unsigned char* buff;
        // Verify that varResponse contains array of unsigned bytes.
        if (varResponse.vt == (VT_ARRAY | VT_UI1)) {
            long Dims = SafeArrayGetDim(varResponse.parray);
            // The array should only have 1 dimension.
            if (Dims == 1) {
                // Get upper and lower array bounds.
                SafeArrayGetLBound(varResponse.parray, 1, 
                                   &LowerBounds);
                SafeArrayGetUBound(varResponse.parray, 1, 
                                   &UpperBounds);
                UpperBounds++;
                // Lock SAFEARRAY for access.
                SafeArrayAccessData (varResponse.parray, 
                                     (void**)&buff);
                // Output array to file temp.gif.
                HANDLE hFile; 
                DWORD  dwBytesWritten;
                // Create file.
                hFile = CreateFile(TEXT("Temp1.gif"),     
                    GENERIC_WRITE,              // Open for writing. 
                    0,                          // Do not share. 
                    NULL,                       // No security. 
                    CREATE_ALWAYS,              // Overwrite existing.
                    FILE_ATTRIBUTE_NORMAL,      // Normal file.
                    NULL);                      // No attribute template.

                if (hFile == INVALID_HANDLE_VALUE) 
                    {
                    wprintf(L"Could not open file."); // Process error.
                    }
                else
                    {
                    WriteFile(hFile, buff, UpperBounds - LowerBounds, 
                        &dwBytesWritten, NULL); 
                    }
                CloseHandle(hFile);
                SafeArrayUnaccessData (varResponse.parray);
            }
        }    
    }

    // ======== Get binary (.gif) file and write 
    // it to disk using IStream. ================
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest for synchronous access.
        BSTR bstrMethod = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(
            L"https://www.microsoft.com/library/homepage/images/ms-banner.gif");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response as an IStream.
        hr = pIWinHttpRequest->get_ResponseStream(&varResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to file temp1.gif.
        IStream*    pStream = NULL; 
        BYTE        bBuffer[8192]; 
        DWORD       cb, cbRead, cbWritten; 
        // Check that an IStream was received.
        if (VT_UNKNOWN == V_VT(&varResponse) || 
            VT_STREAM == V_VT(&varResponse)) 
        { 
            // Get IStream interface pStream.
            hr = V_UNKNOWN(&varResponse)->QueryInterface(IID_IStream, 
                                 reinterpret_cast<void**>(&pStream)); 
            Check(hr, "QI for IStream"); 
        } 
        else 
        { 
            wprintf(L"Unexpected vartype for Response\n"); 
            return -1; 
        } 

        HANDLE hFile; 
        // Open file Temp2.gif for output.
        hFile = CreateFile(TEXT("Temp2.gif"),     
            GENERIC_WRITE,                // Open for writing. 
            0,                            // Do not share. 
            NULL,                         // No security. 
            CREATE_ALWAYS,                // Overwrite existing.
            FILE_ATTRIBUTE_NORMAL,        // Normal file.
            NULL);                        // No attribute template.
        if (hFile == INVALID_HANDLE_VALUE) 
            {
            wprintf(L"Could not open file.");  // Process error.
            }
        else
            {
            // Copy data from the response stream to file. 
            cb = sizeof(bBuffer); 
            hr = pStream->Read(bBuffer, cb, &cbRead); 
            while (SUCCEEDED(hr) && 0 != cbRead) 
                { 
                if (!WriteFile(hFile, bBuffer, 
                               cbRead, &cbWritten, NULL)) 
                    { 
                    TraceErr("WriteFile fails with 0x%08lx\n", 
                             HRESULT_FROM_WIN32(GetLastError())); 
                    return -1; 
                    } 
                hr = pStream->Read(bBuffer, cb, &cbRead); 
                } 
            }
        CloseHandle(hFile);
        pStream->Release(); 
        VariantClear(&varResponse); 
    }
    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrResponse)
        SysFreeString(bstrResponse);
    
    CoUninitialize();
    return 0;
}
```



## <a name="requirements"></a><span data-ttu-id="a0d6d-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0d6d-121">Requirements</span></span>



| <span data-ttu-id="a0d6d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0d6d-122">Requirement</span></span> | <span data-ttu-id="a0d6d-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a0d6d-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0d6d-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0d6d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a0d6d-125">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="a0d6d-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="a0d6d-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0d6d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a0d6d-127">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="a0d6d-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="a0d6d-128">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="a0d6d-128">Redistributable</span></span><br/>          | <span data-ttu-id="a0d6d-129">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a0d6d-129">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="a0d6d-130">IDL</span><span class="sxs-lookup"><span data-stu-id="a0d6d-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a0d6d-131"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a0d6d-131"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="a0d6d-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="a0d6d-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="a0d6d-133"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0d6d-133"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="a0d6d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a0d6d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0d6d-135"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0d6d-135"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a0d6d-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0d6d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0d6d-137">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="a0d6d-137">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="a0d6d-138">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="a0d6d-138">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="a0d6d-139">**ResponseBody**</span><span class="sxs-lookup"><span data-stu-id="a0d6d-139">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)
</dt> <dt>

[<span data-ttu-id="a0d6d-140">**ResponseText**</span><span class="sxs-lookup"><span data-stu-id="a0d6d-140">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)
</dt> <dt>

[<span data-ttu-id="a0d6d-141">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a0d6d-141">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

