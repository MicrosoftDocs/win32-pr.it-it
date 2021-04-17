---
description: Restituisce un valore HRESULT. In questo HRESULT, un valore di S \_ OK indica che il metodo è stato eseguito correttamente.
ms.assetid: 6722a74a-1ec1-4c71-84c6-fb103aca149f
title: Proprietà del controllo di registrazione certificati in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76525f26f318178f122cc0feee6221bbd948bba0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525831"
---
# <a name="certificate-enrollment-control-properties-in-c"></a>Proprietà del controllo di registrazione certificati in C++

Quando si imposta o Recupera una proprietà del controllo di registrazione certificati in C++, la chiamata al metodo restituisce un valore **HRESULT**. In questo **HRESULT**, un valore di S \_ OK indica che il metodo è stato eseguito correttamente.

I programmi scritti in C++ possono recuperare le proprietà del controllo di registrazione certificati per chiamate al metodo nel formato seguente.


```C++
#include <windows.h>

HRESULT get_propertyName( datatype * pPropValue);
```



Dove *PropertyName* specifica il nome della proprietà a cui si accede e *pPropValue* è un puntatore a una variabile con il tipo di dati appropriato. Al termine di questa chiamata al metodo, *pPropValue* punterà alla variabile che contiene il valore della proprietà *PropertyName* .

Ad esempio, per recuperare il valore per la proprietà **RootStoreType** , usare il codice seguente.


```C++
// Get the store type.
// hr is an HRESULT.
// bstrStoreType is a BSTR variable.
hr = pEnroll->get_RootStoreType( &bstrStoreType );
```



I programmi scritti in C++ possono impostare le proprietà del controllo di registrazione dei certificati chiamando i metodi nel formato seguente.


```C++
#include <windows.h>

HRESULT put_propertyName( datatype PropValue);
```



Dove *PropertyName* specifica il nome della proprietà a cui si accede e *PropValue* è un valore del tipo di dati appropriato. Al termine di questa chiamata al metodo, il nuovo valore della proprietà *PropertyName* sarà *PropValue*.

Ad esempio, per impostare il valore della proprietà per **RootStoreType**, è possibile usare il codice seguente.


```C++
// Set the store type.
// bstrNewType previously set to a valid store type
hr = pEnroll->put_RootStoreType( bstrNewType );
```



 

 



