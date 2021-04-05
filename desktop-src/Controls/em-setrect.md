---
title: Messaggio EM_SETRECT (winuser. h)
description: Imposta il rettangolo di formattazione di un controllo di modifica su più righe.
ms.assetid: 4f576e94-3bd3-4416-a960-b7f22da963ea
keywords:
- Controlli di Windows Message EM_SETRECT
topic_type:
- apiref
api_name:
- EM_SETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12b171478b0cb9d47496d20d4d1b6b1e8ddd29a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048301"
---
# <a name="em_setrect-message"></a>\_Messaggio serect em

Imposta il [rettangolo di formattazione](about-edit-controls.md) di un controllo di modifica su più righe. Il rettangolo di formattazione è il rettangolo di limitazione in cui il controllo disegna il testo. Il rettangolo di limitazione è indipendente dalle dimensioni della finestra di controllo di modifica.

Questo messaggio viene elaborato solo dai controlli di modifica su più righe. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

**Rich Edit 2,0 e versioni successive:** Indica se *lParam* specifica le coordinate assolute o relative. Un valore pari a zero indica le coordinate assolute. Il valore 1 indica gli offset relativi al rettangolo di formattazione corrente. Gli offset possono essere positivi o negativi.

**Modificare i controlli e rich edit 1,0:** Questo parametro non viene utilizzato e deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che specifica le nuove dimensioni del rettangolo. Se questo parametro è **null**, il rettangolo di formattazione viene impostato sui valori predefiniti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

L'impostazione di *lParam* su **null** non produce alcun effetto se viene installato un dispositivo touch o se viene inviato **em \_ serect** da un thread con un hook installato (vedere [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)). In questi casi, *lParam* deve contenere un puntatore valido a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) .

Il **messaggio \_ serect em** causa il ridisegnato del testo del controllo di modifica. Per modificare le dimensioni del rettangolo di formattazione senza ridisegnare il testo, usare il [**messaggio \_ SETRECTNP em**](em-setrectnp.md) .

Quando un controllo di modifica viene creato per la prima volta, il rettangolo di formattazione viene impostato su una dimensione predefinita. È possibile utilizzare il **messaggio \_ serect em** per rendere il rettangolo di formattazione più grande o più piccolo della finestra di controllo di modifica.

Se il controllo di modifica non dispone di una barra di scorrimento orizzontale e il rettangolo di formattazione è impostato su un valore maggiore rispetto alla finestra di controllo di modifica, le righe di testo che superano la larghezza della finestra di controllo di modifica, ma inferiori rispetto alla larghezza del rettangolo di formattazione, vengono ritagliate invece di essere sottoposte a incapsulamento.

Se il controllo di modifica contiene un bordo, il rettangolo di formattazione viene ridotto in base alle dimensioni del bordo. Se si sta modificando il rettangolo restituito da un messaggio [**\_ GetRect em**](em-getrect.md) , è necessario rimuovere le dimensioni del bordo prima di utilizzare il rettangolo con il messaggio **em \_ serect** .

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Il rettangolo di formattazione non include la barra di selezione, ovvero un'area non contrassegnata a sinistra di ogni paragrafo. Quando l'utente fa clic sulla barra di selezione, viene selezionata la riga corrispondente. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

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

[**GetRect EM \_**](em-getrect.md)
</dt> <dt>

[**\_SETRECTNP em**](em-setrectnp.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

