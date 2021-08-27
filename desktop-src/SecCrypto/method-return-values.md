---
description: Il valore restituito per i metodi di interfaccia C++ è sempre di tipo HRESULT. Questo valore può essere controllato per determinare l'esito positivo o negativo.
ms.assetid: f6478e72-0fe9-4c3b-b08a-f71c9c943910
title: Valori restituiti dal metodo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073df1d306fb991d7e1347ff90a21d578bf42583c642a694de3160b405963a28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100761"
---
# <a name="method-return-values"></a>Valori restituiti dal metodo

Il valore restituito per i metodi dell'interfaccia C++ è sempre **di tipo HRESULT;** Questo valore può essere controllato per determinare l'esito positivo o negativo. L'uso di parametri "output" consente di assegnare valori alle variabili durante la chiamata al metodo o alla proprietà. L'esempio seguente illustra una chiamata al metodo C++ per enumerare i provider.


```C++
UINT          ucEnumProvIndex = 0;
BSTR          bstrProvider = NULL;
HRESULT       hr;

// pEnroll is previously instantiated CEnroll interface pointer
hr = pEnroll->enumProviders(ucEnumProvIndex, 0, &bstrProvider);
```



Nel frammento di codice precedente, l'esito positivo o negativo viene restituito alla variabile "hr". Se la chiamata ha esito positivo, hr verrà impostato su S OK e la variabile bstrProvider conterrà il \_ nome del provider enumerato.

Una chiamata C++ per recuperare il valore di una proprietà sarà la seguente.


```C++
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated CEnroll interface pointer

// get the storename
hr = pEnroll->get_CAStoreName( &bstrStoreName );

// (When done using bstrStoreName, free it by calling SysFreeString).
```



Una chiamata C++ per impostare il valore di una proprietà sarà la seguente.


```C++
// bstrNewName previously set to a valid store name
hr = pEnroll->put_CAStoreName( bstrNewName );
```



 

 



