---
description: Timestamp dell'oggetto specificato e, facoltativamente, restituisce un puntatore a una struttura SIGNER \_ CONTEXT che contiene un puntatore a un BLOB. Questa funzione può essere usata per eseguire L'infrastruttura a chiave pubblica X.509, RFC 3161&\# 8211; conforme, timestamp.
ms.assetid: fb82545b-c00f-44eb-96f4-aa27a125c8d9
title: Funzione SignerTimeStampEx2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: c5a9bfc81c3196657f611c9263e0d957ca867a64479b34900dce7078237e195f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898270"
---
# <a name="signertimestampex2-function"></a>Funzione SignerTimeStampEx2

La **funzione SignerTimeStampEx2** contrassegna l'oggetto specificato e restituisce facoltativamente un puntatore a una [**struttura SIGNER \_ CONTEXT**](signer-context.md) che contiene un puntatore a un [*BLOB.*](../secgloss/b-gly.md) Questa funzione può essere usata per eseguire timestamp con chiave pubblica X.509, conformi a RFC 3161.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per il collegamento dinamico a Mssign32.dll.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI SignerTimeStampEx2(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       ALG_ID              dwAlgId,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Valore che specifica il tipo di timestamp da generare. Questo parametro può avere uno dei valori seguenti. I valori si escludono a vicenda.



| Valore                                                                                                                                                                                                          | Significato                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt>**\_AUTHENTICODE DEL TIMESTAMP \_ DEL FIRMATARIO**</dt> </dl> | Specifica un timestamp Authenticode.<br/>       |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt>**TIMESTAMP \_ DEL \_ FIRMATARIO RFC3161**</dt> </dl>                | Specifica un timestamp conforme a RFC 3161.<br/> |



 

</dd> <dt>

*pSubjectInfo* \[ Pollici\]
</dt> <dd>

Indirizzo di una struttura [**SIGNER \_ SUBJECT \_ INFO**](signer-subject-info.md) che rappresenta l'oggetto da impostare come timestamp.

</dd> <dt>

*pwszHttpTimeStamp* \[ Pollici\]
</dt> <dd>

Indirizzo di una stringa Unicode con terminazione Null che contiene l'URL di un server timestamp.

</dd> <dt>

*dwAlgId* \[ Pollici\]
</dt> <dd>

Specifica un algoritmo hash da utilizzare per l'esecuzione di timestamp conformi a RFC 3161. Questo parametro viene ignorato per i timestamp Authenticode.

</dd> <dt>

*psRequest* \[ Pollici\]
</dt> <dd>

facoltativo. Indirizzo di una [**struttura CRYPT \_ ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) che contiene attributi aggiuntivi che vengono aggiunti alla richiesta di timestamp.

Questo parametro è facoltativo e può essere **NULL** se non è incluso.

</dd> <dt>

*pSipData* \[ Pollici\]
</dt> <dd>

facoltativo. Valore a 32 bit passato come dati aggiuntivi alle funzioni [*DELS (Subject Interface Package).*](../secgloss/s-gly.md) Il formato e il contenuto di questo parametro sono definiti dal provider SIP.

Questo parametro è facoltativo e può essere **NULL** se non è incluso.

</dd> <dt>

*ppSignerContext* \[ Cambio\]
</dt> <dd>

facoltativo. Indirizzo di un puntatore alla struttura [**SIGNER \_ CONTEXT**](signer-context.md) che contiene il BLOB firmato. Al termine dell'uso della **struttura SIGNER \_ CONTEXT,** liberarla chiamando la [**funzione SignerFreeSignerContext.**](signerfreesignercontext.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce S \_ OK.

Se la funzione ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni](common-hresult-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> <dt>

[**SignerTimeStampEx**](signertimestampex.md)
</dt> </dl>

 

 
