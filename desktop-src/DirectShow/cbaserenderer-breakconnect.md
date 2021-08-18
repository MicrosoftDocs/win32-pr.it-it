---
description: Il metodo BreakConnect rilascia il pin di input da una connessione.
ms.assetid: e295cec1-8c8f-471c-8832-075ac7708cb1
title: Metodo CBaseRenderer.BreakConnect (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cefaa91578f397a5ce967dc9cb6200acbe45f016e81f4552b9d185ad9ffa2609
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044061"
---
# <a name="cbaserendererbreakconnect-method"></a>Metodo CBaseRenderer.BreakConnect

Il `BreakConnect` metodo rilascia il pin di input da una connessione.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                         | Descrizione                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>             | Il pin non è connesso.<br/>  |
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operazione completata.<br/>                    |
| <dl> <dt>**VFW \_ E \_ NON \_ ARRESTATO**</dt> </dl> | Il filtro è ancora attivo.<br/> |



 

## <a name="remarks"></a>Commenti

Il pin di input del filtro chiama questo metodo dall'interno del proprio `BreakConnect` metodo . Per altre informazioni, vedere [**CBasePin::BreakConnect.**](cbasepin-breakconnect.md) Il filtro esegue alcune attività di bookkeeping interne, ad esempio la reimpostazione del flag di fine flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




