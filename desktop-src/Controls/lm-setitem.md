---
title: Messaggio LM_SETITEM (COMmctrl. h)
description: Imposta gli Stati e gli attributi di un elemento.
ms.assetid: 02a68a31-2541-480e-b768-449d40e5e9e0
keywords:
- Controlli di Windows Message LM_SETITEM
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
ms.openlocfilehash: 11888a76b11ccec7e8e659ca3a33bb23a71667ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119022"
---
# <a name="lm_setitem-message"></a>\_Messaggio elemento

Imposta gli Stati e gli attributi di un elemento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere **null**. </dd> <dt>

*lParam* 
</dt> <dd>Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-litem">litey</a> che contiene i nuovi Stati e attributi desiderati per il collegamento. </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se il messaggio riesce a impostare i valori e gli attributi specificati.

## <a name="remarks"></a>Commenti

Con il messaggio [**LM \_ GetItem**](lm-getitem.md) , è possibile accedere ai collegamenti solo tramite l'indice numerico restituito nel membro **iLink** di [**liteo**](/windows/win32/api/commctrl/ns-commctrl-litem). L'accesso al collegamento tramite il nome ID restituito in **szId** non è supportato.

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comctl32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





