---
title: EM_GETFILELINE messaggio (CommCtrl.h)
description: Copia una riga di testo da un controllo di modifica, indipendentemente dalla modalità di visualizzazione delle righe sullo schermo, e la inserisce in un buffer specificato.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- EM_GETFILELINE controlli Windows messaggio
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
ms.openlocfilehash: 470c437280b279f56c3dcc8b45de93cf3f792afc5053b7e312b2c19c7ffcec8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049221"
---
# <a name="em_getfileline-message-commctrlh"></a>EM_GETFILELINE messaggio (CommCtrl.h)

Copia una riga di testo da un controllo di modifica, indipendentemente dalla modalità di visualizzazione delle righe sullo schermo, e la inserisce in un buffer specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della riga da recuperare da un controllo di modifica su più righe. Il valore zero specifica la riga più in alto. Questo parametro viene ignorato da un controllo di modifica a riga singola.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al buffer che riceve una copia della riga. Prima di inviare il messaggio, impostare la prima parola di questo buffer sulla dimensione, in **TCHAR,** del buffer. Per il testo ANSI, questo è il numero di byte. per il testo Unicode, questo è il numero di caratteri. Le dimensioni nella prima parola vengono sovrascritte dalla riga copiata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il numero di **TCHAR** copiati. Il valore restituito è zero se il numero di riga specificato dal *parametro wParam* è maggiore del numero di righe nel controllo di modifica.

## <a name="remarks"></a>Commenti

La riga copiata non contiene un carattere Null di terminazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop 1809 \[\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2019 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ FILELINELENGTH**](em-filelinelength.md)
</dt> <dt>

[**Modificare \_ GetFileLine**](/windows/win32/api/commctrl/nf-commctrl-edit_getfileline)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

