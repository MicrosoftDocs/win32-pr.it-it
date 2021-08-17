---
title: PSM_GETTABCONTROL messaggio (Prsht.h)
description: Recupera l'handle per il controllo Struttura a schede di una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro PropSheet GetTabControl.
ms.assetid: 5ddea541-c8e0-4357-b08e-3b5e64be377f
keywords:
- PSM_GETTABCONTROL di controllo Windows messaggio
topic_type:
- apiref
api_name:
- PSM_GETTABCONTROL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0e26c9489dc839383552b407a16313c94e1fc3b070d93f1d59ddaf0310134d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169661"
---
# <a name="psm_gettabcontrol-message"></a>Messaggio \_ GETTABCONTROL PSM

Recupera l'handle per il controllo Struttura a schede di una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ PropSheet GetTabControl.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per il controllo Struttura a schede.

## <a name="remarks"></a>Commenti

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





