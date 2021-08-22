---
description: Trova un certificato dell'autorità di certificazione dagli archivi certificati specificati che corrisponde al certificato del soggetto specificato.
ms.assetid: c724f602-fc73-4857-941f-0f22a9e472d1
title: Funzione WTHelperCertFindIssuerCertificate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperCertFindIssuerCertificate
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 3c6c7957e969d04eaf65014e023a5f64e0826b6285fb878d9afefbd7cda25721
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895833"
---
# <a name="wthelpercertfindissuercertificate-function"></a>Funzione WTHelperCertFindIssuerCertificate

\[La **funzione WTHelperCertFindIssuerCertificate** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

La **funzione WTHelperCertFindIssuerCertificate** trova un certificato dell'autorità di certificazione dagli archivi certificati specificati che corrisponde al certificato del soggetto specificato.

> [!Note]  
> A questa funzione non è associata alcuna libreria di importazione. È necessario usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi in modo dinamico Wintrust.dll.

 

## <a name="syntax"></a>Sintassi


```C++
PCCERT_CONTEXT WINAPI WTHelperCertFindIssuerCertificate(
  _In_      PCCERT_CONTEXT pChildContext,
  _In_      DWORD          chStores,
  _In_      HCERTSTORE     *pahStores,
  _In_      FILETIME       *psftVerifyAsOf,
  _In_      DWORD          dwEncoding,
  _Out_opt_ DWORD          *pdwConfidence,
  _Out_     DWORD          *dwError
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pChildContext* \[ Pollici\]
</dt> <dd>

Certificato del soggetto per il quale trovare un certificato dell'autorità di certificazione corrispondente.

</dd> <dt>

*chStores* \[ Pollici\]
</dt> <dd>

Numero di elementi nella *matrice pahStores.*

</dd> <dt>

*pahStores* \[ Pollici\]
</dt> <dd>

Matrice di archivi certificati in cui eseguire la ricerca.

</dd> <dt>

*psftVerifyAsOf* \[ Pollici\]
</dt> <dd>

Ora di verifica.

</dd> <dt>

*dwEncoding* \[ Pollici\]
</dt> <dd>

Valore **DWORD** che specifica i tipi di codifica del certificato da controllare. Per informazioni sui tipi di codifica possibili, vedere [Certificate and Message Encoding Types](certificate-and-message-encoding-types.md).

</dd> <dt>

*pdwConfidence* \[ out, facoltativo\]
</dt> <dd>

Questo parametro può essere una combinazione bit per bit di zero o più dei valori di attendibilità seguenti.



| Valore                                                                                                                                                                                                                                                                 | Significato                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="CERT_CONFIDENCE_SIG"></span><span id="cert_confidence_sig"></span><dl> <dt>**CERT \_ CONFIDENCE \_ SIG**</dt> <dt> 0x10000000</dt> </dl>                     | La firma del certificato è valida.<br/>                                           |
| <span id="CERT_CONFIDENCE_TIME"></span><span id="cert_confidence_time"></span><dl> <dt>**CERT \_ TEMPO \_ DI ATTENDIBILITÀ**</dt> <dt> 0x01000000</dt> </dl>                  | L'ora dell'autorità emittente del certificato è valida.<br/>                                         |
| <span id="_CERT_CONFIDENCE_TIMENEST"></span><span id="_cert_confidence_timenest"></span><dl> <dt> **CERT \_ CONFIDENCE \_ TIMENEST**</dt> <dt>0x00100000</dt> </dl>    | L'ora del certificato è valida.<br/>                                                |
| <span id="_CERT_CONFIDENCE_AUTHIDEXT"></span><span id="_cert_confidence_authidext"></span><dl> <dt> **CERT \_ CONFIDENCE \_ AUTHIDEXT**</dt> <dt>0x00010000</dt> </dl> | L'estensione dell'ID autorità è valida.<br/>                                                 |
| <span id="_CERT_CONFIDENCE_HYGIENE"></span><span id="_cert_confidence_hygiene"></span><dl> <dt> **PROTEZIONE \_ DELL'ATTENDIBILITÀ \_ DEI**</dt> <dt>CERTIFICATI 0x00001000</dt> </dl>       | Come minimo, la firma dell'estensione del certificato e dell'ID autorità è valida.<br/> |
| <span id="_CERT_CONFIDENCE_HIGHEST"></span><span id="_cert_confidence_highest"></span><dl> <dt> **CERT \_ CONFIDENCE \_ HIGHEST**</dt> <dt>0x11111000</dt> </dl>       | Combinazione di tutti gli altri valori di attendibilità.<br/>                                 |



 

</dd> <dt>

*dwError* \[ Cambio\]
</dt> <dd>

Puntatore a una **variabile DWORD** che contiene il valore di errore per questo certificato, se applicabile.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un certificato dell'autorità di certificazione che corrisponde al certificato del soggetto specificato dal *parametro pChildContext.*

## <a name="remarks"></a>Commenti

Per trovare correttamente un certificato dell'autorità di certificazione corrispondente, è necessario soddisfare i requisiti seguenti:

-   La firma del certificato del soggetto specificato dal *parametro pChildContext* deve essere valida.
-   Il **membro rgExtension** del membro **pCertInfo** del parametro *pChildContext* deve contenere una [**struttura CERT AUTHORITY KEY ID \_ \_ \_ \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) I **membri CertIssuer** e **CertSerialMember** di questa struttura corrispondono molto ai membri corrispondenti per il certificato dell'autorità di certificazione.
-   Il valore del *parametro psftVerifyAsOf* deve essere compreso nel periodo di validità del certificato del soggetto.
-   Il periodo di validità del certificato soggetto deve essere compreso nel periodo di validità del certificato dell'autorità emittente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



 

 
