---
description: Carica i dati del filtro da un flusso specificato.
ms.assetid: c2bfd379-2916-4698-bc41-653161723706
title: Metodo CPersistStream.Load (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Load
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d65ff2d2ba95f66e6153aa78a9ce376ed144ac24ce8945c1fbc678e9f6894802
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813351"
---
# <a name="cpersiststreamload-method"></a>Metodo CPersistStream.Load

Carica i dati del filtro da un flusso specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Load(
   LPSTREAM pStm
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStm* 
</dt> <dd>

Puntatore al flusso da cui caricare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il **metodo IPersistStream::Load.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pstream.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




