---
title: Messaggio HDM_SETHOTDIVIDER (COMmctrl. h)
description: Modifica il colore di un divisore tra gli elementi di intestazione per indicare la destinazione di un'operazione di trascinamento e rilascio esterna. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetHotDivider dell'intestazione.
ms.assetid: 56f6e5c6-1df3-4b4d-9ad8-97fb168c5462
keywords:
- Controlli di Windows Message HDM_SETHOTDIVIDER
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
ms.openlocfilehash: feb894100878e9b3ee85e8e8367a4b81a022a0a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119658"
---
# <a name="hdm_sethotdivider-message"></a>\_Messaggio HDM SETHOTDIVIDER

Modifica il colore di un divisore tra gli elementi di intestazione per indicare la destinazione di un'operazione di trascinamento e rilascio esterna. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetHotDivider dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di valore rappresentato da *lParam*. I valori validi sono i seguenti:



| Valore                                                                                                                                    | Significato                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE * * * *</dt> </dl>    | Indica che *lParam* include le coordinate client del puntatore.<br/> |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | Indica che *lParam* utilizza un valore di indice del divisore.<br/>                 |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Un valore contenuto in *lParam* viene interpretato in base al valore di *wParam*.

Se *wParam* è **true**, *lParam* rappresenta le coordinate x e y del puntatore. La coordinata x si trova nella parola bassa e la coordinata y si trova nella parola alta. Quando il controllo intestazione riceve il messaggio, evidenzia il separatore appropriato in base alle coordinate *lParam* .

Se *wParam* è **false**, *lParam* rappresenta l'indice Integer del divisore da evidenziare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore uguale all'indice del divisore evidenziato dal controllo.

## <a name="remarks"></a>Commenti

Questo messaggio crea un effetto che un controllo intestazione produce automaticamente quando dispone dello stile [**\_ DragDrop di HDS**](header-control-styles.md) . Il messaggio **HDM \_ SETHOTDIVIDER** deve essere usato quando il proprietario del controllo gestisce manualmente le operazioni di trascinamento della selezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





