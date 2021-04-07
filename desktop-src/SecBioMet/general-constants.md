---
title: Costanti generali (tipi WinBio \_ . h)
description: Specificare lunghezza massima SID, handle, ID, lunghezza massima della stringa e dimensioni massime del buffer di esempio.
ms.assetid: 62e87bd8-a708-4d00-aaa8-9cac8e3736a7
topic_type:
- apiref
api_name:
- SECURITY_MAX_SID_SIZE
- WINBIO_UNIT_ID
- WINBIO_SESSION_HANDLE
- WINBIO_FRAMEWORK_HANDLE
- WINBIO_UUID
- WINBIO_STRING
- WINBIO_MAX_STRING_LEN
- WINBIO_MAX_SAMPLE_BUFFER_SIZE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e35aa4c2cc676935cfb80fdec8729daf64d5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964217"
---
# <a name="general-constants-winbio_typesh"></a>Costanti generali (tipi WinBio \_ . h)

In Windows Biometric Framework vengono utilizzate le costanti seguenti.



| Costante/valore                                                                                                                                                                                                                                                                   | Descrizione                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| <span id="SECURITY_MAX_SID_SIZE"></span><span id="security_max_sid_size"></span><dl> <dt>**\_dimensioni massime \_ SID sicurezza \_**</dt> </dl>                                                                                          | Lunghezza massima del valore di un ID di sicurezza (SID). Attualmente è 68.<br/>   |
| <span id="WINBIO_UNIT_ID"></span><span id="winbio_unit_id"></span><dl> <dt>**\_ID unità \_ WINBIO**</dt> </dl>                                                                                                                | ID del numero di unità biometriche.<br/>                                                   |
| <span id="WINBIO_SESSION_HANDLE"></span><span id="winbio_session_handle"></span><dl> <dt>**\_handle della sessione WINBIO \_**</dt> </dl>                                                                                           | Un long integer senza segno contenente l'handle per una sessione biometrica aperta.<br/> |
| <span id="WINBIO_FRAMEWORK_HANDLE"></span><span id="winbio_framework_handle"></span><dl> <dt>**\_handle WINBIO Framework \_**</dt> </dl>                                                                                     | Valore long integer senza segno contenente l'handle per una sessione di Framework aperta.<br/> |
| <span id="WINBIO_UUID"></span><span id="winbio_uuid"></span><dl> <dt>**\_UUID WINBIO**</dt> </dl>                                                                                                                          | Un valore GUID.<br/>                                                                          |
| <span id="WINBIO_STRING"></span><span id="winbio_string"></span><dl> <dt>**\_stringa WINBIO**</dt> </dl>                                                                                                                    | Matrice di byte che contiene una stringa Unicode con terminazione null.<br/>                     |
| <span id="WINBIO_MAX_STRING_LEN_"></span><span id="winbio_max_string_len_"></span><dl> <dt>**WINBIO \_ \_ \_ lunghezza massima stringa**</dt> </dl>                                                                                       | Lunghezza massima di un valore **\_ stringa WINBIO** . Attualmente è 256.<br/>         |
| <span id="WINBIO_MAX_SAMPLE_BUFFER_SIZE"></span><span id="winbio_max_sample_buffer_size"></span><dl> <dt>**WINBIO \_ \_ \_ \_ Dimensioni massime del buffer di esempio**</dt> <dt>0x7FFFFFFF</dt> </dl> | Il numero massimo di byte in una singola acquisizione di dati biometrici.<br/>                  |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





