---
description: 'Costruttore CBaseStreamControl.CBaseStreamControl : metodo costruttore.'
ms.assetid: c0eff80f-04d3-4919-bb27-1b76c1bd1cce
title: Costruttore CBaseStreamControl.CBaseStreamControl (Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4c6521bec65e0182b8eb48eb5d3efe9ea609c6a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095849"
---
# <a name="cbasestreamcontrolcbasestreamcontrol-constructor"></a>Costruttore CBaseStreamControl.CBaseStreamControl

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CBaseStreamControl(
   HRESULT *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Phr* 
</dt> <dd>

Puntatore a **un valore HRESULT.** Se il costruttore ha esito negativo, questo parametro riceve un codice di errore. In questo caso, l'oggetto non è in uno stato valido.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Strmctl.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




