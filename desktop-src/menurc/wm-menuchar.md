---
title: WM_MENUCHAR messaggio (Winuser.h)
description: Inviato quando un menu è attivo e l'utente preme un tasto che non corrisponde ad alcun tasto di scelta rapida o mnemoico. Questo messaggio viene inviato alla finestra proprietaria del menu.
ms.assetid: de6c91bb-80fd-44b2-8d96-d016477a6547
keywords:
- WM_MENUCHAR menu e altre risorse del messaggio
topic_type:
- apiref
api_name:
- WM_MENUCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d276418636857fb7ce76159111b8e8b24519235823225fccb68fa1523b4137d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869610"
---
# <a name="wm_menuchar-message"></a>Messaggio \_ WM MENUCHAR

Inviato quando un menu è attivo e l'utente preme un tasto che non corrisponde ad alcun tasto di scelta rapida o mnemoico. Questo messaggio viene inviato alla finestra proprietaria del menu.


```C++
#define WM_MENUCHAR                     0x0120
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola più bassa specifica il codice carattere che corrisponde al tasto premuto dall'utente.

La parola più alta specifica il tipo di menu attivo. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                 | Significato                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ POPUP**</dt> <dt>0x00000010L</dt> </dl>       | Menu a discesa, sottomenu o menu di scelta rapida.<br/> |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <dt>**MF \_ SYSMENU**</dt> <dt>0x00002000L</dt> </dl> | Menu della finestra.<br/>                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il menu attivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione che elabora questo messaggio deve restituire uno dei valori seguenti nella parola più alta del valore restituito.



| Codice/valore restituito                                                                                                                                  | Descrizione                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MNC \_ CLOSE**</dt> <dt>1</dt> </dl>   | Informa il sistema che deve chiudere il menu attivo.<br/>                                                                                                                      |
| <dl> <dt>**MNC \_ EXECUTE**</dt> <dt>2</dt> </dl> | Informa il sistema che deve scegliere l'elemento specificato nella parola di ordine più basso del valore restituito. La finestra del proprietario riceve un [**messaggio WM \_ COMMAND.**](wm-command.md)<br/> |
| <dl> <dt>**MNC \_ IGNORE**</dt> <dt>0</dt> </dl>  | Informa il sistema che deve rimuovere il carattere premuto dall'utente e creare un breve segnale acustico sull'altoparlante del sistema.<br/>                                                       |
| <dl> <dt>**MNC \_ SELECT**</dt> <dt>3</dt> </dl>  | Informa il sistema che deve selezionare l'elemento specificato nella parola di ordine più basso del valore restituito. <br/>                                                                       |



 

## <a name="remarks"></a>Commenti

La parola meno importante viene ignorata se la parola più importante contiene 0 o 1.

Un'applicazione deve elaborare questo messaggio quando viene usato un tasto di scelta rapida per selezionare una voce di menu che visualizza una bitmap.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tasti di scelta rapida](keyboard-accelerators.md)
</dt> </dl>

 

