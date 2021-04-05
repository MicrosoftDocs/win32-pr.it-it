---
description: Ottiene un handle per un provider del servizio di crittografia (CSP) in base a un file di chiave privata o a un nome del contenitore di chiavi.
ms.assetid: 82cdaa6f-e747-4c9d-8d2d-5fa206891eed
title: PvkGetCryptProv (funzione)
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
ms.openlocfilehash: 026b31d021dc6ff2569ad9ce8f17d2e7f0d17b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885645"
---
# <a name="pvkgetcryptprov-function"></a>PvkGetCryptProv (funzione)

> [!IMPORTANT]
> Questa API è deprecata. Microsoft può rimuovere questa API nelle versioni future.

 

La funzione **PvkGetCryptProv** ottiene un handle per un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) in base a un file di [*chiave privata*](../secgloss/p-gly.md) o a un nome del contenitore di chiavi.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.

 

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

*HWND* \[ in\]
</dt> <dd>

Se è necessaria una password per decrittografare il file di chiave privata, questo parametro è un handle per l'elemento padre della finestra di dialogo password; in caso contrario, è **null**.

</dd> <dt>

*pwszCaption* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null per la didascalia della finestra di dialogo.

</dd> <dt>

*pwszCapiProvider* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null per il nome CSP.

</dd> <dt>

*dwProviderType* \[ in\]
</dt> <dd>

Valore **DWORD** che rappresenta il tipo di provider di crittografia. Per ulteriori informazioni, vedere [tipi di provider di crittografia](cryptographic-provider-types.md).

</dd> <dt>

*pwszPvkFile* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il nome di un file di chiave privata.

</dd> <dt>

*pwszKeyContainerName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null per il nome del contenitore di chiavi private.

</dd> <dt>

*pdwKeySpec* \[ out\]
</dt> <dd>

Puntatore a un valore **DWORD** per il tipo di chiave del contenitore restituito con *phCryptProv* e *ppwszTmpContainer*.

</dd> <dt>

*ppwszTmpContainer* \[ out, facoltativo\]
</dt> <dd>

Indirizzo di un puntatore a una stringa con terminazione null per il nome del contenitore di chiavi temporaneo. La funzione **PvkGetCryptProv** fornisce e inizializza il contenitore temporaneo. Quando si chiama **PvkGetCryptProv**, l'indirizzo deve puntare a un valore **null** .

</dd> <dt>

*phCryptProv* \[ out\]
</dt> <dd>

Puntatore a un handle per il CSP.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **S \_ OK**.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

## <a name="remarks"></a>Commenti

La funzione **PvkGetCryptProv** tenta prima di tutto di ottenere l'handle del provider dal nome del contenitore di chiavi specificato dal parametro *pwszKeyContainerName* . Se si passa **null** per il parametro *pwszKeyContainerName* , **PvkGetCryptProv** tenta di ottenere il provider dal file di chiave privata specificato nel parametro *pwszPvkFile* .

Al termine dell'utilizzo del CSP, liberare l'handle del provider e il contenitore di chiavi temporaneo chiamando la funzione [**PvkFreeCryptProv**](pvkfreecryptprov.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
