---
description: "Metodo CMediaPosition.GetTypeInfo: il metodo GetTypeInfo recupera le informazioni sul tipo per l'oggetto, che possono quindi essere usate per ottenere le informazioni sul tipo per un'interfaccia."
ms.assetid: 0a04c43d-8b4b-4780-b02f-04053c405c77
title: Metodo CMediaPosition.GetTypeInfo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7827a3599f05061b5760084bed46cd2554b45f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099139"
---
# <a name="cmediapositiongettypeinfo-method"></a>Metodo CMediaPosition.GetTypeInfo

Il metodo recupera le informazioni sul tipo per l'oggetto , che può quindi essere usato per `GetTypeInfo` ottenere le informazioni sul tipo per un'interfaccia.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*itinfo* 
</dt> <dd>

Informazioni sul tipo da restituire. Deve essere zero.

</dd> <dt>

*lcid* 
</dt> <dd>

Identificatore delle impostazioni locali.

</dd> <dt>

*pptinfo* 
</dt> <dd>

Indirizzo di una variabile che riceve un **puntatore ITypeInfo.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                             | Descrizione                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Operazione completata.<br/>                            |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>               | Argomento del puntatore **NULL.**<br/>          |
| <dl> <dt>**TIPO \_ E \_ ELEMENTNOTFOUND**</dt> </dl> | Il *parametro itinfo* non è zero.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




