---
description: Rilascia l'handle a un provider del servizio di crittografia (CSP) ed eventualmente elimina il contenitore temporaneo creato dalla funzione GetCryptProvFromCert.
ms.assetid: 4462eef2-7056-4e48-aa96-c46f29b701d6
title: FreeCryptProvFromCert (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 8201de475a4224aea58267405ccde244e56d59f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884066"
---
# <a name="freecryptprovfromcert-function"></a>FreeCryptProvFromCert (funzione)

> [!IMPORTANT]
> Questa API è deprecata. Microsoft può rimuovere questa API nelle versioni future.

 

La funzione **FreeCryptProvFromCert** rilascia l'handle a un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) ed eventualmente elimina il contenitore temporaneo creato dalla funzione [**GetCryptProvFromCert**](getcryptprovfromcert.md) .

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintassi


```C++
void WINAPI FreeCryptProvFromCert(
  _In_     BOOL       fAcquired,
  _In_     HCRYPTPROV hProv,
  _In_opt_ LPWSTR     pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
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

Puntatore a una struttura [**HCRYPTPROV**](hcryptprov.md) per il CSP.

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
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
