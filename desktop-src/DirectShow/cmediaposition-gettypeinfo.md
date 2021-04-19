---
description: Il metodo GetTypeInfo recupera le informazioni sul tipo per l'oggetto, che può quindi essere usato per ottenere le informazioni sul tipo per un'interfaccia.
ms.assetid: 0a04c43d-8b4b-4780-b02f-04053c405c77
title: Metodo CMediaPosition. GetTypeInfo (Ctlutil. h)
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
ms.openlocfilehash: 6fa776ca71daff67185bf9fd2c1727f9535f8ac4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332331"
---
# <a name="cmediapositiongettypeinfo-method"></a>CMediaPosition. GetTypeInfo, metodo

Il `GetTypeInfo` metodo recupera le informazioni sul tipo per l'oggetto, che può quindi essere usato per ottenere le informazioni sul tipo per un'interfaccia.

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

*ppTInfo* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore **ITypeInfo** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                             | Descrizione                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Esito positivo.<br/>                            |
| <dl> <dt>**\_puntatore E**</dt> </dl>               | Argomento puntatore **null** .<br/>          |
| <dl> <dt>**Digitare \_ E \_ ELEMENTNOTFOUND**</dt> </dl> | Il parametro *itinfo* è diverso da zero.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




