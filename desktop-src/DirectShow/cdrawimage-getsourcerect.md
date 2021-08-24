---
description: Il metodo GetSourceRect recupera il rettangolo di origine corrente.
ms.assetid: e9ca091f-3fd7-4e42-90e9-b7831dd488a9
title: Metodo CDrawImage.GetSourceRect (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81d7de629ec89fe31296a9efd10df3d4895f53a7dc67db58bfde77be8a75a82f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697888"
---
# <a name="cdrawimagegetsourcerect-method"></a>Metodo CDrawImage.GetSourceRect

Il `GetSourceRect` metodo recupera il rettangolo di origine corrente.

## <a name="syntax"></a>Sintassi


```C++
void GetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Puntatore a una **struttura RECT** che riceve il rettangolo di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




