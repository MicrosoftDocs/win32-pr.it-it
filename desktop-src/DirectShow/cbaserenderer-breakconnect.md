---
description: Il metodo BreakConnect rilascia il pin di input da una connessione.
ms.assetid: e295cec1-8c8f-471c-8832-075ac7708cb1
title: Metodo CBaseRenderer. BreakConnect (Renbase. h)
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
ms.openlocfilehash: 98c1e01c15740616541706ca4d9da3ab5e66538c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329404"
---
# <a name="cbaserendererbreakconnect-method"></a>CBaseRenderer. BreakConnect, metodo

Il `BreakConnect` metodo rilascia il pin di input da una connessione.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                         | Descrizione                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>             | Il PIN non era connesso.<br/>  |
| <dl> <dt>**\_OK**</dt> </dl>                | Esito positivo.<br/>                    |
| <dl> <dt>**VFW \_ E \_ non \_ arrestato**</dt> </dl> | Il filtro è ancora attivo.<br/> |



 

## <a name="remarks"></a>Commenti

Il pin di input del filtro chiama questo metodo dall'interno del proprio `BreakConnect` metodo. Per ulteriori informazioni, vedere [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md). Il filtro esegue una contabilità interna, ad esempio la reimpostazione del flag di fine del flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




