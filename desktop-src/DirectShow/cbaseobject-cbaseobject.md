---
description: 'Costruttore CBaseObject.CBaseObject : metodo costruttore.'
ms.assetid: 20c3c4af-b22f-4b74-a6b6-5ee309de4eef
title: Costruttore CBaseObject.CBaseObject (Combase.h)
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
ms.openlocfilehash: 35443d212fc244c80da958f2f87d03363c59348be4189393c1c3493521a0439b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076581"
---
# <a name="cbaseobjectcbaseobject-constructor"></a>Costruttore CBaseObject.CBaseObject

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CBaseObject(
   const TCHAR *pName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Stringa che contiene il nome dell'oggetto a scopo di debug.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo metodo incrementa il conteggio degli oggetti attivi. Vedere [**CBaseObject::ObjectsActive.**](cbaseobject-objectsactive.md)

Allocare il *parametro pName* nella memoria statica:


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



La macro [**NAME**](name.md) viene compilata come **NULL nelle** build per la vendita al dettaglio, in modo che le stringhe statiche vengano visualizzate solo nelle build di debug. Per altre informazioni, vedere [**DbgDumpObjectRegister.**](dbgdumpobjectregister.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Combase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseObject**](cbaseobject.md)
</dt> </dl>

 

 




