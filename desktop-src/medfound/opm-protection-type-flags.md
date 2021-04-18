---
description: I flag nella tabella seguente specificano i meccanismi di protezione dell'output per l'output Protection Manager (OPM).
ms.assetid: 484dfea9-301d-4b2b-b5d1-d785ebaa8c8f
title: Flag del tipo di protezione OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc8b30a18f5c7bf68fb01775751aa56e1e619f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309051"
---
# <a name="opm-protection-type-flags"></a>Flag del tipo di protezione OPM

I flag nella tabella seguente specificano i meccanismi di protezione dell'output per l'output Protection Manager (OPM).



| Costante/valore                                                                                                                                                                                                                                                                                                     | Descrizione                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_PROTECTION_TYPE_OTHER"></span><span id="opm_protection_type_other"></span><dl> <dt>**OPM \_ Tipo di protezione \_ \_ altri**</dt> <dt>0x80000000</dt> </dl>                                                | Meccanismo di protezione sconosciuto.<br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_NONE"></span><span id="opm_protection_type_none"></span><dl> <dt>**OPM \_ Tipo di protezione \_ \_ None**</dt> <dt>0x00000000</dt> </dl>                                                   | Nessun meccanismo di protezione.<br/>                                                                                                                                                                                        |
| <span id="OPM_PROTECTION_TYPE_COPP_COMPATIBLE_HDCP"></span><span id="opm_protection_type_copp_compatible_hdcp"></span><dl> <dt>**OPM \_ Tipo di protezione \_ \_ Copp \_ compatibile con 0x00000001 \_ HDCP**</dt> <dt></dt> </dl> | High-Bandwidth protezione del contenuto digitali (HDCP). Questo flag viene utilizzato per l'emulazione di COPP (Certified Output Protocol). Per altre informazioni, vedere la sezione Osservazioni. Questo flag non è supportato per la semantica di OPM.<br/> |
| <span id="OPM_PROTECTION_TYPE_ACP"></span><span id="opm_protection_type_acp"></span><dl> <dt>**OPM \_ Tipo di protezione \_ \_ ACP**</dt> <dt>0x00000002</dt> </dl>                                                      | Protezione copia analoga (ACP).<br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_CGMSA"></span><span id="opm_protection_type_cgmsa"></span><dl> <dt>**OPM \_ Tipo di protezione \_ \_ CGMSA**</dt> <dt>0x00000004</dt> </dl>                                                | Sistema di gestione della generazione di copia: analogico (CGMS-A).<br/>                                                                                                                                                               |
| <span id="OPM_PROTECTION_TYPE_HDCP"></span><span id="opm_protection_type_hdcp"></span><dl> <dt>**OPM \_ Tipo di protezione \_ \_ HDCP**</dt> <dt>0x00000008</dt> </dl>                                                   | Protocollo HDCP. Questo flag viene usato quando l'oggetto OPM ha la semantica OPM. Non è supportata per la semantica COPP.<br/>                                                                                                           |
| <span id="OPM_PROTECTION_TYPE_DPCP"></span><span id="opm_protection_type_dpcp"></span><dl> <dt>**OPM \_ Tipo di protezione \_ \_ DPCP**</dt> <dt>0x00000010</dt> </dl>                                                   | DisplayPort protezione del contenuto (DPCP).<br/>                                                                                                                                                                           |



## <a name="remarks"></a>Commenti

Questi flag vengono usati nei seguenti comandi e richieste di stato di OPM.

-   [\_livello di \_ protezione \_ set OPM](opm-set-protection-level.md)
-   [\_livello di \_ \_ protezione virtuale \_ di OPM Get](opm-get-virtual-protection-level.md)
-   [OPM \_ ottenere \_ il \_ livello di protezione effettivo \_](opm-get-actual-protection-level.md)

### <a name="hdcp"></a>PROTOCOLLO HDCP

I due flag seguenti sono definiti per HDCP.



| Valore                                         | Descrizione                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| tipo di protezione di OPM \_ \_ \_ HDCP                   | Usare questo flag se il puntatore [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) è stato creato con la semantica OPM.                                                                        |
| \_tipo di protezione OPM \_ \_ Copp \_ compatibile con \_ HDCP | Utilizzare questo flag se il puntatore [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) è stato creato con la semantica di Copp. Questo flag corrisponde al flag COPP \_ ProtectionType \_ HDCP in copp. |



 

Entrambe le modalità (semantica OPM e semantica COPP) supportano le operazioni seguenti per HDCP:

-   Abilitare o disabilitare HDCP usando il comando [OPM \_ set \_ Protection \_ Level](opm-set-protection-level.md) .
-   Eseguire una query per verificare se la funzionalità HDCP è abilitata usando la richiesta di stato del livello di protezione ( [OPM \_ get \_ virtual \_ Protection \_ ](opm-get-virtual-protection-level.md) ) o [OPM \_ get \_ actual \_ \_ ](opm-get-actual-protection-level.md) .

La semantica di OPM supporta inoltre quanto segue:

-   Ripetitori HDCP. Un *Repeater HDCP* è un dispositivo HDCP che può ricevere contenuti HDCP e anche crittografare nuovamente e trasmettere lo stesso contenuto.
-   Revoca HDCP. Se un dispositivo HDCP revocato viene collegato all'output del video OPM, l'output del video non trasmette il video. Non è necessario che l'applicazione analizzi i messaggi di rinnovabilità del sistema HDCP (SRM) o determini se il dispositivo di output è stato revocato. Per altre informazioni, vedere il comando [**OPM \_ set \_ HDCP \_ MSR**](opm-set-hdcp-srm.md) .

Quando si usano la semantica COPP, l'interfaccia [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) non supporta i ripetitori HDCP. Non gestisce inoltre la revoca HDCP. Al contrario, l'applicazione deve analizzare l'SRM per determinare se un dispositivo HDCP è stato revocato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni di OPM](opm-enumerations.md)
</dt> </dl>

 

 




