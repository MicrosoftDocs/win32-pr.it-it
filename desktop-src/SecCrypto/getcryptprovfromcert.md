---
description: Ottiene un handle per un provider del servizio di crittografia (CSP) e una specifica della chiave per un contesto di certificato.
ms.assetid: ff72231f-e10f-49d2-b0e0-0008923803cc
title: Funzione GetCryptProvFromCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: c885c439014a26bafba3be8614981c67d200e9f87cd4e3c4f03e8cbcc1b77e38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006659"
---
# <a name="getcryptprovfromcert-function"></a>Funzione GetCryptProvFromCert

> [!IMPORTANT]
> Questa API è deprecata. Microsoft potrebbe rimuovere questa API nelle versioni future.

 

La **funzione GetCryptProvFromCert** ottiene un handle per un [*provider*](../secgloss/c-gly.md) del servizio di crittografia (CSP) e una specifica della chiave per un [*contesto di*](../secgloss/c-gly.md) certificato. Usare questa funzione per ottenere l'accesso alla [*chiave privata*](../secgloss/p-gly.md) dell'autorità emittente del certificato.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI GetCryptProvFromCert(
  _In_      HWND           hwnd,
  _In_      PCCERT_CONTEXT pCert,
  _Out_     HCRYPTPROV     *phCryptProv,
  _Out_     DWORD          *pdwKeySpec,
  _In_      BOOL           *pfDidCryptAcquire,
  _Out_opt_ LPWSTR         *ppwszTmpContainer,
  _Out_opt_ LPWSTR         *ppwszProviderName,
  _Out_     DWORD          *pdwProviderType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwnd* \[ Pollici\]
</dt> <dd>

Handle della finestra da utilizzare come proprietario di tutte le finestre di dialogo visualizzate. Questo membro non è attualmente usato e viene ignorato. È sicuro passare **NULL per** questo parametro.

</dd> <dt>

*pCert* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura CERT \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) per il certificato.

</dd> <dt>

*phCryptProv* \[ Cambio\]
</dt> <dd>

Puntatore a una [**struttura HCRYPTPROV**](hcryptprov.md) che è un handle per CSP.

</dd> <dt>

*pdwKeySpec* \[ Cambio\]
</dt> <dd>

Specifica della chiave privata da recuperare. I valori possibili **includono AT \_ KEYEXCHANGE** o **AT \_ SIGNATURE.**

</dd> <dt>

*pfDidCryptAcquire* \[ Pollici\]
</dt> <dd>

Valore che specifica se la funzione ha acquisito l'handle del provider in base al certificato.

</dd> <dt>

*ppwszTmpContainer* \[ out, facoltativo\]
</dt> <dd>

Indirizzo di un puntatore a una stringa con terminazione Null per il nome del contenitore di chiavi temporaneo. La **funzione GetCryptProvFromCert** fornisce e inizializza il contenitore temporaneo. Quando si **chiama GetCryptProvFromCert,** l'indirizzo deve puntare a un **valore NULL.**

</dd> <dt>

*ppwszProviderName* \[ out, facoltativo\]
</dt> <dd>

Indirizzo di un puntatore a una stringa con terminazione Null per il nome del provider. La **funzione GetCryptProvFromCert** restituisce il nome del provider. Quando si **chiama GetCryptProvFromCert,** l'indirizzo deve puntare a un **valore NULL.**

</dd> <dt>

*pdwProviderType* \[ Cambio\]
</dt> <dd>

Specifica il tipo CSP. Può essere zero o uno dei tipi [di provider di crittografia](cryptographic-provider-types.md). Se questo membro è zero, il contenitore di chiavi è uno dei provider di archiviazione chiavi CNG.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, questa funzione restituisce **TRUE.** La **funzione GetCryptProvFromCert** restituisce **FALSE in** caso di errore.

## <a name="remarks"></a>Commenti

Lo [strumento MakeCert](makecert.md) chiama **GetCryptProvFromCert** quando lo si richiama usando l'opzione della riga di comando **-is.**

Se il *parametro pfDidCryptAcquire* è impostato su **TRUE,** la funzione imposta i parametri *phCryptProv*, *pdwKeySpec* e *pdwProviderType* sui valori del provider.

Al termine dell'uso del provider di servizi di configurazione, liberarlo chiamando la [**funzione FreeCryptProvFromCert.**](freecryptprovfromcert.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
