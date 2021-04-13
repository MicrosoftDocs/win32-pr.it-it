---
title: appobject (attributo)
description: L'attributo \ appobject \ identifica la coclasse come oggetto applicazione, che è associato a un'applicazione EXE completa.
ms.assetid: f4fcdf55-7431-4d66-8a46-f741c52fbe56
keywords:
- attributo MIDL di appobject
topic_type:
- apiref
api_name:
- appobject
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d937d4a83306bc0c29f3c8c806bc043febec6a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398909"
---
# <a name="appobject-attribute"></a>appobject (attributo)

L'attributo **\[ appobject \]** identifica la [**coclasse**](coclass.md) come oggetto applicazione, che è associato a un'applicazione exe completa.

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

*UUID-numero* 
</dt> <dd>

Specifica un numero di identificazione univoco universale per la [**coclasse**](coclass.md).

</dd> <dt>

*coclass-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi applicabili all'istruzione [**coclass**](coclass.md) . Gli attributi **di coclasse** consentiti sono [**\[ helpstring \]**](helpstring.md) [**\[ \]**](helpcontext.md) [**\[ \]**](version.md) [**\[ \]**](hidden.md) [**\[ \]**](control.md) [**\[ \]**](licensed.md), HelpContext, licensed, Version, Control e Hidden.

</dd> <dt>

*ClassName* 
</dt> <dd>

Specifica il nome in base al quale l'oggetto componente è noto nella libreria dei tipi.

</dd> <dt>

*definizione di coclasse* 
</dt> <dd>

Specifica le istruzioni che compongono la definizione della [**coclasse**](coclass.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ appobject \]** indica anche che le funzioni e le proprietà della [**coclasse**](coclass.md) sono disponibili a livello globale nella libreria dei tipi corrente.

La rappresentazione TypeFlag per questo attributo è TYPEFLAG \_ FAPPOBJECT

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

[**licensed**](licensed.md)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Versione**](version.md)
</dt> </dl>

 

 