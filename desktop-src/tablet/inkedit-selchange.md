---
description: Si verifica quando la selezione corrente di testo nel controllo InkEdit viene modificata o il punto di inserimento viene spostato.
ms.assetid: 14ddffe7-bdfe-4a35-82c7-b3401b5b720c
title: Evento InkEdit.SelChange (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9677aafa254de3d834e9b947ad1b858b893d6a42e53336dd11ad5c54157c13dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712651"
---
# <a name="inkeditselchange-event"></a>Evento InkEdit.SelChange

Si verifica quando la selezione corrente di testo nel [controllo InkEdit](inkedit-control-reference.md) viene modificata o il punto di inserimento viene spostato.

## <a name="syntax"></a>Sintassi


```C++
void SelChange();
```



## <a name="parameters"></a>Parametri

Questo evento non ha parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

È possibile usare l'evento **SelChange** per controllare le varie proprietà che forniscono informazioni sulla selezione corrente,ad esempio [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold), in modo da aggiornare i pulsanti in una barra degli strumenti, ad esempio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Inked.h (richiede anche \_ i.c con input penna)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Inkedit](inkedit-control-reference.md)
</dt> </dl>

 

 




