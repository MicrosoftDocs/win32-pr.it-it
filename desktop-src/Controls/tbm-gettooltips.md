---
title: Messaggio TBM_GETTOOLTIPS (COMmctrl. h)
description: Recupera l'handle per il controllo ToolTip assegnato a TrackBar, se presente.
ms.assetid: 30efef12-1aec-4635-94a7-1843db404c4f
keywords:
- Controlli di Windows Message TBM_GETTOOLTIPS
topic_type:
- apiref
api_name:
- TBM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02b0b757b1aabfef2c9df2e80ca9f96542ba4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873829"
---
# <a name="tbm_gettooltips-message"></a>\_Messaggio TBM GETtooltips

Recupera l'handle per il controllo ToolTip assegnato a TrackBar, se presente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per il controllo ToolTip assegnato a TrackBar oppure **null** se le descrizioni comandi non sono in uso. Se il controllo TrackBar non usa lo stile [**delle \_ descrizioni comandi di TBS**](trackbar-control-styles.md) , il valore restituito è **null**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





