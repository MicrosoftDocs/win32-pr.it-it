---
description: Recupera informazioni dal certificato.
ms.assetid: 57f1c6f9-f06d-4ac7-9070-2a2e6afe93d2
title: Metodo ICertificate2::GetInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.GetInfo
- ICertificate2.GetInfo
- ICertificate.GetInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 401aa077e5f736449e0638fd5cf368224485ec8393b8bddaed1f62296ad90297
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127021"
---
# <a name="icertificate2getinfo-method"></a>Metodo ICertificate2::GetInfo

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei [**nomi System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Il **metodo GetInfo** recupera informazioni dal [*certificato*](../secgloss/c-gly.md).

## <a name="syntax"></a>Sintassi


```VB
Certificate.GetInfo( _
  ByVal InfoType _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*InfoType* \[ Pollici\]
</dt> <dd>

Valore [**dell'enumerazione CAPICOM \_ CERT \_ INFO \_ TYPE**](capicom-cert-info-type.md) che specifica il tipo di dati recuperato dal certificato. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                                     | Significato                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERT_INFO_SUBJECT_SIMPLE_NAME"></span><span id="capicom_cert_info_subject_simple_name"></span><dl> <dt>**CAPICOM \_ CERT \_ INFO \_ SUBJECT \_ SIMPLE \_ NAME**</dt> </dl> | Restituisce il nome visualizzato dal soggetto del certificato.<br/>                            |
| <span id="CAPICOM_CERT_INFO_ISSUER_SIMPLE_NAME"></span><span id="capicom_cert_info_issuer_simple_name"></span><dl> <dt>**CAPICOM \_ CERT \_ INFO \_ ISSUER \_ SIMPLE \_ NAME**</dt> </dl>    | Restituisce il nome visualizzato dell'autorità emittente del certificato.<br/>                        |
| <span id="CAPICOM_CERT_INFO_SUBJECT_EMAIL_NAME"></span><span id="capicom_cert_info_subject_email_name"></span><dl> <dt>**CAPICOM \_ CERT \_ INFO \_ SUBJECT \_ EMAIL \_ NAME**</dt> </dl>    | Restituisce l'indirizzo di posta elettronica del soggetto del certificato.<br/>                             |
| <span id="CAPICOM_CERT_INFO_ISSUER_EMAIL_NAME"></span><span id="capicom_cert_info_issuer_email_name"></span><dl> <dt>**CAPICOM \_ CERT \_ INFO \_ ISSUER \_ EMAIL \_ NAME**</dt> </dl>       | Restituisce l'indirizzo di posta elettronica dell'autorità emittente del certificato.<br/>                       |
| <span id="CAPICOM_CERT_INFO_SUBJECT_UPN"></span><span id="capicom_cert_info_subject_upn"></span><dl> <dt>**CAPICOM \_ CERT \_ INFO \_ SUBJECT \_ UPN**</dt> </dl>                          | Restituisce l'UPN del soggetto del certificato. Introdotto in CAPICOM 2.0.<br/>            |
| <span id="CAPICOM_CERT_INFO_ISSUER_UPN"></span><span id="capicom_cert_info_issuer_upn"></span><dl> <dt>**CAPICOM \_ CERT \_ INFO \_ ISSUER \_ UPN**</dt> </dl>                             | Restituisce l'UPN dell'autorità emittente del certificato. Introdotto in CAPICOM 2.0.<br/>      |
| <span id="CAPICOM_CERT_INFO_SUBJECT_DNS_NAME"></span><span id="capicom_cert_info_subject_dns_name"></span><dl> <dt>**CAPICOM \_ CERT \_ INFO \_ SUBJECT \_ DNS \_ NAME**</dt> </dl>          | Restituisce il nome DNS del soggetto del certificato. Introdotto in CAPICOM 2.0.<br/>       |
| <span id="CAPICOM_CERT_INFO_ISSUER_DNS_NAME"></span><span id="capicom_cert_info_issuer_dns_name"></span><dl> <dt>**CAPICOM \_ CERT \_ INFO \_ ISSUER \_ DNS \_ NAME**</dt> </dl>             | Restituisce il nome DNS dell'autorità emittente del certificato. Introdotto in CAPICOM 2.0.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Stringa che contiene le informazioni richieste.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti di crittografia](cryptography-objects.md)
</dt> <dt>

[**Certificato**](certificate.md)
</dt> </dl>

 

 
