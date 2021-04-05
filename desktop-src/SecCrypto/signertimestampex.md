---
description: Timestamp l'oggetto specificato e, facoltativamente, restituisce un puntatore a una struttura del contesto del FIRMATARIo \_ che contiene un puntatore a un BLOB.
ms.assetid: f3a910f6-64f8-4cf5-b008-2a16872f9a98
title: SignerTimeStampEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a4562ca84f8b3376a22d00a5e9501947152ed875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758771"
---
# <a name="signertimestampex-function"></a>SignerTimeStampEx (funzione)

Il timestamp della funzione **SignerTimeStampEx** indica l'oggetto specificato e, facoltativamente, restituisce un puntatore a una struttura del [**\_ contesto del firmatario**](signer-context.md) che contiene un puntatore a un [*BLOB*](../secgloss/b-gly.md). Questa funzione supporta l'indicatore di data e ora Authenticode. Per eseguire il timestamp dell'infrastruttura a chiave pubblica (RFC 3161) X. 509, usare la funzione [**SignerTimeStampEx2**](signertimestampex2.md) .

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI SignerTimeStampEx(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Riservato. Questo parametro deve essere impostato su zero.

</dd> <dt>

*pSubjectInfo* \[ in\]
</dt> <dd>

Indirizzo di una struttura di [**\_ \_ informazioni sul soggetto del firmatario**](signer-subject-info.md) che rappresenta l'oggetto di cui è stato indicato il timestamp.

</dd> <dt>

*pwszHttpTimeStamp* \[ in\]
</dt> <dd>

Indirizzo di una stringa Unicode con terminazione null che contiene l'URL di un server di timestamp.

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
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>


</dt> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> </dl>

 

 
