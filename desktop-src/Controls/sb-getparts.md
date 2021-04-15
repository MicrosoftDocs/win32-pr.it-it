---
title: Messaggio SB_GETPARTS (COMmctrl. h)
description: Recupera un conteggio delle parti in una finestra di stato. Il messaggio recupera inoltre la coordinata del bordo destro del numero di parti specificato.
ms.assetid: 2535f490-4d6b-468a-b13c-096941e61bf4
keywords:
- Controlli di Windows Message SB_GETPARTS
topic_type:
- apiref
api_name:
- SB_GETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee0f33331c579490cf66a38b9ce6655215ae673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518447"
---
# <a name="sb_getparts-message"></a>\_Messaggio SB GETparts

Recupera un conteggio delle parti in una finestra di stato. Il messaggio recupera inoltre la coordinata del bordo destro del numero di parti specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di parti per le quali recuperare le coordinate. Se questo parametro è maggiore del numero di parti nella finestra, il messaggio recupera le coordinate solo per le parti esistenti.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di interi che ha lo stesso numero di elementi delle parti specificate da *wParam*. Ogni elemento nella matrice riceve la coordinata client del bordo destro della parte corrispondente. Se un elemento è impostato su-1, la posizione del bordo destro della parte viene estesa al bordo destro della finestra. Per recuperare il numero corrente di parti, impostare questo parametro su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di parti nella finestra.

## <a name="remarks"></a>Commenti

Questo messaggio restituisce sempre il numero di parti nella barra di stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





