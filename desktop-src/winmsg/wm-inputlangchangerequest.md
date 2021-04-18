---
description: Inviato alla finestra con lo stato attivo quando l'utente sceglie una nuova lingua di input, con il tasto di scelta rapida (specificato nell'applicazione del pannello di controllo della tastiera) o dall'indicatore sulla barra delle applicazioni del sistema.
ms.assetid: db38c31c-6ae4-4401-82b8-7fd220c1678c
title: Messaggio WM_INPUTLANGCHANGEREQUEST (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df361c479978083c29281764e65c48b131c22b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312378"
---
# <a name="wm_inputlangchangerequest-message"></a>\_Messaggio INPUTLANGCHANGEREQUEST WM

Inviato alla finestra con lo stato attivo quando l'utente sceglie una nuova lingua di input, con il tasto di scelta rapida (specificato nell'applicazione del pannello di controllo della tastiera) o dall'indicatore sulla barra delle applicazioni del sistema. Un'applicazione può accettare la modifica passando il messaggio alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o rifiutare la modifica (e impedirne l'esecuzione) restituendo immediatamente.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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
| <span id="INPUTLANGCHANGE_BACKWARD"></span><span id="inputlangchange_backward"></span><dl> <dt>**INPUTLANGCHANGE \_**</dt> <dt>0x0004</dt> indietro </dl>       | È stato usato un tasto di scelta per scegliere le impostazioni locali di input precedenti nell'elenco installato delle impostazioni locali di input. Questo flag non può essere usato con il \_ flag di avanzamento INPUTLANGCHANGE.<br/> |
| <span id="INPUTLANGCHANGE_FORWARD"></span><span id="inputlangchange_forward"></span><dl> <dt>**INPUTLANGCHANGE \_**</dt> <dt>0X0002</dt> di avanzamento </dl>          | È stato usato un tasto di scelta per scegliere le impostazioni locali di input successive nell'elenco installato delle impostazioni locali di input. Questo flag non può essere usato con il \_ flag INPUTLANGCHANGE indietro.<br/>    |
| <span id="INPUTLANGCHANGE_SYSCHARSET"></span><span id="inputlangchange_syscharset"></span><dl> <dt>**INPUTLANGCHANGE \_**</dt> <dt>0x0001</dt> SYSCHARSET </dl> | Il nuovo layout della tastiera delle impostazioni locali di input può essere utilizzato con il set di caratteri di sistema.<br/>                                                                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificatore delle impostazioni locali di input. Per altre informazioni, vedere [lingue, impostazioni locali e layout di tastiera](../inputdev/about-keyboard-input.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Questo messaggio viene pubblicato, non inviato, all'applicazione, quindi il valore restituito viene ignorato. Per accettare la modifica, l'applicazione deve passare il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Per rifiutare la modifica, l'applicazione deve restituire zero senza chiamare **DefWindowProc**.

## <a name="remarks"></a>Commenti

Quando la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) riceve il messaggio **WM \_ INPUTLANGCHANGEREQUEST** , attiva le nuove impostazioni locali di input e invia una notifica all'applicazione della modifica inviando il messaggio [**WM \_ INPUTLANGCHANGE**](wm-inputlangchange.md) .

L'indicatore della lingua è presente sulla barra delle applicazioni solo se è stato installato più di un layout di tastiera e se è stato abilitato l'indicatore utilizzando l'applicazione del pannello di controllo della tastiera.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**\_INPUTLANGCHANGE WM**](wm-inputlangchange.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
