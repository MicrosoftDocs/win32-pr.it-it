---
description: Costruttore CTransInPlaceFilter.CTransInPlaceFilter - Metodo costruttore.
ms.assetid: f0d30125-5d16-470c-a5fb-a7df96814dad
title: Costruttore CTransInPlaceFilter.CTransInPlaceFilter (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6b14af4b0d1f33933db8ca2fd1835e9711edad9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084779"
---
# <a name="ctransinplacefilterctransinplacefilter-constructor"></a>Costruttore CTransInPlaceFilter.CTransInPlaceFilter

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CTransInPlaceFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   REFCLSID  clsid,
   HRESULT   *phr,
   bool      bModifiesData = TRUE
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pObjectName* 
</dt> <dd>

Stringa contenente il nome di debug del filtro. Per altre informazioni, vedere [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*lpUnk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** di aggregazione. In caso contrario, impostare questo parametro su **NULL.**

</dd> <dt>

*Clsid* 
</dt> <dd>

Identificatore di classe del filtro.

</dd> <dt>

*Phr* 
</dt> <dd>

Ignorato.

</dd> <dt>

*bModifiesData* 
</dt> <dd>

Valore booleano che specifica se il filtro modifica i dati di input. Se **TRUE,** il filtro modifica i dati. In caso contrario, il filtro passa i dati a valle senza modifiche.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




