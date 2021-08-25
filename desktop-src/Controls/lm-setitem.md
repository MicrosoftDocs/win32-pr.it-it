---
title: LM_SETITEM messaggio (Commctrl.h)
description: Imposta gli stati e gli attributi di un elemento.
ms.assetid: 02a68a31-2541-480e-b768-449d40e5e9e0
keywords:
- LM_SETITEM dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- LM_SETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8dccdb37536352c8783f7dd6af6a9475f5bea69111e2f7f09e5395b0ebf25b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062801"
---
# <a name="lm_setitem-message"></a>Messaggio \_ LM SETITEM

Imposta gli stati e gli attributi di un elemento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere **NULL.** </dd> <dt>

*lParam* 
</dt> <dd>Puntatore a una <a href="/windows/win32/api/commctrl/ns-commctrl-litem">struttura LITEM</a> contenente i nuovi stati e attributi desiderati per il collegamento. </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se il messaggio riesce a impostare i valori e gli attributi specificati.

## <a name="remarks"></a>Commenti

Con il [**messaggio \_ LM GETITEM,**](lm-getitem.md) è possibile accedere ai collegamenti solo tramite l'indice numerico restituito nel **membro iLink** di [**LITEM.**](/windows/win32/api/commctrl/ns-commctrl-litem) L'accesso al collegamento tramite il nome ID restituito in **szID** non è supportato.

> [!Note]  
> Per usare questo messaggio, è necessario specificare un manifesto Comctl32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





