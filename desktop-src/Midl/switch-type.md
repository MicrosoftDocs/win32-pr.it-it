---
title: switch_type (attributo)
description: L'attributo \ switch \_ type\ identifica il tipo della variabile usata come discriminante dell'unione. Il tipo switch può essere un integer, un carattere, un valore booleano o un tipo di enumerazione.
ms.assetid: e4c6d33b-d4db-42b7-9d18-fd14bf1fb530
keywords:
- switch_type attributo MIDL
topic_type:
- apiref
api_name:
- switch_type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8695a17c60f9785d7782d77db839499306a9577755e8a6838540f5a0fc2cea48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146234"
---
# <a name="switch_type-attribute"></a>Attributo del \_ tipo di opzione

**\[ \_ L'attributo \] switch** type identifica il tipo della variabile usata come discriminante dell'unione. Il tipo switch può essere un integer, un carattere, un valore booleano o un tipo di enumerazione.

``` syntax
switch_type(switch-type-specifier)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*switch-type-specifier* 
</dt> <dd>

Specifica un [**tipo int**](int.md), [**char**](char-idl.md), [**Boolean**](boolean.md)o [**enum**](enum.md) o un identificatore di tale tipo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Mentre **\[ \_ l'attributo del tipo \]** di opzione identifica il tipo di variabile, l'opzione è l'attributo che specifica il nome del parametro che rappresenta la **\[** [**\_**](switch-is.md) **\]** discriminante dell'unione. **\[ \_ L'attributo \] del** tipo switch si applica a parametri o membri di strutture o unioni.

L'unione e il relativo discriminante devono essere specificati allo stesso livello logico. Quando l'unione è un parametro, la discriminante dell'unione deve essere un altro parametro. Quando l'unione è un campo di una struttura, il discriminante deve essere un altro campo della struttura allo stesso livello del campo di unione.

## <a name="examples"></a>Esempi

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Boolean**](boolean.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[Unioni incapsulate](encapsulated-unions.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[Unioni non incapsulate](nonencapsulated-unions.md)
</dt> <dt>

[**\_l'opzione è**](switch-is.md)
</dt> <dt>

[**Unione**](union.md)
</dt> </dl>

 

 




