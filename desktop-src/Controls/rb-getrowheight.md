---
title: Messaggio RB_GETROWHEIGHT (COMmctrl. h)
description: Recupera l'altezza di una riga specificata in un controllo Rebar.
ms.assetid: 1ff6a32e-b344-4dbc-b4a4-fb13f11a9d8c
keywords:
- Controlli di Windows Message RB_GETROWHEIGHT
topic_type:
- apiref
api_name:
- RB_GETROWHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce137eef6168d95abfe493a6f22ab66d58460b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874113"
---
# <a name="rb_getrowheight-message"></a>\_Messaggio GETROWHEIGHT RB

Recupera l'altezza di una riga specificata in un controllo Rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero di una banda. Verrà recuperata l'altezza della riga che contiene la banda specificata.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **uint** che rappresenta l'altezza della riga, in pixel.

## <a name="remarks"></a>Commenti

Per recuperare il numero di righe in un controllo Rebar, utilizzare il messaggio [**RB \_ GetRowCount**](rb-getrowcount.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





