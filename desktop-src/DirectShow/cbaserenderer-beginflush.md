---
description: "Metodo CBaseRenderer.BeginFlush: il metodo BeginFlush avvia un'operazione di scaricamento."
ms.assetid: dc652394-c24e-4cea-ac28-30a1e6de205f
title: Metodo CBaseRenderer.BeginFlush (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 76dfd77a5170a83813871143781868cae55c45ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095939"
---
# <a name="cbaserendererbeginflush-method"></a>Metodo CBaseRenderer.BeginFlush

Il `BeginFlush` metodo avvia un'operazione di scaricamento.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Il pin di input del filtro chiama questo metodo quando riceve una chiamata al metodo [**IPin::BeginFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) Il filtro rilascia il thread di streaming e rilascia qualsiasi esempio contenuto per il rendering.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




