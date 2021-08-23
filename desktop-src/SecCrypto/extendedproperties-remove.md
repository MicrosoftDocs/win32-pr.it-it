---
description: Rimuove una proprietà estesa dalla raccolta.
ms.assetid: 0329a158-758d-4e73-95a5-bab7307e7d70
title: Metodo ExtendedProperties.Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 684d5abc0a0114e0d2bedb0dc544d50e13337631bb41fb457480dfbe8c5364e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007219"
---
# <a name="extendedpropertiesremove-method"></a>Metodo ExtendedProperties.Remove

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece Platform Invocation Services (PInvoke) per chiamare la funzione API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e ottenere le proprietà. Per informazioni su PInvoke, vedere [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx). Possono essere utili anche .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) parte 1 e .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) parte 2 delle sottosezioni dell'estensione della crittografia .NET con CAPICOM e [P/Invoke.](/previous-versions/ms867087(v=msdn.10))\]

Il **metodo Remove** rimuove una proprietà estesa dalla raccolta.

## <a name="syntax"></a>Sintassi


```VB
ExtendedProperties.Remove( _
  ByVal propID _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*propID* \[ Pollici\]
</dt> <dd>

Valore [**dell'enumerazione CAPICOM \_ PROPID**](capicom-propid.md) che definisce gli identificatori di proprietà CAPICOM della proprietà estesa da rimuovere. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROPID_UNKNOWN"></span><span id="capicom_propid_unknown"></span><dl> <dt>**CAPICOM \_ PROPID \_ UNKNOWN**</dt> </dl>                                                                       | Il tipo della proprietà non è noto.<br/>                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_KEY_PROV_HANDLE"></span><span id="capicom_propid_key_prov_handle"></span><dl> <dt>**HANDLE \_ \_ PROV CHIAVE PROPID CAPICOM \_ \_**</dt> </dl>                                             | Handle per un contenitore di chiavi all'interno [*di un provider del servizio*](../secgloss/c-gly.md) di crittografia (CSP).<br/>                                                                                        |
| <span id="CAPICOM_PROPID_KEY_PROV_INFO"></span><span id="capicom_propid_key_prov_info"></span><dl> <dt>**CAPICOM \_ PROPID \_ KEY \_ PROV \_ INFO**</dt> </dl>                                                   | Informazioni su un contenitore di chiavi all'interno di un CSP.<br/>                                                                                                                                                                                                                                 |
| <span id="CAPICOM_PROPID_SHA1_HASH"></span><span id="capicom_propid_sha1_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ SHA1 \_ HASH**</dt> </dl>                                                                | Oggetto hash SHA1.<br/>                                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_HASH_PROP"></span><span id="capicom_propid_hash_prop"></span><dl> <dt>**CAPICOM \_ PROPID \_ HASH \_ PROP**</dt> </dl>                                                                | Proprietà di un oggetto hash.<br/>                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_MD5_HASH"></span><span id="capicom_propid_md5_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ MD5 \_ HASH**</dt> </dl>                                                                   | Oggetto hash MD5.<br/>                                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_KEY_CONTEXT"></span><span id="capicom_propid_key_context"></span><dl> <dt>**CONTESTO DELLA CHIAVE PROPID CAPICOM \_ \_ \_**</dt> </dl>                                                          | Contesto della [*chiave.*](../secgloss/c-gly.md)<br/>                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_KEY_SPEC"></span><span id="capicom_propid_key_spec"></span><dl> <dt>**SPECIFICA \_ DELLA CHIAVE PROPID \_ \_ CAPICOM**</dt> </dl>                                                                   | Specifiche per una chiave.<br/>                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_IE30_RESERVED"></span><span id="capicom_propid_ie30_reserved"></span><dl> <dt>**CAPICOM \_ PROPID \_ IE30 \_ RESERVED**</dt> </dl>                                                    | Informazioni su se l'oggetto è riservato in Internet Explorer 3.0.<br/>                                                                                                                                                                                                      |
| <span id="CAPICOM_PROPID_PUBKEY_HASH_RESERVED"></span><span id="capicom_propid_pubkey_hash_reserved"></span><dl> <dt>**CAPICOM \_ PROPID \_ PUBKEY \_ HASH \_ RESERVED**</dt> </dl>                              | Informazioni sull'eventuale riserva dell'hash della chiave pubblica.<br/>                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_ENHKEY_USAGE"></span><span id="capicom_propid_enhkey_usage"></span><dl> <dt>**UTILIZZO \_ DI CAPICOM PROPID \_ \_ ENHKEY**</dt> </dl>                                                       | Utilizzo [*chiavi avanzato*](../secgloss/e-gly.md) (EKU).<br/>                                                                                                                                                              |
| <span id="CAPICOM_PROPID_CTL_USAGE"></span><span id="capicom_propid_ctl_usage"></span><dl> <dt>**UTILIZZO CTL DI CAPICOM \_ PROPID \_ \_**</dt> </dl>                                                                | Utilizzo [*di un elenco di*](../secgloss/c-gly.md) certificati attendibili (CTL).<br/>                                                                                                                                             |
| <span id="CAPICOM_PROPID_NEXT_UPDATE_LOCATION"></span><span id="capicom_propid_next_update_location"></span><dl> <dt>**POSIZIONE DI AGGIORNAMENTO SUCCESSIVO DI CAPICOM \_ PROPID \_ \_ \_**</dt> </dl>                              | Percorso del successivo aggiornamento dell'elenco [*di revoche di certificati*](../secgloss/c-gly.md) (CRL).<br/>                                                                                               |
| <span id="CAPICOM_PROPID_FRIENDLY_NAME"></span><span id="capicom_propid_friendly_name"></span><dl> <dt>**NOME \_ DESCRITTIVO DEL PROPID CAPICOM \_ \_**</dt> </dl>                                                    | Nome leggibile.<br/>                                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_PVK_FILE"></span><span id="capicom_propid_pvk_file"></span><dl> <dt>**CAPICOM \_ PROPID \_ PVK \_ FILE**</dt> </dl>                                                                   | File che contiene una chiave privata.<br/>                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_DESCRIPTION"></span><span id="capicom_propid_description"></span><dl> <dt>**DESCRIZIONE \_ DEL PROPID CAPICOM \_**</dt> </dl>                                                           | Descrizione leggibile.<br/>                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_ACCESS_STATE"></span><span id="capicom_propid_access_state"></span><dl> <dt>**STATO DI ACCESSO PROPID CAPICOM \_ \_ \_**</dt> </dl>                                                       | Stato dell'accesso.<br/>                                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SIGNATURE_HASH"></span><span id="capicom_propid_signature_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ SIGNATURE \_ HASH**</dt> </dl>                                                 | Hash della firma.<br/>                                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SMART_CARD_DATA"></span><span id="capicom_propid_smart_card_data"></span><dl> <dt>**DATI \_ DELLA \_ SMART \_ CARD CAPICOM PROPID \_**</dt> </dl>                                             | Dati delle smart card.<br/>                                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_EFS"></span><span id="capicom_propid_efs"></span><dl> <dt>**CAPICOM \_ PROPID \_ EFS**</dt> </dl>                                                                                   | Un Encrypting File System (EFS).<br/>                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_FORTEZZA_DATA"></span><span id="capicom_propid_fortezza_data"></span><dl> <dt>**CAPICOM \_ PROPID \_ FOR DEI \_ DATI**</dt> </dl>                                                    | Dati creati usando i protocolli di crittografia e gli algoritmi di proprietà del [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST).<br/> |
| <span id="CAPICOM_PROPID_ARCHIVED"></span><span id="capicom_propid_archived"></span><dl> <dt>**CAPICOM \_ PROPID \_ ARCHIVED**</dt> </dl>                                                                    | Informazioni sull'archiviazione dell'oggetto.<br/>                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_KEY_IDENTIFIER"></span><span id="capicom_propid_key_identifier"></span><dl> <dt>**IDENTIFICATORE \_ DI CHIAVE PROPID CAPICOM \_ \_**</dt> </dl>                                                 | Identificatore di chiave.<br/>                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_AUTO_ENROLL"></span><span id="capicom_propid_auto_enroll"></span><dl> <dt>**REGISTRAZIONE AUTOMATICA DI CAPICOM \_ PROPID \_ \_**</dt> </dl>                                                          | Informazioni di registrazione automatica per un certificato.<br/>                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROPID_PUBKEY_ALG_PARA"></span><span id="capicom_propid_pubkey_alg_para"></span><dl> <dt>**CAPICOM \_ PROPID \_ PUBKEY \_ ALG \_ PARA**</dt> </dl>                                             | Parametri per un algoritmo a chiave pubblica.<br/>                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_CROSS_CERT_DIST_POINTS"></span><span id="capicom_propid_cross_cert_dist_points"></span><dl> <dt>**CAPICOM \_ PROPID \_ CROSS \_ CERT \_ DIST \_ POINTS**</dt> </dl>                       | Informazioni usate per aggiornare i certificati incrociati dinamici.<br/>                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_ISSUER_PUBLIC_KEY_MD5_HASH"></span><span id="capicom_propid_issuer_public_key_md5_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ ISSUER \_ PUBLIC \_ KEY \_ MD5 \_ HASH**</dt> </dl>          | Hash MD5 della chiave pubblica dell'autorità emittente.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SUBJECT_PUBLIC_KEY_MD5_HASH"></span><span id="capicom_propid_subject_public_key_md5_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ SUBJECT \_ PUBLIC \_ KEY \_ MD5 \_ HASH**</dt> </dl>       | Hash MD5 della chiave pubblica dell'oggetto.<br/>                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROPID_ENROLLMENT"></span><span id="capicom_propid_enrollment"></span><dl> <dt>**REGISTRAZIONE \_ PROPID CAPICOM \_**</dt> </dl>                                                              | Informazioni sulla registrazione del certificato.<br/>                                                                                                                                                                                                                                 |
| <span id="CAPICOM_PROPID_DATE_STAMP"></span><span id="capicom_propid_date_stamp"></span><dl> <dt>**INDICATORE DI DATA DI CAPICOM \_ PROPID \_ \_**</dt> </dl>                                                             | Indicatore di data.<br/>                                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_ISSUER_SERIAL_NUMBER_MD5_HASH"></span><span id="capicom_propid_issuer_serial_number_md5_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ ISSUER \_ SERIAL \_ NUMBER \_ MD5 \_ HASH**</dt> </dl> | Hash MD5 del numero di serie dell'autorità emittente.<br/>                                                                                                                                                                                                                                     |
| <span id="CAPICOM_PROPID_SUBJECT_NAME_MD5_HASH"></span><span id="capicom_propid_subject_name_md5_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ SUBJECT \_ NAME \_ MD5 \_ HASH**</dt> </dl>                          | Hash MD5 del nome del soggetto.<br/>                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_EXTENDED_ERROR_INFO"></span><span id="capicom_propid_extended_error_info"></span><dl> <dt>**INFORMAZIONI SULL'ERRORE ESTESO DI CAPICOM \_ PROPID \_ \_ \_**</dt> </dl>                                 | Informazioni estese su un errore.<br/>                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROPID_RENEWAL"></span><span id="capicom_propid_renewal"></span><dl> <dt>**RINNOVO \_ PROPID CAPICOM \_**</dt> </dl>                                                                       | Informazioni sul rinnovo di [*un'autorità di certificazione.*](../secgloss/c-gly.md)<br/>                                                                                                                     |
| <span id="CAPICOM_PROPID_ARCHIVED_KEY_HASH"></span><span id="capicom_propid_archived_key_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ ARCHIVED \_ KEY \_ HASH**</dt> </dl>                                       | Hash archiviato di una chiave.<br/>                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROPID_FIRST_RESERVED"></span><span id="capicom_propid_first_reserved"></span><dl> <dt>**CAPICOM \_ PROPID \_ FIRST \_ RESERVED**</dt> </dl>                                                 | Informazioni sulla prima prenotazione.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_LAST_RESERVED"></span><span id="capicom_propid_last_reserved"></span><dl> <dt>**CAPICOM \_ PROPID \_ LAST \_ RESERVED**</dt> </dl>                                                    | Informazioni sulla prenotazione più recente.<br/>                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROPID_FIRST_USER"></span><span id="capicom_propid_first_user"></span><dl> <dt>**CAPICOM \_ PROPID \_ FIRST \_ USER**</dt> </dl>                                                             | Informazioni sul primo utente.<br/>                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_LAST_USER"></span><span id="capicom_propid_last_user"></span><dl> <dt>**CAPICOM \_ PROPID \_ LAST \_ USER**</dt> </dl>                                                                | Informazioni sull'utente più recente.<br/>                                                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
