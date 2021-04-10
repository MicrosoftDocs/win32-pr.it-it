---
title: Messaggio TTM_GETMARGIN (COMmctrl. h)
description: Recupera i margini superiore, sinistro, inferiore e destro impostati per una finestra della descrizione comando. Un margine è la distanza, in pixel, tra il bordo della finestra della descrizione comando e il testo contenuto nella finestra della descrizione comando.
ms.assetid: c33ee1de-5fbd-4c7e-a703-576c2ffd3052
keywords:
- Controlli di Windows Message TTM_GETMARGIN
topic_type:
- apiref
api_name:
- TTM_GETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3e795d8eac14522f0994a342c7f781b7112ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964241"
---
# <a name="ttm_getmargin-message"></a>\_Messaggio GETMARGIN TTM

Recupera i margini superiore, sinistro, inferiore e destro impostati per una finestra della descrizione comando. Un margine è la distanza, in pixel, tra il bordo della finestra della descrizione comando e il testo contenuto nella finestra della descrizione comando.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceverà le informazioni sul margine. I membri della struttura **Rect** non definiscono un rettangolo di delimitazione. Ai fini di questo messaggio, i membri della struttura vengono interpretati nel modo seguente:



| Valore                                                                                                                                   | Significato                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <dt>**In alto**</dt> </dl>          | Distanza tra il bordo superiore e il testo della descrizione comando, in pixel.<br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**sinistra**</dt> </dl>       | Distanza tra il bordo sinistro e il lato sinistro del testo della descrizione comando, in pixel.<br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <dt>**parte inferiore**</dt> </dl> | Distanza tra il bordo inferiore e il testo della descrizione comando, in pixel.<br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <dt>**Ok**</dt> </dl>    | Distanza tra il bordo destro e l'estremità destra del testo della descrizione comando, in pixel.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, tutti e quattro i margini sono pari a zero quando si crea il controllo ToolTip.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TTM \_**](ttm-setmargin.md)
</dt> </dl>

 

