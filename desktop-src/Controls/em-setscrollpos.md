---
title: Messaggio di EM_SETSCROLLPOS (RichEdit. h)
description: Scorre il contenuto di un controllo Rich Edit fino al punto specificato.
ms.assetid: 9ec514a4-97b1-44ab-b2ca-973b1f6fc404
keywords:
- Controlli di Windows Message EM_SETSCROLLPOS
topic_type:
- apiref
api_name:
- EM_SETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec41ac5255059b8d40f3a4c2e9b666815b9094fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478557"
---
# <a name="em_setscrollpos-message"></a>\_Messaggio SETSCROLLPOS em

Scorre il contenuto di un controllo Rich Edit fino al punto specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) che specifica un punto nello spazio di testo virtuale del documento, espresso in pixel. Il documento verrà spostato fino a quando questo punto si trova nell'angolo superiore sinistro della finestra di controllo di modifica. Se si desidera modificare la visualizzazione in modo che l'angolo superiore sinistro della visualizzazione sia costituito da due righe e da un carattere nel bordo sinistro. Si passerà un punto di (7, 22).

Il controllo Rich Edit controlla le coordinate x e y e le regola se necessario, in modo che venga visualizzata una riga completa nella parte superiore. Garantisce inoltre che il testo non venga mai completamente spostato al di fuori del rettangolo di visualizzazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce sempre 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Componente ridistribuibile<br/>          | Modifica avanzata 3,0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETSCROLLPOS em**](em-getscrollpos.md)
</dt> </dl>

 

