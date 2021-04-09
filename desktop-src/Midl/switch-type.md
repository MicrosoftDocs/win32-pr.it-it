---
title: switch_type (attributo)
description: L'attributo \ Switch \_ Type \ identifica il tipo della variabile utilizzata come unione discriminante. Il tipo di opzione può essere un Integer, un carattere, un valore booleano o un tipo di enumerazione.
ms.assetid: e4c6d33b-d4db-42b7-9d18-fd14bf1fb530
keywords:
- attributo switch_type MIDL
topic_type:
- apiref
api_name:
- switch_type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14184c5838d9f671f75536714d73c3f6ebf00a0a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857454"
---
# <a name="switch_type-attribute"></a>Switch \_ type-attributo

L'attributo **\[ Switch \_ Type \]** identifica il tipo della variabile utilizzata come unione discriminante. Il tipo di opzione può essere un Integer, un carattere, un valore booleano o un tipo di enumerazione.

``` syntax
switch_type(switch-type-specifier)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*switch-type-specifier* 
</dt> <dd>

Specifica un tipo [**int**](int.md), [**char**](char-idl.md), [**Boolean**](boolean.md)o [**enum**](enum.md) o un identificatore di tale tipo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Mentre l'attributo **\[ Switch \_ Type \]** identifica il tipo di variabile, l' **\[** [**opzione \_ is**](switch-is.md) **\]** attribute specifica il nome del parametro che rappresenta l'unione discriminante. L'attributo **\[ Switch \_ Type \]** si applica ai parametri o ai membri di strutture o unioni.

L'Unione e il relativo discriminante devono essere specificati allo stesso livello logico. Quando l'Unione è un parametro, il discriminante di Unione deve essere un altro parametro. Quando l'Unione è un campo di una struttura, discriminante deve essere un altro campo della struttura allo stesso livello del campo di Unione.

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

[**char**](char-idl.md)
</dt> <dt>

[Unioni incapsulate](encapsulated-unions.md)
</dt> <dt>

[**enum**](enum.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[Unioni non incapsulate](nonencapsulated-unions.md)
</dt> <dt>

[**opzione \_**](switch-is.md)
</dt> <dt>

[**Unione**](union.md)
</dt> </dl>

 

 




