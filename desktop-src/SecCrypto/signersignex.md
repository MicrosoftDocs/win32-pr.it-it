---
description: Firma il file specificato e restituisce un puntatore ai dati firmati.
ms.assetid: 9921ffae-2299-4bf2-b76d-77f7f6afb663
title: SignerSignEx (funzione)
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
ms.openlocfilehash: 9944a09459219ccac74f5fafc9424e9f85a01112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755562"
---
# <a name="signersignex-function"></a>SignerSignEx (funzione)

La funzione **SignerSignEx** firma il file specificato e restituisce un puntatore ai dati firmati.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.

 

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

*dwFlags* \[ in\]
</dt> <dd>

Modifica il comportamento di questa funzione.

Se il file da firmare è un file eseguibile portabile (PE), può essere zero o una combinazione di uno o più dei valori seguenti. Questi identificatori sono definiti in Mssip. h.



| Valore                                                                                                                                                                                                                                                                                    | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ \_Flag di \_ \_ hash \_ della pagina PE EXC**</dt> <dt>0x10</dt> </dl>                    | Escludere gli hash di pagina durante la creazione di dati SIP indiretti per il file PE. Questo flag ha la precedenza sul flag del **flag di hash della \_ pagina del \_ PE \_ \_ \_ SPC Inc** .<br/> Se non viene specificato né il flag di **hash della \_ \_ pagina del PE \_ \_ \_ di SPC** , né il flag del **\_ \_ \_ \_ \_ flag di hash della pagina del PE SPC Inc** , viene usato il valore impostato con la funzione [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) per questa impostazione. Il valore predefinito per questa impostazione consiste nell'escludere gli hash di pagina durante la creazione di dati SIP indiretti per i file PE.<br/> **Windows Server 2003 e Windows XP:** Questo valore non è supportato.<br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <dt>**SPC \_ 0x20 \_ del \_ \_ flag di \_ tabella \_ IND Import PE**</dt> <dt></dt> </dl> | Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <dt>**SPC \_ 0x40 \_ di \_ \_ \_ informazioni di debug PE Inc**</dt> . <dt></dt> </dl>                       | Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <dt>**SPC \_ 0x80 \_ \_ \_ flag risorse PE incl**</dt> <dt></dt> </dl>                           | Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ 0x100 \_ del \_ \_ \_ flag di hash delle pagine PE Inc**</dt> <dt></dt> </dl>                   | Includere gli hash di pagina quando si creano dati SIP indiretti per il file PE.<br/> **Windows Server 2003 e Windows XP:** Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

*pSubjectInfo* \[ in\]
</dt> <dd>

Puntatore a una struttura di [**\_ \_ informazioni sul soggetto del firmatario**](signer-subject-info.md) che specifica l'oggetto da firmare.

</dd> <dt>

*pSignerCert* \[ in\]
</dt> <dd>

Puntatore a una struttura del certificato del [**firmatario \_**](signer-cert.md) che specifica il certificato da usare per creare la firma digitale.

</dd> <dt>

*pSignatureInfo* \[ in\]
</dt> <dd>

Puntatore a una struttura di [**\_ \_ informazioni sulla firma del firmatario**](signer-signature-info.md) che contiene informazioni sulla firma digitale.

</dd> <dt>

*pProviderInfo* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una struttura di [**\_ \_ informazioni del provider del firmatario**](signer-provider-info.md) che specifica le informazioni sul [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) e sulla chiave privata utilizzate per creare la firma digitale.

Se il valore di questo parametro è **null**, il valore del parametro *pSignerCert* deve specificare un certificato associato a un CSP.

</dd> <dt>

*pwszHttpTimeStamp* \[ in, facoltativo\]
</dt> <dd>

URL di un server di timestamp.

</dd> <dt>

*psRequest* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una matrice di strutture [**degli \_ attributi Crypt**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) che vengono aggiunte a una richiesta di firma. Questo parametro viene ignorato se il parametro *pwszHttpTimeStamp* non contiene un valore valido che non è **null**.

</dd> <dt>

*pSipData* \[ in, facoltativo\]
</dt> <dd>

Valore a 32 bit passato come dati aggiuntivi alle funzioni SIP. Il formato e il contenuto di questo oggetto sono definiti dal provider SIP.

</dd> <dt>

*ppSignerContext* \[ out\]
</dt> <dd>

Indirizzo di un puntatore alla struttura del [**\_ contesto del firmatario**](signer-context.md) che contiene il [*BLOB*](../secgloss/b-gly.md)firmato. Al termine dell'uso della struttura del **\_ contesto del firmatario** , liberare la struttura del **\_ contesto del firmatario** chiamando la funzione [**SignerFreeSignerContext**](signerfreesignercontext.md) .

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

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerFreeSignerContext**](signerfreesignercontext.md)
</dt> </dl>

 

 
