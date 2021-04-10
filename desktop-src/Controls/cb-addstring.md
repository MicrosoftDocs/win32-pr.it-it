---
title: Messaggio CB_ADDSTRING (winuser. h)
description: Aggiunge una stringa alla casella di riepilogo di una casella combinata. Se la casella combinata non ha lo stile di \_ ordinamento CBS, la stringa viene aggiunta alla fine dell'elenco. In caso contrario, la stringa viene inserita nell'elenco e l'elenco viene ordinato.
ms.assetid: 201bcb7b-e7d1-41e6-8eb7-a5864b659a52
keywords:
- Controlli di Windows Message CB_ADDSTRING
topic_type:
- apiref
api_name:
- CB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda16367ec24e869f6cb664e89751d7a13efec3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964761"
---
# <a name="cb_addstring-message"></a>\_Messaggio ADDSTRING CB

Aggiunge una stringa alla casella di riepilogo di una casella combinata. Se la casella combinata non ha lo stile [**di \_ ordinamento CBS**](combo-box-styles.md) , la stringa viene aggiunta alla fine dell'elenco. In caso contrario, la stringa viene inserita nell'elenco e l'elenco viene ordinato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore **LPCTSTR** alla stringa con terminazione null da aggiungere. Se si crea la casella combinata con uno stile disegnato dal proprietario ma senza lo [**stile \_ HASSTRINGS CBS**](combo-box-styles.md) , il valore del parametro *lParam* viene archiviato come dati dell'elemento anziché come stringa a cui altrimenti indicherà. È possibile recuperare o modificare i dati dell'elemento inviando il messaggio [**CB \_ GETITEMDATA**](cb-getitemdata.md) o [**CB \_ SETITEMDATA**](cb-setitemdata.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice in base zero della stringa nella casella di riepilogo della casella combinata. Se si verifica un errore, il valore restituito è CB \_ Err. Se è disponibile spazio insufficiente per archiviare la nuova stringa, è CB \_ ERRSPACE.

## <a name="remarks"></a>Commenti

Se si crea una casella combinata creata dal proprietario con lo stile di [**\_ ordinamento CBS**](combo-box-styles.md) ma senza lo stile [**CBS \_ HASSTRINGS**](combo-box-styles.md) , il messaggio [**WM \_ COMPAREITEM**](wm-compareitem.md) viene inviato una o più volte al proprietario della casella combinata, in modo che il nuovo elemento possa essere inserito correttamente nell'elenco.

Per inserire una stringa in una posizione specifica all'interno dell'elenco, usare il messaggio [**CB \_ INSERTSTRING**](cb-insertstring.md) .

Se lo stile della casella combinata è [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) e si aggiunge una stringa più ampia della casella combinata, inviare un messaggio [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) per assicurarsi che venga visualizzata la barra di scorrimento orizzontale.

**Comclt32.dll versione 5,0 o successiva:** Se si imposta [**CBS \_ minuscole**](combo-box-styles.md) o [**CBS \_ maiuscola**](combo-box-styles.md) , la versione Unicode di **CB \_ ADDSTRING** modifica la stringa. Se si utilizza la memoria globale di sola lettura, l'applicazione avrà esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DIR della CB \_**](cb-dir.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> <dt>

[**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md)
</dt> <dt>

[**\_COMPAREITEM WM**](wm-compareitem.md)
</dt> </dl>

 

