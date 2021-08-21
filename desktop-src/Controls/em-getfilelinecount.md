---
title: EM_GETFILELINECOUNT messaggio (CommCtrl.h)
description: Ottiene il numero di righe in un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle righe sullo schermo.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- EM_GETFILELINECOUNT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_GETFILELINECOUNT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 28539af32212a699e12d2cf1d1787fa2e7aaa224f374eb6a63717279fcad16b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019679"
---
# <a name="em_getfilelinecount-message-commctrlh"></a>EM_GETFILELINECOUNT messaggio (CommCtrl.h)

Ottiene il numero di righe in un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle righe sullo schermo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un numero intero che specifica il numero totale di righe di testo nel controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle righe sullo schermo. Se il controllo non contiene testo, il valore restituito è 1. Il valore restituito non sarà mai minore di 1.

## <a name="remarks"></a>Commenti

Il **messaggio EM \_ GETFILELINECOUNT** recupera il numero totale di righe di testo, indipendentemente dalla modalità di visualizzazione delle righe sullo schermo, non solo dal numero di righe attualmente visibili.

Il ritorno a capo automatico non modifica il numero di righe restituite dal messaggio, perché questo messaggio funziona indipendentemente dalla modalità di visualizzazione delle righe sullo schermo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop 1809 \[\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2019 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ GETFILELINE**](em-getfileline.md)
</dt> <dt>

[**EM \_ FILELINELENGTH**](em-filelinelength.md)
</dt> <dt>

[**Modificare \_ GetFileLineCount**](/windows/win32/api/commctrl/nf-commctrl-edit_getfilelinecount)
</dt> </dl>

 

 





