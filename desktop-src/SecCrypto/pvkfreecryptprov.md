---
description: Rilascia l'handle a un provider del servizio di crittografia (CSP) ed eventualmente elimina il contenitore temporaneo creato dalla funzione PvkGetCryptProv.
ms.assetid: e7dcb5c5-dd80-4810-bf1f-4b7b921fa22c
title: PvkFreeCryptProv (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkFreeCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 70ff29c968fe8f50c813f1da71b2e73a112f25f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317709"
---
# <a name="pvkfreecryptprov-function"></a>PvkFreeCryptProv (funzione)

> [!IMPORTANT]
> Questa API è deprecata. Microsoft può rimuovere questa API nelle versioni future.

 

La funzione **PvkFreeCryptProv** rilascia l'handle a un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) ed eventualmente elimina il contenitore temporaneo creato dalla funzione [**PvkGetCryptProv**](pvkgetcryptprov.md) .

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintassi


```C++
void WINAPI PvkFreeCryptProv(
  _In_     HCRYPTPROV hProv,
  _In_     LPCWSTR    pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProv* \[ in\]
</dt> <dd>

Handle per il CSP.

</dd> <dt>

*pwszCapiProvider* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null per il nome CSP.

</dd> <dt>

*dwProviderType* \[ in\]
</dt> <dd>

Valore **DWORD** che rappresenta il tipo di provider di crittografia. Per ulteriori informazioni, vedere [tipi di provider di crittografia](cryptographic-provider-types.md).

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



 

 
