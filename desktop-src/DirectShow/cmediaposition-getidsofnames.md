---
description: Il metodo GetIDsOfNames esegue il mapping di un set di nomi a un set di DISPID corrispondente.
ms.assetid: 4d3780ff-905f-4166-86d4-32395090b5cb
title: Metodo CMediaPosition. GetIDsOfNames (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc2c7eee4304bb32ac1af2759bc2f094aca1d592
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332332"
---
# <a name="cmediapositiongetidsofnames-method"></a>CMediaPosition. GetIDsOfNames, metodo

Il `GetIDsOfNames` metodo esegue il mapping di un set di nomi a un set di DISPID corrispondente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*riid* 
</dt> <dd>

Riservato. Usare IID \_ null.

</dd> <dt>

*rgszNames* 
</dt> <dd>

Indirizzo di una matrice di stringhe di caratteri wide che contengono i nomi di cui eseguire il mapping.

</dd> <dt>

*CNAME* 
</dt> <dd>

Dimensione della matrice specificata dal parametro *rgszNames* .

</dd> <dt>

*lcid* 
</dt> <dd>

Contesto delle impostazioni locali in cui interpretare i nomi. Può essere **null**.

</dd> <dt>

*rgdispid* 
</dt> <dd>

Puntatore a una matrice che riceve i DISPID. Ogni elemento di riceve un identificatore che corrisponde a uno dei nomi passati nel parametro *rgszNames* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                         | Descrizione                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | Esito positivo.<br/>                                 |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>       | Memoria insufficiente.<br/>                     |
| <dl> <dt>**DISP \_ E \_ unknowname**</dt> </dl> | Uno o più nomi non sono noti.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




