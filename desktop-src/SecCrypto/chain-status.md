---
description: Recupera lo stato di validità della catena o di un certificato specifico nella catena.
title: Proprietà IChain2::Status
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Status
- IChain.Status
- Chain.Status
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5307d03d340a0a960a5d78226d26e7b5553d27af72f255131651690e5b723355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769551"
---
# <a name="ichain2status-property"></a>Proprietà IChain2::Status

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) nello spazio dei [**nomi System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **proprietà Status** recupera lo stato di validità della catena o un certificato specifico nella catena.

## <a name="syntax"></a>Sintassi


```VB
Chain.Status( _
  ByVal Index _
) As Long
```



## <a name="property-value"></a>Valore proprietà

Valore **LONG** che rappresenta l'indicatore di stato di validità della catena o del certificato specificato. Nella tabella seguente sono illustrati i possibili valori. Questa proprietà conterrà zero se la catena o il certificato specificato è valido. In caso contrario, questa proprietà conterrà una combinazione di uno o più dei valori seguenti.

<dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM \_ TRUST \_ IS \_ NOT \_ TIME \_ VALID** (&H00000001)


</dt> <dd>

Questo certificato o uno dei certificati nella catena di certificati non è valido in fase di validità.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM \_ TRUST \_ IS \_ NOT \_ TIME \_ NESTED** (&H00000002)


</dt> <dd>

I certificati nella catena non sono annidati correttamente.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM \_ TRUST \_ IS \_ REVOKED** (&H00000004)


</dt> <dd>

L'attendibilità per questo certificato o uno dei certificati nella catena di certificati è stata revocata.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM \_ TRUST \_ IS \_ NOT \_ SIGNATURE \_ VALID** (&H00000008)


</dt> <dd>

Il certificato o uno dei certificati nella catena di certificati non ha una firma valida.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM \_ ATTENDIBILITÀ \_ \_ NON VALIDA PER \_ \_ \_ L'UTILIZZO** (&H00000010)


</dt> <dd>

Il certificato o la catena di certificati non è valida per l'utilizzo proposto.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM \_ TRUST \_ IS \_ UNTRUSTED \_ ROOT** (&H00000020)


</dt> <dd>

Il certificato o la catena di certificati si basa su una radice non attendibile.

</dd> <dt>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM \_ STATO \_ REVOCA \_ TRUST \_ SCONOSCIUTO** (&H00000040)


</dt> <dd>

Lo stato di revoca del certificato o di uno dei certificati nella catena di certificati è sconosciuto.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM \_ TRUST \_ IS \_ CYCLIC** (&H00000080)


</dt> <dd>

Uno dei certificati nella catena è stato rilasciato da [*un'autorità di certificazione*](../secgloss/c-gly.md) certificata dal certificato originale.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM \_ ESTENSIONE \_ TRUST \_ NON VALIDA** (&H00000100)


</dt> <dd>

Uno dei certificati ha un'estensione non valida.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM \_ VINCOLI \_ DI CRITERI TRUST NON \_ \_ VALIDI** (&H00000200)


</dt> <dd>

Il certificato o uno dei certificati nella catena di certificati ha un'estensione dei vincoli dei criteri e uno dei certificati emessi ha un'estensione per il mapping dei criteri non consentita o non ha un'estensione dei criteri di rilascio richiesta.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM \_ TRUST \_ INVALID \_ BASIC \_ CONSTRAINTS** (&H00000400)


</dt> <dd>

Il certificato o uno dei certificati nella catena di certificati ha un'estensione dei vincoli di base e il certificato non può essere usato per rilasciare altri certificati o la lunghezza del percorso della catena è stata superata.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM \_ VINCOLI \_ DI NOME TRUST NON \_ \_ VALIDI** (&H00000800)


</dt> <dd>

Il certificato o uno dei certificati nella catena di certificati ha un'estensione dei vincoli di nome non valida.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM \_ TRUST \_ NON SUPPORTA VINCOLI DI \_ \_ \_ \_ NOME** (&H00001000)


</dt> <dd>

Il certificato o uno dei certificati nella catena di certificati ha un'estensione dei vincoli di nome che contiene campi non supportati. I campi minimo e massimo non sono supportati. Pertanto il valore minimo deve essere sempre zero e il valore massimo deve essere sempre assente. Per un altro nome è supportato solo l'UPN. Le opzioni di nome alternativo seguenti non sono supportate:

-   Indirizzo X400
-   Nome entità EDI
-   ID registrato

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM \_ VINCOLO DI NOME TRUST \_ \_ NON \_ \_ DEFINITO \_** (&H00002000)


</dt> <dd>

Il certificato o uno dei certificati nella catena di certificati ha un'estensione dei vincoli di nome e manca un vincolo di nome per una delle scelte di nome nel certificato finale.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM \_ TRUST \_ HAS \_ NOT \_ PERMITTED \_ NAME \_ CONSTRAINT** (&H00004000)


</dt> <dd>

Il certificato o uno dei certificati nella catena di certificati ha un'estensione dei vincoli di nome e non esiste un vincolo di nome consentito per una delle scelte di nome nel certificato finale.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM \_ TRUST \_ HA \_ \_ ESCLUSO IL VINCOLO \_ DI** NOME (&H00008000)


</dt> <dd>

Il certificato o uno dei certificati nella catena di certificati ha un'estensione dei vincoli di nome e una delle opzioni di nome nel certificato finale viene esclusa in modo esplicito.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM \_ TRUST \_ IS \_ OFFLINE \_ REVOCATION** (&H01000000)


</dt> <dd>

Lo stato di revoca del certificato o di uno dei certificati nella catena di certificati è offline o non aggiornato.

</dd> <dt>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM \_ TRUST \_ NO \_ ISSUANCE \_ CHAIN \_ POLICY** (&H02000000)


</dt> <dd>

Il certificato finale non dispone di criteri di rilascio risultanti e uno dei certificati della CA emittente ha un'estensione dei vincoli dei criteri che lo richiede.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM \_ TRUST \_ IS \_ PARTIAL \_ CHAIN** (&H00010000)


</dt> <dd>

La catena di certificati non è in competizione.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM \_ TRUST \_ CTL \_ IS \_ NOT \_ TIME \_ VALID** (&H00020000)


</dt> <dd>

Un CTL usato per creare questa catena non è valido in tempo.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM \_ TRUST \_ CTL \_ IS \_ NOT \_ SIGNATURE \_ VALID** (&H00040000)


</dt> <dd>

Un CTL utilizzato per creare questa catena non dispone di una firma valida.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM \_ TRUST \_ CTL \_ IS \_ NOT \_ VALID \_ FOR \_ USAGE** (&H00080000)


</dt> <dd>

Un CTL usato per creare questa catena non è valido per questo utilizzo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
