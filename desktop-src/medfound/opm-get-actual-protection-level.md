---
description: Restituisce il livello di protezione globale per un meccanismo di protezione specificato.
ms.assetid: 3dd4f6f0-2305-4470-bbd4-7737fa2d8eae
title: OPM_GET_ACTUAL_PROTECTION_LEVEL (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ed5d895c037fedfa97bbafab8331d685af9a7f1ce81489b8d600bd903aa2a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101920"
---
# <a name="opm_get_actual_protection_level"></a>OPM \_ GET \_ ACTUAL \_ PROTECTION \_ LEVEL

Restituisce il livello di protezione globale per un meccanismo di protezione specificato.



| Requisito | Valore |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID richiesta | OPM \_ GET \_ ACTUAL \_ PROTECTION \_ LEVEL                                                                                                                                       |
| Dati di input   | Meccanismo di protezione su cui eseguire una query, specificato come intero a 32 bit. Il valore viene interpretato come membro dei flag [del tipo di protezione OPM](opm-protection-type-flags.md). |
| Restituisce i dati  | Struttura [**OPM \_ STANDARD \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                                                                               |



 

## <a name="remarks"></a>Commenti

Il livello di protezione globale è il livello di protezione attualmente applicato al connettore, indipendentemente dal modo in cui è stato richiesto al driver di grafica di applicare la protezione. Ad esempio, un'applicazione può impostare il livello di protezione ACP chiamando la **funzione ChangeDisplaySettingsEx.** In tal caso, il livello di protezione globale riflette questa impostazione, anche se non è stata richiesta tramite Output Protection Manager (OPM).

Il livello di protezione viene restituito nel **membro ulInformation** della [**struttura OPM STANDARD \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Il significato di questo valore dipende dal meccanismo di protezione su cui viene eseguita una query. Per ogni meccanismo di protezione, il valore di **ulInformation** è un flag di un'enumerazione diversa, come illustrato nella tabella seguente.



| Meccanismo di protezione | Enumerazione                                                       |
|----------------------|-------------------------------------------------------------------|
| ACP                  | [**LIVELLO DI \_ PROTEZIONE ACP \_ \_ OPM**](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| CGMS-A               | [Flag di protezione CGMS-A](cgms-a-protection-flags.md)            |
| DPCP                 | [**LIVELLO DI \_ PROTEZIONE \_ DPCP \_ OPM**](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| Hdcp                 | [**LIVELLO DI PROTEZIONE HDCP OPM \_ \_ \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

Questa query equivale alla \_ query DXVA COPPQueryGlobalProtectionLevel usata in Certified Output Protection Protocol (COPP).

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

 

 




