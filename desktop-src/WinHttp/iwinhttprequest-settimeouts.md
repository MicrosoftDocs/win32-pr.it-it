---
description: Il metodo setimeouts specifica i singoli componenti di timeout di un'operazione di invio/ricezione, in millisecondi.
ms.assetid: c2b6c432-5f3b-4361-8026-1b843c6697ae
title: 'Metodo IWinHttpRequest:: setimeouts'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetTimeouts
- WinHttpRequest.SetTimeouts
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 3f2f81585fdf444b6b5ab1795f183897687732ed
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104234919"
---
# <a name="iwinhttprequestsettimeouts-method"></a><span data-ttu-id="0fde7-103">Metodo IWinHttpRequest:: setimeouts</span><span class="sxs-lookup"><span data-stu-id="0fde7-103">IWinHttpRequest::SetTimeouts method</span></span>

<span data-ttu-id="0fde7-104">Il metodo **Setimeouts** specifica i singoli componenti di timeout di un'operazione di invio/ricezione, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="0fde7-104">The **SetTimeouts** method specifies the individual time-out components of a send/receive operation, in milliseconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fde7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0fde7-105">Syntax</span></span>


```C++
HRESULT SetTimeouts(
  [in] long ResolveTimeout,
  [in] long ConnectTimeout,
  [in] long SendTimeout,
  [in] long ReceiveTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="0fde7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0fde7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fde7-107">*ResolveTimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0fde7-107">*ResolveTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fde7-108">Valore di timeout applicato durante la risoluzione di un nome host (ad esempio `www.microsoft.com` ) in un indirizzo IP (ad esempio 192.168.131.199), in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="0fde7-108">Time-out value applied when resolving a host name (such as `www.microsoft.com`) to an IP address (such as 192.168.131.199), in milliseconds.</span></span> <span data-ttu-id="0fde7-109">Il valore predefinito è zero, ovvero nessun timeout (infinito).</span><span class="sxs-lookup"><span data-stu-id="0fde7-109">The default value is zero, meaning no time-out (infinite).</span></span> <span data-ttu-id="0fde7-110">Se il timeout DNS viene specificato con \_ il \_ timeout di risoluzione dei nomi, si verifica un sovraccarico di un thread per ogni richiesta.</span><span class="sxs-lookup"><span data-stu-id="0fde7-110">If DNS timeout is specified using NAME\_RESOLUTION\_TIMEOUT, there is an overhead of one thread per request.</span></span>

</dd> <dt>

<span data-ttu-id="0fde7-111">*ConnectTimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0fde7-111">*ConnectTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fde7-112">Valore di timeout applicato quando si stabilisce un socket di comunicazione con il server di destinazione, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="0fde7-112">Time-out value applied when establishing a communication socket with the target server, in milliseconds.</span></span> <span data-ttu-id="0fde7-113">Il valore predefinito è 60.000 (60 secondi).</span><span class="sxs-lookup"><span data-stu-id="0fde7-113">The default value is 60,000 (60 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="0fde7-114">*SendTimeout nell'elemento* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0fde7-114">*SendTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fde7-115">Valore di timeout applicato quando si invia un singolo pacchetto di dati di richiesta sul socket di comunicazione al server di destinazione, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="0fde7-115">Time-out value applied when sending an individual packet of request data on the communication socket to the target server, in milliseconds.</span></span> <span data-ttu-id="0fde7-116">Una richiesta di grandi dimensioni inviata a un server HTTP in genere viene suddivisa in più pacchetti; il timeout di invio si applica all'invio di ogni pacchetto singolarmente.</span><span class="sxs-lookup"><span data-stu-id="0fde7-116">A large request sent to an HTTP server are normally be broken up into multiple packets; the send time-out applies to sending each packet individually.</span></span> <span data-ttu-id="0fde7-117">Il valore predefinito è 30.000 (30 secondi).</span><span class="sxs-lookup"><span data-stu-id="0fde7-117">The default value is 30,000 (30 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="0fde7-118">*ReceiveTimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0fde7-118">*ReceiveTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fde7-119">Valore di timeout applicato durante la ricezione di un pacchetto di dati di risposta dal server di destinazione, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="0fde7-119">Time-out value applied when receiving a packet of response data from the target server, in milliseconds.</span></span> <span data-ttu-id="0fde7-120">Le risposte di grandi dimensioni vengono suddivise in più pacchetti; il timeout di ricezione si applica al recupero di ogni pacchetto di dati dal socket.</span><span class="sxs-lookup"><span data-stu-id="0fde7-120">Large responses are be broken up into multiple packets; the receive time-out applies to fetching each packet of data off the socket.</span></span> <span data-ttu-id="0fde7-121">Il valore predefinito è 30.000 (30 secondi).</span><span class="sxs-lookup"><span data-stu-id="0fde7-121">The default value is 30,000 (30 seconds).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fde7-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0fde7-122">Return value</span></span>

<span data-ttu-id="0fde7-123">Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="0fde7-123">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fde7-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="0fde7-124">Remarks</span></span>

<span data-ttu-id="0fde7-125">Tutti i parametri sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="0fde7-125">All parameters are required.</span></span> <span data-ttu-id="0fde7-126">Un valore pari a 0 o-1 imposta un timeout per un'attesa infinita.</span><span class="sxs-lookup"><span data-stu-id="0fde7-126">A value of 0 or -1 sets a time-out to wait infinitely.</span></span> <span data-ttu-id="0fde7-127">Un valore maggiore di 0 imposta il valore di timeout in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="0fde7-127">A value greater than 0 sets the time-out value in milliseconds.</span></span> <span data-ttu-id="0fde7-128">30.000, ad esempio, imposterà il timeout su 30 secondi.</span><span class="sxs-lookup"><span data-stu-id="0fde7-128">For example, 30,000 would set the time-out to 30 seconds.</span></span> <span data-ttu-id="0fde7-129">Tutti i valori negativi diversi da-1 determinano l'esito negativo di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="0fde7-129">All negative values other than -1 cause this method to fail.</span></span>

<span data-ttu-id="0fde7-130">I valori di timeout vengono applicati a livello di Winsock.</span><span class="sxs-lookup"><span data-stu-id="0fde7-130">Time-out values are applied at the Winsock layer.</span></span>

> [!Note]  
> <span data-ttu-id="0fde7-131">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="0fde7-131">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="0fde7-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="0fde7-132">Examples</span></span>

<span data-ttu-id="0fde7-133">Nell'esempio seguente viene illustrato come impostare tutti i timeout di WinHTTP su 30 secondi, aprire una connessione HTTP, inviare una richiesta HTTP e leggere il testo della risposta.</span><span class="sxs-lookup"><span data-stu-id="0fde7-133">The following example shows how to set all WinHTTP time-outs to 30 seconds, open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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

int main()
{
    // variable for return value
    HRESULT    hr;

    // initialize COM
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varFalse;
    VARIANT         varEmpty;

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

    if (SUCCEEDED(hr))
    {    // Set Time-outs.
        hr = pIWinHttpRequest->SetTimeouts(30000, 30000,
                                           30000, 30000);
    }
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod,
                                    bstrUrl,
                                    varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->GetAllResponseHeaders(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to console.
        wprintf(L"%.256s",bstrResponse);
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



<span data-ttu-id="0fde7-134">Nell'esempio di script seguente viene illustrato come impostare tutti i timeout di WinHTTP su 30 secondi, aprire una connessione HTTP e inviare una richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="0fde7-134">The following scripting example shows how to set all WinHTTP time-outs to 30 seconds, open an HTTP connection, and send an HTTP request.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Set time-outs. If time-outs are set, they must 
// be set before open.
WinHttpReq.SetTimeouts(30000, 30000, 30000, 30000);

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="0fde7-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0fde7-135">Requirements</span></span>



| <span data-ttu-id="0fde7-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fde7-136">Requirement</span></span> | <span data-ttu-id="0fde7-137">Valore</span><span class="sxs-lookup"><span data-stu-id="0fde7-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fde7-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fde7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0fde7-139">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="0fde7-139">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="0fde7-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fde7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0fde7-141">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="0fde7-141">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="0fde7-142">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="0fde7-142">Redistributable</span></span><br/>          | <span data-ttu-id="0fde7-143">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="0fde7-143">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="0fde7-144">IDL</span><span class="sxs-lookup"><span data-stu-id="0fde7-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0fde7-145"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0fde7-145"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="0fde7-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="0fde7-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="0fde7-147"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0fde7-147"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="0fde7-148">DLL</span><span class="sxs-lookup"><span data-stu-id="0fde7-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fde7-149"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fde7-149"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0fde7-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0fde7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fde7-151">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="0fde7-151">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="0fde7-152">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="0fde7-152">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="0fde7-153">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="0fde7-153">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




