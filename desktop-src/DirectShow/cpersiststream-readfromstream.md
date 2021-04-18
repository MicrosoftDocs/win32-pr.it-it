---
description: Legge i dati del filtro dal flusso specificato.
ms.assetid: 009f4812-8cc6-436a-9553-3a3161d5e992
title: Metodo CPersistStream. ReadFromStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.ReadFromStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce6c037fbce9fbaeabf7491b1b840000f67e25d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328926"
---
# <a name="cpersiststreamreadfromstream-method"></a>CPersistStream. ReadFromStream, metodo

Legge i dati del filtro dal flusso specificato.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT ReadFromStream(
   IStream *pStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStream* 
</dt> <dd>

Puntatore a un'interfaccia **IStream** da cui leggere i dati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK. La classe derivata deve restituire un valore **HRESULT** valido.

## <a name="remarks"></a>Commenti

La versione predefinita non legge nulla; è possibile eseguirne l'override per leggere i dati specifici della classe.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PStream. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




