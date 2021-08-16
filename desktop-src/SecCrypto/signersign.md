---
description: Firma il file specificato.
ms.assetid: 5a59e663-057b-4380-aa14-536030e4051d
title: Funzione SignerSign
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
ms.openlocfilehash: d9756fba3a931ddf09715b5086e613a9395c10c57c82fa18c64007aeb02b615c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973135"
---
# <a name="signersign-function"></a>Funzione SignerSign

La **funzione SignerSign** firma il file specificato.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per il collegamento dinamico a Mssign32.dll.

 

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

Puntatore a una [**struttura \_ SIGNER SIGNATURE \_ INFO**](signer-signature-info.md) che contiene informazioni sulla firma digitale.

</dd> <dt>

*pProviderInfo* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura SIGNER \_ PROVIDER \_ INFO**](signer-provider-info.md) che specifica il [](../secgloss/p-gly.md) [*provider*](../secgloss/c-gly.md) del servizio di crittografia (CSP) e le informazioni sulla chiave privata utilizzate per creare la firma digitale.

Se il valore di questo parametro è **NULL,** il valore del *parametro pSignerCert* deve specificare un certificato associato a un CSP.

</dd> <dt>

*pwszHttpTimeStamp* \[ in, facoltativo\]
</dt> <dd>

URL di un server timestamp.

</dd> <dt>

*psRequest* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una matrice [**di strutture ATTRIBUTE CRYPT \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) aggiunte a una richiesta di firma. Questo parametro viene ignorato se *il parametro pwszHttpTimeStamp* non contiene un valore valido diverso da **NULL.**

</dd> <dt>

*pSipData* \[ in, facoltativo\]
</dt> <dd>

Valore a 32 bit passato come dati aggiuntivi alle funzioni SIP. Il formato e il contenuto di questo oggetto sono definiti dal provider SIP.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce S \_ OK.

Se la funzione ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni.](common-hresult-values.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
