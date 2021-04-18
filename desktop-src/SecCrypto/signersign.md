---
description: Firma il file specificato.
ms.assetid: 5a59e663-057b-4380-aa14-536030e4051d
title: SignerSign (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSign
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9aa8ecc15e38c4a502b363898d5845cba5b0e47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314690"
---
# <a name="signersign-function"></a>SignerSign (funzione)

La funzione **SignerSign** firma il file specificato.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI SignerSign(
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

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

Puntatore a una struttura di [**\_ \_ informazioni del provider del firmatario**](signer-provider-info.md) che specifica le informazioni sul [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) e sulla [*chiave privata*](../secgloss/p-gly.md) utilizzate per creare la firma digitale.

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

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
