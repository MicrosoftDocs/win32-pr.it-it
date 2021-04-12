---
title: Sfocature di DWM dietro costanti (dwmapi. h)
description: Flag utilizzati dalla \_ struttura BLURBEHIND di DWM per indicare quali membri contengono informazioni valide.
ms.assetid: d6dd552c-1f3b-4f16-8705-f5016ed55d9e
topic_type:
- apiref
api_name:
- DWM_BB_ENABLE
- DWM_BB_BLURREGION
- DWM_BB_TRANSITIONONMAXIMIZED
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe08e0315d4c4b906cdb897ac7ad5dd34d50fbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518130"
---
# <a name="dwm-blur-behind-constants"></a>Sfocature di DWM dietro costanti

Flag utilizzati dalla struttura [**\_ BLURBEHIND di DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) per indicare quali membri contengono informazioni valide.

<dl> <dt>

<span id="DWM_BB_ENABLE"></span><span id="dwm_bb_enable"></span>**\_Abilitazione di DWM BB \_**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



È stato specificato un valore per il membro **fEnable** .


</dt> </dl> </dd> <dt>

<span id="DWM_BB_BLURREGION"></span><span id="dwm_bb_blurregion"></span>**\_BLURREGION BB \_ DWM**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



È stato specificato un valore per il membro **hRgnBlur** .


</dt> </dl> </dd> <dt>

<span id="DWM_BB_TRANSITIONONMAXIMIZED"></span><span id="dwm_bb_transitiononmaximized"></span>**\_TRANSITIONONMAXIMIZED BB \_ DWM**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



È stato specificato un valore per il membro **fTransitionOnMaximized** .


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Dwmapi. h</dt> </dl> |



 

 





