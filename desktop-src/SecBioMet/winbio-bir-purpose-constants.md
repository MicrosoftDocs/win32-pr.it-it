---
title: WINBIO_BIR_PURPOSE costanti (Winbio \_ types.h)
description: Specificare lo scopo per cui il record di informazioni biometriche (BIR) è destinato o per il quale è adatto.
ms.assetid: AAFD3203-4D3D-43B5-A833-1258E1E281D3
topic_type:
- apiref
api_name:
- WINBIO_NO_PURPOSE_AVAILABLE
- WINBIO_PURPOSE_VERIFY
- WINBIO_PURPOSE_IDENTIFY
- WINBIO_PURPOSE_ENROLL
- WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION
- WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION
- WINBIO_PURPOSE_AUDIT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19cffe266cf30155be3c299b0d1b5e6a3d45f9991aa83fd66e62e705ddc4850f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080791"
---
# <a name="winbio_bir_purpose-constants"></a>Costanti DI WINBIO \_ BIR \_ PURPOSE

I flag seguenti vengono usati dal membro **Purpose** della struttura [**WINBIO \_ BIR \_ HEADER**](winbio-bir-header.md) per specificare lo scopo per cui il record di informazioni biometriche (BIR) è destinato o per il quale è adatto.



| Costante                                                                                                                                                                                                                                          | Descrizione                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_PURPOSE_AVAILABLE"></span><span id="winbio_no_purpose_available"></span><dl> <dt>**WINBIO \_ NON HA ALCUN SCOPO \_ \_ DISPONIBILE**</dt> </dl>                                         | Non è stato specificato alcuno scopo.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="WINBIO_PURPOSE_VERIFY"></span><span id="winbio_purpose_verify"></span><dl> <dt>**VERIFICA DELLO SCOPO DI WINBIO \_ \_**</dt> </dl>                                                            | Verificare l'identità di un utente.<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_IDENTIFY"></span><span id="winbio_purpose_identify"></span><dl> <dt>**IDENTIFICAZIONE DELLO SCOPO DI WINBIO \_ \_**</dt> </dl>                                                      | Identificare un utente.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="WINBIO_PURPOSE_ENROLL"></span><span id="winbio_purpose_enroll"></span><dl> <dt>**WINBIO \_ PURPOSE \_ ENROLL**</dt> </dl>                                                            | Registrare un utente.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION"></span><span id="winbio_purpose_enroll_for_verification"></span><dl> <dt>**WINBIO \_ PURPOSE \_ ENROLL \_ FOR \_ VERIFICATION**</dt> </dl>       | Acquisire un campione biometrico e determinare se l'esempio corrisponde all'identità utente specificata.<br/>                                                                                                                                                                                                                          |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION"></span><span id="winbio_purpose_enroll_for_identification"></span><dl> <dt>**WINBIO \_ PURPOSE \_ ENROLL \_ FOR \_ IDENTIFICATION**</dt> </dl> | Acquisire un campione biometrico e determinare se corrisponde a un modello biometrico esistente.<br/>                                                                                                                                                                                                                                      |
| <span id="WINBIO_PURPOSE_AUDIT"></span><span id="winbio_purpose_audit"></span><dl> <dt>**CONTROLLO DELLO SCOPO DI WINBIO \_ \_**</dt> </dl>                                                               | Informazioni aggiuntive che possono essere usate per la registrazione o la visualizzazione. Questo valore viene ignorato in caso di input da tutte le funzioni. Nell'output sarà disponibile solo se supportato dall'unità biometrica e si specifica **WINBIO \_ DATA FLAG \_ \_ RAW** nel parametro *Flags* della [**funzione WinBioCaptureSample.**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample)<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> <dt>

[**INTESTAZIONE DI WINBIO \_ \_ BIR**](winbio-bir-header.md)
</dt> </dl>

 

 





