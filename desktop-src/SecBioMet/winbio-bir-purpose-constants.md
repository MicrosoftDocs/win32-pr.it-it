---
title: Costanti WINBIO_BIR_PURPOSE (tipi WinBio \_ . h)
description: Specificare lo scopo a cui è destinato il record di informazioni biometriche (BIR) o per cui è adatto.
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
ms.openlocfilehash: f5a662a5ae045d3afc631f93cdf296508dabccf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964276"
---
# <a name="winbio_bir_purpose-constants"></a>Costanti WINBIO per \_ \_ finalità Bir

I flag seguenti vengono usati dal membro **scopo** della struttura dell' [**\_ \_ intestazione WINBIO bir**](winbio-bir-header.md) per specificare lo scopo per cui è previsto il record di informazioni biometriche (Bir) o per cui è adatto.



| Costante                                                                                                                                                                                                                                          | Descrizione                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_PURPOSE_AVAILABLE"></span><span id="winbio_no_purpose_available"></span><dl> <dt>**WINBIO \_ senza \_ scopo \_ disponibile**</dt> </dl>                                         | Nessun scopo specificato.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="WINBIO_PURPOSE_VERIFY"></span><span id="winbio_purpose_verify"></span><dl> <dt>**\_Verifica finalità \_ WINBIO**</dt> </dl>                                                            | Verificare l'identità di un utente.<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_IDENTIFY"></span><span id="winbio_purpose_identify"></span><dl> <dt>**\_Identificazione scopo \_ WINBIO**</dt> </dl>                                                      | Identificare un utente.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="WINBIO_PURPOSE_ENROLL"></span><span id="winbio_purpose_enroll"></span><dl> <dt>**\_registrazione scopo \_ WINBIO**</dt> </dl>                                                            | Registrare un utente.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION"></span><span id="winbio_purpose_enroll_for_verification"></span><dl> <dt>**\_registrazione scopo \_ WINBIO \_ per la \_ Verifica**</dt> </dl>       | Acquisire un campione biometrico e determinare se l'esempio corrisponde all'identità utente specificata.<br/>                                                                                                                                                                                                                          |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION"></span><span id="winbio_purpose_enroll_for_identification"></span><dl> <dt>**\_registrazione scopo \_ WINBIO \_ per l' \_ Identificazione**</dt> </dl> | Acquisire un campione biometrico e determinare se corrisponde a un modello biometrico esistente.<br/>                                                                                                                                                                                                                                      |
| <span id="WINBIO_PURPOSE_AUDIT"></span><span id="winbio_purpose_audit"></span><dl> <dt>**\_controllo scopo \_ WINBIO**</dt> </dl>                                                               | Informazioni aggiuntive che possono essere usate per la registrazione o per la visualizzazione. Questo valore viene ignorato nell'input da tutte le funzioni. Nell'output sarà disponibile solo se supportata dall'unità biometrica e si specifica il flag di **\_ dati WINBIO \_ \_ RAW** nel parametro *Flags* della funzione [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample) .<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> <dt>

[**\_intestazione WINBIO bir \_**](winbio-bir-header.md)
</dt> </dl>

 

 





