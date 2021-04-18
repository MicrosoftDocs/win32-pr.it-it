---
title: Messaggio BCM_GETNOTE (COMmctrl. h)
description: Ottiene il testo della nota associata a un pulsante di collegamento al comando. È possibile inviare questo messaggio in modo esplicito o usare la macro del pulsante \_ getnote.
ms.assetid: ddaf4227-1316-49b5-abf0-00215472c46c
keywords:
- Controlli di Windows Message BCM_GETNOTE
topic_type:
- apiref
api_name:
- BCM_GETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 758dac90ba4c0f3087a6df90d9acf2c1321b1d73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301707"
---
# <a name="bcm_getnote-message"></a>\_Messaggio GETNOTE BCM

Ottiene il testo della nota associata a un pulsante di collegamento al comando. È possibile inviare questo messaggio in modo esplicito o usare la macro del [**pulsante \_ getnote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in uscita\]
</dt> <dd>

**Valore DWORD** che specifica la dimensione del buffer a cui punta *lParam*, in caratteri.

</dd> <dt>

*lParam* \[ out\]
</dt> <dd>

Buffer di stringa per ricevere il testo. Il buffer deve essere sufficientemente grande da contenere il carattere NULL di terminazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, restituisce **true**. In caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Il messaggio **BCM \_ getnote** funziona solo con i pulsanti con lo stile del pulsante [**BS \_ COMMANDLINK**](button-styles.md) o [**BS \_ DEFCOMMANDLINK**](button-styles.md) .

[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) conterrà:

-   ERRORE \_ non \_ supportato, se il pulsante non ha lo stile [**BS \_ DEFCOMMANDLINK**](button-styles.md) o [**BS \_ COMMANDLINK**](button-styles.md) .
-   ERRORE \_ nel \_ buffer insufficiente, se il buffer *lParam* è troppo piccolo. Il parametro *wParam* conterrà le dimensioni del buffer richieste in caratteri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[Stili dei pulsanti](button-styles.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tipi di pulsante](button-types-and-styles.md)
</dt> </dl>

 

