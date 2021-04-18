---
description: 'Il metodo QueryId recupera un identificatore per il PIN. Questo metodo implementa il metodo IPin:: QueryId.'
ms.assetid: 3d83db3a-b919-454d-a91a-91f33a952a22
title: Metodo CTransformOutputPin. QueryId (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e8e5fbc4b4da7b38853df5b4dcf3580a8c198d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330838"
---
# <a name="ctransformoutputpinqueryid-method"></a>CTransformOutputPin. QueryId, metodo

Il `QueryId` metodo recupera un identificatore per il PIN. Questo metodo implementa il metodo [**Ipin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Id* 
</dt> <dd>

Riceve una stringa che contiene l'identificatore del PIN.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione riuscita<br/>                   |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente<br/>       |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Argomento puntatore **null**<br/> |



 

## <a name="remarks"></a>Commenti

L'identificatore del PIN viene usato per la persistenza del grafo. L'identificatore del PIN per questa classe è out. Questa classe esegue l'override del comportamento della classe [**CBasePin**](cbasepin.md) . Nella classe **CBasePin** l'identificatore del PIN è uguale al nome del PIN, specificato nel costruttore della classe. Nella classe **CTransformInputPin** , l'identificatore del PIN e il nome del PIN non sono uguali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




