---
title: Messaggio di EM_SETBIDIOPTIONS (RichEdit. h)
description: Il \_ messaggio SETBIDIOPTIONS em imposta lo stato corrente delle opzioni bidirezionali nel controllo Rich Edit.
ms.assetid: b518e423-317a-4654-9d9f-c501028e2a0a
keywords:
- Controlli di Windows Message EM_SETBIDIOPTIONS
topic_type:
- apiref
api_name:
- EM_SETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84dc4b92f7a989ab5ef283b36708094a143475de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121046"
---
# <a name="em_setbidioptions-message"></a>\_Messaggio SETBIDIOPTIONS em

Il **messaggio \_ SETBIDIOPTIONS em** imposta lo stato corrente delle opzioni bidirezionali nel controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) che indica come impostare lo stato delle opzioni bidirezionali nel controllo Rich Edit.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Il controllo Rich Edit deve essere in modalità testo normale o **em \_ SETBIDIOPTIONS** non eseguirà alcuna operazione.

Nei controlli testo normale, **em \_ SETBIDIOPTIONS** determina automaticamente la direzione e/o l'allineamento del paragrafo in base alle regole di contesto. Queste regole affermano che la direzione e/o l'allineamento derivano dal primo carattere sicuro nel controllo. Un carattere sicuro è uno dei quali è possibile determinare la direzione del testo (vedere Unicode Standard Version 2,0). La direzione e/o l'allineamento del paragrafo viene applicato al formato predefinito.

**Em \_ SETBIDIOPTIONS** passa il formato di paragrafo predefinito a RTL (da destra a sinistra) se trova un carattere RTL,

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Componente ridistribuibile<br/>          | Modifica avanzata 3,0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[**\_GETBIDIOPTIONS em**](em-getbidioptions.md)
</dt> </dl>

 

 





