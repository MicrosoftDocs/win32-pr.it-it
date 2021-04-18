---
description: Il metodo GetIDsOfNames esegue il mapping di un set di nomi a un set di DISPID corrispondente.
ms.assetid: 0c0a2726-e89a-4eaf-aab0-e7e9e82e3c34
title: Metodo CBaseDispatch. GetIDsOfNames (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf11e4aa298f924b69c299c2f411dde88e28e5b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324965"
---
# <a name="cbasedispatchgetidsofnames-method"></a>CBaseDispatch. GetIDsOfNames, metodo

Il `GetIDsOfNames` metodo esegue il mapping di un set di nomi a un set di DISPID corrispondente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*riid* 
</dt> <dd>

Riferimento a un identificatore di interfaccia (IID) che specifica l'interfaccia.

</dd> <dt>

*rgszNames* 
</dt> <dd>

Indirizzo di una matrice di stringhe di caratteri wide che contengono i nomi di cui eseguire il mapping.

</dd> <dt>

*CNAME* 
</dt> <dd>

Dimensione della matrice specificata dal parametro *rgszNames* .

</dd> <dt>

*lcid* 
</dt> <dd>

Contesto delle impostazioni locali in cui interpretare i nomi. Può essere **null**.

</dd> <dt>

*rgdispid* 
</dt> <dd>

Puntatore a una matrice che riceve i DISPID. Ogni elemento di riceve un identificatore che corrisponde a uno dei nomi passati nel parametro *rgszNames* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                         | Descrizione                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | Esito positivo.<br/>                                 |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>       | Memoria insufficiente.<br/>                     |
| <dl> <dt>**DISP \_ E \_ unknowname**</dt> </dl> | Uno o più nomi non sono noti.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo si comporta come il metodo **IDispatch:: GetIDsOfNames** , ma il parametro *riid* specifica l'interfaccia su cui recuperare i DISPID. Nella versione di **IDispatch** , il parametro *riid* è riservato.

Se il metodo restituisce DISP \_ E \_ unknowname, i DISPID restituiti contengono DISPID \_ sconosciuto per ogni voce che corrisponde a un nome sconosciuto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseDispatch**](cbasedispatch.md)
</dt> </dl>

 

 




