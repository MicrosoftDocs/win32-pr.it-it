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
# <a name="internetgetproxyinfo-function"></a>Funzione InternetGetProxyInfo

> [!NOTE]
> Questa funzione è deprecata. Per il supporto del proxy AutoProxy, usare invece la versione 5,1 di servizi HTTP (WinHTTP). Per ulteriori informazioni, vedere [supporto del proxy AutoProxy WinHTTP](../winhttp/winhttp-autoproxy-support.md).

Recupera i dati proxy per l'accesso alle risorse specificate. Questa funzione può essere chiamata solo dal collegamento dinamico a "JSProxy.dll".

## <a name="syntax"></a>Sintassi

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

## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszURL* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica l'URL della risorsa HTTP di destinazione.

</dd> <dt>

*dwUrlLength* \[ in\]
</dt> <dd>

Dimensione, in byte, dell'URL a cui punta *lpszURL*.

</dd> <dt>

*lpszUrlHostName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome host dell'URL di destinazione.

</dd> <dt>

*dwUrlHostNameLength* \[ in\]
</dt> <dd>

Dimensione, in byte, del nome host a cui punta *lpszUrlHostName*.

</dd> <dt>

*lplpszProxyHostName* \[ out\]
</dt> <dd>

Puntatore all'indirizzo di un buffer che riceve l'URL del proxy da utilizzare in una richiesta HTTP per la risorsa specificata. L'applicazione è responsabile della liberazione di questa stringa.

</dd> <dt>

*lpdwProxyHostNameLength* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni, in byte, della stringa restituita nel buffer di *lplpszProxyHostName* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario. Per ottenere i dati degli errori estesi, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Commenti

Per chiamare **InternetGetProxyInfo**, è necessario collegarsi in modo dinamico usando il tipo di puntatore a funzione definito **pfnInternetGetProxyInfo**. Il frammento di codice seguente illustra come dichiarare un'istanza di questo tipo di puntatore a funzione e quindi inizializzarlo e chiamarlo.

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

Come tutti gli altri aspetti dell'API WinINet, questa funzione non può essere chiamata in modo sicuro da DllMain o dai costruttori e dai distruttori di oggetti globali.

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>JSProxy.dll</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[**InternetInitializeAutoProxyDll**](/windows/win32/api/winineti/nf-winineti-internetinitializeautoproxydll)

[**InternetDeInitializeAutoProxyDll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))

[**DetectAutoProxyUrl**](/windows/win32/api/winineti/nf-winineti-detectautoproxyurl)
