---
description: Metodo del costruttore.
ms.assetid: a51d90c9-4046-42dc-b7cf-51b904c5f57a
title: Costruttore CSourceSeeking. CSourceSeeking (Ctlutil. h)
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
ms.openlocfilehash: 309e926ddf001cf9933b19334992f5210fc7f17b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331154"
---
# <a name="csourceseekingcsourceseeking-constructor"></a>Costruttore CSourceSeeking. CSourceSeeking

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

*pName* 
</dt> <dd>

Puntatore a una stringa che contiene il nome dell'oggetto. Per ulteriori informazioni, vedere [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown** dell'oggetto di aggregazione. In caso contrario, impostare questo parametro su **null**.

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a un valore **HRESULT** . Ignorato.

</dd> <dt>

*pLock* 
</dt> <dd>

Puntatore a un oggetto [**CCritSec**](ccritsec.md) . Nella classe derivata dichiarare una variabile membro **CCritSec** e utilizzarne l'indirizzo per questo parametro. La `CSourceSeeking` classe usa questa sezione critica per sincronizzare l'accesso alle ore di inizio e di fine, alla durata e alla velocità di riproduzione. Quando si accede a tali variabili nella classe derivata, mantenere il blocco.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




