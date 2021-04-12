---
title: coclass (attributo)
description: L'istruzione coclass fornisce un elenco delle interfacce supportate per un oggetto Component.
ms.assetid: 2c636327-ad18-4087-b495-d1aa84a07f48
keywords:
- attributo coclass MIDL
topic_type:
- apiref
api_name:
- coclass
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba95b38675869637c679a2409a82fb812709ec8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398960"
---
# <a name="coclass-attribute"></a>coclass (attributo)

L'istruzione **coclass** fornisce un elenco delle interfacce supportate per un oggetto Component.

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

*coclass-Attribute-List* 
</dt> <dd>

L' **\[** attributo [**UUID**](uuid.md) **\]** è obbligatorio in una **coclasse**. Si tratta dello stesso **\[ UUID \]** registrato come CLSID nel database di registrazione del sistema. Gli **\[** attributi [**helpstring**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**licensed**](licensed.md) **\]** , **\[** [**Version**](version.md) **\]** , **\[** [**Control**](control.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** e **\[** [**appobject**](appobject.md) **\]** sono accettati, ma non necessari, prima di una definizione di **coclasse** .

</dd> <dt>

*ClassName* 
</dt> <dd>

Nome con cui l'oggetto comune è noto nella libreria dei tipi.

</dd> <dt>

*Interface-attributi* 
</dt> <dd>

Attributi facoltativi per l'interfaccia o l'interfaccia dispatch. Gli **\[** attributi [**source**](source.md) **\]** , **\[** [**default**](default.md) **\]** e **\[** [**Restricted**](restricted.md) **\]** sono accettati in un'interfaccia o in un'interfaccia dispatch all'interno di una **coclasse**.

</dd> <dt>

*NomeInterfaccia* 
</dt> <dd>

Interfaccia dichiarata con la parola chiave [**Interface**](interface.md) o interfaccia dispatch dichiarata con la parola chiave [**Dispatch**](dispinterface.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

Il Component Object Model Microsoft definisce una classe come implementazione che consente **QueryInterface** tra un set di interfacce.

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

[**controllo**](control.md)
</dt> <dt>

[**predefinita**](default.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**nascosto**](hidden.md)
</dt> <dt>

[**interfaccia**](interface.md)
</dt> <dt>

[**licensed**](licensed.md)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**limitato**](restricted.md)
</dt> <dt>

[**origine**](source.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**uuid**](uuid.md)
</dt> <dt>

[**Versione**](version.md)
</dt> </dl>

 

 