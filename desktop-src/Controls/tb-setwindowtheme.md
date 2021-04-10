---
title: Messaggio TB_SETWINDOWTHEME (COMmctrl. h)
description: Imposta lo stile di visualizzazione di un controllo Toolbar.
ms.assetid: 8b05c561-af66-47e7-8ef3-7f9f81da4840
keywords:
- Controlli di Windows Message TB_SETWINDOWTHEME
topic_type:
- apiref
api_name:
- TB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0c293e974eee2e7827225efb06cc439fdf2c39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121706"
---
# <a name="tb_setwindowtheme-message"></a>TB \_ SETWINDOWTHEME messaggio

Imposta lo stile di visualizzazione di un controllo Toolbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una stringa Unicode che contiene lo stile di visualizzazione della barra degli strumenti da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

L'invio di questo messaggio equivale alla chiamata di [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) sulla barra degli strumenti e del relativo controllo ToolTip, se disponibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





