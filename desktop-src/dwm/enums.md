---
title: Costanti ed enumerazioni DWM
description: Questa sezione contiene informazioni sulle costanti e sulle enumerazioni usate nelle API Gestione finestre desktop (DWM).
ms.assetid: b01f620d-ac87-4e93-88ab-f4297d8cf1d5
keywords:
- Gestione finestre desktop (DWM), informazioni di riferimento
- DWM (Gestione finestre desktop),informazioni di riferimento
- Gestione finestre desktop (DWM), costanti
- DWM (Gestione finestre desktop),costanti
- Gestione finestre desktop (DWM), enumerazioni
- DWM (Gestione finestre desktop),enumerazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149751deb5e8c30f16b0226f8003b03346ae0608017692e07409db1faa08249d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117720655"
---
# <a name="dwm-constants-and-enumerations"></a>Costanti ed enumerazioni DWM

Questa sezione contiene informazioni sulle costanti e sulle enumerazioni usate nelle API Gestione finestre desktop (DWM).

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                     | Descrizione                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Sfocatura DWM dietro le costanti**](dwm-bb-constants.md)<br/>                          | Flag utilizzati dalla [**struttura DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) per indicare quali membri contengono informazioni valide.<br/>                                                                    |
| [**Costanti di composizione DWM Enable**](dwm-ec-constants.md)<br/>                   | Flag usati dalla [**funzione DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)  per modificare lo stato della composizione DWM.<br/>                                                                             |
| [**CAMPIONAMENTO DEI \_ FRAME DI \_ ORIGINE DWM \_**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwm_source_frame_sampling)<br/>              | Flag usati dalla funzione [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) per specificare il tipo di campionamento dei fotogrammi.<br/>                                                                            |
| [**REQUISITI DELLA FINESTRA DELLA SCHEDA DWM \_ \_ \_**](/windows/desktop/api/dwmapi/ne-dwmapi-dwm_tab_window_requirements)<br/>          | Restituito da DwmGetUnmetTabRequirements per indicare i requisiti necessari a una finestra per inserire le schede nella barra del titolo dell'applicazione.<br/>                                                                    |
| [**Costanti \_ TNP DWM**](dwm-tnp-constants.md)<br/>                                | Flag utilizzati dalla struttura [**DWM \_ THUMBNAIL \_ PROPERTIES**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) per indicare quali membri contengono informazioni valide.<br/>                                               |
| [**DWMFLIP3DWINDOWPOLICY**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmflip3dwindowpolicy)<br/>                         | Flag usati dalla funzione [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) per specificare i criteri della finestra Flip3D.<br/>                                                                               |
| [**DWMNCRENDERINGPOLICY**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmncrenderingpolicy)<br/>                           | Flag usati dalla funzione [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) per specificare i criteri di rendering dell'area non client.<br/>                                                                   |
| [**DESTINAZIONE DWMTRANSITION \_ OWNEDWINDOW \_**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmtransition_ownedwindow_target)<br/> | Identifica la destinazione.<br/>                                                                                                                                                                               |
| [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute)<br/>                               | Flag usati dalle funzioni [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) e [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) per specificare gli attributi della finestra per il rendering non client.<br/> |
| [**TIPO DI \_ MOVIMENTO**](/windows/desktop/api/Dwmapi/ne-dwmapi-gesture_type)<br/>                                          | Identifica il tipo di movimento specificato in [**DwmRenderGesture.**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture)<br/>                                                                                                               |



 

 

 





