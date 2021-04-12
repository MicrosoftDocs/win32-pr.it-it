---
title: Messaggio WM_SYSCHAR (winuser. h)
description: Inserito nella finestra con lo stato attivo quando un messaggio WM \_ SYSKEYDOWN viene convertito dalla funzione TranslateMessage.
ms.assetid: 55987105-3c53-42e5-8fab-a3c9f2ca7273
keywords:
- Menu del messaggio WM_SYSCHAR e altre risorse
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
ms.openlocfilehash: 8d14d2f8829cfd199049d3a1b254065918393c18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519197"
---
# <a name="wm_syschar-message"></a>\_Messaggio SYSCHAR WM

Inserito nella finestra con lo stato attivo quando un messaggio [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) viene convertito dalla funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) . Specifica il codice carattere di una chiave carattere di sistema, ovvero un tasto carattere premuto mentre il tasto ALT è premuto.


```C++
#define WM_SYSCHAR                      0x0106
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Codice carattere del tasto menu finestra.

</dd> <dt>

*lParam* 
</dt> <dd>

Il numero di ripetizioni, il codice di analisi, il flag di chiave estesa, il codice del contesto, il flag di stato precedente e il flag di stato di transizione, come illustrato nella tabella seguente.



| BITS                                                                             | Significato                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 15</dt> </dl>  | Numero di ripetizioni per il messaggio corrente. Il valore è il numero di volte in cui la sequenza di tasti è stata ripetuta automaticamente in seguito all'arresto della chiave da parte dell'utente. Se la sequenza di tasti viene mantenuta abbastanza a lungo, vengono inviati più messaggi. Tuttavia, il numero di ripetizioni non è cumulativo.<br/> |
| <dl> <dt>16 23</dt> </dl> | Codice di analisi. Il valore dipende dall'OEM (Original Equipment Manufacturer).<br/>                                                                                                                                                                                          |
| <dl> <dt>24</dt> </dl>    | Indica se la chiave è una chiave estesa, ad esempio i tasti ALT e CTRL a destra che vengono visualizzati in una tastiera migliorata 101 o 102. Il valore è 1 se è una chiave estesa; in caso contrario, è 0.<br/>                                                                |
| <dl> <dt>25 28</dt> </dl> | Riservati Non usare.<br/>                                                                                                                                                                                                                                                   |
| <dl> <dt>29</dt> </dl>    | Codice del contesto. Il valore è 1 se il tasto ALT è premuto mentre il tasto è premuto; in caso contrario, il valore è 0.<br/>                                                                                                                                                       |
| <dl> <dt>30</dt> </dl>    | Stato precedente della chiave. Il valore è 1 se la chiave è inattiva prima dell'invio del messaggio oppure è 0 se la chiave è attiva.<br/>                                                                                                                                                      |
| <dl> <dt>31</dt> </dl>    | Stato di transizione. Il valore è 1 se la chiave viene rilasciata oppure è 0 se viene premuto il tasto.<br/>                                                                                                                                                              |

Per informazioni dettagliate, vedere [flag dei messaggi di sequenza di tasti](../inputdev/about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Quando il codice del contesto è zero, il messaggio può essere passato alla funzione [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) , che lo gestirà come se fosse un messaggio chiave standard anziché un messaggio di chiave del carattere di sistema. In questo modo è possibile utilizzare i tasti di scelta rapida con la finestra attiva anche se la finestra attiva non dispone dello stato attivo della tastiera.

Per le tastiere avanzate 101 e 102-Key, le chiavi estese sono i tasti ALT e CTRL corretti nella sezione principale della tastiera; i tasti INS, CANC, HOME, END, PGSU, PGGIÙ e freccia nei cluster a sinistra del tastierino numerico; chiave Stamp di stampa. tasto INTERr; chiave NUMLOCK; e la divisione (/) e immettere le chiavi nel tastierino numerico. Altre tastiere possono supportare il bit della chiave estesa nel parametro.

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

[**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**\_SYSKEYDOWN WM**](/windows/desktop/inputdev/wm-syskeydown)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tasti di scelta rapida](keyboard-accelerators.md)
</dt> </dl>

