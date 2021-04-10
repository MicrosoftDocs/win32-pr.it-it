---
description: Trova un certificato dell'autorità emittente dagli archivi certificati specificati che corrisponde al certificato dell'oggetto specificato.
ms.assetid: c724f602-fc73-4857-941f-0f22a9e472d1
title: WTHelperCertFindIssuerCertificate (funzione)
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
ms.openlocfilehash: 99135ac22509b288726732ca4a16248b304f294b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231701"
---
# <a name="wthelpercertfindissuercertificate-function"></a>WTHelperCertFindIssuerCertificate (funzione)

\[La funzione **WTHelperCertFindIssuerCertificate** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

La funzione **WTHelperCertFindIssuerCertificate** trova un certificato dell'autorità emittente dagli archivi certificati specificati che corrisponde al certificato dell'oggetto specificato.

> [!Note]  
> A questa funzione non è associata alcuna libreria di importazione. È necessario utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Wintrust.dll.

 

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

*pChildContext* \[ in\]
</dt> <dd>

Certificato dell'oggetto per il quale trovare un certificato dell'autorità emittente corrispondente.

</dd> <dt>

*chStores* \[ in\]
</dt> <dd>

Numero di elementi nella matrice *pahStores* .

</dd> <dt>

*pahStores* \[ in\]
</dt> <dd>

Matrice di archivi certificati in cui eseguire la ricerca.

</dd> <dt>

*psftVerifyAsOf* \[ in\]
</dt> <dd>

Ora della verifica.

</dd> <dt>

*dwEncoding* \[ in\]
</dt> <dd>

Valore **DWORD** che specifica i tipi di codifica del certificato da verificare. Per informazioni sui possibili tipi di codifica, vedere [tipi di codifica di certificati e messaggi](certificate-and-message-encoding-types.md).

</dd> <dt>

*pdwConfidence* \[ out, facoltativo\]
</dt> <dd>

Questo parametro può essere una combinazione bit per bit di zero o più dei valori di confidenza seguenti.



| Valore                                                                                                                                                                                                                                                                 | Significato                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="CERT_CONFIDENCE_SIG"></span><span id="cert_confidence_sig"></span><dl> <dt>**Certificato \_ \_Firma di sicurezza**</dt> <dt> 0x10000000</dt> </dl>                     | La firma del certificato è valida.<br/>                                           |
| <span id="CERT_CONFIDENCE_TIME"></span><span id="cert_confidence_time"></span><dl> <dt>**Certificato \_ \_Tempo di confidenza**</dt> <dt> 0x01000000</dt> </dl>                  | Il tempo dell'emittente del certificato è valido.<br/>                                         |
| <span id="_CERT_CONFIDENCE_TIMENEST"></span><span id="_cert_confidence_timenest"></span><dl> <dt>0x00100000</dt> di <dt> **sicurezza del certificato \_ \_ TIMENEST**</dt> </dl>    | L'ora del certificato è valida.<br/>                                                |
| <span id="_CERT_CONFIDENCE_AUTHIDEXT"></span><span id="_cert_confidence_authidext"></span><dl> <dt>0x00010000</dt> di <dt> **sicurezza del certificato \_ \_ AUTHIDEXT**</dt> </dl> | Estensione ID autorità valida.<br/>                                                 |
| <span id="_CERT_CONFIDENCE_HYGIENE"></span><span id="_cert_confidence_hygiene"></span><dl> <dt>0x00001000</dt> <dt> **\_ \_ igiene certificati attendibilità**</dt> </dl>       | Come minimo, la firma del certificato e l'estensione ID autorità sono validi.<br/> |
| <span id="_CERT_CONFIDENCE_HIGHEST"></span><span id="_cert_confidence_highest"></span><dl> <dt>0x11111000</dt> di <dt> **sicurezza del certificato \_ \_ più alto**</dt> </dl>       | Combinazione di tutti gli altri valori di attendibilità.<br/>                                 |



 

</dd> <dt>

*dwError* \[ out\]
</dt> <dd>

Puntatore a una variabile **DWORD** che contiene il valore di errore per il certificato, se applicabile.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un certificato dell'autorità emittente che corrisponde al certificato dell'oggetto specificato dal parametro *pChildContext* .

## <a name="remarks"></a>Commenti

Per trovare correttamente un certificato dell'autorità emittente corrispondente, è necessario soddisfare i requisiti seguenti:

-   La firma del certificato dell'oggetto specificato dal parametro *pChildContext* deve essere valida.
-   Il membro **rgExtension** del membro **PCertInfo** del parametro *pChildContext* deve contenere una struttura [**\_ \_ \_ \_ info ID chiave dell'autorità di certificazione**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) . I membri di **CertIssuer** e **CertSerialMember** di questa struttura corrispondono in gran parte ai membri corrispondenti per il certificato dell'autorità emittente.
-   Il valore del parametro *psftVerifyAsOf* deve essere compreso nel periodo di validità del certificato dell'oggetto.
-   Il periodo di validità del certificato del soggetto deve essere compreso nel periodo di validità del certificato dell'autorità emittente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



 

 
