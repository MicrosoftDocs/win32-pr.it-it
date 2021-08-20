---
title: coclass (attributo)
description: L'istruzione coclass fornisce un elenco delle interfacce supportate per un oggetto componente.
ms.assetid: 2c636327-ad18-4087-b495-d1aa84a07f48
keywords:
- Attributo coclass MIDL
topic_type:
- apiref
api_name:
- coclass
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbd64ed5565797444b58ea71c0b7daf6c083c4810b0876a8b990a7dd281a84c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807307"
---
# <a name="coclass-attribute"></a>coclass (attributo)

**L'istruzione coclass** fornisce un elenco delle interfacce supportate per un oggetto componente.

``` syntax
[
    coclass-attribute-list
]
coclass classname
{
    [
        interface-attributes
    ] 
    [interface | dispinterface] interfacename 
    {
  . . . 
    }
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*coclass-attribute-list* 
</dt> <dd>

**\[** [**L'attributo uuid**](uuid.md) **\]** è obbligatorio in una **coclasse**. Si tratta dello stesso **\[ uuid \]** registrato come CLSID nel database di registrazione del sistema. Gli attributi helpstring , helpcontext , licensed , version , control , hidden e appobject vengono accettati, ma non **\[** [](helpstring.md) **\]** **\[** [](helpcontext.md) **\]** **\[** [](licensed.md) **\]** **\[** [](version.md) **\]** **\[** [](control.md) **\]** **\[** [](hidden.md) **\]** **\[** [](appobject.md) **\]** obbligatori, prima di una **definizione di coclasse.**

</dd> <dt>

*Classname* 
</dt> <dd>

Nome con cui l'oggetto comune è noto nella libreria dei tipi.

</dd> <dt>

*attributi di interfaccia* 
</dt> <dd>

Attributi facoltativi per l'interfaccia o l'interfaccia dispatch. Gli **\[** [**attributi di**](source.md) **\]** origine , **\[** [**predefinito**](default.md) **\]** e **\[** [**con**](restricted.md) restrizioni **\]** vengono accettati in un'interfaccia o interfaccia dispatch all'interno di una **coclasse**.

</dd> <dt>

*interfacename* 
</dt> <dd>

Un'interfaccia dichiarata con la [**parola chiave interface**](interface.md) o un'interfaccia dispatch dichiarata con la parola chiave [**dispinterface.**](dispinterface.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Microsoft Component Object Model definisce una classe come un'implementazione che consente **QueryInterface** tra un set di interfacce.

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("A class"), 
    helpcontext(2481), appobject
] 
coclass myapp 
{ 
    [source] interface IMydocfuncs : IUnknown; 
    dispinterface DMydocfuncs; 
}; 
 
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
coclass mycoclass 
{ 
    [restricted] interface iface1; 
    interface iface2; 
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**appobject**](appobject.md)
</dt> <dt>

[**Controllo**](control.md)
</dt> <dt>

[**Predefinito**](default.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**Nascosto**](hidden.md)
</dt> <dt>

[**Interfaccia**](interface.md)
</dt> <dt>

[**licensed**](licensed.md)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Limitato**](restricted.md)
</dt> <dt>

[**fonte**](source.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> <dt>

[**Versione**](version.md)
</dt> </dl>

 

 