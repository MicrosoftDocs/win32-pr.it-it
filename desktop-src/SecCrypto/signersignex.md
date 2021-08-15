---
description: Firma il file specificato e restituisce un puntatore ai dati firmati.
ms.assetid: 9921ffae-2299-4bf2-b76d-77f7f6afb663
title: Funzione SignerSignEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 0b880cc02053d5a90089cffc721b057c6fce9f34b8be6517c12ef59fef9e0ed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898324"
---
# <a name="signersignex-function"></a>Funzione SignerSignEx

La **funzione SignerSignEx** firma il file specificato e restituisce un puntatore ai dati firmati.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI SignerSignEx(
  _In_     DWORD                 dwFlags,
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData,
  _Out_    SIGNER_CONTEXT        **ppSignerContext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Modifica il comportamento di questa funzione.

Se il file da firmare è un file eseguibile portabile (PE), può essere zero o una combinazione di uno o più dei valori seguenti. Questi identificatori sono definiti in Mssip.h.



| Valore                                                                                                                                                                                                                                                                                    | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ FLAG HASH PAGINA PE EXC \_ \_ \_ \_ 0x10**</dt> <dt></dt> </dl>                    | Escludere gli hash di pagina durante la creazione di dati indiretti SIP per il file PE. Questo flag ha la precedenza sul flag **\_ SPC INC \_ PE PAGE \_ \_ HASHES \_ FLAG.**<br/> Se non viene specificato il **\_ flag SPC EXC \_ PE PAGE \_ \_ HASHES \_ FLAG** o **SPC INC PE PAGE \_ \_ \_ \_ HASHES \_ FLAG,** per questa impostazione viene usato il valore impostato con la funzione [**WintrustSetDefaultIncludePEPageHashes.**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) L'impostazione predefinita per questa impostazione è escludere gli hash di pagina durante la creazione di dati indiretti SIP per i file PE.<br/> **Windows Server 2003 e Windows XP:** Questo valore non è supportato.<br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <dt>**SPC \_ INC \_ PE \_ IMPORT \_ ADDR TABLE FLAG \_ \_ 0x20**</dt> <dt></dt> </dl> | Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <dt>**SPC \_ FLAG DI \_ INFORMAZIONI \_ \_ DI \_ DEBUG**</dt> DI INC PE <dt>0x40</dt> </dl>                       | Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <dt>**SPC \_ FLAG \_ DELLE \_ RISORSE \_ PE**</dt> <dt>0X80</dt> </dl>                           | Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ FLAG HASH PAGINA PE INC \_ \_ \_ \_ 0x100**</dt> <dt></dt> </dl>                   | Includere gli hash di pagina durante la creazione di dati indiretti SIP per il file PE.<br/> **Windows Server 2003 e Windows XP:** Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

*pSubjectInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura \_ SIGNER SUBJECT \_ INFO**](signer-subject-info.md) che specifica l'oggetto da firmare.

</dd> <dt>

*pSignerCert* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura \_ SIGNER CERT**](signer-cert.md) che specifica il certificato da utilizzare per creare la firma digitale.

</dd> <dt>

*pSignatureInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura SIGNER \_ SIGNATURE \_ INFO**](signer-signature-info.md) che contiene informazioni sulla firma digitale.

</dd> <dt>

*pProviderInfo* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura SIGNER \_ PROVIDER \_ INFO**](signer-provider-info.md) che specifica il [*provider*](../secgloss/c-gly.md) del servizio di crittografia (CSP) e le informazioni sulla chiave privata usate per creare la firma digitale.

Se il valore di questo parametro è **NULL,** il valore del *parametro pSignerCert* deve specificare un certificato associato a un CSP.

</dd> <dt>

*pwszHttpTimeStamp* \[ in, facoltativo\]
</dt> <dd>

URL di un server di timestamp.

</dd> <dt>

*psRequest* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una matrice di [**strutture CRYPT \_ ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) aggiunte a una richiesta di firma. Questo parametro viene ignorato se il *parametro pwszHttpTimeStamp* non contiene un valore valido diverso da **NULL.**

</dd> <dt>

*pSipData* \[ in, facoltativo\]
</dt> <dd>

Valore a 32 bit passato come dati aggiuntivi alle funzioni SIP. Il formato e il contenuto di questo oggetto sono definiti dal provider SIP.

</dd> <dt>

*ppSignerContext* \[ Cambio\]
</dt> <dd>

Indirizzo di un puntatore alla struttura [**SIGNER \_ CONTEXT**](signer-context.md) che contiene il [*BLOB firmato.*](../secgloss/b-gly.md) Al termine dell'uso della **struttura SIGNER \_ CONTEXT,** liberare la struttura **SIGNER \_ CONTEXT** chiamando la [**funzione SignerFreeSignerContext.**](signerfreesignercontext.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce S \_ OK.

Se la funzione ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni](common-hresult-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerFreeSignerContext**](signerfreesignercontext.md)
</dt> </dl>

 

 
