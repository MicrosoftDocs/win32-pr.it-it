---
title: Messaggio di WM_DDE_EXECUTE (DDE. h)
description: Un'applicazione client di Dynamic Data Exchange (DDE) Invia un \_ \_ messaggio di esecuzione DDE di WM a un'applicazione server DDE per inviare una stringa al server da elaborare come una serie di comandi.
ms.assetid: 23c18a57-83ee-4fd3-a5bc-71645bda34eb
keywords:
- Scambio di dati del messaggio WM_DDE_EXECUTE
topic_type:
- apiref
api_name:
- WM_DDE_EXECUTE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 957b5cadcd2383d535aa67258725bafff57ab4f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400687"
---
# <a name="wm_dde_execute-message"></a>\_Messaggio di \_ esecuzione DDE WM

Un'applicazione client di Dynamic Data Exchange (DDE) Invia un messaggio di **\_ \_ esecuzione DDE di WM** a un'applicazione server DDE per inviare una stringa al server da elaborare come una serie di comandi. Si prevede che l'applicazione server invii un [**messaggio \_ \_ ACK DDE WM**](wm-dde-ack.md) in risposta.

Per pubblicare questo messaggio, chiamare la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.


```C++
#define WM_DDE_EXECUTE     0x03E8
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra client che invia il messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene un oggetto memoria globale che fa riferimento a una stringa di comando ANSI o Unicode, a seconda dei tipi di Windows necessari per la conversazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

La stringa di comando è una stringa con terminazione null costituita da una o più stringhe opcode racchiuse tra parentesi quadre ( \[ \] ). Ogni stringa opcode presenta la sintassi seguente, in cui l'elenco *Parameters* è facoltativo:

*parametri OpCode*

Il *codice operativo* è qualsiasi singolo token definito dall'applicazione. Non può includere spazi, virgole, parentesi, parentesi quadre o virgolette.

L'elenco *Parameters* può contenere qualsiasi valore o valore definito dall'applicazione. Più parametri sono separati da virgole e l'intero elenco di parametri è racchiuso tra parentesi. I parametri non possono includere virgole o parentesi tranne che all'interno di una stringa racchiusa tra virgolette. Se un carattere tra parentesi quadre o parentesi deve essere visualizzato in una stringa racchiusa tra virgolette, non è necessario raddoppiarlo, come nel caso delle regole precedenti.

Di seguito sono riportate stringhe di comando valide:


```
[connect][download(query1,results.txt)][disconnect] 
[query("sales per employee for each district")] 
[open("sample.xlm")][run("r1c1")] 
[quote_case("This is a "" character")] 
[bracket_or_paren_case("()s or []s should be no problem.")] 
```



Si noti che, in base alle regole precedenti, le parentesi e le parentesi quadre devono essere raddoppiate, come indicato di seguito:


```
[bracket_or_paren_case("(())s or [[]]s should be no problem.")] 
```



I server devono essere in grado di analizzare i comandi in entrambi i moduli.

Le stringhe di esecuzione Unicode devono essere utilizzate solo quando entrambe le finestre client e server gestiscono la funzione [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) per restituire **true**.

### <a name="posting"></a>Distacco

L'applicazione client alloca l'oggetto memoria globale chiamando la funzione [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .

Quando si elabora il messaggio [**\_ \_ ACK di WM DDE**](wm-dde-ack.md) che il server invia come risposta a un messaggio di **\_ \_ esecuzione DDE WM** , l'applicazione client deve eliminare l'oggetto restituito dal messaggio **\_ \_ ACK DDE WM** .

### <a name="receiving"></a>Ricezione

L'applicazione server inserisce il [**messaggio \_ \_ ACK DDE di WM**](wm-dde-ack.md) per rispondere in modo positivo o negativo. Il server deve riutilizzare l'oggetto memoria globale.

Se non specificato diversamente da un sottoprotocollo, il server non deve inserire il messaggio [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) finché non vengono completate tutte le azioni specificate dalla stringa di comando Execute. L'unica eccezione a questa regola è rappresentata dal caso in cui la stringa causa la terminazione della conversazione da parte del server.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>DDE. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode)
</dt> <dt>

[**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**\_ACK DDE \_ WM**](wm-dde-ack.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni su Dynamic Data Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

