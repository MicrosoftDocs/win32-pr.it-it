---
description: Contrassegna l'oggetto specificato e supporta l'impostazione di timestamp su più firme.
ms.assetid: A290ED4F-8803-4EAA-8CE1-68879F7F754A
title: Funzione SignerTimeStampEx3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx3
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 7eb5c19292b451b1a3d0265da4bb178eafcc6f00
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468558"
---
# <a name="signertimestampex3-function"></a>Funzione SignerTimeStampEx3

La **funzione SignerTimeStampEx3** contrassegna l'oggetto specificato e supporta l'impostazione di timestamp su più firme.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI SignerTimeStampEx3(
  _In_       DWORD                  dwFlags,
  _In_       DWORD                  dwIndex,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       PCWSTR                 pwszHttpTimeStamp,
  _In_       PCWSTR                 pszAlgorithmOid,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Flag che specifica il tipo di timestamp da generare. Questo parametro può avere uno dei valori seguenti. I valori si escludono a vicenda.




| valore | Significato | 
|-------|---------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl><dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt></dl> | Specifica un timestamp Authenticode.<br /><blockquote>[!Note]<br />Authenticode non è più il tipo preferito di timestamp. Il supporto per i timestamp Authenticode potrebbe essere rimosso in futuro. È consigliabile usare invece RFC 3161.</blockquote><br /> | 
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl><dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt></dl> | Specifica un timestamp conforme a RFC 3161.<br /> | 




 

</dd> <dt>

*dwIndex* \[ Pollici\]
</dt> <dd>

Specifica il numero di sequenza della firma a cui verrà aggiunto il timestamp. Se questo valore è zero (0), la firma esterna verrà contrassegnata con timestamp.

</dd> <dt>

*pSubjectInfo* \[ Pollici\]
</dt> <dd>

Indirizzo di una struttura [**SIGNER \_ SUBJECT \_ INFO**](signer-subject-info.md) che rappresenta l'oggetto da impostare come timestamp.

</dd> <dt>

*pwszHttpTimeStamp* \[ Pollici\]
</dt> <dd>

Indirizzo di una stringa Unicode con terminazione Null che contiene l'URL di un server timestamp.

</dd> <dt>

*pszAlgorithmOid* \[ Pollici\]
</dt> <dd>

Algoritmo hash da usare per l'esecuzione di timestamp conformi a RFC 3161. Questo parametro viene ignorato per i timestamp Authenticode.

</dd> <dt>

*psRequest* \[ in, facoltativo\]
</dt> <dd>

facoltativo. Indirizzo di una [**struttura CRYPT \_ ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) che contiene attributi aggiuntivi che vengono aggiunti alla richiesta di timestamp.

Questo parametro è facoltativo e può essere **NULL** se non è incluso.

</dd> <dt>

*pSipData* \[ in, facoltativo\]
</dt> <dd>

facoltativo. Valore a 32 bit passato come dati aggiuntivi alle funzioni [*DELS (Subject Interface Package).*](../secgloss/s-gly.md) Il formato e il contenuto di questo parametro sono definiti dal provider SIP.

Questo parametro è facoltativo e può essere **NULL** se non è incluso.

</dd> <dt>

*ppSignerContext* \[ Cambio\]
</dt> <dd>

facoltativo. Indirizzo di un puntatore alla struttura [**SIGNER \_ CONTEXT**](signer-context.md) che contiene il BLOB firmato. Al termine dell'uso della **struttura SIGNER \_ CONTEXT,** liberarla chiamando la [**funzione SignerFreeSignerContext.**](signerfreesignercontext.md)

</dd> <dt>

*pCryptoPolicy* \[ in, facoltativo\]
</dt> <dd>

Se presente, puntatore a una [**struttura CERT \_ STRONG SIGN \_ \_ PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) che contiene i parametri usati per verificare la presenza di firme forti. Il timestamp deve superare questo criterio crittografico.

</dd> <dt>

*Conservato* 
</dt> <dd>

Riservato. Questo valore deve essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce S \_ OK.

Se la funzione ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. I possibili codici di errore restituiti da questa funzione includono, ma non sono limitati, i seguenti. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni](common-hresult-values.md).




| Codice restituito | Descrizione | 
|-------------|-------------|
| <dl><dt><strong>E_INVALIDARG</strong></dt></dl> | Questo errore può essere restituito per le condizioni seguenti:<br /><ul><li>È necessario impostare <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> o <strong>SIGNER_TIMESTAMP_RFC3161</strong> per il <em>parametro dwFlags.</em></li><li>Il <em>parametro pReserved</em> deve essere <strong>NULL.</strong></li><li>Se si imposta il <strong>flag SIGNER_TIMESTAMP_AUTHENTICODE</strong> nel <em>parametro dwFlags,</em> è necessario impostare il <em>parametro dwIndex</em> su zero.</li></ul> | 




 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> <dt>

[**SignerTimeStampEx**](signertimestampex.md)
</dt> <dt>

[**SignerTimeStampEx2**](signertimestampex2.md)
</dt> </dl>

 

 
