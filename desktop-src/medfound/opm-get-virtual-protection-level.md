---
description: Restituisce il livello di protezione virtuale per un meccanismo di protezione specificato.
ms.assetid: 635d54de-2735-4390-8bac-ba63b9503909
title: OPM_GET_VIRTUAL_PROTECTION_LEVEL (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09fb4130b4ad700de2328114dbf900ff7d122045b277c8a5ae812332c730a5d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972920"
---
# <a name="opm_get_virtual_protection_level"></a>OPM \_ GET \_ VIRTUAL \_ PROTECTION \_ LEVEL

Restituisce il livello di protezione virtuale per un meccanismo di protezione specificato.

Il *livello* di protezione virtuale è il livello richiesto dall'applicazione durante la sessione corrente di Output Protection Manager (OPM). Il driver potrebbe applicare un livello superiore, a causa di eventi esterni a questa sessione OPM. Per trovare il livello di protezione effettivo, inviare la query [**OPM \_ GET ACTUAL \_ PROTECTION \_ \_ LEVEL.**](opm-get-actual-protection-level.md)



| Requisito | Valore |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID richiesta | OPM \_ GET \_ VIRTUAL \_ PROTECTION \_ LEVEL                                                                                                                                          |
| Dati di input   | Meccanismo di protezione su cui eseguire una query, specificato come intero a 32 bit. Il valore viene interpretato come membro dei flag [**del tipo di protezione OPM**](opm-protection-type-flags.md). |
| Restituisce i dati  | Struttura [**OPM \_ STANDARD \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                                                                                   |



 

## <a name="remarks"></a>Commenti

Il livello di protezione viene restituito nel **membro ulInformation** della [**struttura OPM STANDARD \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Il significato di questo valore dipende dal meccanismo di protezione su cui viene eseguita una query. Per ogni meccanismo di protezione, il valore di **ulInformation** è un flag di un'enumerazione diversa, come illustrato nella tabella seguente.



| Meccanismo di protezione | Enumerazione                                                       |
|----------------------|-------------------------------------------------------------------|
| ACP                  | [**LIVELLO DI \_ PROTEZIONE ACP \_ \_ OPM**](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| CGMS-A               | [**Flag di protezione CGMS-A**](cgms-a-protection-flags.md)        |
| DPCP                 | [**LIVELLO DI \_ PROTEZIONE \_ DPCP \_ OPM**](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| Hdcp                 | [**LIVELLO DI PROTEZIONE HDCP OPM \_ \_ \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

Questa query equivale alla \_ query DXVA COPPQueryLocalProtectionLevel usata in Certified Output Protection Protocol (COPP).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Richieste di stato OPM](opm-status-requests.md)
</dt> </dl>

 

 




