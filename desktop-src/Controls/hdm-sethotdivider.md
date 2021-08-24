---
title: HDM_SETHOTDIVIDER messaggio (Commctrl.h)
description: Modifica il colore di un divisore tra gli elementi dell'intestazione per indicare la destinazione di un'operazione di trascinamento della selezione esterna. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Header SetHotDivider.
ms.assetid: 56f6e5c6-1df3-4b4d-9ad8-97fb168c5462
keywords:
- HDM_SETHOTDIVIDER di controllo Windows messaggio
topic_type:
- apiref
api_name:
- HDM_SETHOTDIVIDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eedfca7a6f0d10651984efb63c4db63116c4a53d2b9f9b85905c93fc12e6ca16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544751"
---
# <a name="hdm_sethotdivider-message"></a>Messaggio \_ HDM SETHOTDIVIDER

Modifica il colore di un divisore tra gli elementi dell'intestazione per indicare la destinazione di un'operazione di trascinamento della selezione esterna. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Header SetHotDivider.**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di valore rappresentato da *lParam*. I valori validi sono i seguenti:



| Valore                                                                                                                                    | Significato                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE****</dt> </dl>    | Indica che *lParam contiene* le coordinate client del puntatore.<br/> |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE****</dt> </dl> | Indica che *lParam* contiene un valore di indice divisore.<br/>                 |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Un valore in *lParam* viene interpretato a seconda del valore di *wParam*.

Se *wParam* è **TRUE,** *lParam* rappresenta le coordinate x e y del puntatore. La coordinata x è nella parola bassa e la coordinata y è nella parola alta. Quando il controllo intestazione riceve il messaggio, evidenzia il divisore appropriato in base alle coordinate *lParam.*

Se *wParam* è **FALSE,** *lParam* rappresenta l'indice intero del divisore da evidenziare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore uguale all'indice del divisore evidenziato dal controllo.

## <a name="remarks"></a>Commenti

Questo messaggio crea un effetto generato automaticamente da un controllo intestazione quando ha lo [**stile \_ HDS DRAGDROP.**](header-control-styles.md) Il **messaggio HDM \_ SETHOTDIVIDER** deve essere usato quando il proprietario del controllo gestisce manualmente le operazioni di trascinamento della selezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





