---
description: Rimuove una proprietà estesa dalla raccolta.
ms.assetid: 0329a158-758d-4e73-95a5-bab7307e7d70
title: Metodo ExtendedProperties. Remove
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
ms.openlocfilehash: 1774ce0fc8b03bed621c58b0f7a9a0f16a7d4156
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329227"
---
# <a name="extendedpropertiesremove-method"></a>Metodo ExtendedProperties. Remove

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare la funzione API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e ottenere le proprietà. Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx). Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

Il metodo **Remove** rimuove una proprietà estesa dalla raccolta.

## <a name="syntax"></a>Sintassi


```VB
ExtendedProperties.Remove( _
  ByVal propID _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*propid* \[ in\]
</dt> <dd>

Valore dell'enumerazione [**\_ propid di CAPICOM**](capicom-propid.md) che definisce gli identificatori della proprietà CAPICOM della proprietà estesa da rimuovere. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROPID_UNKNOWN"></span><span id="capicom_propid_unknown"></span><dl> <dt>**CAPICOM \_ propid \_ sconosciuto**</dt> </dl>                                                                       | Il tipo della proprietà non è noto.<br/>                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_KEY_PROV_HANDLE"></span><span id="capicom_propid_key_prov_handle"></span><dl> <dt>**HANDLE di capicot \_ propid \_ chiave \_ prov \_**</dt> </dl>                                             | Handle per un contenitore di chiavi all'interno di un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).<br/>                                                                                        |
| <span id="CAPICOM_PROPID_KEY_PROV_INFO"></span><span id="capicom_propid_key_prov_info"></span><dl> <dt>**CAPICOM \_ propid \_ chiave \_ prova \_ informazioni**</dt> </dl>                                                   | Informazioni su un contenitore di chiavi all'interno di un CSP.<br/>                                                                                                                                                                                                                                 |
| <span id="CAPICOM_PROPID_SHA1_HASH"></span><span id="capicom_propid_sha1_hash"></span><dl> <dt>**\_ \_ Hash SHA1 propid di CAPICOM \_**</dt> </dl>                                                                | Oggetto hash SHA1.<br/>                                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_HASH_PROP"></span><span id="capicom_propid_hash_prop"></span><dl> <dt>**\_ \_ prop propid hash \_ prop**</dt> </dl>                                                                | Proprietà di un oggetto hash.<br/>                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_MD5_HASH"></span><span id="capicom_propid_md5_hash"></span><dl> <dt>**\_ \_ Hash MD5 propid di CAPICOM \_**</dt> </dl>                                                                   | Oggetto hash MD5.<br/>                                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_KEY_CONTEXT"></span><span id="capicom_propid_key_context"></span><dl> <dt>**contesto della chiave capicol \_ propid \_ \_**</dt> </dl>                                                          | [*Contesto*](../secgloss/c-gly.md)della chiave.<br/>                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_KEY_SPEC"></span><span id="capicom_propid_key_spec"></span><dl> <dt>**specifiche della chiave capicol \_ propid \_ \_**</dt> </dl>                                                                   | Specifiche per una chiave.<br/>                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_IE30_RESERVED"></span><span id="capicom_propid_ie30_reserved"></span><dl> <dt>**CAPICOM \_ propid \_ Ie30 \_ riservato**</dt> </dl>                                                    | Informazioni sul fatto che l'oggetto sia riservato in Internet Explorer 3,0.<br/>                                                                                                                                                                                                      |
| <span id="CAPICOM_PROPID_PUBKEY_HASH_RESERVED"></span><span id="capicom_propid_pubkey_hash_reserved"></span><dl> <dt>**CAPICOM \_ propid \_ PUBKEY \_ hash \_ riservato**</dt> </dl>                              | Informazioni che indica se l'hash della chiave pubblica è riservato.<br/>                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_ENHKEY_USAGE"></span><span id="capicom_propid_enhkey_usage"></span><dl> <dt>**utilizzo di capicol \_ propid \_ ENHKEY \_**</dt> </dl>                                                       | [*Utilizzo chiavi avanzato*](../secgloss/e-gly.md) (EKU).<br/>                                                                                                                                                              |
| <span id="CAPICOM_PROPID_CTL_USAGE"></span><span id="capicom_propid_ctl_usage"></span><dl> <dt>**utilizzo di CAPICOM \_ propid \_ CTL \_**</dt> </dl>                                                                | Utilizzo di un [*elenco di certificati attendibili*](../secgloss/c-gly.md) (CTL).<br/>                                                                                                                                             |
| <span id="CAPICOM_PROPID_NEXT_UPDATE_LOCATION"></span><span id="capicom_propid_next_update_location"></span><dl> <dt>**\_ \_ \_ percorso di aggiornamento successivo \_ di CAPICOM propid**</dt> </dl>                              | Percorso del successivo aggiornamento dell' [*elenco di revoche di certificati*](../secgloss/c-gly.md) (CRL).<br/>                                                                                               |
| <span id="CAPICOM_PROPID_FRIENDLY_NAME"></span><span id="capicom_propid_friendly_name"></span><dl> <dt>**\_ \_ nome descrittivo propid di CAPICOM \_**</dt> </dl>                                                    | Nome leggibile.<br/>                                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_PVK_FILE"></span><span id="capicom_propid_pvk_file"></span><dl> <dt>**FILE capicol \_ propid \_ PVK \_**</dt> </dl>                                                                   | Un file che contiene una chiave privata.<br/>                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_DESCRIPTION"></span><span id="capicom_propid_description"></span><dl> <dt>**CAPICOM \_ propid \_ Descrizione**</dt> </dl>                                                           | Descrizione leggibile.<br/>                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_ACCESS_STATE"></span><span id="capicom_propid_access_state"></span><dl> <dt>**stato di accesso di CAPICOM \_ propid \_ \_**</dt> </dl>                                                       | Stato dell'accesso.<br/>                                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SIGNATURE_HASH"></span><span id="capicom_propid_signature_hash"></span><dl> <dt>**\_ \_ hash della firma CAPICOM propid \_**</dt> </dl>                                                 | Hash della firma.<br/>                                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SMART_CARD_DATA"></span><span id="capicom_propid_smart_card_data"></span><dl> <dt>**\_ \_ dati della smart card propid \_ di \_ CAPICOM**</dt> </dl>                                             | Dati della smart card.<br/>                                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_EFS"></span><span id="capicom_propid_efs"></span><dl> <dt>**\_propid \_ EFS**</dt> </dl>                                                                                   | Un Encrypting File System (EFS).<br/>                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_FORTEZZA_DATA"></span><span id="capicom_propid_fortezza_data"></span><dl> <dt>**dati di capicol \_ propid \_ fortezza \_**</dt> </dl>                                                    | Dati creati usando i protocolli di crittografia e gli algoritmi di proprietà del [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST).<br/> |
| <span id="CAPICOM_PROPID_ARCHIVED"></span><span id="capicom_propid_archived"></span><dl> <dt>**CAPICOM \_ propid \_ archiviato**</dt> </dl>                                                                    | Informazioni sull'eventuale archiviazione dell'oggetto.<br/>                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_KEY_IDENTIFIER"></span><span id="capicom_propid_key_identifier"></span><dl> <dt>**identificatore di chiave capicol \_ propid \_ \_**</dt> </dl>                                                 | Identificatore di chiave.<br/>                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_AUTO_ENROLL"></span><span id="capicom_propid_auto_enroll"></span><dl> <dt>**\_ \_ registrazione automatica di CAPICOM propid \_**</dt> </dl>                                                          | Informazioni di registrazione automatica per un certificato.<br/>                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROPID_PUBKEY_ALG_PARA"></span><span id="capicom_propid_pubkey_alg_para"></span><dl> <dt>**CAPICOM \_ propid \_ PUBKEY \_ ALG \_ para**</dt> </dl>                                             | Parametri per un algoritmo a chiave pubblica.<br/>                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_CROSS_CERT_DIST_POINTS"></span><span id="capicom_propid_cross_cert_dist_points"></span><dl> <dt>**\_punti di dist propid \_ Cross \_ CERT \_ \_**</dt> </dl>                       | Informazioni utilizzate per aggiornare i certificati incrociati dinamici.<br/>                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_ISSUER_PUBLIC_KEY_MD5_HASH"></span><span id="capicom_propid_issuer_public_key_md5_hash"></span><dl> <dt>**L' \_ \_ \_ \_ \_ hash MD5 della chiave pubblica dell'autorità emittente \_ propid CAPICOM**</dt> </dl>          | Hash MD5 della chiave pubblica dell'autorità emittente.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SUBJECT_PUBLIC_KEY_MD5_HASH"></span><span id="capicom_propid_subject_public_key_md5_hash"></span><dl> <dt>**L' \_ \_ \_ \_ \_ hash MD5 della chiave pubblica del soggetto CAPICOM propid \_**</dt> </dl>       | Hash MD5 della chiave pubblica dell'oggetto.<br/>                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROPID_ENROLLMENT"></span><span id="capicom_propid_enrollment"></span><dl> <dt>**\_registrazione propid CAPICOM \_**</dt> </dl>                                                              | Informazioni sulla registrazione del certificato.<br/>                                                                                                                                                                                                                                 |
| <span id="CAPICOM_PROPID_DATE_STAMP"></span><span id="capicom_propid_date_stamp"></span><dl> <dt>**\_indicatore di data propid \_ CAPICOM \_**</dt> </dl>                                                             | Indicatore di data.<br/>                                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_ISSUER_SERIAL_NUMBER_MD5_HASH"></span><span id="capicom_propid_issuer_serial_number_md5_hash"></span><dl> <dt>**Il numero di \_ \_ serie dell'emittente \_ propid \_ \_ di CAPICOM \_**</dt> </dl> | Hash MD5 del numero di serie dell'emittente.<br/>                                                                                                                                                                                                                                     |
| <span id="CAPICOM_PROPID_SUBJECT_NAME_MD5_HASH"></span><span id="capicom_propid_subject_name_md5_hash"></span><dl> <dt>**\_Nome del soggetto propid \_ \_ \_ di \_ CAPICOM**</dt> </dl>                          | Hash MD5 del nome del soggetto.<br/>                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_EXTENDED_ERROR_INFO"></span><span id="capicom_propid_extended_error_info"></span><dl> <dt>**\_ \_ informazioni sugli errori estesi di CAPICOM propid \_ \_**</dt> </dl>                                 | Informazioni estese su un errore.<br/>                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROPID_RENEWAL"></span><span id="capicom_propid_renewal"></span><dl> <dt>**\_rinnovo propid di CAPICOM \_**</dt> </dl>                                                                       | Informazioni sul rinnovo di un' [*autorità di certificazione*](../secgloss/c-gly.md).<br/>                                                                                                                     |
| <span id="CAPICOM_PROPID_ARCHIVED_KEY_HASH"></span><span id="capicom_propid_archived_key_hash"></span><dl> <dt>**\_ \_ \_ hash della chiave archiviato \_ di CAPICOM propid**</dt> </dl>                                       | Hash archiviato di una chiave.<br/>                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROPID_FIRST_RESERVED"></span><span id="capicom_propid_first_reserved"></span><dl> <dt>**CAPICOM \_ propid \_ primo \_ riservato**</dt> </dl>                                                 | Informazioni sulla prima prenotazione.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_LAST_RESERVED"></span><span id="capicom_propid_last_reserved"></span><dl> <dt>**\_ \_ ultimo riservato di CAPICOM propid \_**</dt> </dl>                                                    | Informazioni sulla prenotazione più recente.<br/>                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROPID_FIRST_USER"></span><span id="capicom_propid_first_user"></span><dl> <dt>**CAPICOM \_ propid \_ primo \_ utente**</dt> </dl>                                                             | Informazioni sul primo utente.<br/>                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_LAST_USER"></span><span id="capicom_propid_last_user"></span><dl> <dt>**\_ \_ ultimo utente di CAPICOM propid \_**</dt> </dl>                                                                | Informazioni sull'utente più recente.<br/>                                                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
