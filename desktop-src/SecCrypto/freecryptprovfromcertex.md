---
description: "Rilascia l'handle a un provider del servizio di crittografia (CSP) o a una chiave Cryptography API: Next Generation (CNG)."
ms.assetid: 76cbf8ae-c4ab-43d9-b06d-ea0b2a66368a
title: FreeCryptProvFromCertEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCertEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1be6270ebf9320a9c7527736b9fc4894cd50de9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884065"
---
# <a name="freecryptprovfromcertex-function"></a>FreeCryptProvFromCertEx (funzione)

La funzione **FreeCryptProvFromCertEx** rilascia l'handle a un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) o a una chiave Cryptography API: Next Generation (CNG).

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintassi


```C++
void WINAPI FreeCryptProvFromCertEx(
  _In_     BOOL                            fAcquired,
  _In_     HCRYPTPROV_OR_NCRYPT_KEY_HANDLE hProv,
           DWORD                           dwKeySpec,
  _In_opt_ LPWSTR                          pwszCapiProvider,
  _In_     DWORD                           dwProviderType,
  _In_opt_ LPWSTR                          pwszTmpContainer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fAcquired* \[ in\]
</dt> <dd>

Valore che specifica se l'handle del provider è stato acquisito dal [*certificato*](../secgloss/c-gly.md).

</dd> <dt>

*hProv* \[ in\]
</dt> <dd>

Handle per un CSP di CAPICOM o un handle per una chiave CNG.

</dd> <dt>

*dwKeySpec* 
</dt> <dd>

Indirizzo di una variabile **DWORD** che riceve informazioni aggiuntive sulla chiave. Può corrispondere a uno dei valori seguenti.



| Valore                                                                                                                                                                                | Significato                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <dt>**in \_ scambio di valute**</dt> </dl>                     | La coppia di chiavi è una coppia di scambio di chiavi.<br/>                                                                  |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <dt>**ALLA \_ firma**</dt> </dl>                           | La coppia di chiavi è una coppia di firme.<br/>                                                                     |
| <span id="CERT_NCRYPT_KEY_SPEC"></span><span id="cert_ncrypt_key_spec"></span><dl> <dt>**\_specifica della \_ chiave CERT NCRYPT \_**</dt> </dl> | La chiave è una chiave CNG.<br/> **Windows Server 2003 e Windows XP:** Questo valore non è supportato.<br/> |



 

</dd> <dt>

*pwszCapiProvider* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una stringa con terminazione null per il nome del provider.

</dd> <dt>

*dwProviderType* \[ in\]
</dt> <dd>

Specifica il tipo CSP. Può essere zero o uno dei tipi di [provider di crittografia](cryptographic-provider-types.md). Se questo membro è zero, il contenitore di chiavi è uno dei provider di archiviazione delle chiavi CNG.

</dd> <dt>

*pwszTmpContainer* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una stringa con terminazione null per il nome del contenitore di chiavi temporaneo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
