---
title: WINBIO_OPERATION_TYPE costanti (Winbio \_ types.h)
description: Specificare il tipo di operazione asincrona eseguita.
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
ms.openlocfilehash: b39dd6e2656ad73623df9d6a92d514e90371bc3761563e5f24c41211680c2455
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909950"
---
# <a name="winbio_operation_type-constants"></a>Costanti WINBIO \_ OPERATION \_ TYPE

Le costanti seguenti possono essere restituite da Windows Biometric Framework in UN RISULTATO [**\_ ASINCRONO \_ WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) per specificare il tipo di operazione asincrona eseguita.

<dl> <dt>

<span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**OPERAZIONE WINBIO \_ \_ NONE**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Non è stata identificata alcuna operazione.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**OPERAZIONE WINBIO \_ \_ APERTA**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



È stata aperta una sessione biometrica. Per altre informazioni, [**vedere WinBioAsyncOpenSession.**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**CHIUSURA DELL'OPERAZIONE WINBIO \_ \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Una sessione biometrica è stata chiusa. Per altre informazioni, vedere [**WinBioCloseSession.**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**VERIFICA DELL'OPERAZIONE WINBIO \_ \_**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



È stato verificato un campione biometrico rispetto a un'identità utente. Per altre informazioni, vedere [**WinBioVerify.**](/windows/desktop/api/Winbio/nf-winbio-winbioverify)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**IDENTIFICAZIONE DELL'OPERAZIONE WINBIO \_ \_**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Un campione biometrico è stato acquisito e confrontato con un modello esistente. Per altre informazioni, vedere [**WinBioIdentify.**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**INDIVIDUAZIONE DEL SENSORE \_ NELL'OPERAZIONE WINBIO \_ \_**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



È stato recuperato il numero ID di un'unità biometrica. Per altre informazioni, vedere [**WinBioLocateSensor.**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**INIZIO REGISTRAZIONE OPERAZIONE WINBIO \_ \_ \_**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



È stata avviata una sequenza di registrazione biometrica. Per altre informazioni, vedere [**WinBioEnrollBegin.**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**ACQUISIZIONE DI REGISTRAZIONE \_ DELL'OPERAZIONE WINBIO \_ \_**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Un campione biometrico è stato acquisito e aggiunto al modello. Per altre informazioni, vedere [**WinBioEnrollCapture.**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**COMMIT DI REGISTRAZIONE \_ DELL'OPERAZIONE WINBIO \_ \_**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



È stato finalizzato un modello biometrico in sospeso. Per altre informazioni, vedere [**WinBioEnrollCommit.**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**OPERAZIONE WINBIO \_ \_ ENROLL \_ DISCARD**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Un modello biometrico in sospeso è stato eliminato. Per altre informazioni, vedere [**WinBioEnrollDiscard.**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**REGISTRAZIONI DI \_ ENUMERAZIONE DELLE OPERAZIONI WINBIO \_ \_**
</dt> <dd> <dl> <dt>

10
</dt> <dt>



Sono stati enumerati i fattori secondari per un determinato modello. Per altre informazioni, vedere [**WinBioEnumEnrollments.**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**MODELLO DI ELIMINAZIONE DELL'OPERAZIONE WINBIO \_ \_ \_**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Un modello biometrico è stato eliminato dall'archivio. Per altre informazioni, vedere [**WinBioDeleteTemplate.**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**ESEMPIO DI ACQUISIZIONE \_ DI OPERAZIONI WINBIO \_ \_**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



È stato acquisito un campione biometrico. Per altre informazioni, vedere [**WinBioCaptureSample.**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**PROPRIETÀ GET \_ DELL'OPERAZIONE \_ \_ WINBIO**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



È stata recuperata una sessione biometrica, un'unità o una proprietà modello. Per altre informazioni, vedere [**WinBioGetProperty.**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**PROPRIETÀ \_ SET DELL'OPERAZIONE \_ WINBIO \_**
</dt> <dd> <dl> <dt>

14
</dt> <dt>



È stata impostata una sessione biometrica, un'unità, un modello o una proprietà dell'account. Per altre informazioni, vedere [**WinBioSetProperty.**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**EVENTO GET \_ DELL'OPERAZIONE WINBIO \_ \_**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



Non usato.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**UNITÀ DI BLOCCO \_ DELL'OPERAZIONE WINBIO \_ \_**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Un'unità biometrica è stata bloccata per l'uso esclusivo da parte di una sessione. Per altre informazioni, vedere [**WinBioLockUnit.**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**UNITÀ DI \_ SBLOCCO DELL'OPERAZIONE WINBIO \_ \_**
</dt> <dd> <dl> <dt>

17
</dt> <dt>



È stato rilasciato il blocco di sessione su un'unità biometrica. Per altre informazioni, vedere [**WinBioUnlockUnit.**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**UNITÀ DI CONTROLLO DELLE OPERAZIONI WINBIO \_ \_ \_**
</dt> <dd> <dl> <dt>

18
</dt> <dt>



Le operazioni definite dal fornitore sono state eseguite su un'unità di controllo. Per altre informazioni, vedere [**WinBioControlUnit.**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**UNITÀ DI CONTROLLO \_ DELL'OPERAZIONE WINBIO \_ \_ CON \_ PRIVILEGI**
</dt> <dd> <dl> <dt>

19
</dt> <dt>



Le operazioni definite dal fornitore con privilegi sono state eseguite su un'unità di controllo. Per altre informazioni, vedere [**WinBioControlUnitPrivileged.**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**WINBIO \_ OPERATION \_ OPEN \_ FRAMEWORK**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



È stato aperto un handle per il framework biometrico.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**WINBIO \_ OPERATION \_ CLOSE \_ FRAMEWORK**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Un handle per il framework biometrico è stato chiuso. Per altre informazioni, vedere [**WinBioCloseFramework.**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**PROVIDER DI SERVIZI \_ \_ DI ENUMERAZIONE DELLE OPERAZIONI \_ WINBIO \_**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



I provider di servizi biometrici installati sono stati enumerati. Per altre informazioni, vedere [**WinBioEnumServiceProviders.**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**UNITÀ BIOMETRICHE \_ \_ DI ENUMERAZIONE DELL'OPERAZIONE \_ WINBIO \_**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



Le unità biometriche collegate sono state enumerate. Per altre informazioni, vedere [**WinBioAsyncEnumBiometricUnits.**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**DATABASE DI ENUMERAZIONE DELLE OPERAZIONI WINBIO \_ \_ \_**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



I database registrati sono stati enumerati. Per altre informazioni, vedere [**WinBioEnumDatabases.**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**ARRIVO UNITÀ OPERATIVA WINBIO \_ \_ \_**
</dt> <dd> <dl> <dt>

25
</dt> <dt>



È stata creata un'unità biometrica. Per altre informazioni, vedere [**WinBioAsyncMonitorFrameworkChanges.**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**RIMOZIONE DELL'UNITÀ \_ OPERATIVA WINBIO \_ \_**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



È stata eliminata un'unità biometrica. Per altre informazioni, vedere [**WinBioAsyncMonitorFrameworkChanges.**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**ID OPERAZIONE WINBIO \_ \_ E TICKET DI \_ \_ \_ RILASCIO**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



Riservato. Questo valore è supportato a partire da Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**VERIFICA \_ DELL'OPERAZIONE WINBIO E TICKET DI \_ \_ \_ \_ RILASCIO**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Riservato. Questo valore è supportato a partire da Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**PRESENZA DI MONITORAGGIO OPERAZIONI WINBIO \_ \_ \_**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



Il meccanismo di riconoscimento facciale o monitoraggio dell'iris è stato attivato. Per altre informazioni, vedere [**WinBioMonitorPresence.**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence) Questo valore è supportato a partire da Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**SELEZIONE DELLA REGISTRAZIONE \_ DELL'OPERAZIONE WINBIO \_ \_**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Un utente di un gruppo di individui rappresentati da dati nel buffer di esempio è stato specificato come utente singolo da registrare. Per altre informazioni, vedere [**WinBioEnrollSelect.**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect) Questo valore è supportato a partire da Windows 10.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                                                                                               |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (includere Winbio.h per le applicazioni client o Winbio \_ adapters.h per gli adapter)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





