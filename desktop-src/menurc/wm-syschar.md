---
title: WM_SYSCHAR messaggio (Winuser.h)
description: Inviato alla finestra con lo stato attivo della tastiera quando un messaggio WM \_ SYSKEYDOWN viene convertito dalla funzione TranslateMessage.
ms.assetid: 55987105-3c53-42e5-8fab-a3c9f2ca7273
keywords:
- WM_SYSCHAR messaggio Menu e altre risorse
topic_type:
- apiref
api_name:
- WM_SYSCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b42d88d5ae1346032da2c663dd8c9189c030d5bb7d538ab7ef84403d42fba76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472089"
---
# <a name="wm_syschar-message"></a>Messaggio \_ SYSCHAR WM

Inviato alla finestra con lo stato attivo della tastiera quando [**un messaggio WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) viene convertito dalla [**funzione TranslateMessage.**](/windows/desktop/api/winuser/nf-winuser-translatemessage) Specifica il codice carattere di un tasto carattere di sistema, un tasto di scelta rapida che viene premuto mentre il tasto ALT è premuto.


```C++
#define WM_SYSCHAR                      0x0106
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Codice carattere del tasto di menu della finestra.

</dd> <dt>

*lParam* 
</dt> <dd>

Numero di ripetizioni, codice di analisi, flag di chiave estesa, codice di contesto, flag di stato della chiave precedente e flag di stato di transizione, come illustrato nella tabella seguente.



| BITS                                                                             | Significato                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 15</dt> </dl>  | Numero di ripetizioni per il messaggio corrente. Il valore è il numero di volte in cui la sequenza di tasti è stata ripetuta automaticamente in seguito alla pressione del tasto da parte dell'utente. Se la sequenza di tasti viene mantenuta abbastanza a lungo, vengono inviati più messaggi. Tuttavia, il conteggio delle ripetizioni non è cumulativo.<br/> |
| <dl> <dt>16 23</dt> </dl> | Codice di analisi. Il valore dipende dal produttore originale delle apparecchiature (OEM).<br/>                                                                                                                                                                                          |
| <dl> <dt>24</dt> </dl>    | Indica se il tasto è un tasto esteso, ad esempio i tasti ALT e CTRL di destra visualizzati su una tastiera avanzata a 101 o 102 tasti. Il valore è 1 se è una chiave estesa. in caso contrario, è 0.<br/>                                                                |
| <dl> <dt>25 28</dt> </dl> | Riservato; non utilizzare .<br/>                                                                                                                                                                                                                                                   |
| <dl> <dt>29</dt> </dl>    | Codice del contesto. Il valore è 1 se il tasto ALT viene premuto mentre il tasto viene premuto; in caso contrario, il valore è 0.<br/>                                                                                                                                                       |
| <dl> <dt>30</dt> </dl>    | Stato della chiave precedente. Il valore è 1 se la chiave non è disponibile prima dell'invio del messaggio oppure è 0 se la chiave è in alto.<br/>                                                                                                                                                      |
| <dl> <dt>31</dt> </dl>    | Stato della transizione. Il valore è 1 se il tasto viene rilasciato oppure è 0 se il tasto viene premuto.<br/>                                                                                                                                                              |

Per altre informazioni, vedere [Flag dei messaggi di sequenza di tasti](../inputdev/about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Quando il codice di contesto è zero, il messaggio può essere passato alla funzione [**TranslateAccelerator,**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) che lo gestirà come se fosse un messaggio di chiave standard anziché un messaggio di sistema di tasti di scelta rapida. In questo modo è possibile usare i tasti di scelta rapida con la finestra attiva anche se la finestra attiva non ha lo stato attivo della tastiera.

Per le tastiere avanzate da 101 e 102 tasti, i tasti estesi sono i tasti ALT e CTRL di destra nella sezione principale della tastiera; i tasti INS, DEL, HOME, END, PGGIS, PGGIUTO e i tasti di direzione nei cluster a sinistra del tastierino numerico; il tasto PRINT SCRN; il tasto BREAK; tasto NUMLOCK; e i tasti di divisione (/) e INVIO nel tastierino numerico. Altre tastiere possono supportare il bit del tasto esteso nel parametro .

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

[**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tasti di scelta rapida](keyboard-accelerators.md)
</dt> </dl>

