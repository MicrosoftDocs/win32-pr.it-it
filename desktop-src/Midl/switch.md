---
title: attributo switch
description: La parola chiave switch seleziona discriminante per un'Unione incapsulata \_ .
ms.assetid: 66179b68-852f-4943-9105-e9fb310f3c2e
keywords:
- cambia attributo MIDL
topic_type:
- apiref
api_name:
- switch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdf9342789d5603a3b64d778bd60364eebde50e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103955975"
---
# <a name="switch-attribute"></a>attributo switch

La parola chiave **Switch** seleziona discriminante per un' [**\_ Unione incapsulata**](encapsulated-unions.md).

``` syntax
switch (switch-type switch-name)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*switch-type* 
</dt> <dd>

Specifica un tipo [**int**](int.md), [**char**](-char.md), [**enum**](enum.md) o un identificatore che viene risolto in uno di questi tipi.

</dd> <dt>

*Switch-name* 
</dt> <dd>

Specifica il nome della variabile di tipo *switch-type* che funge da discriminante di Unione.

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

[**opzione \_**](switch-is.md)
</dt> <dt>

[**tipo di opzione \_**](switch-type.md)
</dt> <dt>

[**Unione**](union.md)
</dt> </dl>

 

 




