---
title: Messaggio WM_HOTKEY (winuser. h)
description: Inviato quando l'utente preme un tasto di scelta registrato dalla funzione RegisterHotKey. Il messaggio viene inserito nella parte superiore della coda di messaggi associata al thread che ha registrato il tasto di scelta.
ms.assetid: 28d87c2f-b2bb-4176-910b-0addea6beb93
keywords:
- Input della tastiera e del mouse WM_HOTKEY messaggio
topic_type:
- apiref
api_name:
- WM_HOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f09e81a964542a6a8166ae54a0df4d7127466c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400506"
---
# <a name="wm_hotkey-message"></a>\_Messaggio di scelta rapida WM

Inviato quando l'utente preme un tasto di scelta registrato dalla funzione [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) . Il messaggio viene inserito nella parte superiore della coda di messaggi associata al thread che ha registrato il tasto di scelta.


```C++
#define WM_HOTKEY                       0x0312
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore del tasto di scelta rapida che ha generato il messaggio. Se il messaggio è stato generato da un tasto di scelta rapida definito dal sistema, questo parametro sarà uno dei valori seguenti.



| Valore                                                                                                                                                                                                                             | Significato                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="IDHOT_SNAPDESKTOP"></span><span id="idhot_snapdesktop"></span><dl> <dt>**IDHOT \_ SNAPDESKTOP**</dt> <dt>-2</dt> </dl> | È stato premuto il tasto di scelta rapida "snap desktop".<br/> |
| <span id="IDHOT_SNAPWINDOW"></span><span id="idhot_snapwindow"></span><dl> <dt>**IDHOT \_ SNAPWINDOW**</dt> <dt>-1</dt> </dl>    | È stato premuto il tasto di scelta rapida "finestra snap".<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine inferiore specifica le chiavi che devono essere premuti insieme alla chiave specificata dalla parola più significativa per generare il messaggio di **\_ scelta rapida WM** . Questa parola può essere costituita da uno o più dei valori seguenti. La parola più ordinata specifica il codice chiave virtuale del tasto di scelta.



| Valore                                                                                                                                                                                                               | Significato                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MOD_ALT"></span><span id="mod_alt"></span><dl> <dt>**Mod \_ ALT**</dt> <dt>0x0001</dt> </dl>             | Il tasto ALT è stato premuto.<br/>                                                                                                                                      |
| <span id="MOD_CONTROL"></span><span id="mod_control"></span><dl> <dt>**Mod \_**</dt> <dt>0X0002</dt> di controllo </dl> | Il tasto CTRL è stato premuto.<br/>                                                                                                                                     |
| <span id="MOD_SHIFT"></span><span id="mod_shift"></span><dl> <dt>**Mod \_ MAIUSC**</dt> <dt>0x0004</dt> </dl>       | Il tasto MAIUSC è stato premuto.<br/>                                                                                                                                    |
| <span id="MOD_WIN"></span><span id="mod_win"></span><dl> <dt>**Mod \_ WIN**</dt> <dt>0x0008</dt> </dl>             | Il tasto WINDOWS è stato premuto. Queste chiavi sono contrassegnate dal logo Windows. I tasti di scelta rapida che coinvolgono il tasto Windows sono riservati per l'uso da parte del sistema operativo.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

**WM \_ Il tasto di scelta rapida** non è correlato ai tasti di scelta rapida [**WM \_ GetHotKey**](wm-gethotkey.md) e [**WM \_**](wm-sethotkey.md) . Il messaggio di **\_ scelta rapida WM** viene inviato per i tasti di scelta rapida generici mentre i messaggi WM **\_ sehotkey** e **WM \_ GetHotKey** sono correlati ai tasti di scelta rapida per attivazione finestra.

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

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**WM \_ GEThotkey**](wm-gethotkey.md)
</dt> <dt>

[**sehotkey WM \_**](wm-sethotkey.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

