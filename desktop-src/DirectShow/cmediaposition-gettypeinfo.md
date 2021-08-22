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
ms.openlocfilehash: 5a23632078fb4aa9b3aaa3f80c9c85ea5f8e0d0adfff49a057dc5b554f104fa3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832421"
---
# <a name="cmediapositiongettypeinfo-method"></a>Metodo CMediaPosition.GetTypeInfo

Il metodo recupera le informazioni sul tipo per l'oggetto , che possono quindi essere usate per `GetTypeInfo` ottenere le informazioni sul tipo per un'interfaccia.

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

Digitare le informazioni da restituire. Deve essere zero.

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
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>               | Argomento del puntatore **NULL.**<br/>          |
| <dl> <dt>**TIPO \_ E \_ ELEMENTNOTFOUND**</dt> </dl> | Il *parametro itinfo* non è zero.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




