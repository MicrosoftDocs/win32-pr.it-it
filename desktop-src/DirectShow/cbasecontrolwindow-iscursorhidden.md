---
description: Il metodo IsCursorHidden recupera lo stato corrente del \_ membro dati m bCursorHidden.
ms.assetid: 4b97b89d-876a-470c-ac41-a88fecb52b2d
title: Metodo CBaseControlWindow. IsCursorHidden (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsCursorHidden
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 90f02c6cac5fb3ef1edeaa8e03f7bc54a03acb49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333614"
---
# <a name="cbasecontrolwindowiscursorhidden-method"></a>CBaseControlWindow. IsCursorHidden, metodo

Il `IsCursorHidden` metodo recupera lo stato corrente del membro dati **m \_ bCursorHidden** .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsCursorHidden(
   long *CursorHidden
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CursorHidden* 
</dt> <dd>

Puntatore al valore di **m \_ bCursorHidden**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Quando viene chiamato senza un parametro, restituisce OATRUE se il cursore è nascosto oppure OAFALSE se il cursore è visibile.

## <a name="remarks"></a>Commenti

Gli oggetti interni devono chiamare questa funzione membro senza il parametro *CursorHidden* per evitare di bloccare la sezione critica. Gli oggetti esterni accedono a questa funzione membro con il parametro *CursorHidden* tramite il metodo [**IVideoWindow:: IsCursorHidden**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




