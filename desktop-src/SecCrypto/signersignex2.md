---
description: Firma e contrassegna il file specificato, consentendo più firme annidate.
ms.assetid: 216EFFCF-CD23-484A-ADBF-94B5AD52289F
title: Funzione SignerSignEx2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1498ca76adb755bf346f99788033acc53c9c09c34df623a0f65bc86b6d2e657e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973108"
---
# <a name="signersignex2-function"></a>Funzione SignerSignEx2

La **funzione SignerSignEx2 firma** e contrassegna il file specificato, consentendo più firme annidate.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per il collegamento dinamico a Mssign32.dll.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI SignerSignEx2(
  _In_       DWORD                  dwFlags,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       SIGNER_CERT            *pSignerCert,
  _In_       SIGNER_SIGNATURE_INFO  *pSignatureInfo,
  _In_opt_   SIGNER_PROVIDER_INFO   *pProviderInfo,
  _In_opt_   DWORD                  dwTimestampFlags,
  _In_opt_   PCSTR                  pszTimestampAlgorithmOid,
  _In_opt_   PCWSTR                 pwszHttpTimeStamp,
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

Modifica il comportamento di questa funzione.

Se il file da firmare è un file eseguibile portabile (PE), può essere zero o una combinazione di uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                    | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ FLAG HASH DI PAGINA PE EXC \_ \_ \_ \_ 0x10**</dt> <dt></dt> </dl>                    | Escludere gli hash di pagina durante la creazione di dati indiretti SIP per il file PE. Questo flag ha la precedenza sul flag **SPC \_ INC PE PAGE \_ \_ \_ HASHES \_ FLAG.**<br/> Se non viene specificato né **il flag SPC \_ EXC PE PAGE \_ \_ \_ HASHES \_ FLAG** né il flag **SPC INC PE PAGE \_ \_ \_ \_ HASHES \_ FLAG,** per questa impostazione viene usato il valore impostato con la funzione [**WintrustSetDefaultIncludePEPageHashes.**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) L'impostazione predefinita per questa impostazione è l'esclusione degli hash di pagina durante la creazione di dati indiretti SIP per i file PE.<br/> Questo valore è definito nel file di intestazione Mssip.h.<br/> **Windows Server 2003 e Windows XP:** Questo valore non è supportato.<br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <dt>**SPC \_ FLAG DI TABELLA DI INC \_ PE \_ IMPORT \_ \_ ADDR \_ 0x20**</dt> <dt></dt> </dl> | Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <dt>**SPC \_ INC \_ PE DEBUG INFO FLAG \_ \_ \_ 0x40**</dt> <dt></dt> </dl>                       | Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <dt>**SPC \_ INC \_ PE RESOURCES FLAG \_ \_ 0x80**</dt> <dt></dt> </dl>                           | Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ \_FLAG HASH PAGINA INC PE \_ \_ \_ 0x100**</dt> <dt></dt> </dl>                   | Includere gli hash di pagina durante la creazione di dati indiretti SIP per il file PE.<br/> **Windows Server 2003 e Windows XP:** Questo valore non è supportato.<br/> Questo valore è definito nel file di intestazione Mssip.h.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SIG_APPEND"></span><span id="sig_append"></span><dl> <dt>**SIG \_ Appendice**</dt> <dt>0x1000</dt> </dl>                                                                         | La firma verrà annidata. Se si imposta questo flag prima dell'aggiunta di qualsiasi firma, la firma generata verrà aggiunta come firma esterna. Se non si imposta questo flag, la firma generata sostituisce la firma esterna, eliminando tutte le firme interne.<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*pSubjectInfo* \[ Pollici\]
</dt> <dd>

Puntatore a [**una struttura SUBJECT INFO del \_ \_ FIRMATARIO**](signer-subject-info.md) che specifica l'oggetto da firmare.

</dd> <dt>

*pSignerCert* \[ Pollici\]
</dt> <dd>

Puntatore a [**una \_ struttura SIGNER CERT**](signer-cert.md) che specifica il certificato da utilizzare per creare la firma digitale.

</dd> <dt>

*pSignatureInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura \_ SIGNER SIGNATURE \_ INFO**](signer-signature-info.md) che contiene informazioni sulla firma digitale.

</dd> <dt>

*pProviderInfo* \[ in, facoltativo\]
</dt> <dd>

Puntatore a [**una struttura SIGNER \_ PROVIDER \_ INFO**](signer-provider-info.md) che specifica il [*provider*](../secgloss/c-gly.md) del servizio di crittografia (CSP) e le informazioni sulla chiave privata utilizzate per creare la firma digitale.

Se il valore di questo parametro è **NULL,** il *parametro pSignerCert* deve specificare un certificato associato a un CSP.

</dd> <dt>

*dwTimestampFlags* \[ in, facoltativo\]
</dt> <dd>

Flag che verranno passati a [**SignerTimeStampEx3**](signertimestampex3.md) se il *parametro pwszHttpTimeStamp* non è **NULL.** Può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                          | Significato                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt>**TIMESTAMP DEL \_ \_ FIRMATARIO AUTHENTICODE**</dt> </dl> | Valore predefinito. Specifica un timestamp Authenticode.<br/> |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt>**TIMESTAMP DEL \_ \_ FIRMATARIO RFC3161**</dt> </dl>                | Specifica un timestamp RFC 3161.<br/>                    |



 

Questo parametro viene ignorato se il *parametro pwszHttpTimeStamp* è **NULL.**

</dd> <dt>

*pszTimestampAlgorithmOid* \[ in, facoltativo\]
</dt> <dd>

Identificatore di oggetto dell'algoritmo da utilizzare per la creazione di un timestamp RFC 3161. Questo parametro viene ignorato per i timestamp Authenticode.

</dd> <dt>

*pwszHttpTimeStamp* \[ in, facoltativo\]
</dt> <dd>

URL del server timestamp.

</dd> <dt>

*psRequest* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una matrice [**di strutture \_ ATTRIBUTE CRYPT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) aggiunte a una richiesta di firma. Questo parametro viene ignorato se *il parametro pwszHttpTimeStamp* non contiene un valore valido o è **NULL.**

</dd> <dt>

*pSipData* \[ in, facoltativo\]
</dt> <dd>

Valore a 32 bit passato come dati aggiuntivi alle funzioni SIP. Il formato e il contenuto di questo oggetto sono definiti dal provider SIP.

</dd> <dt>

*ppSignerContext* \[ Cambio\]
</dt> <dd>

Indirizzo di un puntatore alla struttura [**SIGNER \_ CONTEXT**](signer-context.md) che contiene il BLOB [*firmato.*](../secgloss/b-gly.md) Dopo aver terminato di usare la **struttura SIGNER \_ CONTEXT,** liberare la struttura **SIGNER \_ CONTEXT** chiamando la [**funzione SignerFreeSignerContext.**](signerfreesignercontext.md)

</dd> <dt>

*pCryptoPolicy* \[ in, facoltativo\]
</dt> <dd>

Se presente, puntatore a una [**struttura CERT \_ STRONG SIGN \_ \_ PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) che contiene i parametri usati per verificare la presenza di firme forti. Se un certificato o la relativa catena non passa, il file non viene modificato in alcun modo. Se viene passato un URL per specificare un'autorità di timestamp (TSA), questo criterio viene applicato anche al timestamp.

</dd> <dt>

*Conservato* 
</dt> <dd>

Riservato. Questo valore deve essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce S \_ OK.

Se la funzione ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. I codici di errore possibili restituiti da questa funzione includono, ma non sono limitati, i seguenti. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni.](common-hresult-values.md)



| Codice restituito                                                                                  | Descrizione                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Se si imposta il *parametro dwTimestampFlags* su **SIGNER \_ TIMESTAMP \_ AUTHENTICODE**, non è possibile impostare il *parametro dwFlags* su **SIG \_ APPEND**.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Firma del firmatario**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> <dt>

[**SignerFreeSignerContext**](signerfreesignercontext.md)
</dt> </dl>

 

 
