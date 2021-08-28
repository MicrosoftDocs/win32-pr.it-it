---
title: Costanti generali (Winbio \_ types.h)
description: Specificare la lunghezza massima del SID, gli handle, gli ID, la lunghezza massima della stringa e le dimensioni massime del buffer di campionamento.
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
ms.openlocfilehash: 686e94c936855d3b5466071fba7d8b629a492579de11a53a62d8b23345707c53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119740450"
---
# <a name="general-constants-winbio_typesh"></a>Costanti generali (Winbio \_ types.h)

Le costanti seguenti vengono usate in tutto il Windows Biometric Framework.



| Costante/valore                                                                                                                                                                                                                                                                   | Descrizione                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| <span id="SECURITY_MAX_SID_SIZE"></span><span id="security_max_sid_size"></span><dl> <dt>**DIMENSIONI \_ MASSIME \_ SID \_ DI SICUREZZA**</dt> </dl>                                                                                          | Lunghezza massima di un valore dell'identificatore di sicurezza (SID). Attualmente è 68.<br/>   |
| <span id="WINBIO_UNIT_ID"></span><span id="winbio_unit_id"></span><dl> <dt>**ID UNITÀ WINBIO \_ \_**</dt> </dl>                                                                                                                | Numero ID di un'unità biometrica.<br/>                                                   |
| <span id="WINBIO_SESSION_HANDLE"></span><span id="winbio_session_handle"></span><dl> <dt>**HANDLE DI SESSIONE WINBIO \_ \_**</dt> </dl>                                                                                           | Oggetto non firmato long integer contenente l'handle per una sessione biometrica aperta.<br/> |
| <span id="WINBIO_FRAMEWORK_HANDLE"></span><span id="winbio_framework_handle"></span><dl> <dt>**HANDLE DI \_ WINBIO FRAMEWORK \_**</dt> </dl>                                                                                     | Oggetto senza segno long integer che contiene l'handle per una sessione del framework aperta.<br/> |
| <span id="WINBIO_UUID"></span><span id="winbio_uuid"></span><dl> <dt>**WINBIO \_ UUID**</dt> </dl>                                                                                                                          | Un valore GUID.<br/>                                                                          |
| <span id="WINBIO_STRING"></span><span id="winbio_string"></span><dl> <dt>**STRINGA \_ WINBIO**</dt> </dl>                                                                                                                    | Matrice di byte contenente una stringa Unicode con terminazione Null.<br/>                     |
| <span id="WINBIO_MAX_STRING_LEN_"></span><span id="winbio_max_string_len_"></span><dl> <dt>**WINBIO \_ NUMERO \_ MASSIMO \_ DI STRINGHE**</dt> </dl>                                                                                       | Lunghezza massima di un **valore WINBIO \_ STRING.** Attualmente è 256.<br/>         |
| <span id="WINBIO_MAX_SAMPLE_BUFFER_SIZE"></span><span id="winbio_max_sample_buffer_size"></span><dl> <dt>**WINBIO \_ DIMENSIONI \_ MASSIME \_ BUFFER \_ DI**</dt> <dt>ESEMPIO 0x7FFFFFFF</dt> </dl> | Numero massimo di byte in un singolo data capture biometrico.<br/>                  |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





