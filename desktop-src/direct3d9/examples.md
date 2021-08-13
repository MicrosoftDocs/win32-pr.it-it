---
description: Seguono due definizioni di modello binario di esempio e un esempio di oggetto dati binario.
ms.assetid: vs|directx_sdk|~\examples.htm
title: Esempi (grafica Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f8b8e2a9c500042e9b8d7c7fd911ab74b2f428d1ef814aca9e5fda1be7dcab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523098"
---
# <a name="examples-direct3d-9-graphics"></a>Esempi (grafica Direct3D 9)

Seguono due definizioni di modello binario di esempio e un esempio di oggetto dati binario.

> [!Note]  
> I dati vengono archiviati in formato little-endian, che non è illustrato in questi esempi.

 

Il modello chiuso RGB è identificato dall'UUID {55b6d780-37ec-11d0-ab39-0020af71e433} e ha tre membri, r, g e b, ognuno di tipo float.


```
TOKEN_TEMPLATE, TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_OBRACE,
TOKEN_GUID, 55b6d780, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_FLOAT, TOKEN_NAME, 1, 'r', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'g', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'b', TOKEN_SEMICOLON,
TOKEN_CBRACE
```



Il modello chiuso Matrix4x4 è identificato dall'UUID {55b6d781-37ec-11d0-ab39-0020af71e433} e ha un membro, una matrice bidimensionale denominata matrix, di tipo float.


```
TOKEN_TEMPLATE, TOKEN_NAME, 9, 'M', 'a', 't', 'r', 'i', 'x', '4', 'x', '4', TOKEN_OBRACE,
TOKEN_GUID, 55b6d781, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_ARRAY, TOKEN_FLOAT, TOKEN_NAME, 6, 'm', 'a', 't', 'r', 'i', 'x',
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_CBRACE
```



L'oggetto dati binario che segue mostra un'istanza del modello RGB definito in precedenza. L'oggetto di esempio è denominato blu e i tre membri, r, g e b, hanno rispettivamente i valori 0,0, 0,0 e 1,0.


```
TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_NAME, 4, 'b', 'l', 'u', 'e', TOKEN_OBRACE,
TOKEN_FLOAT_LIST, 3, 0.0, 0.0, 1.0, TOKEN_CBRACE
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codifica binaria](binary-encoding.md)
</dt> </dl>

 

 



