---
description: Salva una chiave privata e la relativa chiave pubblica corrispondente in un file specificato.
ms.assetid: 491a128a-b4aa-4cca-a835-d0e8d7df6720
title: PvkPrivateKeySave (funzione)
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
ms.openlocfilehash: ef60c3f615a704248fbcb8630322fa6b598141ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315368"
---
# <a name="pvkprivatekeysave-function"></a>PvkPrivateKeySave (funzione)

> [!IMPORTANT]
> Questa API è deprecata. Microsoft può rimuovere questa API nelle versioni future.

 

La funzione **PvkPrivateKeySave** salva una [*chiave privata*](../secgloss/p-gly.md) e la [*chiave pubblica*](../secgloss/p-gly.md) corrispondente in un file specificato.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.

 

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

*hCryptProv* \[ in\]
</dt> <dd>

Handle per un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).

</dd> <dt>

*hFile* \[ in\]
</dt> <dd>

Handle per un file creato con l'autorizzazione di lettura/scrittura iniziale e l'autorizzazione di sola lettura successiva.

</dd> <dt>

*dwKeySpec* \[ in\]
</dt> <dd>

Valore long integer per il tipo di chiave. I valori possibili sono **in fase di \_ scambio** o **di \_ firma**.

</dd> <dt>

*hwndOwner* \[ in\]
</dt> <dd>

Se è necessaria una password per crittografare la chiave privata, questo parametro è un handle per l'elemento padre della finestra di dialogo; in caso contrario, è **null**.

</dd> <dt>

*pwszKeyName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null per il nome della chiave da salvare.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Valore **DWORD** che specifica opzioni aggiuntive per la funzione. Per ulteriori informazioni, vedere il parametro *dwFlags* in [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Al termine dell'operazione, la funzione restituisce **true**. Se l'operazione ha esito negativo, la funzione **PvkPrivateKeySave** restituisce **false** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
