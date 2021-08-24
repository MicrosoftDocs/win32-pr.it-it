---
title: licensed (attributo)
description: L'attributo \ licensed\ indica che la coclasse a cui si applica è concessa in licenza e deve essere creata un'istanza usando IClassFactory2.
ms.assetid: c4789ea2-8ff6-423e-8b69-22a7a5392854
keywords:
- attributo concesso in licenza MIDL
topic_type:
- apiref
api_name:
- licensed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b4320157216db18f595d67e172bc49de2d6050551732265060cb5a21339c908
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067207"
---
# <a name="licensed-attribute"></a>licensed (attributo)

**\[ \] L'attributo** licensed indica che la [**coclasse**](coclass.md) a cui si applica è concessa in licenza e deve essere creata un'istanza [**usando IClassFactory2.**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2)

``` syntax
[
    licensed
    [ , attribute-list ] 
]
coclass classname 
{
  coclass-definition
};
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*attribute-list* 
</dt> <dd>

Specifica zero o più attributi che si applicano [**all'istruzione coclasse.**](coclass.md) Gli attributi **di coclasse** consentiti **\[** [**sono helpstring,**](helpstring.md) **\]** **\[** [**helpcontext,**](helpcontext.md) **\]** **\[ licensed, \]** **\[** [**version,**](version.md) **\]** **\[** [**control**](control.md) **\]** e **\[** [**hidden.**](hidden.md) **\]**

</dd> <dt>

*Classname* 
</dt> <dd>

Specifica il nome con cui l'oggetto componente è noto nella libreria dei tipi.

</dd> <dt>

*coclass-definition* 
</dt> <dd>

Specifica le istruzioni che costituiscono la definizione [**della coclasse.**](coclass.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La gestione delle licenze è una funzionalità di COM che consente il controllo sulla creazione di oggetti. Gli oggetti concessi in licenza possono essere creati solo dai client autorizzati a usarli. Le licenze vengono implementate in COM tramite [**l'interfaccia IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) e il supporto per un codice di licenza che può essere passato in fase di esecuzione.

### <a name="flags"></a>Flags

TYPEFLAG \_ FLICENSED

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    licensed, 
    helpstring("A meaningfulcomment"
]
coclass MyClass
{
    // coclass definition statements
};
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[Contenuto di una libreria dei tipi](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**Controllo**](control.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**Nascosto**](hidden.md)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Versione**](version.md)
</dt> </dl>

 

 