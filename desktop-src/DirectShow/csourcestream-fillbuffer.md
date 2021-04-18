---
description: Il metodo FillBuffer compila un campione multimediale con i dati.
ms.assetid: dddad8c7-44f1-4ba3-8fb1-7e7e88e40941
title: Metodo CSourceStream. FillBuffer (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.FillBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3611ad8b590bb823abccdecf9d3d138c70441a07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326935"
---
# <a name="csourcestreamfillbuffer-method"></a>CSourceStream. FillBuffer, metodo

Il `FillBuffer` metodo compila un campione multimediale con i dati.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT FillBuffer(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione              |
|-----------------------------------------------------------------------------------------|--------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Fine del flusso<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Operazione riuscita<br/>       |



 

## <a name="remarks"></a>Commenti

La classe derivata deve implementare questo metodo.

Il campione multimediale assegnato a questo metodo non ha timestamp. La classe derivata deve chiamare il metodo [**IMediaSample:: setime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) per impostare gli indicatori temporali. Se appropriato per il tipo di supporto, la classe derivata deve impostare anche i tempi dei supporti, chiamando il metodo [**IMediaSample:: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) . Per altre informazioni, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).

Restituisce \_ false alla fine del flusso. In questo modo la classe **CSourceStream** Invia la notifica di fine flusso e interrompe il ciclo di elaborazione del buffer. Per ulteriori informazioni, vedere [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




