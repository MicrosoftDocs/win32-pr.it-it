---
description: Consente di creare un contenitore temporaneo nel provider del servizio di crittografia (CSP) e di caricare una chiave privata dalla memoria nel contenitore.
ms.assetid: 9388b49b-fad4-4499-a391-fe58ed672552
title: PvkPrivateKeyAcquireContextFromMemory (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeyAcquireContextFromMemory
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1552d1e35845ffb7407d11d6e520b914ab805d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348486"
---
# <a name="pvkprivatekeyacquirecontextfrommemory-function"></a>PvkPrivateKeyAcquireContextFromMemory (funzione)

> [!IMPORTANT]
> Questa API è deprecata. Microsoft può rimuovere questa API nelle versioni future.

 

La funzione **PvkPrivateKeyAcquireContextFromMemory** crea un contenitore temporaneo nel [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) e carica una [*chiave privata*](../secgloss/p-gly.md) dalla memoria nel contenitore.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI PvkPrivateKeyAcquireContextFromMemory(
  _In_        LPCWSTR    pwszProvName,
  _In_        DWORD      dwProvType,
  _In_        BYTE       *pbData,
  _In_        DWORD      cbData,
  _In_        HWND       hwndOwner,
  _In_        LPCWSTR    pwszKeyName,
  _Inout_opt_ DWORD      *pdwKeySpec,
  _Out_       HCRYPTPROV *phCryptProv,
  _Out_       LPTSTR     *ppwszTmpContainer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwszProvName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il nome del CSP il cui tipo è richiesto in *dwProvType*.

</dd> <dt>

*dwProvType* \[ in\]
</dt> <dd>

Valore **DWORD** per il tipo CSP. Per ulteriori informazioni sui tipi CSP, vedere [tipi di provider di crittografia](cryptographic-provider-types.md).

</dd> <dt>

*pbData* \[ in\]
</dt> <dd>

Puntatore a un buffer per ricevere i dati di contesto. Il chiamante deve fornire questa risorsa.

</dd> <dt>

*cbData* \[ in\]
</dt> <dd>

Valore **DWORD** che specifica la dimensione, in byte, del buffer *pbData* . Il chiamante deve fornire questo valore.

</dd> <dt>

*hwndOwner* \[ in\]
</dt> <dd>

Se è necessaria una password per decrittografare i dati di contesto a cui punta il parametro *pbData* , questo parametro è un handle per l'elemento padre della finestra di dialogo. in caso contrario, è **null**.

</dd> <dt>

*pwszKeyName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il nome della chiave da recuperare.

</dd> <dt>

*pdwKeySpec* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a un valore **DWORD** che specifica il tipo di chiave. I valori possibili sono **in fase di \_ scambio** o **di \_ firma**.

</dd> <dt>

*phCryptProv* \[ out\]
</dt> <dd>

Puntatore a un handle per il CSP.

</dd> <dt>

*ppwszTmpContainer* \[ out\]
</dt> <dd>

Indirizzo di un puntatore a una stringa con terminazione null per il nome del contenitore temporaneo. La funzione **PvkPrivateKeyAcquireContextFromMemory** fornisce il buffer per questa stringa e lo inizializza. Quando si chiama **PvkPrivateKeyAcquireContextFromMemory**, l'indirizzo deve puntare a un valore **null** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Al termine dell'operazione, la funzione restituisce **true**. Se l'operazione ha esito negativo, la funzione **PvkPrivateKeyAcquireContextFromMemory** restituisce **false** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
