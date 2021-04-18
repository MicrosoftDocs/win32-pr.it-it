---
description: Il metodo di scaricamento notifica alla classe di base che il pin ha avviato o interrotto lo svuotamento.
ms.assetid: a3c000e1-18a1-48f7-9e2e-fe63cf13fc5c
title: Metodo CBaseStreamControl. Flushing (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.Flushing
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d4a3a2375ca799f5dd35def03295f29f61c0583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330526"
---
# <a name="cbasestreamcontrolflushing-method"></a>Metodo CBaseStreamControl. Flushing

Il `Flushing` metodo notifica alla classe di base che il pin ha avviato o interrotto lo svuotamento.

## <a name="syntax"></a>Sintassi


```C++
void Flushing(
   BOOL bInProgress
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bInProgress* 
</dt> <dd>

Specifica un valore booleano che indica se il PIN sta per essere scaricato. Usare il valore **true** quando il pin inizia un'operazione di scaricamento e **false** quando il pin termina un'operazione di scaricamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il PIN deve chiamare questo metodo dall'interno dei metodi [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) e [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) . Specificare **true** in **BeginFlush** e **false** in **EndFlush**.

Questo metodo fa in modo che il metodo [**CBaseStreamControl:: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) interrompa l'attesa. Durante lo scaricamento del PIN, **CheckStreamState** restituisce sempre lo \_ scarto del flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Strmctl. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




