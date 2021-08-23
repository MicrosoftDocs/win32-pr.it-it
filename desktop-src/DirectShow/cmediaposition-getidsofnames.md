---
description: 'Metodo CMediaPosition.GetIDsOfNames: il metodo GetIDsOfNames esegue il mapping di un set di nomi a un set corrispondente di DISPID.'
ms.assetid: 4d3780ff-905f-4166-86d4-32395090b5cb
title: Metodo CMediaPosition.GetIDsOfNames (Ctlutil.h)
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
ms.openlocfilehash: eebd32638afdf957024f54f6a601e95bae274dc4ab9a8265e9a618d635a23530
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634797"
---
# <a name="cmediapositiongetidsofnames-method"></a>Metodo CMediaPosition.GetIDsOfNames

Il `GetIDsOfNames` metodo esegue il mapping di un set di nomi a un set corrispondente di DISPID.

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

*Riid* 
</dt> <dd>

Riservato. Usare IID \_ NULL.

</dd> <dt>

*rgszNames* 
</dt> <dd>

Indirizzo di una matrice di stringhe di caratteri wide che contengono i nomi di cui eseguire il mapping.

</dd> <dt>

*cNames* 
</dt> <dd>

Dimensione della matrice specificata dal *parametro rgszNames.*

</dd> <dt>

*lcid* 
</dt> <dd>

Contesto delle impostazioni locali in cui interpretare i nomi. Può essere **NULL.**

</dd> <dt>

*rgdispid* 
</dt> <dd>

Puntatore a una matrice che riceve i DISPID. Ogni elemento di riceve un identificatore che corrisponde a uno dei nomi passati nel *parametro rgszNames.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                         | Descrizione                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operazione completata.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Memoria insufficiente.<br/>                     |
| <dl> <dt>**DISP \_ E \_ UNKNOWNNAME**</dt> </dl> | Uno o più nomi non erano noti.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




