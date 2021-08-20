---
description: Rilascia l'handle a un provider del servizio di crittografia (CSP) ed eventualmente elimina il contenitore temporaneo creato dalla funzione PvkGetCryptProv.
ms.assetid: e7dcb5c5-dd80-4810-bf1f-4b7b921fa22c
title: Funzione PvkFreeCryptProv
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
ms.openlocfilehash: 7a49c97927cede4695f970ef4ef93623d7302724ed220605f650352987246157
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117975960"
---
# <a name="pvkfreecryptprov-function"></a>Funzione PvkFreeCryptProv

> [!IMPORTANT]
> Questa API è deprecata. Microsoft potrà rimuovere questa API nelle versioni future.

 

La **funzione PvkFreeCryptProv** rilascia l'handle a un [*provider*](../secgloss/c-gly.md) del servizio di crittografia (CSP) ed eventualmente elimina il contenitore temporaneo creato dalla [**funzione PvkGetCryptProv.**](pvkgetcryptprov.md)

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per il collegamento dinamico a Mssign32.dll.

 

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

*hProv* \[ Pollici\]
</dt> <dd>

Handle per il CSP.

</dd> <dt>

*pwszCapiProvider* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null per il nome CSP.

</dd> <dt>

*dwProviderType* \[ Pollici\]
</dt> <dd>

Valore **DWORD** che rappresenta il tipo di provider del servizio di crittografia. Per altre informazioni, vedere [Tipi di provider del servizio di crittografia.](cryptographic-provider-types.md)

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
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
