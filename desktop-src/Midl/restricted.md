---
title: restricted (attributo)
description: L'attributo \ Restricted \ specifica che una libreria o un membro di un modulo, un'interfaccia o un'interfaccia dispatch non può essere chiamata in modo arbitrario.
ms.assetid: ad1ae84f-77f4-4028-bd71-ff01414e474e
keywords:
- attributo MIDL limitato
topic_type:
- apiref
api_name:
- restricted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca610c0dcf29ebc3a767005b4c22e3231947e88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398958"
---
# <a name="restricted-attribute"></a>restricted (attributo)

L'attributo **\[ Restricted \]** specifica che una libreria o un membro di un modulo, un'interfaccia o un'interfaccia dispatch non può essere chiamata in modo arbitrario.

``` syntax
[
    restricted
    [, other-attributes]
] 
statement-type statement-name 
{
    definitions
};
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*altri attributi* 
</dt> <dd>

Zero o più attributi MIDL.

</dd> <dt>

*tipo di istruzione* 
</dt> <dd>

Uno dei seguenti: [**libreria**](library.md), [**modulo**](module.md), [**interfaccia**](interface.md), interfaccia [**Dispatch**](dispinterface.md).

</dd> <dt>

*nome istruzione* 
</dt> <dd>

Identificatore con cui il software fa riferimento a questa istruzione.

</dd> <dt>

*definizioni* 
</dt> <dd>

Elementi del linguaggio MIDL che definiscono il contenuto di questa istruzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo attributo consente di controllare l'accesso a elementi di interfacce, librerie, moduli e dispinterfaces. Ad esempio, può impedire l'utilizzo di un elemento di dati da un programmatore di macro. È possibile applicare questo attributo a un membro di una [**coclasse**](coclass.md), indipendentemente dal fatto che il membro sia un'interfaccia dispatch o un'interfaccia e indipendentemente dal fatto che il membro sia un sink (in ingresso) o un'origine (in uscita). Un membro di una **coclasse** non può avere sia gli attributi **\[ limitati \]** che quelli **\[ predefiniti \]** .

### <a name="flags"></a>Flags

IMPLTYPEFLAG \_ FRESTRICTED, FUNCFLAG \_ FRESTRICTED

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version (1.0), 
    restricted
] 
library MyLibrary
{
    // Library definition statements.
};

[propget, restricted] HRESULT MyProc(void);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**libreria**](library.md)
</dt> <dt>

[**interfaccia**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**modulo**](module.md)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 