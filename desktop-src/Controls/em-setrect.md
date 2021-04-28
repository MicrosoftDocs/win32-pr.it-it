---
title: EM_SETRECT messaggio (Winuser.h)
description: 'EM_SETRECT messaggio: imposta il rettangolo di formattazione di un controllo di modifica su più righe.'
ms.assetid: 4f576e94-3bd3-4416-a960-b7f22da963ea
keywords:
- EM_SETRECT messaggio Controlli Windows
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
ms.openlocfilehash: 042428a236b8e9a23f03cdcceaf5d76eb977efd8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085969"
---
# <a name="em_setrect-message"></a>Messaggio \_ EM SETRECT

Imposta il [rettangolo di formattazione](about-edit-controls.md) di un controllo di modifica su più righe. Il rettangolo di formattazione è il rettangolo di limitazione in cui il controllo disegna il testo. Il rettangolo di limitazione è indipendente dalle dimensioni della finestra del controllo di modifica.

Questo messaggio viene elaborato solo dai controlli di modifica su più righe. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

**Rich Edit 2.0 e versioni successive:** Indica se *lParam specifica* coordinate assolute o relative. Il valore zero indica le coordinate assolute. Il valore 1 indica gli offset relativi al rettangolo di formattazione corrente. Gli offset possono essere positivi o negativi.

**Controlli di modifica e Rich Edit 1.0:** Questo parametro non viene usato e deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che specifica le nuove dimensioni del rettangolo. Se questo parametro è **NULL,** il rettangolo di formattazione viene impostato su valori predefiniti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

L'impostazione di *lParam* su **NULL** non ha alcun effetto se è installato un dispositivo touch o se **EM \_ SETRECT** viene inviato da un thread in cui è installato un hook (vedere [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)). In questi casi, *lParam* deve contenere un puntatore valido a una [**struttura RECT.**](/previous-versions//dd162897(v=vs.85))

Il **messaggio EM \_ SETRECT** fa sì che il testo del controllo di modifica venga ridisegnato. Per modificare le dimensioni del rettangolo di formattazione senza ridisegnare il testo, usare il [**messaggio EM \_ SETRECTNP.**](em-setrectnp.md)

Quando viene creato un controllo di modifica per la prima volta, il rettangolo di formattazione viene impostato su una dimensione predefinita. È possibile usare il **messaggio EM \_ SETRECT per** rendere il rettangolo di formattazione più grande o più piccolo della finestra di controllo di modifica.

Se il controllo di modifica non dispone di una barra di scorrimento orizzontale e il rettangolo di formattazione è impostato in modo da essere più grande della finestra del controllo di modifica, le righe di testo che superano la larghezza della finestra del controllo di modifica (ma inferiori alla larghezza del rettangolo di formattazione) vengono ritagliate anziché a capo.

Se il controllo di modifica contiene un bordo, il rettangolo di formattazione viene ridotto delle dimensioni del bordo. Se si modifica il rettangolo restituito da un messaggio [**EM \_ GETRECT,**](em-getrect.md) è necessario rimuovere le dimensioni del bordo prima di usare il rettangolo con il **messaggio EM \_ SETRECT.**

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Il rettangolo di formattazione non include la barra di selezione, ovvero un'area non contrassegnata a sinistra di ogni paragrafo. Quando l'utente fa clic sulla barra di selezione, viene selezionata la riga corrispondente. Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                                           |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ GETRECT**](em-getrect.md)
</dt> <dt>

[**EM \_ SETRECTNP**](em-setrectnp.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

