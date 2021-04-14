---
title: Messaggio LVM_GETISEARCHSTRING (COMmctrl. h)
description: Recupera la stringa di ricerca incrementale di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetISearchString di ListView.
ms.assetid: e953c4a0-0556-4987-8abf-3276e787fe49
keywords:
- Controlli di Windows Message LVM_GETISEARCHSTRING
topic_type:
- apiref
api_name:
- LVM_GETISEARCHSTRING
- LVM_GETISEARCHSTRINGA
- LVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9040cf96c5c483b29764b1ccfb67e0e4fff3f897
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478526"
---
# <a name="lvm_getisearchstring-message"></a>\_Messaggio GETISEARCHSTRING LVM

Recupera la stringa di ricerca incrementale di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetISearchString di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un buffer che riceve la stringa di ricerca incrementale. Per recuperare solo la lunghezza della stringa, impostare *lParam* su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di caratteri nella stringa di ricerca incrementale, escluso il carattere NULL di terminazione, oppure zero se il controllo di visualizzazione elenco non è in modalità di ricerca incrementale.

## <a name="remarks"></a>Commenti

**Avviso di sicurezza:** L'utilizzo errato di questo messaggio potrebbe compromettere la sicurezza del programma. Questo messaggio non fornisce un modo per stabilire le dimensioni del buffer. Se si utilizza questo messaggio, chiamare prima il messaggio passando **null** in *lParam*, viene restituito il numero di caratteri, esclusi i **valori null** richiesti. Chiamare quindi il messaggio una seconda volta per recuperare la stringa. Prima di continuare, è necessario esaminare le [considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md) .

La *stringa di ricerca incrementale* è la sequenza di caratteri che l'utente digita mentre la visualizzazione elenco dispone dello stato attivo per l'input. Ogni volta che l'utente digita un carattere, il sistema accoda il carattere alla stringa di ricerca e quindi Cerca un elemento corrispondente. Se il sistema rileva una corrispondenza, seleziona l'elemento e, se necessario, lo scorre nella visualizzazione.

Un periodo di timeout è associato a ogni carattere che l'utente digita. Se il periodo di timeout scade prima che l'utente digita un altro carattere, la stringa di ricerca incrementale viene reimpostata.

Verificare che il buffer sia sufficientemente grande da mantenere la stringa e il carattere NULL di terminazione. Se è troppo piccolo, verrà generato un errore di pagina non valido immediato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ GETISEARCHSTRINGW** (Unicode) e **LVM \_ GETISEARCHSTRINGA** (ANSI)<br/> |



 

 





