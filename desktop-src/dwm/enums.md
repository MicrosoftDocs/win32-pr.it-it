---
title: Costanti ed enumerazioni di DWM
description: In questa sezione vengono fornite informazioni sulle costanti e sulle enumerazioni utilizzate nelle API di Gestione finestre desktop (DWM).
ms.assetid: b01f620d-ac87-4e93-88ab-f4297d8cf1d5
keywords:
- Gestione finestre desktop (DWM), riferimento
- DWM (Gestione finestre desktop), riferimento
- Gestione finestre desktop (DWM), costanti
- DWM (Gestione finestre desktop), costanti
- Gestione finestre desktop (DWM), enumerazioni
- DWM (Gestione finestre desktop), enumerazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280fff527f95176b47fc99f88d09453dbf579f38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711185"
---
# <a name="dwm-constants-and-enumerations"></a>Costanti ed enumerazioni di DWM

In questa sezione vengono fornite informazioni sulle costanti e sulle enumerazioni utilizzate nelle API di Gestione finestre desktop (DWM).

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                     | Descrizione                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Sfocature di DWM dietro costanti**](dwm-bb-constants.md)<br/>                          | Flag utilizzati dalla struttura [**\_ BLURBEHIND di DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) per indicare quali membri contengono informazioni valide.<br/>                                                                    |
| [**Le costanti di composizione sono abilitate da DWM**](dwm-ec-constants.md)<br/>                   | Flag utilizzati dalla funzione [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)  per modificare lo stato della composizione di DWM.<br/>                                                                             |
| [**\_ \_ campionamento frame di origine DWM \_**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwm_source_frame_sampling)<br/>              | Flag utilizzati dalla funzione [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) per specificare il tipo di campionamento dei frame.<br/>                                                                            |
| [**\_requisiti della \_ finestra della scheda DWM \_**](/windows/desktop/api/dwmapi/ne-dwmapi-dwm_tab_window_requirements)<br/>          | Restituito da DwmGetUnmetTabRequirements per indicare i requisiti necessari a una finestra per inserire le schede nella barra del titolo dell'applicazione.<br/>                                                                    |
| [**\_Costanti TNP di DWM**](dwm-tnp-constants.md)<br/>                                | Flag utilizzati dalla struttura [**delle \_ \_ proprietà di anteprima di DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) per indicare quali membri contengono informazioni valide.<br/>                                               |
| [**DWMFLIP3DWINDOWPOLICY**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmflip3dwindowpolicy)<br/>                         | Flag utilizzati dalla funzione [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) per specificare i criteri della finestra di Flip3D.<br/>                                                                               |
| [**DWMNCRENDERINGPOLICY**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmncrenderingpolicy)<br/>                           | Flag utilizzati dalla funzione [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) per specificare i criteri di rendering dell'area non client.<br/>                                                                   |
| [**\_destinazione OWNEDWINDOW \_ DWMTRANSITION**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmtransition_ownedwindow_target)<br/> | Identifica la destinazione.<br/>                                                                                                                                                                               |
| [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute)<br/>                               | Flag utilizzati dalle funzioni [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) e [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) per specificare gli attributi della finestra per il rendering non client.<br/> |
| [**tipo di movimento \_**](/windows/desktop/api/Dwmapi/ne-dwmapi-gesture_type)<br/>                                          | Identifica il tipo di movimento specificato in [**DwmRenderGesture**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture).<br/>                                                                                                               |



 

 

 





