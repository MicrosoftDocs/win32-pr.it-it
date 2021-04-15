---
title: Messaggio EM_GETFILELINE (CommCtrl. h)
description: Copia una riga di testo da un controllo di modifica, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo e la inserisce in un buffer specificato.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- Controlli di Windows Message EM_GETFILELINE
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 6b3be3ea4ae883fc808f7ddc8fb60f0d93bcd6ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477920"
---
# <a name="em_getfileline-message-commctrlh"></a>Messaggio EM_GETFILELINE (CommCtrl. h)

Copia una riga di testo da un controllo di modifica, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo e la inserisce in un buffer specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della riga da recuperare da un controllo di modifica su più righe. Un valore pari a zero specifica la riga più in alto. Questo parametro viene ignorato da un controllo di modifica a riga singola.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al buffer che riceve una copia della riga. Prima di inviare il messaggio, impostare la prima parola di questo buffer sulle dimensioni, in **TCHAR** s, del buffer. Per testo ANSI, indica il numero di byte; per il testo Unicode, indica il numero di caratteri. La dimensione nella prima parola viene sovrascritta dalla riga copiata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il numero di **TCHAR** copiate. Il valore restituito è zero se il numero di riga specificato dal parametro *wParam* è maggiore del numero di righe nel controllo di modifica.

## <a name="remarks"></a>Commenti

La riga copiata non contiene un carattere null di terminazione.

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

[**\_FILELINELENGTH em**](em-filelinelength.md)
</dt> <dt>

[**Modifica \_ GetFileLine**](/windows/win32/api/commctrl/nf-commctrl-edit_getfileline)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**WM \_ GETtext**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

