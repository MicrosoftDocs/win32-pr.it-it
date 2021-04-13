---
title: Messaggio di WM_DDE_INITIATE (DDE. h)
description: Un'applicazione client di Dynamic Data Exchange (DDE) Invia un \_ \_ messaggio di inizializzazione di WM DDE per avviare una conversazione con un'applicazione server che risponde ai nomi di applicazione e di argomento specificati.
ms.assetid: d486f584-75a3-4ffd-ba5d-f95f2692cd6c
keywords:
- Scambio di dati del messaggio WM_DDE_INITIATE
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
ms.openlocfilehash: 36485db262c46d5364ee0ee26e7e6f39ccf0e677
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400554"
---
# <a name="wm_dde_initiate-message"></a>\_Messaggio di avvio DDE di WM \_

Un'applicazione client di Dynamic Data Exchange (DDE) Invia un messaggio di **\_ \_ inizializzazione di WM DDE** per avviare una conversazione con un'applicazione server che risponde ai nomi di applicazione e di argomento specificati. Al momento della ricezione di questo messaggio, è previsto che tutte le applicazioni server con nomi corrispondenti all'applicazione specificata e che supportano l'argomento specificato lo riconosca. Per ulteriori informazioni, vedere il messaggio [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) .


```C++
#define WM_DDE_INITIATE        0x03E0
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra client che invia il messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine inferiore contiene un Atom che identifica l'applicazione con cui viene richiesta una conversazione. Il nome dell'applicazione non può contenere barre (/) o barre rovesciate ( \) . Questi caratteri sono riservati per le implementazioni di rete. Se questo parametro è **null**, viene richiesta una conversazione con tutte le applicazioni.

La parola più significativa contiene un atomo che identifica l'argomento per il quale viene richiesta una conversazione. Se l'argomento è **null**, vengono richieste le conversazioni per tutti gli argomenti disponibili.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se la parola di ordine inferiore di *lParam* è **null**, qualsiasi applicazione server può rispondere. Se la parola più ordinata di *lParam* è **null**, qualsiasi argomento è valido. Al momento della ricezione di una richiesta di **\_ \_ avvio di WM DDE** con la parola più ordinata del parametro *lParam* impostato su **null**, un server deve inviare un messaggio [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) per ogni argomento supportato.

### <a name="sending"></a>Invio

Il client trasmette il messaggio a tutte le finestre di primo livello impostando il primo parametro di [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) sulla **\_ trasmissione HWND**.

Se l'applicazione client ha già ottenuto l'handle di finestra del server desiderato, può inviare l' **\_ \_ avvio di WM DDE** direttamente alla finestra del server passando l'handle della finestra del server come primo parametro di [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).

L'applicazione client alloca gli atomi chiamando la funzione [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

Quando [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) restituisce, l'applicazione client deve eliminare gli atomi.

### <a name="receiving"></a>Ricezione

Per completare l'avvio di una conversazione, l'applicazione server deve rispondere con uno o più messaggi [**di \_ \_ ACK DDE WM**](wm-dde-ack.md) , dove ogni messaggio è per un argomento separato. Quando si invia un messaggio **\_ \_ ACK di WM DDE** , il server deve creare nuovi atomi. non deve riutilizzare gli atomi inviati con l' **\_ \_ avvio di WM DDE**.

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

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**\_ACK DDE \_ WM**](wm-dde-ack.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni su Dynamic Data Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

