---
title: WM_DDE_POKE messaggio (Dde.h)
description: Un'Dynamic Data Exchange client DDE (DDE) invia un messaggio POKE WM \_ DDE \_ a un'applicazione server DDE.
ms.assetid: 848142b7-a7ef-4206-9bb3-b511388cfaaa
keywords:
- WM_DDE_POKE messaggio Dati Exchange
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
ms.openlocfilehash: df1329c6667698a0b633deb2726c47469b515e8fcd78d735a3949e7c8e19a4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736288"
---
# <a name="wm_dde_poke-message"></a>Messaggio \_ \_ POKE WM DDE

Un'Dynamic Data Exchange client DDE (DDE) invia un messaggio **\_ \_ POKE WM DDE** a un'applicazione server DDE. Un client usa questo messaggio per richiedere al server di accettare un elemento di dati non richiesto. Il server deve rispondere con un messaggio [**WM \_ DDE \_ ACK**](wm-dde-ack.md) che indica se ha accettato l'elemento di dati.

Per pubblicare questo messaggio, chiamare la [**funzione PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.


```C++
#define WM_DDE_POKE        0x03E7
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra client che pubblica il messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine basso è un handle per un oggetto di memoria globale contenente una [**struttura DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke) con i dati e informazioni aggiuntive.

La parola di ordine elevato contiene un atom globale che identifica l'elemento di dati per il quale vengono inviati i dati o la notifica.

</dd> </dl>

## <a name="remarks"></a>Commenti

### <a name="posting"></a>Distacco

L'applicazione client deve allocare memoria per l'oggetto di memoria globale usando la [**funzione GlobalAlloc.**](/windows/desktop/api/winbase/nf-winbase-globalalloc) L'applicazione client deve eliminare l'oggetto se si verifica una delle condizioni seguenti:

-   L'applicazione server risponde con un messaggio [**\_ \_ ACK WM DDE**](wm-dde-ack.md) negativo.
-   Il **membro fRelease** è **FALSE,** ma l'applicazione server risponde con un [**ACK WM \_ DDE \_ positivo o negativo.**](wm-dde-ack.md)

L'applicazione client deve creare l'atom usando la [**funzione GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)

L'applicazione client deve creare o riutilizzare il parametro POKE *lParam* **DI WM \_ DDE \_** chiamando la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**la funzione ReuseDDElParam.**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)

### <a name="receiving"></a>Ricezione

L'applicazione server deve inviare il [**messaggio \_ WM DDE \_ ACK**](wm-dde-ack.md) per rispondere in modo positivo o negativo. Quando si **pubblica WM \_ DDE \_ ACK,** il server può riutilizzare l'atomo oppure eliminarlo e crearne uno nuovo.

Il server deve creare o riutilizzare il parametro [**\_ WM DDE \_ ACK**](wm-dde-ack.md) *lParam* chiamando la [**funzione PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**la funzione ReuseDDElParam.**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)

Per liberare l'oggetto di memoria globale, il server deve chiamare la [**funzione GlobalFree.**](/windows/desktop/api/winbase/nf-winbase-globalfree) Inoltre, se il formato dei dati è [**CF \_ DSPMETAFILEPICT**](clipboard-formats.md) o **CF \_ METAFILEPICT,** il server deve chiamare [**anche DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) con l'handle del metafile incorporato. Questi due formati hanno un livello aggiuntivo di riferimento indiretto. ciò significa che un'applicazione deve bloccare l'oggetto per ottenere un puntatore a un handle, quindi bloccare tale handle per ottenere un puntatore a una struttura [**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) e infine chiamare **DeleteMetaFile** con l'handle dal membro **hMF** della struttura **METAFILEPICT.**

Per liberare l'oggetto, il server deve chiamare la [**funzione FreeDDElParam.**](/windows/desktop/api/Dde/nf-dde-freeddelparam)

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

[**Decomprimere UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**WM \_ DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni Dynamic Data Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

