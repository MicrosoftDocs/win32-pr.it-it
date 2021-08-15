---
description: Ottiene un handle per un provider del servizio di crittografia (CSP) basato su un file di chiave privata o su un nome di contenitore di chiavi.
ms.assetid: 82cdaa6f-e747-4c9d-8d2d-5fa206891eed
title: Funzione PvkGetCryptProv
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkGetCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 5ba60ca31bf75e355126484608bfe9650b00fea60eaf876022e2de2bf5030470
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901321"
---
# <a name="pvkgetcryptprov-function"></a>Funzione PvkGetCryptProv

> [!IMPORTANT]
> Questa API è deprecata. Microsoft potrà rimuovere questa API nelle versioni future.

 

La **funzione PvkGetCryptProv** ottiene un handle per un [*provider*](../secgloss/c-gly.md) del servizio di crittografia (CSP) basato su un [*file*](../secgloss/p-gly.md) di chiave privata o su un nome di contenitore di chiavi.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per il collegamento dinamico a Mssign32.dll.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI PvkGetCryptProv(
  _In_      HWND       hwnd,
  _In_      LPCWSTR    pwszCaption,
  _In_      LPCWSTR    pwszCapiProvider,
  _In_      DWORD      dwProviderType,
  _In_      LPCWSTR    pwszPvkFile,
  _In_      LPCWSTR    pwszKeyContainerName,
  _Out_     DWORD      *pdwKeySpec,
  _Out_opt_ LPWSTR     *ppwszTmpContainer,
  _Out_     HCRYPTPROV *phCryptProv
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwnd* \[ Pollici\]
</dt> <dd>

Se è necessaria una password per decrittografare il file di chiave privata, questo parametro è un handle per l'elemento padre della finestra di dialogo della password. in caso contrario, è **NULL.**

</dd> <dt>

*pwszCaption* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null per la didascalia della finestra di dialogo.

</dd> <dt>

*pwszCapiProvider* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null per il nome CSP.

</dd> <dt>

*dwProviderType* \[ Pollici\]
</dt> <dd>

Valore **DWORD** che rappresenta il tipo di provider del servizio di crittografia. Per altre informazioni, vedere [Tipi di provider del servizio di crittografia.](cryptographic-provider-types.md)

</dd> <dt>

*pwszPvkFile* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che contiene il nome di un file di chiave privata.

</dd> <dt>

*pwszKeyContainerName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null per il nome del contenitore di chiavi private.

</dd> <dt>

*pdwKeySpec* \[ Cambio\]
</dt> <dd>

Puntatore a un **valore DWORD** per il tipo di chiave del contenitore restituito con *phCryptProv* e *ppwszTmpContainer.*

</dd> <dt>

*ppwszTmpContainer* \[ out, facoltativo\]
</dt> <dd>

Indirizzo di un puntatore a una stringa con terminazione Null per il nome del contenitore di chiavi temporaneo. La **funzione PvkGetCryptProv** fornisce e inizializza il contenitore temporaneo. Quando si **chiama PvkGetCryptProv,** l'indirizzo deve puntare a un **valore NULL.**

</dd> <dt>

*phCryptProv* \[ Cambio\]
</dt> <dd>

Puntatore a un handle per il CSP.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **S \_ OK**.

Se il metodo ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni.](common-hresult-values.md)

## <a name="remarks"></a>Commenti

La **funzione PvkGetCryptProv** tenta prima di tutto di ottenere l'handle del provider dal nome del contenitore di chiavi specificato dal *parametro pwszKeyContainerName.* Se si passa **NULL** per il *parametro pwszKeyContainerName,* **PvkGetCryptProv** tenta di ottenere il provider dal file di chiave privata specificato nel *parametro pwszPvkFile.*

Dopo aver terminato di usare il CSP, liberare l'handle del provider e il contenitore di chiavi temporaneo chiamando la [**funzione PvkFreeCryptProv.**](pvkfreecryptprov.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
