---
title: Attributo switch
description: La parola chiave switch seleziona il discriminante per un'unione \_ incapsulata.
ms.assetid: 66179b68-852f-4943-9105-e9fb310f3c2e
keywords:
- attributo switch MIDL
topic_type:
- apiref
api_name:
- switch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422b52a339a83cbaf59a9d65c0ed0e4e7e41533dcbf0be962147327145588a7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013549"
---
# <a name="switch-attribute"></a>Attributo switch

La parola chiave **switch** seleziona il discriminante per [**un'unione \_ incapsulata.**](encapsulated-unions.md)

``` syntax
switch (switch-type switch-name)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*switch-type* 
</dt> <dd>

Specifica un [**tipo int**](int.md), [**char**](-char.md), [**enum**](enum.md) o un identificatore che viene risolto in uno di questi tipi.

</dd> <dt>

*switch-name* 
</dt> <dd>

Specifica il nome della variabile di tipo *switch-type* che funge da discriminante dell'unione.

</dd> </dl>

## <a name="examples"></a>Esempi

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[Unioni non incapsulate](nonencapsulated-unions.md)
</dt> <dt>

[**\_l'opzione è**](switch-is.md)
</dt> <dt>

[**tipo di \_ commutatore**](switch-type.md)
</dt> <dt>

[**Unione**](union.md)
</dt> </dl>

 

 




