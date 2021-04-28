---
description: 'Costruttore CPersistStream.CPersistStream : metodo costruttore.'
ms.assetid: 48143a61-5ba7-4bf9-bffa-244f2769144d
title: Costruttore CPersistStream.CPersistStream (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.CPersistStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e3be9233d76929ebfcb79121c60ef6c1af35b56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085609"
---
# <a name="cpersiststreamcpersiststream-constructor"></a>Costruttore CPersistStream.CPersistStream

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CPersistStream(
   IUnknown *pUnk,
   HRESULT  *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Punk* 
</dt> <dd>

Puntatore **all'interfaccia IUnknown** dell'oggetto delegante.

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore al valore restituito COM generale. Questo valore viene modificato solo se questa funzione ha esito negativo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pstream.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




