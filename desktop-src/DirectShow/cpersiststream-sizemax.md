---
description: Recupera la dimensione massima in byte necessaria per il flusso corrente, senza includere il numero di versione.
ms.assetid: ca1a68e2-02b4-4eea-916a-e0418ae811ae
title: Metodo CPersistStream. SizeMax (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afa29e2c81cc454a9e85b9038486221f6f44aaf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328921"
---
# <a name="cpersiststreamsizemax-method"></a>CPersistStream. SizeMax, metodo

Recupera la dimensione massima in byte necessaria per il flusso corrente, senza includere il numero di versione.

## <a name="syntax"></a>Sintassi


```C++
virtual int SizeMax();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il numero di byte necessari per i dati, escluso il numero di versione.

## <a name="remarks"></a>Commenti

La versione predefinita restituisce zero. è necessario eseguirne l'override per fornire un altro valore appropriato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PStream. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




