---
description: Restituisce il livello di protezione virtuale per un meccanismo di protezione specificato.
ms.assetid: 635d54de-2735-4390-8bac-ba63b9503909
title: OPM_GET_VIRTUAL_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7ac36abd0a043a74a18401205bbb5e661ac17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309056"
---
# <a name="opm_get_virtual_protection_level"></a>\_livello di \_ \_ protezione virtuale \_ di OPM Get

Restituisce il livello di protezione virtuale per un meccanismo di protezione specificato.

Il livello di protezione *virtuale* è il livello richiesto dall'applicazione durante la sessione di output Protection Manager (OPM) corrente. Il driver potrebbe applicare un livello superiore, a causa di eventi esterni a questa sessione di OPM. Per individuare il livello di protezione effettivo attivo, inviare la query del [**\_ livello di \_ \_ protezione effettivo \_ dell'OPM**](opm-get-actual-protection-level.md) .



| Requisito | Valore |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID richiesta | \_livello di \_ \_ protezione virtuale \_ di OPM Get                                                                                                                                          |
| Dati di input   | Meccanismo di protezione per la query, specificato come intero a 32 bit. Il valore viene interpretato come un membro dei [**flag del tipo di protezione OPM**](opm-protection-type-flags.md). |
| Restituisce i dati  | Struttura [**di \_ \_ informazioni standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                                                                                   |



 

## <a name="remarks"></a>Commenti

Il livello di protezione viene restituito nel membro **ulInformation** della struttura [**di \_ \_ informazioni standard di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . Il significato di questo valore dipende dal meccanismo di protezione su cui viene eseguita una query. Per ogni meccanismo di protezione, il valore di **ulInformation** è un flag di un'enumerazione diversa, come illustrato nella tabella seguente.



| Meccanismo di protezione | Enumerazione                                                       |
|----------------------|-------------------------------------------------------------------|
| ACP                  | [**\_livello di \_ protezione \_ ACP di OPM**](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| CGMS-A               | [**CGMS-flag di protezione**](cgms-a-protection-flags.md)        |
| DPCP                 | [**\_livello di \_ protezione \_ DPCP OPM**](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| PROTOCOLLO HDCP                 | [**\_livello di \_ protezione \_ HDCP di OPM**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

Questa query equivale alla \_ query DXVA COPPQueryLocalProtectionLevel utilizzata in Certified Output Protocol (Copp).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Richieste di stato di OPM](opm-status-requests.md)
</dt> </dl>

 

 




