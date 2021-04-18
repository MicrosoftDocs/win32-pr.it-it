---
title: Messaggio CBEM_DELETEITEM (COMmctrl. h)
description: Rimuove un elemento da un controllo ComboBoxEx.
ms.assetid: 688cf388-54ba-4b45-88d7-628da49d8615
keywords:
- Controlli di Windows Message CBEM_DELETEITEM
topic_type:
- apiref
api_name:
- CBEM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa3034f79dffabcd7d7aa780582646e17d30b62f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302648"
---
# <a name="cbem_deleteitem-message"></a>\_Messaggio CBEM DeleteItem

Rimuove un elemento da un controllo ComboBoxEx.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento da rimuovere.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore INT che rappresenta il numero di elementi rimanenti nel controllo. Se *iIndex* non è valido, il messaggio restituisce CB \_ Err.

## <a name="remarks"></a>Commenti

Questo messaggio viene mappato al messaggio di controllo casella combinata [**CB \_ DELETESTRING**](cb-deletestring.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





