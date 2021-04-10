---
title: Messaggio TB_SETDRAWTEXTFLAGS (COMmctrl. h)
description: Imposta i flag di disegno del testo per la barra degli strumenti.
ms.assetid: b088af32-ea8a-4304-89f1-a7cec5497f85
keywords:
- Controlli di Windows Message TB_SETDRAWTEXTFLAGS
topic_type:
- apiref
api_name:
- TB_SETDRAWTEXTFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890a24239ff2257ffaccff6613b3765711b2ef7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964629"
---
# <a name="tb_setdrawtextflags-message"></a>TB \_ SETDRAWTEXTFLAGS messaggio

Imposta i flag di disegno del testo per la barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Uno o più \_ flag DT, specificati in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), che indicano quali bit in *lParam* verranno utilizzati durante il disegno del testo.

</dd> <dt>

*lParam* 
</dt> <dd>

Uno o più \_ flag DT, specificati in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), che indicano come verrà disegnato il testo del pulsante. Questo valore verrà passato alla funzione **DrawText** quando viene disegnato il testo del pulsante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce i flag di disegno del testo precedenti.

## <a name="remarks"></a>Commenti

Il parametro *wParam* consente di specificare i flag che verranno usati durante la creazione del testo, anche se questi flag sono disattivati. Se, ad esempio, non si desidera utilizzare il \_ flag DT Center durante il disegno del testo, è necessario aggiungere il \_ flag DT Center a *wParam* e non specificare il \_ flag DT Center in *lParam*. In questo modo si impedisce al controllo di passare il \_ flag DT Center alla funzione [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

