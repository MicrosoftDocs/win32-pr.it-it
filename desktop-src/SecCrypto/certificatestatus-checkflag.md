---
description: Imposta o recupera i flag di verifica della validità per un certificato.
ms.assetid: c80c95a0-8a9b-441d-b243-7ee0552731e4
title: Proprietà CertificateStatus. CheckFlag
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
ms.openlocfilehash: 00b0c648de17f6aca931ab3f3417d9ecb53ac558
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326038"
---
# <a name="certificatestatuscheckflag-property"></a>Proprietà CertificateStatus. CheckFlag

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **CheckFlag** imposta o recupera i flag di verifica della validità per un certificato.

## <a name="syntax"></a>Sintassi


```VB
CertificateStatus.CheckFlag As CAPICOM_CHECK_FLAG
```



## <a name="property-value"></a>Valore proprietà

Valore dell'enumerazione del [**\_ \_ flag di controllo CAPICOM**](capicom-check-flag.md) che descrive i controlli di validità per il certificato. Il valore predefinito è **CApicot \_ controlla \_ \_ tutto online**.

**CAPICOM 2.0.0.3/2.0.0.2/2.0.0.1:** Il valore predefinito è [**CAPICOM verificare la \_ \_ \_ validità della firma**](capicom-check-flag.md), la [**\_ \_ \_ validità del controllo**](capicom-check-flag.md)capicol, il controllo della [**\_ \_ \_ radice attendibile**](capicom-check-flag.md)e il controllo capicot sulla [**\_ \_ \_ catena completa**](capicom-check-flag.md).

**Capicom 2,0 e versioni precedenti:** Il valore predefinito è [**CAPICOM controlla la \_ \_ \_ validità della firma**](capicom-check-flag.md), la [**\_ \_ \_ validità del controllo capicol**](capicom-check-flag.md)e il controllo della [**\_ \_ \_ radice attendibile**](capicom-check-flag.md).

Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                                          | Significato                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CHECK_BASIC_CONSTRAINTS"></span><span id="capicom_check_basic_constraints"></span><dl> <dt>**i vincoli di \_ base del controllo CAPICOM \_ \_**</dt> </dl>                          | Verifica i vincoli di base. Introdotta in capicol 2,0.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_CHECK_COMPLETE_CHAIN"></span><span id="capicom_check_complete_chain"></span><dl> <dt>**sequenza di controllo di capicol \_ \_ completa \_**</dt> </dl>                                   | Controlla la catena completa. Introdotta in capicol 2,0.<br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_CHECK_NAME_CONSTRAINTS"></span><span id="capicom_check_name_constraints"></span><dl> <dt>**vincoli del nome del \_ controllo CAPICOM \_ \_**</dt> </dl>                             | Verifica i vincoli del nome. Introdotta in capicol 2,0.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <span id="CAPICOM_CHECK_NESTED_VALIDITY_PERIOD"></span><span id="capicom_check_nested_validity_period"></span><dl> <dt>**\_ \_ periodo di validità nidificato del controllo \_ CAPICOM \_**</dt> </dl>          | Verifica la validità nidificata. Introdotta in capicol 2,0.<br/>                                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_CHECK_NONE"></span><span id="capicom_check_none"></span><dl> <dt>**\_controllo CAPICOM \_ None**</dt> </dl>                                                                  | Non è stato eseguito alcun controllo di validità.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| <span id="CAPICOM_CHECK_OFFLINE_ALL"></span><span id="capicom_check_offline_all"></span><dl> <dt>**controllo CAPICOM non \_ in \_ linea \_**</dt> </dl>                                            | Verifica tutte le modalità offline. I controlli di revoca vengono eseguiti su tutti i certificati nella catena, ad eccezione del certificato radice. Introdotta in capicol 2,0.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_CHECK_ONLINE_ALL"></span><span id="capicom_check_online_all"></span><dl> <dt>**capicot \_ controlla \_ \_ tutto online**</dt> </dl>                                               | Controlla tutti online. I controlli di revoca vengono eseguiti su tutti i certificati nella catena, ad eccezione del certificato radice. Introdotta in capicol 2,0.<br/>                                                                                                                                                                                                                                         |
| <span id="CAPICOM_CHECK_OFFLINE_REVOCATION_STATUS"></span><span id="capicom_check_offline_revocation_status"></span><dl> <dt>**\_controlla \_ stato di revoca offline \_ \_ per CAPICOM**</dt> </dl> | Controlla lo stato di revoca di tutti i certificati nella catena utilizzando solo i CRL offline.<br/>                                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_CHECK_ONLINE_REVOCATION_STATUS"></span><span id="capicom_check_online_revocation_status"></span><dl> <dt>**\_verifica \_ stato di revoca online \_ \_ di CAPICOM**</dt> </dl>    | Controlla lo stato di revoca di tutti i certificati nella catena utilizzando i CRL disponibili online. I CRL vengono scaricati usando l'estensione CDP nel certificato.<br/> Se il CRL è stato scaricato e non è scaduto, CAPICOM lo usa e non passa alla rete.<br/> Se un CRL non è stato scaricato o non è aggiornato, CAPICOM passa online per tentare di scaricare il CRL.<br/> |
| <span id="CAPICOM_CHECK_SIGNATURE_VALIDITY"></span><span id="capicom_check_signature_validity"></span><dl> <dt>**validità della firma del \_ controllo CAPICOM \_ \_**</dt> </dl>                       | Verifica se sono presenti firme valide per tutti i certificati della catena.<br/>                                                                                                                                                                                                                                                                                                                           |
| <span id="CAPICOM_CHECK_TIME_VALIDITY"></span><span id="capicom_check_time_validity"></span><dl> <dt>**\_validità controllo CApicol \_ \_**</dt> </dl>                                      | Verifica la validità dell'ora di tutti i certificati nella catena.<br/>                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_CHECK_TRUSTED_ROOT"></span><span id="capicom_check_trusted_root"></span><dl> <dt>**capicot \_ controlla \_ radice attendibile \_**</dt> </dl>                                         | Verifica la presenza di una radice attendibile della catena di certificati.<br/>                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
