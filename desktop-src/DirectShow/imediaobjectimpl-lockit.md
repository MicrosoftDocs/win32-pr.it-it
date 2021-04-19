---
description: La classe LockIt è una classe interna che blocca e sblocca DMO.
ms.assetid: f516ce22-17ad-488e-a768-3f3849c56087
title: 'Classe IMediaObjectImpl:: LockIt (Dmoimpl. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24fe896ea293ec5e60b038f908cab794274d26e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326273"
---
# <a name="imediaobjectimpllockit-class"></a>Classe IMediaObjectImpl:: LockIt

La `LockIt` classe è una classe interna che blocca e sblocca DMO.

``` syntax
LockIt(
    _DERIVED_ *p
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="p"></span><span id="P"></span>*p*
</dt> <dd>

Puntatore all'oggetto derivato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il `LockIt` Costruttore blocca il DMO e il distruttore Sblocca il DMO. Per bloccare l'oggetto dall'interno della classe derivata, dichiarare una variabile locale di tipo `LockIt` . DMO è bloccato mentre l' `LockIt` oggetto rimane nell'ambito:


```C++
void SomeMethod()
{
    // The DMO is not locked.
    {
        LockIt dmoLock(this); // Locks the DMO.
        /* ... */
    } 
    // dmoLock goes out of scope, DMO is unlocked.
}
```



I metodi in **IMediaObjectImpl** bloccano automaticamente DMO.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Dmoimpl. h</dt> </dl>                                                                     |
| Libreria<br/> | <dl> <dt>Dmoguids. lib; </dt> <dt>Msdmo. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Modello di classe IMediaObjectImpl**](imediaobjectimpl-class-template.md)
</dt> </dl>

 

 




