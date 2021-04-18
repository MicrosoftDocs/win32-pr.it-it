---
description: Scrive i dati del filtro nel flusso specificato.
ms.assetid: 1b405050-6cfd-4b69-b449-f00a6ecfac6a
title: Metodo CPersistStream. WriteToStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.WriteToStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 893d58986db92e50cbafefe74676481162808abf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328915"
---
# <a name="cpersiststreamwritetostream-method"></a>CPersistStream. WriteToStream, metodo

Scrive i dati del filtro nel flusso specificato.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT WriteToStream(
   IStream *pStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStream* 
</dt> <dd>

Puntatore a un'interfaccia **IStream** che specifica il flusso di destinazione dei dati del filtro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK. La classe derivata deve restituire un valore **HRESULT** valido.

## <a name="remarks"></a>Commenti

La versione predefinita non scrive nulla; è possibile eseguirne l'override per scrivere i dati specifici della classe.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PStream. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




