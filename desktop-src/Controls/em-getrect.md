---
title: Messaggio EM_GETRECT (winuser. h)
description: Ottiene il rettangolo di formattazione di un controllo di modifica.
ms.assetid: eef0150d-9b7a-4247-acbf-6fea2efd1dc3
keywords:
- Controlli di Windows Message EM_GETRECT
topic_type:
- apiref
api_name:
- EM_GETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8192fd4c3aa7fbe953a36217f6b1408f055d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873934"
---
# <a name="em_getrect-message"></a>\_Messaggio GETRECT em

Ottiene il [rettangolo di formattazione](about-edit-controls.md) di un controllo di modifica. Il rettangolo di formattazione è il rettangolo di limitazione in cui il controllo disegna il testo. Il rettangolo di limitazione è indipendente dalle dimensioni della finestra di modifica del controllo. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceve il rettangolo di formattazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non è significativo.

## <a name="remarks"></a>Commenti

È possibile modificare il rettangolo di formattazione di un controllo di modifica su più righe usando i messaggi [**em \_ serect**](em-setrect.md) e [**em \_ SETRECTNP**](em-setrectnp.md) .

In determinate condizioni, **em \_ GetRect** potrebbe non restituire i valori esatti impostati da [**em \_ serect**](em-setrect.md) o [**em \_ SETRECTNP**](em-setrectnp.md) , che saranno approssimativamente corretti, ma possono essere disattivati con pochi pixel.

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Il rettangolo di formattazione non include la barra di selezione, ovvero un'area non contrassegnata a sinistra di ogni paragrafo. Quando si fa clic sulla barra di selezione, la riga viene selezionata. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

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

[**serect EM \_**](em-setrect.md)
</dt> <dt>

[**\_SETRECTNP em**](em-setrectnp.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

