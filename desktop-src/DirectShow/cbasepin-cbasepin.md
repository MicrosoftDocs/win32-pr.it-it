---
description: Metodo del costruttore.
ms.assetid: e8cb5f1d-171f-4bf8-8ab6-6e547c4678d2
title: Costruttore CBasePin. CBasePin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CBasePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd4883d3d8e906e1da2f377344b735037c5e5cd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332771"
---
# <a name="cbasepincbasepin-constructor"></a>Costruttore CBasePin. CBasePin

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CBasePin(
   TCHAR         *pObjectName,
   CBaseFilter   *pFilter,
   CCritSec      *pLock,
   HRESULT       *phr,
   LPCWSTR       pName,
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pObjectName* 
</dt> <dd>

Stringa contenente il nome di debug per l'oggetto. Per ulteriori informazioni, vedere [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Puntatore al filtro che ha creato questo pin.

</dd> <dt>

*pLock* 
</dt> <dd>

Puntatore a un blocco [**CCritSec**](ccritsec.md) , usato per serializzare le modifiche di stato. Può essere la stessa sezione critica del blocco del filtro, [**CBaseFilter:: m \_ pLock**](cbasefilter-m-plock.md).

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a una variabile che riceve un valore **HRESULT** che indica l'esito positivo o negativo del metodo. Inizializzare il valore su S \_ OK prima di creare l'oggetto. Il valore viene modificato solo se si verifica un errore.

</dd> <dt>

*pName* 
</dt> <dd>

Stringa di caratteri wide contenente il nome del PIN. Per ulteriori informazioni, vedere [**CBasePin:: QueryPinInfo**](cbasepin-querypininfo.md).

</dd> <dt>

*dir* 
</dt> <dd>

Membro dell'enumerazione [**di \_ direzione del pin**](/windows/win32/api/strmif/ne-strmif-pin_direction) che specifica la direzione del PIN.

</dd> </dl>

## <a name="remarks"></a>Commenti

La sezione critica specificata da *pLock* serializza lo stato del PIN, incluso lo stato della connessione, la scelta dell'allocatore, il tipo di supporto e lo stato delle operazioni di scaricamento. Non usare questa sezione critica per serializzare le operazioni di streaming. Per altre informazioni, vedere [flusso di dati nel grafico del filtro](data-flow-in-the-filter-graph.md).

Un filtro potrebbe creare pin nel metodo del costruttore, pertanto a questo punto il puntatore *pFilter* potrebbe non riferirsi a un oggetto valido. Archiviare il puntatore, ma non dereferenziarlo all'interno del costruttore del PIN.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




