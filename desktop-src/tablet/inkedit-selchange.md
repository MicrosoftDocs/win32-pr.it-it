---
description: Si verifica quando la selezione corrente del testo nel controllo InkEdit è stata modificata o se il punto di inserimento è stato spostato.
ms.assetid: 14ddffe7-bdfe-4a35-82c7-b3401b5b720c
title: Evento InkEdit. SelChange (inchiostrata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b51ef4edbf7d7fb02be17dc416c0a777a9519a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313939"
---
# <a name="inkeditselchange-event"></a>Evento InkEdit. SelChange

Si verifica quando la selezione corrente del testo nel controllo [InkEdit](inkedit-control-reference.md) è stata modificata o se il punto di inserimento è stato spostato.

## <a name="syntax"></a>Sintassi


```C++
void SelChange();
```



## <a name="parameters"></a>Parametri

Questo evento non contiene parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

È possibile utilizzare l'evento **selChange** per verificare le varie proprietà che forniscono informazioni sulla selezione corrente (ad esempio [**Selbold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)), in modo che sia possibile aggiornare i pulsanti in una barra degli strumenti, ad esempio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Inchiostrato. h (richiede anche il \_ . c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 




