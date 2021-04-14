---
title: Messaggio RB_PUSHCHEVRON (COMmctrl. h)
description: Inviato a un controllo Rebar per eseguire il push a livello di codice di una freccia di espansione.
ms.assetid: 00a8ce10-1fb2-488a-a6f9-1814f73f82bd
keywords:
- Controlli di Windows Message RB_PUSHCHEVRON
topic_type:
- apiref
api_name:
- RB_PUSHCHEVRON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e09e558d5574d4fd28cf01e9794657556dda4ae8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518274"
---
# <a name="rb_pushchevron-message"></a>\_Messaggio PUSHCHEVRON RB

Inviato a un controllo Rebar per eseguire il push a livello di codice di una freccia di espansione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della banda di cui deve essere eseguito il push della freccia di espansione.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore a 32 bit definito dall'applicazione. Viene passato nuovamente all'applicazione come membro **lParamNM** della struttura [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) che viene passata con la notifica [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="remarks"></a>Commenti

Quando questo messaggio viene inviato, il controllo Rebar invierà all'applicazione un codice di notifica [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) , in cui viene richiesto di visualizzare il menu della freccia di espansione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





