---
title: Messaggio WM_MENUCHAR (winuser. h)
description: Inviato quando un menu è attivo e l'utente preme un tasto che non corrisponde ad alcun tasto di scelta rapida o tasto di scelta rapida. Questo messaggio viene inviato alla finestra che possiede il menu.
ms.assetid: de6c91bb-80fd-44b2-8d96-d016477a6547
keywords:
- Menu del messaggio WM_MENUCHAR e altre risorse
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
ms.openlocfilehash: a278e4a1b4333631741a6a542318a8a55e40b512
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743831"
---
# <a name="wm_menuchar-message"></a>\_Messaggio MENUCHAR WM

Inviato quando un menu è attivo e l'utente preme un tasto che non corrisponde ad alcun tasto di scelta rapida o tasto di scelta rapida. Questo messaggio viene inviato alla finestra che possiede il menu.


```C++
#define WM_MENUCHAR                     0x0120
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola di ordine inferiore specifica il codice carattere che corrisponde alla chiave che l'utente ha premuto.

La parola di ordine superiore specifica il tipo di menu attivo. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                 | Significato                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ POPUP**</dt> <dt>0x00000010L</dt> </dl>       | Menu A discesa, sottomenu o menu di scelta rapida.<br/> |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <dt>**MF \_**</dt> <dt>0x00002000L</dt> SYSMENU </dl> | Menu finestra.<br/>                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il menu attivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione che elabora questo messaggio deve restituire uno dei valori seguenti nella parola più ordinata del valore restituito.



| Codice/valore restituito                                                                                                                                  | Descrizione                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> Multipagina <dt>**\_ Chiudi**</dt> <dt>1</dt> </dl>   | Informa il sistema che dovrebbe chiudere il menu attivo.<br/>                                                                                                                      |
| <dl> Multipagina <dt>**\_ ESECUZIONE**</dt> <dt>2</dt> </dl> | Informa il sistema che deve scegliere l'elemento specificato nella parola di ordine inferiore del valore restituito. La finestra proprietaria riceve un messaggio di [**\_ comando WM**](wm-command.md) .<br/> |
| <dl> Multipagina <dt>**\_ Ignora**</dt> <dt>0</dt> </dl>  | Informa il sistema che deve eliminare il carattere premuto dall'utente e creare un breve beep sull'altoparlante del sistema.<br/>                                                       |
| <dl> Multipagina <dt>**\_ SELEZIONARE**</dt> <dt>3</dt> </dl>  | Informa il sistema che deve selezionare l'elemento specificato nella parola di ordine inferiore del valore restituito. <br/>                                                                       |



 

## <a name="remarks"></a>Commenti

La parola di basso livello viene ignorata se la parola più significativa contiene 0 o 1.

Un'applicazione deve elaborare questo messaggio quando viene usato un acceleratore per selezionare una voce di menu che visualizza una bitmap.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



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

 

