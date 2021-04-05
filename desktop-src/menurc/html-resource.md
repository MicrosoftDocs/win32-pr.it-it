---
title: Risorsa HTML
description: Definisce un file HTML.
ms.assetid: d3cf8348-8c10-41d9-a061-cdce0e13abf4
keywords:
- Menu risorse HTML e altre risorse
topic_type:
- apiref
api_name:
- HTML
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9db6477aed5180ae18b99f53f4ebadf9d0ad0c91
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857494"
---
# <a name="html-resource"></a>Risorsa HTML

Definisce un file HTML.

``` syntax
nameID HTML filename
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nome univoco o valore di Unsigned Integer a 16 bit che identifica la risorsa.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*filename*
</dt> <dd>

Nome del file HTML. Deve essere un percorso completo o relativo se il file non si trova nella directory di lavoro corrente. Il percorso deve essere una stringa racchiusa tra virgolette.

</dd> </dl>

## <a name="examples"></a>Esempio

Nell'esempio seguente viene definita una risorsa HTML:

``` syntax
ID_RESPONSE_ERROR_PAGE  HTML "res\\responseerorpage.htm"
```

 

 




