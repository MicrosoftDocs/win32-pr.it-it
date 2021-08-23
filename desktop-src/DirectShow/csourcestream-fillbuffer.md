---
description: Il metodo FillBuffer riempie un campione multimediale con dati.
ms.assetid: dddad8c7-44f1-4ba3-8fb1-7e7e88e40941
title: Metodo CSourceStream.FillBuffer (Source.h)
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
ms.openlocfilehash: b9a522dd2b10e7ced60b65c84621bb1817be4b8abbca8656ba23f49e95fe3892
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687401"
---
# <a name="csourcestreamfillbuffer-method"></a>Metodo CSourceStream.FillBuffer

Il `FillBuffer` metodo riempie un campione multimediale con dati.

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

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione              |
|-----------------------------------------------------------------------------------------|--------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Fine del flusso<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Operazione riuscita<br/>       |



 

## <a name="remarks"></a>Commenti

La classe derivata deve implementare questo metodo.

L'esempio multimediale fornito a questo metodo non ha timestamp. La classe derivata deve chiamare il [**metodo IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) per impostare i timestamp. Se appropriato per il tipo di supporto, anche la classe derivata deve impostare gli orari dei supporti chiamando il metodo [**IMediaSample::SetMediaTime.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) Per altre informazioni, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).

Restituisce S \_ FALSE alla fine del flusso. In questo modo la **classe CSourceStream** invia la notifica di fine flusso e arresta il ciclo di elaborazione del buffer. Per altre informazioni, vedere [**CSourceStream::D oBufferProcessingLoop.**](csourcestream-dobufferprocessingloop.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (include Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




