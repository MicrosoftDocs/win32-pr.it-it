---
description: Timestamp l'oggetto specificato e, facoltativamente, restituisce un puntatore a una struttura del contesto del FIRMATARIo \_ che contiene un puntatore a un BLOB. Questa funzione può essere usata per eseguire l'infrastruttura a chiave pubblica X. 509, i timestamp RFC 3161&\# 8211; conformi.
ms.assetid: fb82545b-c00f-44eb-96f4-aa27a125c8d9
title: SignerTimeStampEx2 (funzione)
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
ms.openlocfilehash: 07dc9162c9cb8832e93e2518c7208d235d878875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316654"
---
# <a name="signertimestampex2-function"></a>SignerTimeStampEx2 (funzione)

Il timestamp della funzione **SignerTimeStampEx2** indica l'oggetto specificato e, facoltativamente, restituisce un puntatore a una struttura del [**\_ contesto del firmatario**](signer-context.md) che contiene un puntatore a un [*BLOB*](../secgloss/b-gly.md). Questa funzione può essere usata per eseguire l'infrastruttura a chiave pubblica X. 509, conforme a RFC 3161, timestamp.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.

 

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

*dwFlags* \[ in\]
</dt> <dd>

Valore che specifica il tipo di timestamp da generare. Questo parametro può avere uno dei valori seguenti. I valori si escludono a vicenda.



| Valore                                                                                                                                                                                                          | Significato                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt>**TIMESTAMP del FIRMATARIo \_ \_ AUTHENTICODE**</dt> </dl> | Specifica un timestamp Authenticode.<br/>       |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt>**TIMESTAMP del FIRMATARIo \_ \_ RFC3161**</dt> </dl>                | Specifica un timestamp conforme a RFC 3161.<br/> |



 

</dd> <dt>

*pSubjectInfo* \[ in\]
</dt> <dd>

Indirizzo di una struttura di [**\_ \_ informazioni sul soggetto del firmatario**](signer-subject-info.md) che rappresenta l'oggetto di cui è stato indicato il timestamp.

</dd> <dt>

*pwszHttpTimeStamp* \[ in\]
</dt> <dd>

Indirizzo di una stringa Unicode con terminazione null che contiene l'URL di un server di timestamp.

</dd> <dt>

*dwAlgId* \[ in\]
</dt> <dd>

Specifica un algoritmo hash da usare per l'esecuzione di timestamp conformi a RFC 3161. Questo parametro viene ignorato per gli indicatori di data e ora Authenticode.

</dd> <dt>

*psRequest* \[ in\]
</dt> <dd>

facoltativo. Indirizzo di una struttura [**degli \_ attributi Crypt**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) che contiene attributi aggiuntivi aggiunti alla richiesta del timestamp.

Questo parametro è facoltativo e può essere **null** se non è incluso.

</dd> <dt>

*pSipData* \[ in\]
</dt> <dd>

facoltativo. Valore a 32 bit passato come dati aggiuntivi alle funzioni SIP ( [*Subject Interface Package*](../secgloss/s-gly.md) ). Il formato e il contenuto di questo parametro sono definiti dal provider SIP.

Questo parametro è facoltativo e può essere **null** se non è incluso.

</dd> <dt>

*ppSignerContext* \[ out\]
</dt> <dd>

facoltativo. Indirizzo di un puntatore alla struttura del [**\_ contesto del firmatario**](signer-context.md) che contiene il BLOB firmato. Al termine dell'uso della struttura del **\_ contesto del firmatario** , liberarla chiamando la funzione [**SignerFreeSignerContext**](signerfreesignercontext.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce S \_ OK.

Se la funzione ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> <dt>

[**SignerTimeStampEx**](signertimestampex.md)
</dt> </dl>

 

 
