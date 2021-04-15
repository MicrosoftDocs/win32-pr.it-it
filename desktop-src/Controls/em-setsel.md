---
title: Messaggio EM_SETSEL (winuser. h)
description: Seleziona un intervallo di caratteri in un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- Controlli di Windows Message EM_SETSEL
topic_type:
- apiref
api_name:
- EM_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4981fa179ae4bdd454ab0b0a6d7485185ed31d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476097"
---
# <a name="em_setsel-message"></a>\_Messaggio SETSEL em

Seleziona un intervallo di caratteri in un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Posizione iniziale del carattere della selezione.

</dd> <dt>

*lParam* 
</dt> <dd>

Posizione del carattere finale della selezione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Il valore iniziale può essere maggiore del valore finale. Il minore dei due valori specifica la posizione del carattere del primo carattere nella selezione. Il valore più alto specifica la posizione del primo carattere oltre la selezione.

Il valore iniziale è il punto di ancoraggio della selezione e il valore finale è l'estremità attiva. Se l'utente usa il tasto MAIUSC per modificare le dimensioni della selezione, l'estremità attiva può essere spostata, ma il punto di ancoraggio rimane lo stesso.

Se l'inizio è 0 e la fine è-1, viene selezionato tutto il testo nel controllo di modifica. Se l'inizio è-1, viene deselezionata la selezione corrente.

**Controlli di modifica:** Il controllo Visualizza un cursore lampeggiante nella posizione finale indipendentemente dai valori relativi di inizio e fine.

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

Se il controllo di modifica ha lo stile [**es \_ NOHIDESEL**](edit-control-styles.md) , il testo selezionato viene evidenziato indipendentemente dal fatto che il controllo abbia lo stato attivo. Senza lo stile **es \_ NOHIDESEL** , il testo selezionato viene evidenziato solo quando il controllo di modifica ha lo stato attivo.

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

[**\_GETSEL em**](em-getsel.md)
</dt> <dt>

[**\_REPLACESEL em**](em-replacesel.md)
</dt> <dt>

[**\_SCROLLCARET em**](em-scrollcaret.md)
</dt> <dt>

[**\_EXSETSEL em**](em-exsetsel.md)
</dt> </dl>

 

 





