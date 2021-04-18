---
description: Il valore restituito per i metodi dell'interfaccia C++ è sempre di tipo HRESULT; Questo valore può essere controllato per determinare l'esito positivo o negativo.
ms.assetid: f6478e72-0fe9-4c3b-b08a-f71c9c943910
title: Valori restituiti dal metodo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3871cf00bd48c7fbe1432ec86b503fba7795592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307690"
---
# <a name="method-return-values"></a>Valori restituiti dal metodo

Il valore restituito per i metodi dell'interfaccia C++ è sempre di tipo **HRESULT**; Questo valore può essere controllato per determinare l'esito positivo o negativo. L'uso dei parametri "output" consente l'assegnazione di valori alle variabili durante la chiamata al metodo o alla proprietà. Nell'esempio seguente viene illustrata una chiamata al metodo C++ per enumerare i provider.


```C++
UINT          ucEnumProvIndex = 0;
BSTR          bstrProvider = NULL;
HRESULT       hr;

// pEnroll is previously instantiated CEnroll interface pointer
hr = pEnroll->enumProviders(ucEnumProvIndex, 0, &bstrProvider);
```



Nel frammento di codice precedente, l'esito positivo o negativo viene restituito alla variabile "HR". Se la chiamata ha esito positivo, HR verrà impostato su S \_ OK e la variabile bstrProvider conterrà il nome del provider enumerato.

Una chiamata C++ per recuperare il valore di una proprietà è la seguente.


```C++
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated CEnroll interface pointer

// get the storename
hr = pEnroll->get_CAStoreName( &bstrStoreName );

// (When done using bstrStoreName, free it by calling SysFreeString).
```



Una chiamata C++ per impostare un valore della proprietà sarà come segue.


```C++
// bstrNewName previously set to a valid store name
hr = pEnroll->put_CAStoreName( bstrNewName );
```



 

 



