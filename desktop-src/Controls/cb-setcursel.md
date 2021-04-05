---
title: Messaggio CB_SETCURSEL (winuser. h)
description: Un'applicazione invia un \_ messaggio di errore CB per selezionare una stringa nell'elenco di una casella combinata.
ms.assetid: d4ce3811-6e0a-4952-97cf-ba6efde0de0d
keywords:
- Controlli di Windows Message CB_SETCURSEL
topic_type:
- apiref
api_name:
- CB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd130204e6dc8bb4166c21bc9c4d52950182c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048347"
---
# <a name="cb_setcursel-message"></a>\_Messaggio SEcursel CB

Un'applicazione invia un messaggio di errore **CB \_** per selezionare una stringa nell'elenco di una casella combinata. Se necessario, l'elenco scorre la stringa nella visualizzazione. Il testo nel controllo di modifica della casella combinata viene modificato in modo da riflettere la nuova selezione e qualsiasi selezione precedente nell'elenco viene rimossa.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'indice in base zero della stringa da selezionare. Se questo parametro è-1, qualsiasi selezione corrente nell'elenco verrà rimossa e il controllo di modifica verrà cancellato.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è l'indice dell'elemento selezionato. Se *wParam* è maggiore del numero di elementi nell'elenco o se *wParam* è-1, il valore restituito è CB \_ Err e la selezione viene deselezionata.

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

[**CB \_ FindString**](cb-findstring.md)
</dt> <dt>

[**CB \_ GETcursel**](cb-getcursel.md)
</dt> <dt>

[**CB \_ SELECTSTRING**](cb-selectstring.md)
</dt> </dl>

 

 





