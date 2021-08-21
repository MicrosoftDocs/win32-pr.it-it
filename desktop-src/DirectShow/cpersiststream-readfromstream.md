---
description: Legge i dati del filtro dal flusso specificato.
ms.assetid: 009f4812-8cc6-436a-9553-3a3161d5e992
title: Metodo CPersistStream.ReadFromStream (Pstream.h)
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
ms.openlocfilehash: 39f40871e12a069045197d0cc61970c7d7f88c784f6b0873c294727b75121ae6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073645"
---
# <a name="cpersiststreamreadfromstream-method"></a>Metodo CPersistStream.ReadFromStream

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

Puntatore a **un'interfaccia IStream** da cui devono essere letti i dati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK. La classe derivata deve restituire un valore **HRESULT** valido.

## <a name="remarks"></a>Commenti

La versione predefinita non legge nulla. può essere sottoposto a override per leggere i dati specifici della classe.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pstream.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




