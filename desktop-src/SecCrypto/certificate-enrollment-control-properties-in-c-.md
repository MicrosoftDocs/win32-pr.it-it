---
description: Restituisce un HRESULT. In questo caso, un valore HRESULT di S \_ OK indica che il metodo è stato eseguito correttamente.
ms.assetid: 6722a74a-1ec1-4c71-84c6-fb103aca149f
title: Proprietà del controllo registrazione certificati in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0941967b7b4be0bfa6d7db2f9b31e2971f8ca1d0deb9d9f92540a1ae5300791a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771920"
---
# <a name="certificate-enrollment-control-properties-in-c"></a>Proprietà del controllo registrazione certificati in C++

Quando si imposta o si recupera una proprietà certificate enrollment control in C++, la chiamata al metodo restituisce un **HRESULT.** In questo caso **un HRESULT**, un valore S \_ OK indica che il metodo è stato eseguito correttamente.

I programmi scritti in C++ possono recuperare le proprietà del controllo di registrazione certificati tramite chiamate al metodo nel formato seguente.


```C++
#include <windows.h>

HRESULT get_propertyName( datatype * pPropValue);
```



Dove *propertyName* specifica il nome della proprietà a cui si accede e *pPropValue* è un puntatore a una variabile del tipo di dati appropriato. Al termine della chiamata al metodo, *pPropValue* farà riferimento alla variabile che contiene il valore della *proprietà propertyName.*

Ad esempio, per recuperare il valore per **la proprietà RootStoreType,** usare il codice seguente.


```C++
// Get the store type.
// hr is an HRESULT.
// bstrStoreType is a BSTR variable.
hr = pEnroll->get_RootStoreType( &bstrStoreType );
```



I programmi scritti in C++ possono impostare le proprietà del controllo di registrazione certificati chiamando i metodi nel formato seguente.


```C++
#include <windows.h>

HRESULT put_propertyName( datatype PropValue);
```



Dove *propertyName* specifica il nome della proprietà a cui si accede e *PropValue* è un valore del tipo di dati appropriato. Al termine della chiamata al metodo, il nuovo valore della proprietà *propertyName* sarà *PropValue*.

Ad esempio, per impostare il valore della proprietà per **RootStoreType,** è possibile usare il codice seguente.


```C++
// Set the store type.
// bstrNewType previously set to a valid store type
hr = pEnroll->put_RootStoreType( bstrNewType );
```



 

 



