---
description: Salva una chiave privata e la chiave pubblica corrispondente in un file specificato.
ms.assetid: 491a128a-b4aa-4cca-a835-d0e8d7df6720
title: Funzione PvkPrivateKeySave
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeySave
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 3a2eed4b907f7c22414634a4b1ef49df6ca780181109a7396de2f8aa1776b7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901210"
---
# <a name="pvkprivatekeysave-function"></a>Funzione PvkPrivateKeySave

> [!IMPORTANT]
> Questa API è deprecata. Microsoft potrebbe rimuovere questa API nelle versioni future.

 

La **funzione PvkPrivateKeySave** [](../secgloss/p-gly.md) salva una chiave privata e la chiave [*pubblica corrispondente*](../secgloss/p-gly.md) in un file specificato.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI PvkPrivateKeySave(
  _In_ HCRYPTPROV hCryptProv,
  _In_ HANDLE     hFile,
  _In_ DWORD      dwKeySpec,
  _In_ HWND       hwndOwner,
  _In_ LPCWSTR    pwszKeyName,
  _In_ DWORD      dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hCryptProv* \[ Pollici\]
</dt> <dd>

Handle per un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).

</dd> <dt>

*hFile* \[ Pollici\]
</dt> <dd>

Handle per un file creato con l'autorizzazione di lettura/scrittura iniziale e l'autorizzazione di sola lettura successiva.

</dd> <dt>

*dwKeySpec* \[ Pollici\]
</dt> <dd>

Un long integer per il tipo di chiave. I valori possibili **includono AT \_ KEYEXCHANGE** o **AT \_ SIGNATURE.**

</dd> <dt>

*hwndOwner* \[ Pollici\]
</dt> <dd>

Se è necessaria una password per crittografare la chiave privata, questo parametro è un handle per l'elemento padre della finestra di dialogo. in caso contrario, è **NULL.**

</dd> <dt>

*pwszKeyName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null per il nome della chiave da salvare.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Valore **DWORD** che specifica opzioni aggiuntive per la funzione. Per altre informazioni, vedere *il parametro dwFlags* in [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, questa funzione restituisce **TRUE.** La **funzione PvkPrivateKeySave** restituisce **FALSE** se non riesce.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
