---
description: Restituisce il livello di protezione globale per un meccanismo di protezione specificato.
ms.assetid: 3dd4f6f0-2305-4470-bbd4-7737fa2d8eae
title: OPM_GET_ACTUAL_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 960d704fd44ca779f128795b26603698bb0ad622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049659"
---
# <a name="opm_get_actual_protection_level"></a>OPM \_ ottenere \_ il \_ livello di protezione effettivo \_

Restituisce il livello di protezione globale per un meccanismo di protezione specificato.



| Requisito | Valore |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID richiesta | OPM \_ ottenere \_ il \_ livello di protezione effettivo \_                                                                                                                                       |
| Dati di input   | Meccanismo di protezione per la query, specificato come intero a 32 bit. Il valore viene interpretato come un membro dei [flag del tipo di protezione OPM](opm-protection-type-flags.md). |
| Restituisce i dati  | Struttura [**di \_ \_ informazioni standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                                                                               |



 

## <a name="remarks"></a>Commenti

Il livello di protezione globale è il livello di protezione attualmente applicato al connettore, indipendentemente dal modo in cui il driver di grafica ha richiesto di applicare la protezione. Ad esempio, un'applicazione può impostare il livello di protezione ACP chiamando la funzione **ChangeDisplaySettingsEx** . In tal caso, il livello di protezione globale rifletterebbe questa impostazione, anche se non è stata richiesta tramite output Protection Manager (OPM).

Il livello di protezione viene restituito nel membro **ulInformation** della struttura [**di \_ \_ informazioni standard di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . Il significato di questo valore dipende dal meccanismo di protezione su cui viene eseguita una query. Per ogni meccanismo di protezione, il valore di **ulInformation** è un flag di un'enumerazione diversa, come illustrato nella tabella seguente.



| Meccanismo di protezione | Enumerazione                                                       |
|----------------------|-------------------------------------------------------------------|
| ACP                  | [**\_livello di \_ protezione \_ ACP di OPM**](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| CGMS-A               | [CGMS-flag di protezione](cgms-a-protection-flags.md)            |
| DPCP                 | [**\_livello di \_ protezione \_ DPCP OPM**](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| PROTOCOLLO HDCP                 | [**\_livello di \_ protezione \_ HDCP di OPM**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

Questa query equivale alla \_ query DXVA COPPQueryGlobalProtectionLevel utilizzata in Certified Output Protocol (Copp).

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

 

 




