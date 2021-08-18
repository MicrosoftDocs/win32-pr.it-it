---
description: I flag nella tabella seguente specificano i meccanismi di protezione dell'output per Output Protection Manager (OPM).
ms.assetid: 484dfea9-301d-4b2b-b5d1-d785ebaa8c8f
title: Flag del tipo di protezione OPM (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ee61b17ee1708f8c2fc7e2f91b33d966b17f8fd2e198e2772c30ccccf837d04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101890"
---
# <a name="opm-protection-type-flags"></a>Flag del tipo di protezione OPM

I flag nella tabella seguente specificano i meccanismi di protezione dell'output per Output Protection Manager (OPM).



| Costante/valore                                                                                                                                                                                                                                                                                                     | Descrizione                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_PROTECTION_TYPE_OTHER"></span><span id="opm_protection_type_other"></span><dl> <dt>**OPM \_ PROTECTION \_ TYPE \_ OTHER**</dt> <dt>0x80000000</dt> </dl>                                                | Meccanismo di protezione sconosciuto.<br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_NONE"></span><span id="opm_protection_type_none"></span><dl> <dt>**OPM \_ TIPO \_ DI \_ PROTEZIONE NONE**</dt> <dt>0x00000000</dt> </dl>                                                   | Nessun meccanismo di protezione.<br/>                                                                                                                                                                                        |
| <span id="OPM_PROTECTION_TYPE_COPP_COMPATIBLE_HDCP"></span><span id="opm_protection_type_copp_compatible_hdcp"></span><dl> <dt>**OPM \_ PROTECTION \_ TYPE \_ COPP \_ COMPATIBLE \_ HDCP**</dt> <dt>0x00000001</dt> </dl> | High-Bandwidth Digital protezione del contenuto (HDCP). Questo flag viene usato per l'emulazione del protocollo COPP (Certified Output Protection Protocol). Per altre informazioni, vedere la sezione Osservazioni. Questo flag non è supportato per la semantica OPM.<br/> |
| <span id="OPM_PROTECTION_TYPE_ACP"></span><span id="opm_protection_type_acp"></span><dl> <dt>**OPM \_ PROTECTION \_ TYPE \_ ACP**</dt> <dt>0x00000002</dt> </dl>                                                      | Analog Copy Protection (ACP).<br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_CGMSA"></span><span id="opm_protection_type_cgmsa"></span><dl> <dt>**OPM \_ PROTECTION \_ TYPE \_ CGMSA**</dt> <dt>0x00000004</dt> </dl>                                                | Copy Generation Management System- Analog (CGMS-A).<br/>                                                                                                                                                               |
| <span id="OPM_PROTECTION_TYPE_HDCP"></span><span id="opm_protection_type_hdcp"></span><dl> <dt>**OPM \_ TIPO \_ DI \_ PROTEZIONE HDCP**</dt> <dt>0x00000008</dt> </dl>                                                   | Hdcp. Questo flag viene usato quando l'oggetto OPM ha la semantica OPM. Non è supportata per la semantica COPP.<br/>                                                                                                           |
| <span id="OPM_PROTECTION_TYPE_DPCP"></span><span id="opm_protection_type_dpcp"></span><dl> <dt>**OPM \_ TIPO \_ DI \_ PROTEZIONE DPCP**</dt> <dt>0x00000010</dt> </dl>                                                   | DisplayPort protezione del contenuto (DPCP).<br/>                                                                                                                                                                           |



## <a name="remarks"></a>Commenti

Questi flag vengono usati nei comandi OPM e nelle richieste di stato seguenti.

-   [OPM \_ SET \_ PROTECTION \_ LEVEL](opm-set-protection-level.md)
-   [OPM \_ GET \_ VIRTUAL \_ PROTECTION \_ LEVEL](opm-get-virtual-protection-level.md)
-   [OPM \_ GET \_ ACTUAL \_ PROTECTION \_ LEVEL](opm-get-actual-protection-level.md)

### <a name="hdcp"></a>Hdcp

I due flag seguenti sono definiti per HDCP.



| Valore                                         | Descrizione                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TIPO DI PROTEZIONE OPM \_ \_ \_ HDCP                   | Usare questo flag se il [**puntatore IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) è stato creato con la semantica OPM.                                                                        |
| HDCP COMPATIBILE CON COPP DI TIPO \_ \_ PROTEZIONE \_ \_ \_ OPM | Usare questo flag se il [**puntatore IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) è stato creato con la semantica COPP. Questo flag corrisponde al \_ flag HDCP COPP ProtectionType \_ in COPP. |



 

Entrambe le modalità (semantica OPM e semantica COPP) supportano le operazioni seguenti per HDCP:

-   Abilitare o disabilitare HDCP usando il [comando OPM \_ SET PROTECTION \_ \_ LEVEL.](opm-set-protection-level.md)
-   Eseguire una query per determinare se HDCP è abilitato usando la richiesta di stato [OPM \_ GET VIRTUAL PROTECTION \_ \_ \_ LEVEL](opm-get-virtual-protection-level.md) o [OPM GET ACTUAL PROTECTION \_ \_ \_ \_ LEVEL.](opm-get-actual-protection-level.md)

La semantica OPM supporta anche quanto segue:

-   Ripetitori HDCP. Un *ripetitore HDCP è* un dispositivo HDCP che può ricevere contenuto HDCP e anche crittografare e trasmettere lo stesso contenuto.
-   Revoca HDCP. Se un dispositivo HDCP revocato è collegato all'output video OPM, l'output video non trasmetterà il video. L'applicazione non deve analizzare i messaggi di rinnovo del sistema HDCP o determinare se il dispositivo di output è stato revocato. Per altre informazioni, vedere il [**comando OPM \_ SET \_ HDCP \_ SRM.**](opm-set-hdcp-srm.md)

Quando si usa la semantica COPP, [**l'interfaccia IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) non supporta i ripetitori HDCP. Inoltre, non gestisce la revoca HDCP. Al contrario, l'applicazione deve analizzare SRM per determinare se un dispositivo HDCP è stato revocato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni OPM](opm-enumerations.md)
</dt> </dl>

 

 




