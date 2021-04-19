---
description: Il metodo Transform trasforma un esempio di input per produrre un esempio di output.
ms.assetid: 30ef8c0c-e834-481a-93ff-d06e6fa1ddeb
title: Metodo CTransformFilter. Transform (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8498a9a6ce266e0646dbbdcb4f322c093d6e0cc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326664"
---
# <a name="ctransformfiltertransform-method"></a>Metodo CTransformFilter. Transform

Il `Transform` metodo trasforma un esempio di input per produrre un esempio di output.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT Transform(
   IMediaSample *pIn,
   IMediaSample *pOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pIn* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio di input.

</dd> <dt>

*Broncio* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La classe base restituisce E \_ imprevisto.

La classe derivata deve restituire un valore **HRESULT** che indica l'esito positivo o negativo. I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Non recapitare questo esempio.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>                    |



 

## <a name="remarks"></a>Commenti

Eseguire l'override di questo metodo per produrre dati di output. Leggere i dati di input dall'esempio specificato dal parametro *pin* e scrivere i nuovi dati nell'esempio specificato dal parametro *broncio* .

Prima che il filtro chiami questo metodo, copia le proprietà dall'esempio di input nell'esempio di output. Il `Transform` metodo deve impostare qualsiasi proprietà che differisca tra i due esempi, usando i metodi **IMediaSample** o l'interfaccia [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) (se disponibile).

Se il filtro non deve fornire questo esempio (ad esempio per supportare il controllo di qualità), il metodo deve restituire S \_ false.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




