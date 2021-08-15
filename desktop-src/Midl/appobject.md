---
title: appobject (attributo)
description: L'attributo \ appobject\ identifica la coclasse come oggetto applicazione, associato a un'applicazione EXE completa.
ms.assetid: f4fcdf55-7431-4d66-8a46-f741c52fbe56
keywords:
- Attributo appobject MIDL
topic_type:
- apiref
api_name:
- appobject
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54cbe8d5c1c7a573216ae9cb55075ba3b3766d0d8c7898233be9364488131e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808333"
---
# <a name="appobject-attribute"></a>appobject (attributo)

**\[ L'attributo \] appobject** identifica la [**coclasse**](coclass.md) come oggetto applicazione, associato a un'applicazione EXE completa.

``` syntax
[
    uuid(uuid-number), 
    appobject 
  [, coclass-attribute-list]
]
coclass classname 
{ 
    [coclass definition]
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*uuid-number* 
</dt> <dd>

Specifica un numero di identificazione univoco universale per la [**coclasse**](coclass.md).

</dd> <dt>

*coclass-attribute-list* 
</dt> <dd>

Specifica zero o più attributi che si applicano [**all'istruzione coclasse.**](coclass.md) Gli attributi **di coclasse** consentiti [**\[ sono \] helpstring**](helpstring.md), [**\[ helpcontext \]**](helpcontext.md), [**\[ licensed \]**](licensed.md), [**\[ version \]**](version.md), [**\[ control \]**](control.md)e [**\[ hidden \]**](hidden.md).

</dd> <dt>

*Classname* 
</dt> <dd>

Specifica il nome con cui l'oggetto componente è noto nella libreria dei tipi.

</dd> <dt>

*definizione di coclasse* 
</dt> <dd>

Specifica le istruzioni che costituiscono la definizione [**della coclasse.**](coclass.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

**\[ L'attributo \] appobject** indica anche che le funzioni e le proprietà della [**coclasse**](coclass.md) sono disponibili a livello globale nella libreria dei tipi corrente.

La rappresentazione typeflag per questo attributo è TYPEFLAG \_ FAPPOBJECT

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**coclass**](coclass.md)
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

[**licensed**](licensed.md)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Versione**](version.md)
</dt> </dl>

 

 