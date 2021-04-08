---
description: Timestamp dell'oggetto specificato. Questa funzione supporta l'indicatore di data e ora Authenticode. Per eseguire il timestamp dell'infrastruttura a chiave pubblica (RFC 3161) X. 509, usare la funzione SignerTimeStampEx2.
ms.assetid: fb2c149b-dba2-4879-be97-831037e1110b
title: SignerTimeStamp (funzione)
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
ms.openlocfilehash: c4c57f231f70477a76b4d4f6156354ebc847a715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968205"
---
# <a name="signertimestamp-function"></a>SignerTimeStamp (funzione)

Il timestamp della funzione **SignerTimeStamp** contrassegna l'oggetto specificato. Questa funzione supporta l'indicatore di data e ora Authenticode. Per eseguire il timestamp dell'infrastruttura a chiave pubblica (RFC 3161) X. 509, usare la funzione [**SignerTimeStampEx2**](signertimestampex2.md) .

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.

 

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

*pSubjectInfo* \[ in\]
</dt> <dd>

Indirizzo di una struttura di [**\_ \_ informazioni sul soggetto del firmatario**](signer-subject-info.md) che rappresenta l'oggetto di cui è stato indicato il timestamp.

</dd> <dt>

*pwszHttpTimeStamp* \[ in\]
</dt> <dd>

Indirizzo di una stringa Unicode con terminazione null che contiene l'URL di un server di timestamp.

</dd> <dt>

*psRequest* \[ in, facoltativo\]
</dt> <dd>

Indirizzo di una struttura [**degli \_ attributi Crypt**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) che contiene attributi aggiuntivi aggiunti alla richiesta del timestamp.

Questo parametro è facoltativo e può essere **null** se non è incluso.

</dd> <dt>

*pSipData* \[ in, facoltativo\]
</dt> <dd>

Valore a 32 bit passato come dati aggiuntivi alle funzioni SIP. Il formato e il contenuto di questo oggetto sono definiti dal provider SIP.

Questo parametro è facoltativo e può essere **null** se non è incluso.

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



 

 
