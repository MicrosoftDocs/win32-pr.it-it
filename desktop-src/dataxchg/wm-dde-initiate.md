---
title: WM_DDE_INITIATE messaggio (Dde.h)
description: Un'applicazione client Dynamic Data Exchange (DDE) invia un messaggio WM DDE INITIATE per avviare una conversazione con un'applicazione server che risponde ai nomi dell'applicazione e \_ \_ dell'argomento specificati.
ms.assetid: d486f584-75a3-4ffd-ba5d-f95f2692cd6c
keywords:
- WM_DDE_INITIATE scambio di dati del messaggio
topic_type:
- apiref
api_name:
- WM_DDE_INITIATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf65e222c7711d429db44e391d4f03c35997e219
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386729"
---
# <a name="wm_dde_initiate-message"></a>Messaggio WM \_ DDE \_ INITIATE

Un'applicazione client Dynamic Data Exchange (DDE) invia un messaggio **WM \_ DDE \_ INITIATE** per avviare una conversazione con un'applicazione server che risponde ai nomi dell'applicazione e degli argomenti specificati. Quando si riceve questo messaggio, tutte le applicazioni server con nomi che corrispondono all'applicazione specificata e che supportano l'argomento specificato devono confermarlo. Per altre informazioni, vedere il [**messaggio WM \_ DDE \_ ACK.**](wm-dde-ack.md)


```C++
#define WM_DDE_INITIATE        0x03E0
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle alla finestra client che invia il messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine basso contiene un atom che identifica l'applicazione con cui viene richiesta una conversazione. Il nome dell'applicazione non può contenere barre (/) o barre rovesciate ( \\ ). Questi caratteri sono riservati per le implementazioni di rete. Se questo parametro è **NULL,** viene richiesta una conversazione con tutte le applicazioni.

La parola di ordine elevato contiene un atomo che identifica l'argomento per cui è richiesta una conversazione. Se l'argomento è **NULL,** vengono richieste conversazioni per tutti gli argomenti disponibili.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se la parola di basso livello *di lParam* è **NULL,** qualsiasi applicazione server può rispondere. Se la parola di ordine superiore di *lParam* è **NULL,** qualsiasi argomento è valido. Quando si riceve una richiesta WM DDE INITIATE con la parola più alta del parametro *lParam* impostata su **NULL,** un server deve inviare un messaggio WM **\_ \_ DDE** [**\_ \_ ACK**](wm-dde-ack.md) per ognuno degli argomenti supportati.

### <a name="sending"></a>Invio

Il client trasmette il messaggio a tutte le finestre di primo livello impostando il primo parametro di [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) su **HWND \_ BROADCAST**.

Se l'applicazione client ha già ottenuto l'handle di finestra del server desiderato, può inviare **WM \_ DDE \_ INITIATE** direttamente alla finestra del server passando l'handle di finestra del server come primo parametro di [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).

L'applicazione client alloca atom chiamando la [**funzione GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)

Quando [**sendMessage viene**](/windows/desktop/api/winuser/nf-winuser-sendmessage) restituito, l'applicazione client deve eliminare gli atom.

### <a name="receiving"></a>Ricezione

Per completare l'avvio di una conversazione, l'applicazione server deve rispondere con uno o più messaggi [**\_ WM DDE \_ ACK,**](wm-dde-ack.md) in cui ogni messaggio è relativo a un argomento separato. Quando si invia un messaggio **\_ WM DDE \_ ACK,** il server deve creare nuovi atomi e non riusare gli atomi inviati con **WM \_ DDE \_ INITIATE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>Dde.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**WM \_ DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni Dynamic Data Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

