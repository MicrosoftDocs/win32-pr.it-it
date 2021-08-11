---
title: Risorsa FONT
description: Definisce un file che contiene un tipo di carattere.
ms.assetid: 0e19edd5-6cfc-44e6-add4-7413eb94867a
keywords:
- Menu delle risorse FONT e altre risorse
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf08abd68d5d99640435d355609d5647c71116f9fa29c137ba67a311d41f493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235273"
---
# <a name="font-resource"></a>Risorsa FONT

Definisce un file che contiene un tipo di carattere.

``` syntax
nameID FONT filename
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*Nameid*
</dt> <dd>

Valore intero senza segno a 16 bit univoco che identifica la risorsa.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Filename*
</dt> <dd>

Nome del file che contiene la risorsa. Il nome deve essere un nome di file valido. deve essere un percorso completo se il file non si trova nella directory di lavoro corrente. Il percorso deve essere una stringa tra virgolette.

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [Attributi comuni delle risorse](common-resource-attributes.md).

## <a name="examples"></a>Esempio

L'esempio seguente definisce una singola risorsa carattere:

``` syntax
5 FONT  "cmroman.fnt"
```

 

 




