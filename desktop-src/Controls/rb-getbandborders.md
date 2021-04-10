---
title: Messaggio RB_GETBANDBORDERS (COMmctrl. h)
description: Recupera i bordi di una banda. Il risultato di questo messaggio può essere utilizzato per calcolare l'area utilizzabile di una banda.
ms.assetid: 45f2ae7e-636e-474b-a0d0-5235c6401e6a
keywords:
- Controlli di Windows Message RB_GETBANDBORDERS
topic_type:
- apiref
api_name:
- RB_GETBANDBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521dfecaf5e2573b30f606b7b4d7ecdec9bd896d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964552"
---
# <a name="rb_getbandborders-message"></a>\_Messaggio GETBANDBORDERS RB

Recupera i bordi di una banda. Il risultato di questo messaggio può essere utilizzato per calcolare l'area utilizzabile di una banda.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della banda per cui verranno recuperati i bordi.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceverà i bordi della banda. Se il controllo Rebar dispone dello [**stile \_ BANDBORDERS RBS**](rebar-control-styles.md) , ogni membro della struttura riceverà il numero di pixel, sul lato corrispondente della banda, che costituiscono il bordo. Se il controllo Rebar non dispone dello stile **\_ BANDBORDERS di RBS** , solo il membro **sinistro** di questa struttura riceve informazioni valide.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

