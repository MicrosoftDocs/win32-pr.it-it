---
title: Messaggio TB_SETINSERTMARKCOLOR (COMmctrl. h)
description: Imposta il colore utilizzato per creare il segno di inserimento per la barra degli strumenti.
ms.assetid: 09a04449-9a1f-4f9a-b09f-9f22f930d735
keywords:
- Controlli di Windows Message TB_SETINSERTMARKCOLOR
topic_type:
- apiref
api_name:
- TB_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 954654d71a3e3b7bba9af287d3e92fb2362e8711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118971"
---
# <a name="tb_setinsertmarkcolor-message"></a>TB \_ SETINSERTMARKCOLOR messaggio

Imposta il colore utilizzato per creare il segno di inserimento per la barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valore di **COLORREF** che contiene il nuovo colore del segno di inserimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **COLORREF** che contiene il colore del segno di inserimento precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TB \_ GETINSERTMARKCOLOR**](tb-getinsertmarkcolor.md)
</dt> </dl>

 

 





