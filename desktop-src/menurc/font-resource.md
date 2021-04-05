---
title: Risorsa carattere
description: Definisce un file che contiene un tipo di carattere.
ms.assetid: 0e19edd5-6cfc-44e6-add4-7413eb94867a
keywords:
- Menu delle risorse dei tipi di carattere e altre risorse
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e205d80779a1a228ee50e062f6904c1ed4a4934
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718739"
---
# <a name="font-resource"></a>Risorsa carattere

Definisce un file che contiene un tipo di carattere.

``` syntax
nameID FONT filename
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Valore Unsigned Integer univoco a 16 bit che identifica la risorsa.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*filename*
</dt> <dd>

Nome del file che contiene la risorsa. Il nome deve essere un nome di file valido. deve essere un percorso completo se il file non si trova nella directory di lavoro corrente. Il percorso deve essere una stringa racchiusa tra virgolette.

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene definita una singola risorsa del tipo di carattere:

``` syntax
5 FONT  "cmroman.fnt"
```

 

 




