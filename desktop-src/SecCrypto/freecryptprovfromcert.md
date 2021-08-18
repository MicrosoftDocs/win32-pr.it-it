---
description: Rilascia l'handle a un provider del servizio di crittografia (CSP) ed elimina facoltativamente il contenitore temporaneo creato dalla funzione GetCryptProvFromCert.
ms.assetid: 4462eef2-7056-4e48-aa96-c46f29b701d6
title: Funzione FreeCryptProvFromCert
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
ms.openlocfilehash: 8797a6f48bcfb973a6c07a4b05ae0d39bc3b4522ab6f7ae70a80eaa77081da44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006789"
---
# <a name="freecryptprovfromcert-function"></a>Funzione FreeCryptProvFromCert

> [!IMPORTANT]
> Questa API è deprecata. Microsoft potrebbe rimuovere questa API nelle versioni future.

 

La **funzione FreeCryptProvFromCert** rilascia l'handle a un [*provider*](../secgloss/c-gly.md) del servizio di crittografia (CSP) ed elimina facoltativamente il contenitore temporaneo creato dalla [**funzione GetCryptProvFromCert.**](getcryptprovfromcert.md)

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente a Mssign32.dll.

 

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

*fAcquired* \[ Pollici\]
</dt> <dd>

Valore che specifica se l'handle del provider è stato acquisito dal [*certificato*](../secgloss/c-gly.md).

</dd> <dt>

*hProv* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura HCRYPTPROV**](hcryptprov.md) per CSP.

</dd> <dt>

*pwszCapiProvider* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una stringa con terminazione Null per il nome del provider.

</dd> <dt>

*dwProviderType* \[ Pollici\]
</dt> <dd>

Specifica il tipo CSP. Può essere zero o uno dei tipi [di provider di crittografia](cryptographic-provider-types.md). Se questo membro è zero, il contenitore di chiavi è uno dei provider di archiviazione chiavi CNG.

</dd> <dt>

*pwszTmpContainer* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una stringa con terminazione Null per il nome del contenitore di chiavi temporaneo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
