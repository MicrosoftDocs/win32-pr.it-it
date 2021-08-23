---
title: restricted (attributo)
description: L'attributo \ restricted\ specifica che non è possibile chiamare in modo arbitrario una libreria o un membro di un modulo, un'interfaccia o un'interfaccia dispatch.
ms.assetid: ad1ae84f-77f4-4028-bd71-ff01414e474e
keywords:
- attributo con restrizioni MIDL
topic_type:
- apiref
api_name:
- restricted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc68bbea9e1834fd1b1953f8dbf16a79e5356f49bf6058615904d78c244668a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822091"
---
# <a name="restricted-attribute"></a>restricted (attributo)

**\[ L'attributo \] con** restrizioni specifica che non è possibile chiamare arbitrariamente una libreria o un membro di un modulo, un'interfaccia o un'interfaccia dispatch.

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

*statement-type* 
</dt> <dd>

Uno dei seguenti: [**library**](library.md), [**module**](module.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md).

</dd> <dt>

*statement-name* 
</dt> <dd>

Identificatore in base al quale il software fa riferimento a questa istruzione.

</dd> <dt>

*Definizioni* 
</dt> <dd>

Elementi del linguaggio MIDL che definiscono il contenuto di questa istruzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo attributo consente di controllare l'accesso a elementi di interfacce, librerie, moduli e interfacce dispatch. Ad esempio, può impedire l'uso di un elemento di dati da parte di un programmatore di macro. È possibile applicare questo attributo a un membro di [**una coclasse**](coclass.md), indipendentemente dal fatto che sia un'interfaccia o un'interfaccia dispatch e dal fatto che il membro sia un sink (in ingresso) o un'origine (in uscita). Un membro di una **coclasse** non può avere entrambi gli **\[ attributi con \]** restrizioni e **\[ predefiniti. \]**

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

[**Libreria**](library.md)
</dt> <dt>

[**Interfaccia**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**Modulo**](module.md)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 