---
description: Scrive i dati del filtro nel flusso specificato.
ms.assetid: 1b405050-6cfd-4b69-b449-f00a6ecfac6a
title: Metodo CPersistStream.WriteToStream (Pstream.h)
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
ms.openlocfilehash: 139818d1434163255c62dd5cb109dbf505cea03b5876de14eb2aa4a0636f072f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813291"
---
# <a name="cpersiststreamwritetostream-method"></a>Metodo CPersistStream.WriteToStream

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

Puntatore a **un'interfaccia IStream** che specifica il flusso di destinazione dei dati del filtro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK. La classe derivata deve restituire un valore **HRESULT** valido.

## <a name="remarks"></a>Commenti

La versione predefinita non scrive nulla. può essere sottoposto a override per scrivere dati specifici per la classe.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pstream.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




