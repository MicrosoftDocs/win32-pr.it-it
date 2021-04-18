---
description: Accede a un contenitore di chiavi esistente. Questo metodo associa il contenitore di chiavi al certificato che corrisponde alla chiave privata aggiungendo la \_ Proprietà CERT Key \_ prova \_ info \_ prop \_ ID usando le informazioni specificate.
ms.assetid: e5e19452-bfdc-4427-ac1d-cf8aa349bb89
title: Metodo PrivateKey. Open
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.Open
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7e39738a6e28ebbaffbc867f3098270d5043887a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326895"
---
# <a name="privatekeyopen-method"></a>Metodo PrivateKey. Open

\[Il metodo **Open** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**Proprietà X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo **Open** accede a un [*contenitore di chiavi*](../secgloss/k-gly.md)esistente. Questo metodo associa il contenitore di chiavi al [*certificato*](../secgloss/c-gly.md) che corrisponde alla [*chiave privata*](../secgloss/p-gly.md) aggiungendo la \_ Proprietà CERT Key \_ prova \_ info \_ prop \_ ID usando le informazioni specificate.

## <a name="syntax"></a>Sintassi


```VB
PrivateKey.Open( _
  ByVal ContainerName, _
  [ ByVal ProviderName ], _
  [ ByVal ProviderType ], _
  [ ByVal KeySpec ], _
  [ ByVal StoreLocation ], _
  [ ByVal bCheckExistence ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ContainerName* \[ in\]
</dt> <dd>

Stringa che contiene il nome del contenitore di chiavi.

</dd> <dt>

*Provider di provider* \[ in, facoltativo\]
</dt> <dd>

Stringa che contiene il nome del provider. Il valore predefinito è capicol \_ provo \_ \_ \_ . Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                      | Significato                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_MS_DEF_PROV"></span><span id="capicom_prov_ms_def_prov"></span><dl> <dt>**CAPICOM \_ prova \_ MS \_ def \_ prova**</dt> </dl>                                          | Provider di crittografia di base Microsoft.<br/>                            |
| <span id="CAPICOM_PROV_MS_ENHANCED_PROV"></span><span id="capicom_prov_ms_enhanced_prov"></span><dl> <dt>**capicol \_ provo \_ MS \_ Enhanced \_ Pro**</dt> </dl>                           | Microsoft Enhanced Cryptographic Provider.<br/>                        |
| <span id="CAPICOM_PROV_MS_STRONG_PROV"></span><span id="capicom_prov_ms_strong_prov"></span><dl> <dt>**capicol \_ provo prova \_ MS \_ Strong \_**</dt> </dl>                                 | Microsoft Strong Cryptographic Provider.<br/>                          |
| <span id="CAPICOM_PROV_MS_DEF_RSA_SIG_PROV"></span><span id="capicom_prov_ms_def_rsa_sig_prov"></span><dl> <dt>**CAPICOM \_ prova \_ MS \_ def \_ RSA \_ firma \_**</dt> </dl>                | Provider di crittografia Microsoft RSA Signature.<br/>                   |
| <span id="CAPICOM_PROV_MS_DEF_RSA_SCHANNEL_PROV"></span><span id="capicom_prov_ms_def_rsa_schannel_prov"></span><dl> <dt>**capicol \_ prova \_ MS \_ def \_ RSA \_ Schannel \_ prov**</dt> </dl> | Provider di crittografia Microsoft RSA SChannel.<br/>                    |
| <span id="CAPICOM_PROV_MS_DEF_DSS_PROV"></span><span id="capicom_prov_ms_def_dss_prov"></span><dl> <dt>**CAPICOM \_ prova \_ MS \_ def \_ DSS \_ prov**</dt> </dl>                             | Provider di crittografia Microsoft Base DSS.<br/>                        |
| <span id="CAPICOM_PROV_MS_DEF_DSS_DH_PROV"></span><span id="capicom_prov_ms_def_dss_dh_prov"></span><dl> <dt>**capicol \_ prov \_ MS \_ def \_ DSS \_ DH \_ prova**</dt> </dl>                   | Microsoft Base DSS e Diffie-Hellman provider di crittografia.<br/>     |
| <span id="CAPICOM_PROV_MS_ENH_DSS_DH_PROV"></span><span id="capicom_prov_ms_enh_dss_dh_prov"></span><dl> <dt>**CAPICOM \_ prova \_ MS \_ Enh \_ DSS \_ DH \_ prov**</dt> </dl>                   | Microsoft Enhanced DSS e Diffie-Hellman provider di crittografia.<br/> |
| <span id="CAPICOM_PROV_MS_DEF_DH_SCHANNEL_PROV"></span><span id="capicom_prov_ms_def_dh_schannel_prov"></span><dl> <dt>**CAPICOM \_ prov \_ MS \_ def \_ DH \_ Schannel \_ prova**</dt> </dl>    | Microsoft DH SChannel Cryptographic Provider.<br/>                     |
| <span id="CAPICOM_PROV_MS_SCARD_PROV"></span><span id="capicom_prov_ms_scard_prov"></span><dl> <dt>**capicol \_ provo \_ MS \_ SCard \_ prova**</dt> </dl>                                    | Provider di crittografia Smart Card Microsoft base.<br/>                 |
| <span id="CAPICOM_PROV_MS_ENH_RSA_AES_PROV"></span><span id="capicom_prov_ms_enh_rsa_aes_prov"></span><dl> <dt>**CAPICOM \_ prova \_ MS \_ Enh \_ RSA \_ AES \_ prov**</dt> </dl>                | Microsoft Enhanced RSA e AES Cryptographic Provider.<br/>            |



 

</dd> <dt>

*ProviderType* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione del [**\_ \_ tipo capicot**](capicom-prov-type.md) che specifica un tipo di provider. Il valore predefinito è CAPICOM \_ prova \_ RSA \_ full. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_RSA_FULL"></span><span id="capicom_prov_rsa_full"></span><dl> <dt>**capicol \_ prova \_ RSA \_ completo**</dt> </dl>                 | Il [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) completo di [*RSA*](../secgloss/r-gly.md) . Questo tipo di provider supporta le [*firme digitali*](../secgloss/d-gly.md) e la [*crittografia*](../secgloss/e-gly.md)dei dati.<br/> |
| <span id="CAPICOM_PROV_RSA_SIG"></span><span id="capicom_prov_rsa_sig"></span><dl> <dt>**capicol \_ prov \_ RSA \_ sig**</dt> </dl>                    | Subset del CSP RSA che supporta solo le funzioni e gli algoritmi richiesti per gli [*hash*](../secgloss/h-gly.md) e le [*firme digitali*](../secgloss/d-gly.md).<br/>                                                                                                                                                                              |
| <span id="CAPICOM_PROV_DSS"></span><span id="capicom_prov_dss"></span><dl> <dt>**capicol \_ prov \_ DSS**</dt> </dl>                                 | Il CSP di [*Digital Signature standard*](../secgloss/d-gly.md) (DSS). Questo tipo di provider supporta solo hash e firme digitali. DSS usa l' [*algoritmo di firma digitale*](../secgloss/d-gly.md) (DSA).<br/>                                                                                     |
| <span id="CAPICOM_PROV_FORTEZZA"></span><span id="capicom_prov_fortezza"></span><dl> <dt>**capicol \_ prova di \_ fortezza**</dt> </dl>                  | CSP che contiene i protocolli e gli algoritmi di crittografia di proprietà del [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST).<br/>                                                                                                                                                                          |
| <span id="CAPICOM_PROV_MS_EXCHANGE"></span><span id="capicom_prov_ms_exchange"></span><dl> <dt>**CAPICOM \_ provare \_ MS \_ Exchange**</dt> </dl>        | CSP che supporta l'applicazione di posta elettronica di Microsoft Exchange e altre applicazioni compatibili con Microsoft Mail.<br/>                                                                                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROV_SSL"></span><span id="capicom_prov_ssl"></span><dl> <dt>**capicol \_ prova \_ SSL**</dt> </dl>                                 | CSP che supporta il protocollo [*Secure Sockets Layer*](../secgloss/s-gly.md) (SSL).<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROV_RSA_SCHANNEL"></span><span id="capicom_prov_rsa_schannel"></span><dl> <dt>**CAPICOM \_ prova \_ RSA \_ Schannel**</dt> </dl>     | CSP che supporta sia i protocolli RSA che i protocolli [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_PROV_DSS_DH"></span><span id="capicom_prov_dss_dh"></span><dl> <dt>**CAPICOM \_ prova \_ DSS \_ DH**</dt> </dl>                       | CSP che supporta i protocolli DSS e [*Diffie-Hellman*](../secgloss/d-gly.md) .<br/>                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_EC_ECDSA_SIG"></span><span id="capicom_prov_ec_ecdsa_sig"></span><dl> <dt>**capicol \_ prova \_ EC \_ ECDSA \_ sig**</dt> </dl>    | CSP che supporta le funzioni e gli algoritmi ECDSA (ellittica Digital Signature Algorithm) necessari per le firme digitali.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_EC_ECNRA_SIG"></span><span id="capicom_prov_ec_ecnra_sig"></span><dl> <dt>**capicol \_ prova \_ EC \_ ECNRA \_ sig**</dt> </dl>    | CSP che supporta la curva ellittica Nyberg-Rueppel le funzioni analogiche (ECNRA) e gli algoritmi richiesti per le firme digitali.<br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROV_EC_ECDSA_FULL"></span><span id="capicom_prov_ec_ecdsa_full"></span><dl> <dt>**capicol \_ prove \_ EC \_ ECDSA \_ completo**</dt> </dl> | CSP che supporta il ECDSA completo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_EC_ECNRA_FULL"></span><span id="capicom_prov_ec_ecnra_full"></span><dl> <dt>**capicol \_ prove \_ EC \_ ECNRA \_ completo**</dt> </dl> | CSP che supporta il ECNRA completo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_DH_SCHANNEL"></span><span id="capicom_prov_dh_schannel"></span><dl> <dt>**CAPICOM \_ prova \_ DH \_ Schannel**</dt> </dl>        | CSP che supporta sia i protocolli [*Diffie-Hellman*](../secgloss/d-gly.md) che i protocolli [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_SPYRUS_LYNKS"></span><span id="capicom_prov_spyrus_lynks"></span><dl> <dt>**CAPICOM \_ prova \_ Spyrus Deployment \_ Lynks**</dt> </dl>     | CSP che supporta il dispositivo Spyrus Deployment LYNKS card.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CAPICOM_PROV_RNG"></span><span id="capicom_prov_rng"></span><dl> <dt>**capicol \_ prov \_ RNG**</dt> </dl>                                 | CSP che gestisce la generazione di numeri casuali.<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_INTEL_SEC"></span><span id="capicom_prov_intel_sec"></span><dl> <dt>**CAPICOM \_ prova \_ Intel \_ sec**</dt> </dl>              | CSP che fornisce la sicurezza di Intel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_REPLACE_OWF"></span><span id="capicom_prov_replace_owf"></span><dl> <dt>**CAPICOM prova a \_ \_ sostituire \_ OWF**</dt> </dl>        | CSP che supporta la sostituzione del modo in cui vengono generati formati unidirezionali da password.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_RSA_AES"></span><span id="capicom_prov_rsa_aes"></span><dl> <dt>**CAPICOM \_ prova \_ RSA \_ AES**</dt> </dl>                    | CSP che supporta le firme digitali e la crittografia dei dati tramite l'algoritmo Advanced Encryption Standard ([*AES*](../secgloss/a-gly.md)).<br/>                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

*Spec* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione delle [**\_ \_ specifiche della chiave capicot**](capicom-key-spec.md) che specifica il tipo di chiave privata. Il valore predefinito è la firma della \_ specifica della chiave CAPICOM \_ \_ . Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                        | Significato                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="CAPICOM_KEY_SPEC_KEYEXCHANGE"></span><span id="capicom_key_spec_keyexchange"></span><dl> <dt>**chiave per lo \_ scambio di chiavi di CAPICOM \_ \_**</dt> </dl> | La chiave può essere usata per la crittografia e la firma.<br/> |
| <span id="CAPICOM_KEY_SPEC_SIGNATURE"></span><span id="capicom_key_spec_signature"></span><dl> <dt>**firma della specifica della \_ chiave CAPICOM \_ \_**</dt> </dl>       | La chiave può essere usata solo per la firma.<br/>           |



 

</dd> <dt>

*StoreLocation* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione del [**\_ \_ percorso dell'archivio CAPICOM**](capicom-store-location.md) che specifica la posizione dell'archivio in cui risiede la chiave. Il valore predefinito è CAPICOM ( \_ \_ archivio utente corrente) \_ . Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                              | Significato                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <dt>**\_Archivio di memoria CAPICOM \_**</dt> </dl>                                                | L'archivio è un archivio di memoria. Eventuali modifiche apportate al contenuto dell'archivio non vengono rese permanente.<br/>                                                                                                                                                                                |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <dt>**\_Archivio del computer locale \_ CAPICOM \_**</dt> </dl>                          | L'archivio è un archivio del computer locale. Gli archivi del computer locale possono essere archivi di lettura/scrittura solo se l'utente dispone di autorizzazioni di lettura/scrittura. Se l'utente dispone di autorizzazioni di lettura/scrittura e se l'archivio è aperto in lettura/scrittura, le modifiche apportate al contenuto dell'archivio vengono rese permanente.<br/> |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <dt>**\_ \_ archivio utente corrente CAPICOM \_**</dt> </dl>                             | L'archivio è un archivio utente corrente. Un archivio utente corrente può essere un archivio di lettura/scrittura. In caso contrario, le modifiche apportate al contenuto dell'archivio vengono rese permanente.<br/>                                                                                                                        |
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <dt>**\_archivio utenti di Active \_ directory \_ di \_ CAPICOM**</dt> </dl> | L'archivio è un archivio Active Directory. Gli archivi di Active Directory possono essere aperti solo in modalità di sola lettura. I certificati non possono essere aggiunti o rimossi dagli archivi Active Directory.<br/>                                                                                          |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <dt>**\_ \_ \_ archivio utenti smart card \_ CAPICOM**</dt> </dl>                   | L'archivio è il gruppo di smart card presenti. Introdotta in capicol 2,0.<br/>                                                                                                                                                                                               |



 

</dd> <dt>

*bCheckExistence* \[ in, facoltativo\]
</dt> <dd>

Valore booleano che indica se capicol tenterà di accedere alla chiave. Se **true**, CAPICOM tenta di accedere alla chiave. Se la chiave è protetta dall'utente o in una smart card o in un altro dispositivo, è possibile che venga generata una finestra di dialogo. Il valore predefinito è **False**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo restituisce capicol \_ E \_ non \_ è consentito quando viene inserito nello script da un'applicazione basata sul Web.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> <dt>

[**Certificate. HasPrivateKey**](certificate-hasprivatekey.md)
</dt> </dl>

 

 
