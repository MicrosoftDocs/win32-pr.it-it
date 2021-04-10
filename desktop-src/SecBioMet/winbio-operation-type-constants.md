---
title: Costanti WINBIO_OPERATION_TYPE (tipi WinBio \_ . h)
description: Consente di specificare il tipo di operazione asincrona eseguita.
ms.assetid: D4ECEF91-BEC7-4A42-8808-F09F5C141180
topic_type:
- apiref
api_name:
- WINBIO_OPERATION_NONE
- WINBIO_OPERATION_OPEN
- WINBIO_OPERATION_CLOSE
- WINBIO_OPERATION_VERIFY
- WINBIO_OPERATION_IDENTIFY
- WINBIO_OPERATION_LOCATE_SENSOR
- WINBIO_OPERATION_ENROLL_BEGIN
- WINBIO_OPERATION_ENROLL_CAPTURE
- WINBIO_OPERATION_ENROLL_COMMIT
- WINBIO_OPERATION_ENROLL_DISCARD
- WINBIO_OPERATION_ENUM_ENROLLMENTS
- WINBIO_OPERATION_DELETE_TEMPLATE
- WINBIO_OPERATION_CAPTURE_SAMPLE
- WINBIO_OPERATION_GET_PROPERTY
- WINBIO_OPERATION_SET_PROPERTY
- WINBIO_OPERATION_GET_EVENT
- WINBIO_OPERATION_LOCK_UNIT
- WINBIO_OPERATION_UNLOCK_UNIT
- WINBIO_OPERATION_CONTROL_UNIT
- WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED
- WINBIO_OPERATION_OPEN_FRAMEWORK
- WINBIO_OPERATION_CLOSE_FRAMEWORK
- WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS
- WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS
- WINBIO_OPERATION_ENUM_DATABASES
- WINBIO_OPERATION_UNIT_ARRIVAL
- WINBIO_OPERATION_UNIT_REMOVAL
- WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_MONITOR_PRESENCE
- WINBIO_OPERATION_ENROLL_SELECT
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83f32b9f98a24d0ed4d9995bf5fcb7eaa3a2b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121647"
---
# <a name="winbio_operation_type-constants"></a>Costanti del tipo di \_ operazione WINBIO \_

Le costanti seguenti possono essere restituite dal Windows Biometric Framework in un [**\_ \_ risultato asincrono WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) per specificare il tipo di operazione asincrona eseguita.

<dl> <dt>

<span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**\_operazione WINBIO \_ None**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Nessuna operazione identificata.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**\_operazione WINBIO \_ aperta**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



È stata aperta una sessione biometrica. Per ulteriori informazioni, vedere [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**\_chiusura operazione \_ WINBIO**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Una sessione biometrica è stata chiusa. Per ulteriori informazioni, vedere [**WinBioCloseSession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**\_Verifica operazione \_ WINBIO**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



È stato verificato un campione biometrico rispetto a un'identità utente. Per ulteriori informazioni, vedere [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**\_Identificazione operazione \_ WINBIO**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Un campione biometrico è stato acquisito e confrontato con un modello esistente. Per ulteriori informazioni, vedere [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**\_individuazione del \_ \_ sensore nell'operazione WINBIO**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Il numero di ID di un'unità biometrica è stato recuperato. Per ulteriori informazioni, vedere [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**\_ \_ inizio registrazione operazione \_ WINBIO**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



È stata avviata una sequenza di registrazione biometrica. Per ulteriori informazioni, vedere [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**\_ \_ acquisizione registrazione operazione \_ WINBIO**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Un campione biometrico è stato acquisito e aggiunto al modello. Per ulteriori informazioni, vedere [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**\_ \_ commit registrazione operazione \_ WINBIO**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



Un modello biometrico in sospeso è stato finalizzato. Per ulteriori informazioni, vedere [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**\_eliminazione della \_ registrazione dell'operazione WINBIO \_**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Un modello biometrico in sospeso è stato rimosso. Per ulteriori informazioni, vedere [**WinBioEnrollDiscard**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**\_registrazioni dell' \_ enumerazione dell'operazione WINBIO \_**
</dt> <dd> <dl> <dt>

10
</dt> <dt>



Sono stati enumerati i sottofattori per un determinato modello. Per ulteriori informazioni, vedere [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**\_modello operazione di \_ eliminazione \_ WINBIO**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Un modello biometrico è stato eliminato dall'archivio. Per ulteriori informazioni, vedere [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**\_esempio di \_ acquisizione dell'operazione WINBIO \_**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



È stato acquisito un campione biometrico. Per ulteriori informazioni, vedere [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**\_ \_ Proprietà Get dell'operazione WINBIO \_**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



È stata recuperata una sessione biometrica, un'unità o una proprietà di modello. Per ulteriori informazioni, vedere [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**\_proprietà del \_ set di operazioni WINBIO \_**
</dt> <dd> <dl> <dt>

14
</dt> <dt>



È stata impostata una sessione biometrica, un'unità, un modello o una proprietà dell'account. Per ulteriori informazioni, vedere [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**\_ \_ evento Get operazione \_ WINBIO**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



Non usato.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**\_unità di \_ blocco \_ operazione WINBIO**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Un'unità biometrica è stata bloccata per l'uso esclusivo da una sessione. Per ulteriori informazioni, vedere [**WinBioLockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**\_unità di \_ sblocco \_ operazione WINBIO**
</dt> <dd> <dl> <dt>

17
</dt> <dt>



Il blocco della sessione su un'unità biometrica è stato rilasciato. Per ulteriori informazioni, vedere [**WinBioUnlockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**\_unità di \_ controllo dell'operazione WINBIO \_**
</dt> <dd> <dl> <dt>

18
</dt> <dt>



Le operazioni definite dal fornitore sono state eseguite su un'unità di controllo. Per ulteriori informazioni, vedere [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**unità di controllo dell'operazione WINBIO con \_ \_ \_ \_ privilegi**
</dt> <dd> <dl> <dt>

19
</dt> <dt>



Le operazioni definite dal fornitore con privilegi sono state eseguite su un'unità di controllo. Per ulteriori informazioni, vedere [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**WINBIO \_ operazione di \_ apertura \_ Framework**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



È stato aperto un handle per il Framework biometrico.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**\_Framework di \_ chiusura dell'operazione WINBIO \_**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Un handle per il Framework biometrico è stato chiuso. Per ulteriori informazioni, vedere [**WinBioCloseFramework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**\_provider di \_ \_ servizi enum operazione WINBIO \_**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



Sono stati enumerati i provider di servizi biometrici installati. Per ulteriori informazioni, vedere [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**\_ \_ \_ unità biometriche enum operazione WINBIO \_**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



Sono state enumerate le unità biometriche collegate. Per ulteriori informazioni, vedere [**WinBioAsyncEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**\_ \_ database enum operazione \_ WINBIO**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



I database registrati sono stati enumerati. Per ulteriori informazioni, vedere [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**\_ \_ arrivo unità operazione \_ WINBIO**
</dt> <dd> <dl> <dt>

25
</dt> <dt>



È stata creata un'unità biometrica. Per ulteriori informazioni, vedere [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**\_ \_ rimozione unità operazione \_ WINBIO**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



Un'unità biometrica è stata eliminata. Per ulteriori informazioni, vedere [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**\_ \_ identificazione \_ e rilascio del \_ \_ ticket per l'operazione WINBIO**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



Riservato. Questo valore è supportato a partire da Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**\_Verifica dell'operazione WINBIO \_ \_ e \_ \_ ticket versione**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Riservato. Questo valore è supportato a partire da Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**\_presenza di \_ monitoraggio \_ operazione WINBIO**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



Il meccanismo di monitoraggio del riconoscimento facciale o Iris è stato attivato. Per ulteriori informazioni, vedere [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence). Questo valore è supportato a partire da Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**\_ \_ selezione registrazione operazione \_ WINBIO**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Un individuo di un gruppo di singoli individui rappresentati dai dati nel buffer di esempio è stato specificato come singolo da registrare. Per ulteriori informazioni, vedere [**WinBioEnrollSelect**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect). Questo valore è supportato a partire da Windows 10.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                                                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





