---
description: Timestamp l'oggetto specificato e supporta l'impostazione di timestamp su più firme.
ms.assetid: A290ED4F-8803-4EAA-8CE1-68879F7F754A
title: SignerTimeStampEx3 (funzione)
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
ms.openlocfilehash: 538b92160ddbbb9ca9515a65575fdea67990de5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128090"
---
# <a name="signertimestampex3-function"></a>SignerTimeStampEx3 (funzione)

Il timestamp della funzione **SignerTimeStampEx3** timbra l'oggetto specificato e supporta l'impostazione dei timestamp su più firme.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.

 

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

*dwFlags* \[ in\]
</dt> <dd>

Flag che specifica il tipo di timestamp da generare. Questo parametro può avere uno dei valori seguenti. I valori si escludono a vicenda.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt> </dl></td>
<td>Specifica un timestamp Authenticode.<br/>
<blockquote>
[!Note]<br />
Authenticode non è più il tipo di timestamp preferito. Il supporto per i timestamp Authenticode potrebbe essere rimosso in futuro. Si consiglia di usare invece RFC 3161.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt> </dl></td>
<td>Specifica un timestamp conforme a RFC 3161.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*dwIndex* \[ in\]
</dt> <dd>

Specifica il numero di sequenza della firma a cui verrà aggiunto il timestamp. Se questo valore è zero (0), la firma esterna verrà contrassegnata con il timestamp.

</dd> <dt>

*pSubjectInfo* \[ in\]
</dt> <dd>

Indirizzo di una struttura di [**\_ \_ informazioni sul soggetto del firmatario**](signer-subject-info.md) che rappresenta l'oggetto di cui è stato indicato il timestamp.

</dd> <dt>

*pwszHttpTimeStamp* \[ in\]
</dt> <dd>

Indirizzo di una stringa Unicode con terminazione null che contiene l'URL di un server di timestamp.

</dd> <dt>

*pszAlgorithmOid* \[ in\]
</dt> <dd>

Algoritmo hash da utilizzare per l'esecuzione di indicatori di tempo conformi a RFC 3161. Questo parametro viene ignorato per gli indicatori di data e ora Authenticode.

</dd> <dt>

*psRequest* \[ in, facoltativo\]
</dt> <dd>

facoltativo. Indirizzo di una struttura [**degli \_ attributi Crypt**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) che contiene attributi aggiuntivi aggiunti alla richiesta del timestamp.

Questo parametro è facoltativo e può essere **null** se non è incluso.

</dd> <dt>

*pSipData* \[ in, facoltativo\]
</dt> <dd>

facoltativo. Valore a 32 bit passato come dati aggiuntivi alle funzioni SIP ( [*Subject Interface Package*](../secgloss/s-gly.md) ). Il formato e il contenuto di questo parametro sono definiti dal provider SIP.

Questo parametro è facoltativo e può essere **null** se non è incluso.

</dd> <dt>

*ppSignerContext* \[ out\]
</dt> <dd>

facoltativo. Indirizzo di un puntatore alla struttura del [**\_ contesto del firmatario**](signer-context.md) che contiene il BLOB firmato. Al termine dell'uso della struttura del **\_ contesto del firmatario** , liberarla chiamando la funzione [**SignerFreeSignerContext**](signerfreesignercontext.md) .

</dd> <dt>

*pCryptoPolicy* \[ in, facoltativo\]
</dt> <dd>

Se presente, puntatore a una struttura [**del \_ \_ segno \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) di firma forte del certificato che contiene i parametri utilizzati per verificare le firme sicure. Il timestamp deve superare questo criterio di crittografia.

</dd> <dt>

*Mantenuto* 
</dt> <dd>

Riservato. Questo valore deve essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce S \_ OK.

Se la funzione ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. I codici di errore possibili restituiti da questa funzione includono, ma non sono limitati a, quanto segue. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Codice restituito</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>E_INVALIDARG</strong></dt> </dl></td>
<td>Questo errore può essere restituito per le condizioni seguenti:<br/>
<ul>
<li>Per il parametro <em>dwFlags</em> è necessario impostare <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> o <strong>SIGNER_TIMESTAMP_RFC3161</strong> .</li>
<li>Il parametro <em>mantenuto</em> deve essere <strong>null</strong>.</li>
<li>Se si imposta il flag di <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> nel parametro <em>dwFlags</em> , è necessario impostare il parametro <em>dwIndex</em> su zero.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> <dt>

[**SignerTimeStampEx**](signertimestampex.md)
</dt> <dt>

[**SignerTimeStampEx2**](signertimestampex2.md)
</dt> </dl>

 

 
