---
title: Messaggio di WM_DDE_REQUEST (DDE. h)
description: Un'applicazione client di Dynamic Data Exchange (DDE) Invia un \_ \_ messaggio di richiesta DDE di WM a un'applicazione server DDE per richiedere il valore di un elemento di dati. Per pubblicare questo messaggio, chiamare la funzione PostMessage con i parametri seguenti.
ms.assetid: 922452d2-455c-43e1-a8a8-e3c52b0fab51
keywords:
- Scambio di dati del messaggio WM_DDE_REQUEST
topic_type:
- apiref
api_name:
- WM_DDE_REQUEST
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7d5eab75d3b7298d78547b17fccfb164a47ae4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741087"
---
# <a name="wm_dde_request-message"></a>\_Messaggio di \_ richiesta DDE WM

Un'applicazione client di Dynamic Data Exchange (DDE) Invia un messaggio di **\_ \_ richiesta DDE di WM** a un'applicazione server DDE per richiedere il valore di un elemento di dati.

Per pubblicare questo messaggio, chiamare la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.


```C++
#define WM_DDE_REQUEST     0x03E6
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra client che invia il messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine inferiore specifica un formato degli Appunti standard o registrato.

La parola più ordinata contiene un Atom che identifica l'elemento dati richiesto dal server.

</dd> </dl>

## <a name="remarks"></a>Commenti

### <a name="posting"></a>Distacco

L'applicazione client alloca il Atom chiamando la funzione [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

### <a name="receiving"></a>Ricezione

Se l'applicazione ricevente (Server) può soddisfare la richiesta, risponde con un messaggio [**di \_ \_ dati DDE WM**](wm-dde-data.md) contenente i dati richiesti. In caso contrario, risponde con un messaggio [**di \_ \_ ACK DDE WM**](wm-dde-ack.md) negativo.

Quando si rispondono a un messaggio [**WM \_ DDE \_**](wm-dde-data.md) o a un messaggio [**\_ \_ ACK DDE**](wm-dde-ack.md) , l'applicazione server può riutilizzare il formato Atom o eliminare l'Atom e crearne uno nuovo.

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

[**\_dati DDE di WM \_**](wm-dde-data.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni su Dynamic Data Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

