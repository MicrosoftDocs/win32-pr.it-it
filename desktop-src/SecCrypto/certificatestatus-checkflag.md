---
description: Imposta o recupera i flag di controllo di validità per un certificato.
ms.assetid: c80c95a0-8a9b-441d-b243-7ee0552731e4
title: CertificateStatus.CheckFlag - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CheckFlag
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1c47d7f1c59ecd629db1d6fc735f61b8d1fe59c864ffa8a5a9f013c86bd30faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877451"
---
# <a name="certificatestatuscheckflag-property"></a>CertificateStatus.CheckFlag - proprietà

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **proprietà CheckFlag** imposta o recupera i flag di controllo di validità per un certificato.

## <a name="syntax"></a>Sintassi


```VB
CertificateStatus.CheckFlag As CAPICOM_CHECK_FLAG
```



## <a name="property-value"></a>Valore proprietà

Valore [**dell'enumerazione CAPICOM \_ CHECK \_ FLAG**](capicom-check-flag.md) che descrive i controlli di validità per il certificato. Il valore predefinito è **CAPICOM \_ CHECK ONLINE \_ \_ ALL.**

**CAPICOM 2.0.0.3/2.0.0.2/2.0.0.1:** Il valore predefinito è [**CAPICOM \_ CHECK SIGNATURE \_ \_ VALIDITY,**](capicom-check-flag.md) [**CAPICOM CHECK TIME \_ \_ \_ VALIDITY,**](capicom-check-flag.md) [**CAPICOM CHECK TRUSTED \_ \_ \_ ROOT**](capicom-check-flag.md)e [**CAPICOM CHECK COMPLETE \_ \_ \_ CHAIN.**](capicom-check-flag.md)

**CAPICOM 2.0 e versioni precedenti:** Il valore predefinito è [**CAPICOM \_ CHECK SIGNATURE \_ \_ VALIDITY,**](capicom-check-flag.md) [**CAPICOM CHECK TIME \_ \_ \_ VALIDITY**](capicom-check-flag.md)e [**CAPICOM CHECK TRUSTED \_ \_ \_ ROOT.**](capicom-check-flag.md)

Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                                          | Significato                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CHECK_BASIC_CONSTRAINTS"></span><span id="capicom_check_basic_constraints"></span><dl> <dt>**VINCOLI DI \_ BASE DI CAPICOM CHECK \_ \_**</dt> </dl>                          | Controlla i vincoli di base. Introduzione a CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_CHECK_COMPLETE_CHAIN"></span><span id="capicom_check_complete_chain"></span><dl> <dt>**CATENA DI \_ COMPLETAMENTO DEL CONTROLLO \_ \_ CAPICOM**</dt> </dl>                                   | Controlla la catena completa. Introduzione a CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_CHECK_NAME_CONSTRAINTS"></span><span id="capicom_check_name_constraints"></span><dl> <dt>**VINCOLI DEI \_ NOMI CHECK \_ \_ CAPICOM**</dt> </dl>                             | Controlla i vincoli di nome. Introduzione a CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <span id="CAPICOM_CHECK_NESTED_VALIDITY_PERIOD"></span><span id="capicom_check_nested_validity_period"></span><dl> <dt>**VERIFICA CAPICOM \_ \_ PERIODO DI \_ VALIDITÀ \_ ANNIDATA**</dt> </dl>          | Controlla la validità annidata. Introduzione a CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_CHECK_NONE"></span><span id="capicom_check_none"></span><dl> <dt>**CAPICOM \_ CHECK \_ NONE**</dt> </dl>                                                                  | Non viene eseguito alcun controllo di validità.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| <span id="CAPICOM_CHECK_OFFLINE_ALL"></span><span id="capicom_check_offline_all"></span><dl> <dt>**CAPICOM \_ CHECK \_ OFFLINE \_ ALL**</dt> </dl>                                            | Controlla tutti offline. I controlli di revoca vengono eseguiti su tutti i certificati nella catena, ad eccezione del certificato radice. Introduzione a CAPICOM 2.0.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_CHECK_ONLINE_ALL"></span><span id="capicom_check_online_all"></span><dl> <dt>**CAPICOM \_ CHECK \_ ONLINE \_ ALL**</dt> </dl>                                               | Controlla tutti online. I controlli di revoca vengono eseguiti su tutti i certificati nella catena, ad eccezione del certificato radice. Introduzione a CAPICOM 2.0.<br/>                                                                                                                                                                                                                                         |
| <span id="CAPICOM_CHECK_OFFLINE_REVOCATION_STATUS"></span><span id="capicom_check_offline_revocation_status"></span><dl> <dt>**VERIFICA DELLO \_ STATO \_ DI REVOCA \_ OFFLINE \_ DI CAPICOM**</dt> </dl> | Controlla lo stato di revoca di tutti i certificati nella catena usando solo CRL offline.<br/>                                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_CHECK_ONLINE_REVOCATION_STATUS"></span><span id="capicom_check_online_revocation_status"></span><dl> <dt>**VERIFICA DELLO \_ STATO DI REVOCA ONLINE \_ \_ DI \_ CAPICOM**</dt> </dl>    | Controlla lo stato di revoca di tutti i certificati nella catena usando gli elenchi di revoche di certificati disponibili online. I CRL vengono scaricati usando l'estensione CDP nel certificato.<br/> Se il CRL è stato scaricato e non è scaduto, CAPICOM lo usa e non passa online.<br/> Se un CRL non è stato scaricato o non è aggiornato, CAPICOM passa online per tentare di scaricare il CRL.<br/> |
| <span id="CAPICOM_CHECK_SIGNATURE_VALIDITY"></span><span id="capicom_check_signature_validity"></span><dl> <dt>**VERIFICA \_ DELLA \_ \_ VALIDITÀ DELLA FIRMA CAPICOM**</dt> </dl>                       | Verifica la presenza di firme valide in tutti i certificati nella catena.<br/>                                                                                                                                                                                                                                                                                                                           |
| <span id="CAPICOM_CHECK_TIME_VALIDITY"></span><span id="capicom_check_time_validity"></span><dl> <dt>**VALIDITÀ \_ DEL TEMPO DI CONTROLLO \_ \_ CAPICOM**</dt> </dl>                                      | Controlla la validità temporale di tutti i certificati nella catena.<br/>                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_CHECK_TRUSTED_ROOT"></span><span id="capicom_check_trusted_root"></span><dl> <dt>**VERIFICA RADICE \_ \_ ATTENDIBILE CAPICOM \_**</dt> </dl>                                         | Verifica la presenza di una radice attendibile della catena di certificati.<br/>                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
