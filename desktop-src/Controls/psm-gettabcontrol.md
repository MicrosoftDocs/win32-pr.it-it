---
title: Messaggio PSM_GETTABCONTROL (Prsht. h)
description: Recupera l'handle per il controllo struttura a schede di una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro PropSheet GetTabControl.
ms.assetid: 5ddea541-c8e0-4357-b08e-3b5e64be377f
keywords:
- Controlli di Windows Message PSM_GETTABCONTROL
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
ms.openlocfilehash: ab296159cac4dbfb4ef894d90d31bcd74d6ca2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518526"
---
# <a name="psm_gettabcontrol-message"></a>\_Messaggio PSM GETtabcontrol

Recupera l'handle per il controllo struttura a schede di una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o usando la macro [**PropSheet \_ GetTabControl**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) .

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

Restituisce l'handle per il controllo struttura a schede.

## <a name="remarks"></a>Commenti

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





