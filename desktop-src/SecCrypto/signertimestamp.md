---
description: Timestamp dell'oggetto specificato. Questa funzione supporta il timestamp Authenticode. Per eseguire il timestamp X.509 Public Key Infrastructure (RFC 3161), usare la funzione SignerTimeStampEx2.
ms.assetid: fb2c149b-dba2-4879-be97-831037e1110b
title: Funzione SignerTimeStamp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStamp
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: cb33852cb2860a29d43a41b2331a910a098384b872e972a74cf94f627bebf75a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898297"
---
# <a name="signertimestamp-function"></a>Funzione SignerTimeStamp

La **funzione SignerTimeStamp** indica l'oggetto specificato. Questa funzione supporta il timestamp Authenticode. Per eseguire il timestamp X.509 Public Key Infrastructure (RFC 3161), usare la [**funzione SignerTimeStampEx2.**](signertimestampex2.md)

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per il collegamento dinamico a Mssign32.dll.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI SignerTimeStamp(
  _In_     SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_     LPCWSTR             pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES   psRequest,
  _In_opt_ LPVOID              pSipData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSubjectInfo* \[ Pollici\]
</dt> <dd>

Indirizzo di una struttura [**SIGNER \_ SUBJECT \_ INFO**](signer-subject-info.md) che rappresenta l'oggetto da impostare come timestamp.

</dd> <dt>

*pwszHttpTimeStamp* \[ Pollici\]
</dt> <dd>

Indirizzo di una stringa Unicode con terminazione Null che contiene l'URL di un server timestamp.

</dd> <dt>

*psRequest* \[ in, facoltativo\]
</dt> <dd>

Indirizzo di una [**struttura CRYPT \_ ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) che contiene attributi aggiuntivi che vengono aggiunti alla richiesta del timestamp.

Questo parametro è facoltativo e può **essere NULL** se non è incluso.

</dd> <dt>

*pSipData* \[ in, facoltativo\]
</dt> <dd>

Valore a 32 bit passato come dati aggiuntivi alle funzioni SIP. Il formato e il contenuto di questo oggetto sono definiti dal provider SIP.

Questo parametro è facoltativo e può **essere NULL** se non è incluso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce S \_ OK.

Se la funzione ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni.](common-hresult-values.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
