---
title: Funzione InternetGetProxyInfo
description: Recupera i dati proxy per l'accesso alle risorse specificate.
ms.assetid: 5fc0f471-420c-4125-8323-cb1e1e72e43f
keywords:
- Funzione InternetGetProxyInfo WinINet
topic_type:
- apiref
api_name:
- InternetGetProxyInfo
api_location:
- JSProxy.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef441754fd5de09e3792d9269f05d96ecc08aa23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400639"
---
# <a name="internetgetproxyinfo-function"></a><span data-ttu-id="b515c-104">Funzione InternetGetProxyInfo</span><span class="sxs-lookup"><span data-stu-id="b515c-104">InternetGetProxyInfo function</span></span>

> [!NOTE]
> <span data-ttu-id="b515c-105">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="b515c-105">This function is deprecated.</span></span> <span data-ttu-id="b515c-106">Per il supporto del proxy AutoProxy, usare invece la versione 5,1 di servizi HTTP (WinHTTP).</span><span class="sxs-lookup"><span data-stu-id="b515c-106">For autoproxy support, use HTTP Services (WinHTTP) version 5.1 instead.</span></span> <span data-ttu-id="b515c-107">Per ulteriori informazioni, vedere [supporto del proxy AutoProxy WinHTTP](../winhttp/winhttp-autoproxy-support.md).</span><span class="sxs-lookup"><span data-stu-id="b515c-107">For more information, see [WinHTTP AutoProxy Support](../winhttp/winhttp-autoproxy-support.md).</span></span>

<span data-ttu-id="b515c-108">Recupera i dati proxy per l'accesso alle risorse specificate.</span><span class="sxs-lookup"><span data-stu-id="b515c-108">Retrieves proxy data for accessing specified resources.</span></span> <span data-ttu-id="b515c-109">Questa funzione può essere chiamata solo dal collegamento dinamico a "JSProxy.dll".</span><span class="sxs-lookup"><span data-stu-id="b515c-109">This function can only be called by dynamically linking to "JSProxy.dll".</span></span>

## <a name="syntax"></a><span data-ttu-id="b515c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b515c-110">Syntax</span></span>

```cpp
BOOL InternetGetProxyInfo(
  _In_  LPCSTR  lpszUrl,
  _In_  DWORD   dwUrlLength,
  _In_  LPSTR   lpszUrlHostName,
  _In_  DWORD   dwUrlHostNameLength,
  _Out_ LPSTR   *lplpszProxyHostName,
  _Out_ LPDWORD lpdwProxyHostNameLength
);
```

## <a name="parameters"></a><span data-ttu-id="b515c-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="b515c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b515c-112">*lpszURL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b515c-112">*lpszUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b515c-113">Puntatore a una stringa con terminazione null che specifica l'URL della risorsa HTTP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b515c-113">A pointer to a null-terminated string that specifies the URL of the target HTTP resource.</span></span>

</dd> <dt>

<span data-ttu-id="b515c-114">*dwUrlLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b515c-114">*dwUrlLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b515c-115">Dimensione, in byte, dell'URL a cui punta *lpszURL*.</span><span class="sxs-lookup"><span data-stu-id="b515c-115">The size, in bytes, of the URL pointed to by *lpszUrl*.</span></span>

</dd> <dt>

<span data-ttu-id="b515c-116">*lpszUrlHostName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b515c-116">*lpszUrlHostName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b515c-117">Puntatore a una stringa con terminazione null che specifica il nome host dell'URL di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b515c-117">A pointer to a null-terminated string that specifies the host name of the target URL.</span></span>

</dd> <dt>

<span data-ttu-id="b515c-118">*dwUrlHostNameLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b515c-118">*dwUrlHostNameLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b515c-119">Dimensione, in byte, del nome host a cui punta *lpszUrlHostName*.</span><span class="sxs-lookup"><span data-stu-id="b515c-119">The size, in bytes, of the host name pointed to by *lpszUrlHostName*.</span></span>

</dd> <dt>

<span data-ttu-id="b515c-120">*lplpszProxyHostName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b515c-120">*lplpszProxyHostName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b515c-121">Puntatore all'indirizzo di un buffer che riceve l'URL del proxy da utilizzare in una richiesta HTTP per la risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="b515c-121">A pointer to the address of a buffer that receives the URL of the proxy to use in an HTTP request for the specified resource.</span></span> <span data-ttu-id="b515c-122">L'applicazione è responsabile della liberazione di questa stringa.</span><span class="sxs-lookup"><span data-stu-id="b515c-122">The application is responsible for freeing this string.</span></span>

</dd> <dt>

<span data-ttu-id="b515c-123">*lpdwProxyHostNameLength* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b515c-123">*lpdwProxyHostNameLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b515c-124">Puntatore a una variabile che riceve le dimensioni, in byte, della stringa restituita nel buffer di *lplpszProxyHostName* .</span><span class="sxs-lookup"><span data-stu-id="b515c-124">A pointer to a variable that receives the size, in bytes, of the string returned in the *lplpszProxyHostName* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b515c-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b515c-125">Return value</span></span>

<span data-ttu-id="b515c-126">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b515c-126">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="b515c-127">Per ottenere i dati degli errori estesi, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="b515c-127">To get extended error data, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="b515c-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="b515c-128">Remarks</span></span>

<span data-ttu-id="b515c-129">Per chiamare **InternetGetProxyInfo**, è necessario collegarsi in modo dinamico usando il tipo di puntatore a funzione definito **pfnInternetGetProxyInfo**.</span><span class="sxs-lookup"><span data-stu-id="b515c-129">To call **InternetGetProxyInfo**, you must dynamically link to it using the defined function-pointer type **pfnInternetGetProxyInfo**.</span></span> <span data-ttu-id="b515c-130">Il frammento di codice seguente illustra come dichiarare un'istanza di questo tipo di puntatore a funzione e quindi inizializzarlo e chiamarlo.</span><span class="sxs-lookup"><span data-stu-id="b515c-130">The code snippet below shows how to declare an instance of this function-pointer type and then initialize and call it.</span></span>

```cpp
  HMODULE hModJS;                               // Handle for loading the DLL
  pfnInternetGetProxyInfo pIGPI;                // Function-pointer instance

  hModJS = LoadLibrary( TEXT("jsproxy.dll") );
  if (!hModJS)
  {
    _tprintf( TEXT("\nLoadLibrary failed to load jsproxy.dll with error: %d\n"),
            GetLastError( ) );
    return( FALSE );
  }

  pIGPI = (pfnInternetGetProxyInfo)
          GetProcAddress( hModJS, "InternetGetProxyInfo" );
  if (!pIGPI)         
  {
    _tprintf( TEXT("\nGetProcAddress failed to find InternetGetProxyInfo, error: %d\n"),
            GetLastError( ) );
    return( FALSE );
  }

  // The pIGPI function pointer can now be used to call InternetGetProxyInfo.
```

<span data-ttu-id="b515c-131">Come tutti gli altri aspetti dell'API WinINet, questa funzione non può essere chiamata in modo sicuro da DllMain o dai costruttori e dai distruttori di oggetti globali.</span><span class="sxs-lookup"><span data-stu-id="b515c-131">Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.</span></span>

> [!Note]  
> <span data-ttu-id="b515c-132">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="b515c-132">WinINet does not support server implementations.</span></span> <span data-ttu-id="b515c-133">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="b515c-133">In addition, it should not be used from a service.</span></span> <span data-ttu-id="b515c-134">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="b515c-134">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

## <a name="requirements"></a><span data-ttu-id="b515c-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b515c-135">Requirements</span></span>

| <span data-ttu-id="b515c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b515c-136">Requirement</span></span> | <span data-ttu-id="b515c-137">Valore</span><span class="sxs-lookup"><span data-stu-id="b515c-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b515c-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b515c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b515c-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b515c-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b515c-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b515c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b515c-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b515c-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b515c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b515c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b515c-143"><dt>JSProxy.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b515c-143"><dt>JSProxy.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="b515c-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b515c-144">See also</span></span>

[<span data-ttu-id="b515c-145">**InternetInitializeAutoProxyDll**</span><span class="sxs-lookup"><span data-stu-id="b515c-145">**InternetInitializeAutoProxyDll**</span></span>](/windows/win32/api/winineti/nf-winineti-internetinitializeautoproxydll)

<span data-ttu-id="b515c-146">[**InternetDeInitializeAutoProxyDll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b515c-146">[**InternetDeInitializeAutoProxyDll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))</span></span>

[<span data-ttu-id="b515c-147">**DetectAutoProxyUrl**</span><span class="sxs-lookup"><span data-stu-id="b515c-147">**DetectAutoProxyUrl**</span></span>](/windows/win32/api/winineti/nf-winineti-detectautoproxyurl)
