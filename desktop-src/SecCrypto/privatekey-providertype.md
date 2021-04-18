---
description: Recupera un valore dell'enumerazione del tipo capicol \_ dimostrata \_ che specifica il tipo di provider.
ms.assetid: bc6a579f-5532-45e3-97f4-adcde2cd29e5
title: Proprietà PrivateKey. ProviderType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.ProviderType
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b38cc9a030bc27a30a66624f1faeca080104e7fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324893"
---
# <a name="privatekeyprovidertype-property"></a>Proprietà PrivateKey. ProviderType

\[La proprietà **ProviderType** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**Proprietà X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **ProviderType** recupera un valore dell'enumerazione del [**tipo capicot \_ \_ dimostrata**](capicom-prov-type.md) che specifica il tipo di provider.

## <a name="syntax"></a>Sintassi


```VB
PrivateKey.ProviderType As CAPICOM_PROV_TYPE
```



## <a name="property-value"></a>Valore proprietà

Valore dell'enumerazione del [**\_ \_ tipo capicol**](capicom-prov-type.md) che indica il tipo di provider. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_RSA_FULL"></span><span id="capicom_prov_rsa_full"></span><dl> <dt>**capicol \_ prova \_ RSA \_ completo**</dt> </dl>                 | Il [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) completo di [*RSA*](../secgloss/r-gly.md) . Questo tipo di provider supporta le [*firme digitali*](../secgloss/d-gly.md) e la [*crittografia*](../secgloss/e-gly.md)dei dati.<br/> |
| <span id="CAPICOM_PROV_RSA_SIG"></span><span id="capicom_prov_rsa_sig"></span><dl> <dt>**capicol \_ prov \_ RSA \_ sig**</dt> </dl>                    | Subset del CSP RSA che supporta solo le funzioni e gli algoritmi richiesti per gli hash e le firme digitali.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <span id="CAPICOM_PROV_DSS"></span><span id="capicom_prov_dss"></span><dl> <dt>**capicol \_ prov \_ DSS**</dt> </dl>                                 | Il CSP di [*Digital Signature standard*](../secgloss/d-gly.md) (DSS). Questo tipo di provider supporta solo hash e firme digitali. DSS usa l' [*algoritmo di firma digitale*](../secgloss/d-gly.md) (DSA).<br/>                                                                                     |
| <span id="CAPICOM_PROV_FORTEZZA"></span><span id="capicom_prov_fortezza"></span><dl> <dt>**capicol \_ prova di \_ fortezza**</dt> </dl>                  | CSP che contiene i protocolli e gli algoritmi di crittografia di proprietà del [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST).<br/>                                                                                                                                                                          |
| <span id="CAPICOM_PROV_MS_EXCHANGE"></span><span id="capicom_prov_ms_exchange"></span><dl> <dt>**CAPICOM \_ provare \_ MS \_ Exchange**</dt> </dl>        | CSP progettato per le esigenze crittografiche dell'applicazione Microsoft Exchange mail e di altre applicazioni compatibili con Microsoft Mail.<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_SSL"></span><span id="capicom_prov_ssl"></span><dl> <dt>**capicol \_ prova \_ SSL**</dt> </dl>                                 | CSP che supporta il protocollo [*Secure Sockets Layer*](../secgloss/s-gly.md) (SSL).<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROV_RSA_SCHANNEL"></span><span id="capicom_prov_rsa_schannel"></span><dl> <dt>**CAPICOM \_ prova \_ RSA \_ Schannel**</dt> </dl>     | CSP che supporta sia i protocolli RSA che i protocolli [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_PROV_DSS_DH"></span><span id="capicom_prov_dss_dh"></span><dl> <dt>**CAPICOM \_ prova \_ DSS \_ DH**</dt> </dl>                       | CSP che supporta i protocolli DSS ( [*Digital Signature Standard*](../secgloss/d-gly.md) ) e [*Diffie-Hellman*](../secgloss/d-gly.md) .<br/>                                                                                                                                                           |
| <span id="CAPICOM_PROV_EC_ECDSA_SIG"></span><span id="capicom_prov_ec_ecdsa_sig"></span><dl> <dt>**capicol \_ prova \_ EC \_ ECDSA \_ sig**</dt> </dl>    | CSP che supporta le funzioni e gli algoritmi ECDSA (ellittica Digital Signature Algorithm) necessari per le firme digitali.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_EC_ECNRA_SIG"></span><span id="capicom_prov_ec_ecnra_sig"></span><dl> <dt>**capicol \_ prova \_ EC \_ ECNRA \_ sig**</dt> </dl>    | CSP che supporta la curva ellittica Nyberg-Rueppel le funzioni analogiche (ECNRA) e gli algoritmi richiesti per le firme digitali.<br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROV_EC_ECDSA_FULL"></span><span id="capicom_prov_ec_ecdsa_full"></span><dl> <dt>**capicol \_ prove \_ EC \_ ECDSA \_ completo**</dt> </dl> | CSP che supporta il ECDSA completo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_EC_ECNRA_FULL"></span><span id="capicom_prov_ec_ecnra_full"></span><dl> <dt>**capicol \_ prove \_ EC \_ ECNRA \_ completo**</dt> </dl> | CSP che supporta il ECNRA completo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_DH_SCHANNEL"></span><span id="capicom_prov_dh_schannel"></span><dl> <dt>**CAPICOM \_ prova \_ DH \_ Schannel**</dt> </dl>        | CSP che supporta sia i protocolli [*Diffie-Hellman*](../secgloss/d-gly.md) che i protocolli [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_SPYRUS_LYNKS"></span><span id="capicom_prov_spyrus_lynks"></span><dl> <dt>**CAPICOM \_ prova \_ Spyrus Deployment \_ Lynks**</dt> </dl>     | CSP che supporta il dispositivo Spyrus Deployment LYNKS card.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CAPICOM_PROV_RNG"></span><span id="capicom_prov_rng"></span><dl> <dt>**capicol \_ prov \_ RNG**</dt> </dl>                                 | CSP che gestisce la generazione di numeri casuali.<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_INTEL_SEC"></span><span id="capicom_prov_intel_sec"></span><dl> <dt>**CAPICOM \_ prova \_ Intel \_ sec**</dt> </dl>              | CSP che fornisce la sicurezza di Intel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_REPLACE_OWF"></span><span id="capicom_prov_replace_owf"></span><dl> <dt>**CAPICOM prova a \_ \_ sostituire \_ OWF**</dt> </dl>        | CSP che supporta la sostituzione del modo in cui vengono generati formati unidirezionali (OWFs) da password.<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROV_RSA_AES"></span><span id="capicom_prov_rsa_aes"></span><dl> <dt>**CAPICOM \_ prova \_ RSA \_ AES**</dt> </dl>                    | CSP che supporta le firme digitali e la crittografia dei dati tramite l'algoritmo [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES).<br/>                                                                                                                                                                                                                                                                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
