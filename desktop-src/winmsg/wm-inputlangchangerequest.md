---
description: Inviato alla finestra con lo stato attivo quando l'utente sceglie una nuova lingua di input, con il tasto di scelta rapida (specificato nell'applicazione Pannello di controllo tastiera) o dall'indicatore sulla barra delle applicazioni del sistema.
ms.assetid: db38c31c-6ae4-4401-82b8-7fd220c1678c
title: WM_INPUTLANGCHANGEREQUEST messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644fa4764c5172edc34f16509c6a6b00be6356b80c460a08233be8aa64ef69c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056061"
---
# <a name="wm_inputlangchangerequest-message"></a>Messaggio WM \_ INPUTLANGCHANGEREQUEST

Inviato alla finestra con lo stato attivo quando l'utente sceglie una nuova lingua di input, con il tasto di scelta rapida (specificato nell'applicazione Pannello di controllo tastiera) o dall'indicatore sulla barra delle applicazioni del sistema. Un'applicazione può accettare la modifica passando il messaggio alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o rifiutando la modifica (e impederne l'esecuzione) tramite la restituzione immediata.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_INPUTLANGCHANGEREQUEST       0x0050
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Nuove impostazioni locali di input. Questo parametro può essere una combinazione dei flag seguenti.



| Valore                                                                                                                                                                                                                                                            | Significato                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INPUTLANGCHANGE_BACKWARD"></span><span id="inputlangchange_backward"></span><dl> <dt>**INPUTLANGCHANGE \_ BACKWARD**</dt> <dt>0x0004</dt> </dl>       | È stato usato un tasto di scelta rapida per scegliere le impostazioni locali di input precedenti nell'elenco installato di impostazioni locali di input. Questo flag non può essere usato con il flag INPUTLANGCHANGE \_ FORWARD.<br/> |
| <span id="INPUTLANGCHANGE_FORWARD"></span><span id="inputlangchange_forward"></span><dl> <dt>**INPUTLANGCHANGE \_ INOLTRO**</dt> <dt>0x0002</dt> </dl>          | È stato usato un tasto di scelta rapida per scegliere le impostazioni locali di input seguenti nell'elenco installato di impostazioni locali di input. Questo flag non può essere usato con il flag INPUTLANGCHANGE \_ BACKWARD.<br/>    |
| <span id="INPUTLANGCHANGE_SYSCHARSET"></span><span id="inputlangchange_syscharset"></span><dl> <dt>**INPUTLANGCHANGE \_ SysCHARSET**</dt> <dt>0x0001</dt> </dl> | Il nuovo layout di tastiera delle impostazioni locali di input può essere usato con il set di caratteri di sistema.<br/>                                                                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificatore delle impostazioni locali di input. Per altre informazioni, vedere [Lingue, impostazioni locali e layout di tastiera.](../inputdev/about-keyboard-input.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Questo messaggio viene inviato, non inviato, all'applicazione, quindi il valore restituito viene ignorato. Per accettare la modifica, l'applicazione deve passare il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Per rifiutare la modifica, l'applicazione deve restituire zero senza **chiamare DefWindowProc**.

## <a name="remarks"></a>Commenti

Quando la [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) riceve il messaggio **WM \_ INPUTLANGCHANGEREQUEST,** attiva le nuove impostazioni locali di input e notifica all'applicazione la modifica inviando il [**messaggio WM \_ INPUTLANGCHANGE.**](wm-inputlangchange.md)

L'indicatore di lingua è presente sulla barra delle applicazioni solo se sono stati installati più layout di tastiera e se l'indicatore è stato abilitato usando l'applicazione Pannello di controllo tastiera.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ INPUTLANGCHANGE**](wm-inputlangchange.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
