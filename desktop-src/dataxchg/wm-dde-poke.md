---
title: Messaggio di WM_DDE_POKE (DDE. h)
description: Un'applicazione client di Dynamic Data Exchange (DDE) Invia un \_ \_ messaggio di poke DDE di WM a un'applicazione server DDE.
ms.assetid: 848142b7-a7ef-4206-9bb3-b511388cfaaa
keywords:
- Scambio di dati del messaggio WM_DDE_POKE
topic_type:
- apiref
api_name:
- WM_DDE_POKE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 001697cbd5328b9c8d9eb72ebddff5f86ef6381c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743695"
---
# <a name="wm_dde_poke-message"></a>\_ \_ Messaggio poke DDE WM

Un'applicazione client di Dynamic Data Exchange (DDE) Invia un messaggio di **\_ \_ poke DDE di WM** a un'applicazione server DDE. Un client utilizza questo messaggio per richiedere al server di accettare un elemento di dati non richiesto. Si prevede che il server risponda con un messaggio di [**\_ \_ ACK DDE WM**](wm-dde-ack.md) che indica se l'elemento di dati è stato accettato.

Per pubblicare questo messaggio, chiamare la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.


```C++
#define WM_DDE_POKE        0x03E7
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra client che invia il messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine inferiore è un handle per un oggetto memoria globale contenente una struttura [**DDEPoke**](/windows/desktop/api/Dde/ns-dde-ddepoke) con i dati e informazioni aggiuntive.

La parola più ordinata contiene un Atom globale che identifica l'elemento di dati per il quale vengono inviati i dati o la notifica.

</dd> </dl>

## <a name="remarks"></a>Commenti

### <a name="posting"></a>Distacco

L'applicazione client deve allocare memoria per l'oggetto memoria globale usando la funzione [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) . L'applicazione client deve eliminare l'oggetto se si verifica una delle condizioni seguenti:

-   L'applicazione server risponde con un messaggio di [**\_ \_ ACK DDE WM**](wm-dde-ack.md) negativo.
-   Il membro **fRelease** è **false**, ma l'applicazione server risponde con un [**\_ \_ ACK DDE WM**](wm-dde-ack.md)positivo o negativo.

L'applicazione client deve creare il Atom usando la funzione [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

L'applicazione client deve creare o riutilizzare *il parametro di* **WM \_ DDE \_ poke** , chiamando la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

### <a name="receiving"></a>Ricezione

L'applicazione server deve pubblicare il [**messaggio \_ \_ ACK DDE di WM**](wm-dde-ack.md) per rispondere in modo positivo o negativo. Quando si invia un **\_ \_ ACK DDE WM**, il server può riutilizzare il formato Atom o eliminarlo e crearne uno nuovo.

Il server deve creare o riutilizzare il parametro *lParam* del [**\_ \_ ACK DDE WM**](wm-dde-ack.md) chiamando la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Per liberare l'oggetto memoria globale, il server deve chiamare la funzione [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) . Inoltre, se il formato dei dati è [**CF \_ DSPMETAFILEPICT**](clipboard-formats.md) o **CF \_ METAFILEPICT**, il server deve anche chiamare [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) con l'handle del metafile incorporato. Questi due formati hanno un ulteriore livello di riferimento indiretto; Ciò significa che un'applicazione deve bloccare l'oggetto per ottenere un puntatore a un handle, quindi bloccare tale handle per ottenere un puntatore a una struttura [**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) e infine chiamare **DeleteMetaFile** con l'handle del membro **HMF** della struttura **METAFILEPICT** .

Per liberare l'oggetto, il server deve chiamare la funzione [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) .

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

[**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict)
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

 

