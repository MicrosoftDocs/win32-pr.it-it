---
title: Messaggio EM_GETFILELINECOUNT (CommCtrl. h)
description: Ottiene il numero di righe in un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- Controlli di Windows Message EM_GETFILELINECOUNT
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
ms.openlocfilehash: bf48b3abeb10b98bf0c22a7dd2ef93c73a2a59c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120539"
---
# <a name="em_getfilelinecount-message-commctrlh"></a>Messaggio EM_GETFILELINECOUNT (CommCtrl. h)

Ottiene il numero di righe in un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.

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

Il valore restituito è un Integer che specifica il numero totale di righe di testo nel controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo. Se il controllo non ha testo, il valore restituito è 1. Il valore restituito non sarà mai minore di 1.

## <a name="remarks"></a>Commenti

Il **messaggio \_ GETFILELINECOUNT em** Recupera il numero totale di righe di testo, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo, non solo dal numero di righe attualmente visibili.

Il ritorno a capo automatico non modifica il numero di righe restituite da questo messaggio, perché questo messaggio funziona indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10, 1809 \[\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2019\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_GETFILELINE em**](em-getfileline.md)
</dt> <dt>

[**\_FILELINELENGTH em**](em-filelinelength.md)
</dt> <dt>

[**Modifica \_ GetFileLineCount**](/windows/win32/api/commctrl/nf-commctrl-edit_getfilelinecount)
</dt> </dl>

 

 





