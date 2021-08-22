---
title: LVM_GETISEARCHSTRING messaggio (Commctrl.h)
description: Recupera la stringa di ricerca incrementale di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro ListView GetISearchString.
ms.assetid: e953c4a0-0556-4987-8abf-3276e787fe49
keywords:
- LVM_GETISEARCHSTRING dei controlli Windows messaggio
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
ms.openlocfilehash: d612a6c1ba303bc08b6d5067ccb4dd3802354456159e3aea4120bd122348e74f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540821"
---
# <a name="lvm_getisearchstring-message"></a>Messaggio LVM \_ GETISEARCHSTRING

Recupera la stringa di ricerca incrementale di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetISearchString.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un buffer che riceve la stringa di ricerca incrementale. Per recuperare solo la lunghezza della stringa, impostare *lParam* su **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di caratteri nella stringa di ricerca incrementale, senza includere il carattere NULL di terminazione oppure zero se il controllo visualizzazione elenco non è in modalità di ricerca incrementale.

## <a name="remarks"></a>Commenti

**Avviso di sicurezza:** L'uso non corretto di questo messaggio potrebbe compromettere la sicurezza del programma. Questo messaggio non consente di conoscere le dimensioni del buffer. Se si usa questo messaggio, chiamare prima il messaggio passando **NULL** in *lParam*, verrà restituito il numero di caratteri, esclusi **i VALORI NULL** necessari. Chiamare quindi il messaggio una seconda volta per recuperare la stringa. Prima di continuare, vedere Considerazioni sulla [sicurezza: Microsoft Windows Controlli.](sec-comctls.md)

La *stringa di ricerca incrementale* è la sequenza di caratteri immessa dall'utente mentre la visualizzazione elenco ha lo stato attivo per l'input. Ogni volta che l'utente digitare un carattere, il sistema aggiunge il carattere alla stringa di ricerca e quindi cerca un elemento corrispondente. Se il sistema trova una corrispondenza, seleziona l'elemento e, se necessario, lo scorre nella visualizzazione.

Un periodo di timeout è associato a ogni carattere tipiato dall'utente. Se il periodo di timeout è trascorso prima che l'utente tipi un altro carattere, la stringa di ricerca incrementale viene reimpostata.

Assicurarsi che le dimensioni del buffer siano sufficienti per contenere la stringa e il carattere NULL di terminazione. Se è troppo piccolo, verrà restituito un errore di pagina non valida immediato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ GETISEARCHSTRINGW** (Unicode) e **LVM \_ GETISEARCHSTRINGA** (ANSI)<br/> |



 

 





