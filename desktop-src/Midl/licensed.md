---
title: licensed (attributo)
description: L'attributo \ licensed \ indica che la coclasse a cui si applica è concessa in licenza ed è necessario crearne un'istanza usando IClassFactory2.
ms.assetid: c4789ea2-8ff6-423e-8b69-22a7a5392854
keywords:
- attributo MIDL con licenza
topic_type:
- apiref
api_name:
- licensed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f24d8b6136cab86615e74838737bbda543b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046613"
---
# <a name="licensed-attribute"></a>licensed (attributo)

L'attributo **\[ licensed \]** indica che la [**coclasse**](coclass.md) a cui si applica è concessa in licenza ed è necessario crearne un'istanza utilizzando [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2).

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

*elenco attributi* 
</dt> <dd>

Specifica zero o più attributi applicabili all'istruzione [**coclass**](coclass.md) . Gli attributi di **coclasse** consentiti sono **\[** [**helpstring**](helpstring.md) **\]** **\[** [](helpcontext.md) **\]** **\[ \]**, HelpContext, licensed, **\[** [**Version**](version.md) **\]** , **\[** [**Control**](control.md) **\]** e **\[** [**Hidden**](hidden.md) **\]** .

</dd> <dt>

*ClassName* 
</dt> <dd>

Specifica il nome in base al quale l'oggetto componente è noto nella libreria dei tipi.

</dd> <dt>

*coclasse-definizione* 
</dt> <dd>

Specifica le istruzioni che compongono la definizione della [**coclasse**](coclass.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

Le licenze sono una funzionalità di COM che consente di controllare la creazione di oggetti. Gli oggetti con licenza possono essere creati solo dai client autorizzati a utilizzarli. Le licenze sono implementate in COM tramite l'interfaccia [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) e dal supporto di un codice di licenza che può essere passato in fase di esecuzione.

### <a name="flags"></a>Flags

\_FLICENSED TYPEFLAG

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

[**controllo**](control.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**nascosto**](hidden.md)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Versione**](version.md)
</dt> </dl>

 

 