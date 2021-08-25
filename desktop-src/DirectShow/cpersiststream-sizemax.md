---
description: Recupera le dimensioni massime in byte necessarie per il flusso corrente, senza includere il numero di versione.
ms.assetid: ca1a68e2-02b4-4eea-916a-e0418ae811ae
title: Metodo CPersistStream.SizeMax (Pstream.h)
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
ms.openlocfilehash: 2b8f2c547e75303e4c54a49651f2118a90768bc0f42161ee3dae0de9bec2dcad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813301"
---
# <a name="cpersiststreamsizemax-method"></a>Metodo CPersistStream.SizeMax

Recupera le dimensioni massime in byte necessarie per il flusso corrente, senza includere il numero di versione.

## <a name="syntax"></a>Sintassi


```C++
virtual int SizeMax();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il numero di byte necessari per i dati, senza includere il numero di versione.

## <a name="remarks"></a>Commenti

La versione predefinita restituisce zero. deve essere sottoposto a override per fornire un altro valore appropriato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pstream.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




