---
description: 'Costruttore CSourceSeeking.CSourceSeeking : metodo del costruttore.'
ms.assetid: a51d90c9-4046-42dc-b7cf-51b904c5f57a
title: Costruttore CSourceSeeking.CSourceSeeking (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fcca70408e76466a88c620e3907271d49930973
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098819"
---
# <a name="csourceseekingcsourceseeking-constructor"></a>Costruttore CSourceSeeking.CSourceSeeking

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CSourceSeeking(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         CCritSec  *pLock
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Puntatore a una stringa contenente il nome dell'oggetto. Per altre informazioni, vedere [**CBaseObject.**](cbaseobject.md)

</dd> <dt>

*Punk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** aggregatore. In caso contrario, impostare questo parametro su **NULL.**

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a un **valore HRESULT.** Ignorato.

</dd> <dt>

*Plock* 
</dt> <dd>

Puntatore a [**un oggetto CCritSec.**](ccritsec.md) Nella classe derivata dichiarare una **variabile membro CCritSec** e usare l'indirizzo per questo parametro. La classe usa questa sezione critica per sincronizzare l'accesso a ora di inizio e `CSourceSeeking` arresto, durata e velocità di riproduzione. Ogni volta che si accede a tali variabili nella classe derivata, mantenere questo blocco.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




