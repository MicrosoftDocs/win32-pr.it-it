---
description: Recupera le informazioni dal certificato.
ms.assetid: 57f1c6f9-f06d-4ac7-9070-2a2e6afe93d2
title: 'Metodo ICertificate2:: GetInfo'
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
ms.openlocfilehash: 41b3cb6cde796f64ee3a5953ed848d105a10bc5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325606"
---
# <a name="icertificate2getinfo-method"></a>Metodo ICertificate2:: GetInfo

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo **GetInfo** recupera le informazioni dal [*certificato*](../secgloss/c-gly.md).

## <a name="syntax"></a>Sintassi


```VB
Certificate.GetInfo( _
  ByVal InfoType _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*InfoType* \[ in\]
</dt> <dd>

Valore dell'enumerazione del [**\_ \_ \_ tipo di informazioni del certificato capicol**](capicom-cert-info-type.md) che specifica il tipo di dati che viene recuperato dal certificato. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                                     | Significato                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERT_INFO_SUBJECT_SIMPLE_NAME"></span><span id="capicom_cert_info_subject_simple_name"></span><dl> <dt>**\_ \_ \_ \_ nome semplice soggetto informazioni sul certificato capicot \_**</dt> </dl> | Restituisce il nome visualizzato dal soggetto del certificato.<br/>                            |
| <span id="CAPICOM_CERT_INFO_ISSUER_SIMPLE_NAME"></span><span id="capicom_cert_info_issuer_simple_name"></span><dl> <dt>**\_ \_ \_ nome semplice dell'emittente informazioni \_ sul certificato capicot \_**</dt> </dl>    | Restituisce il nome visualizzato dell'emittente del certificato.<br/>                        |
| <span id="CAPICOM_CERT_INFO_SUBJECT_EMAIL_NAME"></span><span id="capicom_cert_info_subject_email_name"></span><dl> <dt>**\_ \_ \_ nome di \_ posta elettronica dell'oggetto \_ del certificato di capicol**</dt> </dl>    | Restituisce l'indirizzo di posta elettronica del soggetto del certificato.<br/>                             |
| <span id="CAPICOM_CERT_INFO_ISSUER_EMAIL_NAME"></span><span id="capicom_cert_info_issuer_email_name"></span><dl> <dt>**\_ \_ \_ nome di \_ posta elettronica dell'autorità emittente informazioni sul certificato CAPICOM \_**</dt> </dl>       | Restituisce l'indirizzo di posta elettronica dell'emittente del certificato.<br/>                       |
| <span id="CAPICOM_CERT_INFO_SUBJECT_UPN"></span><span id="capicom_cert_info_subject_upn"></span><dl> <dt>**nome \_ \_ \_ UPN oggetto informazioni del certificato \_ CAPICOM**</dt> </dl>                          | Restituisce l'UPN dell'oggetto del certificato. Introdotta in capicol 2,0.<br/>            |
| <span id="CAPICOM_CERT_INFO_ISSUER_UPN"></span><span id="capicom_cert_info_issuer_upn"></span><dl> <dt>**nome UPN dell' \_ \_ \_ autorità emittente informazioni sul certificato capicot \_**</dt> </dl>                             | Restituisce l'UPN dell'emittente del certificato. Introdotta in capicol 2,0.<br/>      |
| <span id="CAPICOM_CERT_INFO_SUBJECT_DNS_NAME"></span><span id="capicom_cert_info_subject_dns_name"></span><dl> <dt>**\_ \_ \_ nome DNS dell'oggetto informazioni \_ sul certificato capicol \_**</dt> </dl>          | Restituisce il nome DNS del soggetto del certificato. Introdotta in capicol 2,0.<br/>       |
| <span id="CAPICOM_CERT_INFO_ISSUER_DNS_NAME"></span><span id="capicom_cert_info_issuer_dns_name"></span><dl> <dt>**\_ \_ \_ nome DNS dell'autorità emittente informazioni sul \_ certificato \_ CAPICOM**</dt> </dl>             | Restituisce il nome DNS dell'emittente del certificato. Introdotta in capicol 2,0.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Stringa che contiene le informazioni richieste.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti Cryptography](cryptography-objects.md)
</dt> <dt>

[**Certificato**](certificate.md)
</dt> </dl>

 

 
