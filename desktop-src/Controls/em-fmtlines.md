---
title: Messaggio EM_FMTLINES (winuser. h)
description: Imposta un flag che determina se un controllo di modifica su più righe include caratteri di interruzioni di riga morbidi. Un'interruzione di riga flessibile è costituita da due ritorni a capo e un avanzamento riga e viene inserito alla fine di una riga interrotta a causa di wordwrapping.
ms.assetid: bfc08062-b0a7-4ba7-8858-00cb20895c77
keywords:
- Controlli di Windows Message EM_FMTLINES
topic_type:
- apiref
api_name:
- EM_FMTLINES
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c12a22ee8c30ffa74705f670a16caa3651e9b44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477117"
---
# <a name="em_fmtlines-message"></a>\_Messaggio FMTLINES em

Imposta un flag che determina se un controllo di modifica su più righe include caratteri di interruzioni di riga morbidi. Un'interruzione di riga flessibile è costituita da due ritorni a capo e un avanzamento riga e viene inserito alla fine di una riga interrotta a causa di wordwrapping.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica se devono essere inseriti caratteri di interruzioni di riga soft. Il valore **true** inserisce i caratteri; il valore **false** li rimuove.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è identico al parametro *wParam* .

## <a name="remarks"></a>Commenti

Questo messaggio ha effetto solo sul buffer restituito dal [**messaggio \_ GetHandle em**](em-gethandle.md) e dal testo restituito dal messaggio [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext) . Non ha alcun effetto sulla visualizzazione del testo all'interno del controllo di modifica.

Il **messaggio \_ FMTLINES em** non influisce su una riga che termina con un'interruzioni di riga rigido. Un'interruzioni di riga dura è costituita da un ritorno a capo e da un avanzamento riga.

> [!Note]  
> Le dimensioni del testo cambiano quando il messaggio viene elaborato.

 

**Modifica avanzata:** Il **messaggio \_ FMTLINES em** non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**GetHandle EM \_**](em-gethandle.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**WM \_ GETtext**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

