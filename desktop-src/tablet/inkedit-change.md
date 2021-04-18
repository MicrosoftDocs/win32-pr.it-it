---
description: Si verifica in seguito alla modifica del contenuto del controllo InkEdit.
ms.assetid: 6c65fcca-c84a-414c-a4e5-c5fdffb13e51
title: Evento InkEdit. Change (inchiostrate. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1ad11ef335a397070001f1ae6be785d60fe9cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316849"
---
# <a name="inkeditchange-event"></a>Evento InkEdit. Change

Si verifica in seguito alla modifica del contenuto del controllo [InkEdit](inkedit-control-reference.md) .

## <a name="syntax"></a>Sintassi


```C++
void Change();
```



## <a name="parameters"></a>Parametri

Questo evento non contiene parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo evento si verifica ogni volta che vengono modificate le proprietà che interessano il contenuto del controllo [InkEdit](inkedit-control-reference.md) .

Questo metodo di evento è definito nell'interfaccia **\_ IInkEditEvents** . L'interfaccia **\_ IInkEditEvents** implementa l'interfaccia IDispatch con un identificatore di **DISPID \_ IeeChange**.

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

 

 




