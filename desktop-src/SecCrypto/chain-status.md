---
description: Recupera lo stato di validità della catena o di un certificato specifico nella catena.
title: 'Proprietà IChain2:: status'
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
ms.openlocfilehash: 23673289e2ff39d4180a4be8dc0be61f4a5cffc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329347"
---
# <a name="ichain2status-property"></a>Proprietà IChain2:: status

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **status** recupera lo stato di validità della catena o di un certificato specifico nella catena.

## <a name="syntax"></a>Sintassi


```VB
Chain.Status( _
  ByVal Index _
) As Long
```



## <a name="property-value"></a>Valore proprietà

Valore **Long** che rappresenta l'indicatore di stato della validità della catena o del certificato specificato. Nella tabella seguente sono illustrati i possibili valori. Questa proprietà conterrà zero se la catena o il certificato specificato è valido. In caso contrario, questa proprietà conterrà una combinazione di uno o più dei valori seguenti.

<dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM \_ L'ATTENDIBILità \_ \_ non è \_ ora \_ valida** (&H00000001)


</dt> <dd>

Questo certificato o uno dei certificati nella catena di certificati non è ora valido.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM \_ L'ATTENDIBILità \_ non è un' \_ \_ ora \_ annidata** (&H00000002)


</dt> <dd>

I certificati nella catena non sono ora annidati correttamente.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM \_ Il TRUST \_ è \_ revocato** (&H00000004)


</dt> <dd>

La relazione di trust per questo certificato o uno dei certificati nella catena di certificati è stata revocata.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM \_ L'ATTENDIBILità \_ \_ non è \_ \_ valida per la firma** (&H00000008)


</dt> <dd>

Il certificato o uno dei certificati della catena di certificati non dispone di una firma valida.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM \_ L'ATTENDIBILità \_ \_ non è \_ valida \_ per l' \_ utilizzo** (&H00000010)


</dt> <dd>

Il certificato o la catena di certificati non è valida per l'utilizzo proposto.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM \_ L'ATTENDIBILità \_ è una \_ \_ radice non attendibile** (&H00000020)


</dt> <dd>

Il certificato o la catena di certificati si basa su una radice non attendibile.

</dd> <dt>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM \_ Stato di revoca ATTENDIBILe \_ \_ \_ sconosciuto** (&H00000040)


</dt> <dd>

Lo stato di revoca del certificato o di uno dei certificati nella catena di certificati è sconosciuto.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM \_ Il TRUST \_ è \_ ciclico** (&H00000080)


</dt> <dd>

Uno dei certificati della catena è stato emesso da un' [*autorità di certificazione*](../secgloss/c-gly.md) che il certificato originale certificava.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM \_ \_ \_ Estensione attendibile non valida** (&H00000100)


</dt> <dd>

Uno dei certificati ha un'estensione non valida.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM \_ \_Vincoli di \_ criteri \_ non validi** (&H00000200)


</dt> <dd>

Il certificato o uno dei certificati nella catena di certificati ha un'estensione di vincoli di criteri e uno dei certificati emessi ha un'estensione di mapping dei criteri non consentita o non dispone di un'estensione dei criteri di rilascio richiesta.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM \_ ATTENDIBILità \_ \_ \_ vincoli di base non validi** (&H00000400)


</dt> <dd>

Il certificato o uno dei certificati nella catena di certificati ha un'estensione di vincoli di base e il certificato non può essere usato per emettere altri certificati oppure la lunghezza del percorso della catena è stata superata.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM \_ \_Vincoli di \_ nome \_ attendibile non validi** (&H00000800)


</dt> <dd>

Il certificato o uno dei certificati nella catena di certificati ha un'estensione di vincoli di nome non valida.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM \_ Il \_ \_ vincolo di \_ \_ nome \_ non è supportato dal trust** (&H00001000)


</dt> <dd>

Il certificato o uno dei certificati nella catena di certificati ha un'estensione di vincoli di nome che contiene campi non supportati. I campi minimo e massimo non sono supportati. Quindi il valore minimo deve essere sempre zero e il valore massimo deve essere sempre assente. Per un altro nome è supportato solo UPN. Le opzioni di nome alternativo seguenti non sono supportate:

-   Indirizzo X400
-   Nome entità EDI
-   ID registrato

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM \_ \_Vincolo di \_ \_ \_ nome \_ non definito dal trust** (&H00002000)


</dt> <dd>

Il certificato o uno dei certificati nella catena di certificati ha un'estensione di vincoli di nome e non è presente un vincolo di nome per una delle opzioni del nome nel certificato finale.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM \_ \_ \_ \_ \_ \_ Vincolo Name non consentito** (&H00004000)


</dt> <dd>

Il certificato o uno dei certificati nella catena di certificati ha un'estensione di vincoli di nome e non è consentito un vincolo di nome per una delle opzioni del nome nel certificato finale.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM \_ Il \_ \_ vincolo di \_ nome \_ è stato escluso dal trust** (&H00008000)


</dt> <dd>

Il certificato o uno dei certificati nella catena di certificati ha un'estensione per i vincoli di nome e una delle opzioni relative al nome nel certificato finale viene esclusa in modo esplicito.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM \_ Il TRUST \_ è la \_ \_ revoca offline** (&H01000000)


</dt> <dd>

Lo stato di revoca del certificato o uno dei certificati nella catena di certificati è offline o non aggiornato.

</dd> <dt>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM \_ \_Criterio della \_ \_ catena di \_ rilascio non attendibile** (&H02000000)


</dt> <dd>

Il certificato finale non ha criteri di rilascio risultanti e uno dei certificati della CA emittente ha un'estensione di vincoli dei criteri che lo richiede.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM \_ TRUST \_ è \_ una \_ catena parziale** (&H00010000)


</dt> <dd>

La catena di certificati non è competitiva.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM \_ Il \_ trust \_ CTL \_ non è \_ ora \_ valido** (&H00020000)


</dt> <dd>

Un CTL utilizzato per creare la catena non è tempo valido.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM \_ Il \_ trust \_ CTL \_ non \_ è \_ valido per la firma** (&H00040000)


</dt> <dd>

Un CTL utilizzato per creare la catena non dispone di una firma valida.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM \_ Il \_ trust \_ CTL \_ non è \_ valido \_ per l' \_ utilizzo** (&H00080000)


</dt> <dd>

Un CTL utilizzato per creare la catena non è valido per questo utilizzo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
