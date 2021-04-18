---
description: Metodo del costruttore.
ms.assetid: 20c3c4af-b22f-4b74-a6b6-5ee309de4eef
title: Costruttore CBaseObject. CBaseObject (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b13fe906af1900dbf067e8aa9273d811b3c1ef3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324689"
---
# <a name="cbaseobjectcbaseobject-constructor"></a>Costruttore CBaseObject. CBaseObject

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CBaseObject(
   const TCHAR *pName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pName* 
</dt> <dd>

Stringa che contiene il nome dell'oggetto, a scopo di debug.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo metodo incrementa il conteggio degli oggetti attivi. Vedere [**CBaseObject:: ObjectsActive**](cbaseobject-objectsactive.md).

Allocare il parametro *pname* nella memoria statica:


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



La macro del [**nome**](name.md) viene compilata in **null** nelle compilazioni finali, in modo che le stringhe statiche vengano visualizzate solo nelle build di debug. Per ulteriori informazioni, vedere [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseObject**](cbaseobject.md)
</dt> </dl>

 

 




