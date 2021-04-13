---
description: Ottiene un handle per un provider del servizio di crittografia (CSP) e una specifica della chiave per un contesto del certificato.
ms.assetid: ff72231f-e10f-49d2-b0e0-0008923803cc
title: GetCryptProvFromCert (funzione)
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
ms.openlocfilehash: bcd396c45333dee42bae4cb8bdfdd52792f1bdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350126"
---
# <a name="getcryptprovfromcert-function"></a>GetCryptProvFromCert (funzione)

> [!IMPORTANT]
> Questa API è deprecata. Microsoft può rimuovere questa API nelle versioni future.

 

La funzione **GetCryptProvFromCert** ottiene un handle per un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) e una specifica della chiave per un contesto del [*certificato*](../secgloss/c-gly.md) . Usare questa funzione per ottenere l'accesso alla [*chiave privata*](../secgloss/p-gly.md) dell'autorità emittente del certificato.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.

 

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

*HWND* \[ in\]
</dt> <dd>

Handle della finestra da utilizzare come proprietario di tutte le finestre di dialogo visualizzate. Questo membro non è attualmente in uso e viene ignorato. È possibile passare il **valore null** per questo parametro.

</dd> <dt>

*pCert* \[ in\]
</dt> <dd>

Puntatore a una struttura [**del \_ contesto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del certificato per il certificato.

</dd> <dt>

*phCryptProv* \[ out\]
</dt> <dd>

Puntatore a una struttura [**HCRYPTPROV**](hcryptprov.md) che rappresenta un handle per il CSP.

</dd> <dt>

*pdwKeySpec* \[ out\]
</dt> <dd>

Specifica della chiave privata da recuperare. I valori possibili sono **in fase di \_ scambio** o **di \_ firma**.

</dd> <dt>

*pfDidCryptAcquire* \[ in\]
</dt> <dd>

Valore che specifica se la funzione ha acquisito l'handle del provider in base al certificato.

</dd> <dt>

*ppwszTmpContainer* \[ out, facoltativo\]
</dt> <dd>

Indirizzo di un puntatore a una stringa con terminazione null per il nome del contenitore di chiavi temporaneo. La funzione **GetCryptProvFromCert** fornisce e inizializza il contenitore temporaneo. Quando si chiama **GetCryptProvFromCert**, l'indirizzo deve puntare a un valore **null** .

</dd> <dt>

*ppwszProviderName* \[ out, facoltativo\]
</dt> <dd>

Indirizzo di un puntatore a una stringa con terminazione null per il nome del provider. La funzione **GetCryptProvFromCert** restituisce il nome del provider. Quando si chiama **GetCryptProvFromCert**, l'indirizzo deve puntare a un valore **null** .

</dd> <dt>

*pdwProviderType* \[ out\]
</dt> <dd>

Specifica il tipo CSP. Può essere zero o uno dei tipi di [provider di crittografia](cryptographic-provider-types.md). Se questo membro è zero, il contenitore di chiavi è uno dei provider di archiviazione delle chiavi CNG.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Al termine dell'operazione, la funzione restituisce **true**. Se l'operazione ha esito negativo, la funzione **GetCryptProvFromCert** restituisce **false** .

## <a name="remarks"></a>Commenti

Lo strumento [Makecert](makecert.md) chiama **GetCryptProvFromCert** quando viene richiamato usando l'opzione della riga di comando **-is** .

Se il parametro *pfDidCryptAcquire* è impostato su **true**, la funzione imposta i parametri *phCryptProv*, *pdwKeySpec* e *pdwProviderType* sui valori del provider.

Al termine dell'utilizzo del CSP, liberarlo chiamando la funzione [**FreeCryptProvFromCert**](freecryptprovfromcert.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
