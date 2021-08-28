---
description: "Metodo CBaseDispatch.GetTypeInfo: il metodo GetTypeInfo recupera le informazioni sul tipo per l'oggetto, che possono quindi essere usate per ottenere le informazioni sul tipo per un'interfaccia."
ms.assetid: aa06b97c-541b-44fc-bdef-97fd1f014e85
title: Metodo CBaseDispatch.GetTypeInfo (Ctlutil.h)
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
ms.openlocfilehash: 294b9758aa79ab033c1e3cf8932056ca10e7bf2424de97a1cf9f3b509f1906bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076681"
---
# <a name="cbasedispatchgettypeinfo-method"></a>Metodo CBaseDispatch.GetTypeInfo

Il metodo recupera le informazioni sul tipo per l'oggetto , che può quindi essere usato per `GetTypeInfo` ottenere le informazioni sul tipo per un'interfaccia.

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

*Riid* 
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
| <dl> <dt>**TYPE \_ E \_ ELEMENTNOTFOUND**</dt> </dl> | Il *parametro itinfo* non è zero.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo si comporta come **il metodo IDispatch::GetTypeInfo.** Include tuttavia un parametro aggiuntivo, *riid*, che specifica l'interfaccia per cui recuperare le informazioni sul tipo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseDispatch**](cbasedispatch.md)
</dt> </dl>

 

 




