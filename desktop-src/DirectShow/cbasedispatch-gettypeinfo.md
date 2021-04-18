---
description: Il metodo GetTypeInfo recupera le informazioni sul tipo per l'oggetto, che può quindi essere usato per ottenere le informazioni sul tipo per un'interfaccia.
ms.assetid: aa06b97c-541b-44fc-bdef-97fd1f014e85
title: Metodo CBaseDispatch. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f63d79327d2f2bf2a60f06e0290aa34891e78ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327971"
---
# <a name="cbasedispatchgettypeinfo-method"></a>CBaseDispatch. GetTypeInfo, metodo

Il `GetTypeInfo` metodo recupera le informazioni sul tipo per l'oggetto, che può quindi essere usato per ottenere le informazioni sul tipo per un'interfaccia.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTypeInfo(
   REFIID    riid,
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*riid* 
</dt> <dd>

Riferimento a un identificatore di interfaccia (IID) che specifica l'interfaccia.

</dd> <dt>

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



 

## <a name="remarks"></a>Commenti

Questo metodo si comporta come il metodo **IDispatch:: GetTypeInfo** . Tuttavia, include un parametro aggiuntivo, *riid*, che specifica l'interfaccia per la quale recuperare le informazioni sul tipo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseDispatch**](cbasedispatch.md)
</dt> </dl>

 

 




