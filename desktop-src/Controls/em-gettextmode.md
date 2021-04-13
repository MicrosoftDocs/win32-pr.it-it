---
title: Messaggio di EM_GETTEXTMODE (RichEdit. h)
description: Ottiene la modalità testo corrente e il livello di annullamento di un controllo Rich Edit.
ms.assetid: 5c976a82-9c51-4700-9db4-a6b0ed7bb852
keywords:
- Controlli di Windows Message EM_GETTEXTMODE
topic_type:
- apiref
api_name:
- EM_GETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 012a12aec573518c859ec7f2a0319036dcd1ef87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478113"
---
# <a name="em_gettextmode-message"></a>\_Messaggio GETTEXTMODE em

Ottiene la modalità testo corrente e il livello di annullamento di un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è uno o più valori del tipo di enumerazione [**TextMode**](/windows/win32/api/richedit/ne-richedit-textmode) . I valori indicano la modalità testo corrente e il livello di annullamento del controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_SETTEXTMODE em**](em-settextmode.md)
</dt> <dt>

[**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> </dl>

 

 





