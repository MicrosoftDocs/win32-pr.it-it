---
description: Il metodo SetRealize specifica se la finestra realizza i palette.
ms.assetid: ab4a6069-c11f-4126-93bf-6de5277970a1
title: Metodo CBaseWindow.SetRealize (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetRealize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 825a020b73bc74b38a32daa6f6870b76a009f5b8090e253370c77dfce7d7dc31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954567"
---
# <a name="cbasewindowsetrealize-method"></a>Metodo CBaseWindow.SetRealize

Il `SetRealize` metodo specifica se la finestra realizza i colori.

## <a name="syntax"></a>Sintassi


```C++
void SetRealize(
   BOOL bRealize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bRealize* 
</dt> <dd>

Valore booleano che specifica se realizzare i palette. Se **TRUE,** il [**metodo CBaseWindow::SetPalette**](cbasewindow-setpalette.md) realizza i colori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il **metodo SetPalette** realizza il riquadro specificato. Chiamare questo metodo per modificare il comportamento predefinito, in modo che i tavolozze siano selezionati ma non realizzati. Questo metodo imposta la [**variabile membro CBaseWindow::m \_ bNoRealize.**](cbasewindow-m-bnorealize.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




