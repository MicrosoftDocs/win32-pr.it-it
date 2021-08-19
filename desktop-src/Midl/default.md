---
title: attributo default
description: L'attributo \ default\ indica che l'interfaccia o l'interfaccia dispatch, definita all'interno di una coclasse, rappresenta l'interfaccia di programmabilità predefinita. Questo attributo è destinato all'uso da parte dei linguaggi macro.
ms.assetid: 66769dff-60a0-4e6e-9357-c4339c0bfa3f
keywords:
- attributo predefinito MIDL
topic_type:
- apiref
api_name:
- default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ea717048a89c626ef19d5b1c41fcd558a163f7b4ade9c05eee0e3ea362d50ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013939"
---
# <a name="default-attribute"></a>attributo default

**\[ L'attributo \]** predefinito Indica che [**l'interfaccia**](interface.md) o [**l'interfaccia dispatch,**](dispinterface.md)definita all'interno di una [**coclasse**](coclass.md), rappresenta l'interfaccia di programmabilità predefinita. Questo attributo è destinato all'uso da parte dei linguaggi macro.

``` syntax
[
    uuid(uuid-number) 
    [, attribute-list]
] 
coclass coclass-name
{
    [ default [, optional-interface-attribute] ]; 
    interface | dispinterface interface-name;
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*uuid-number* 
</dt> <dd>

Specifica un numero di identificazione univoco universale per la [**coclasse**](coclass.md).

</dd> <dt>

*attribute-list* 
</dt> <dd>

Specifica attributi [**di coclasse**](coclass.md) aggiuntivi. Separare più attributi con virgole.

</dd> <dt>

*coclass-name* 
</dt> <dd>

Specifica il nome con cui altri componenti software possono fare riferimento a [**questa coclasse**](coclass.md).

</dd> <dt>

*optional-interface-attribute* 
</dt> <dd>

**\[** [**L'attributo**](source.md) **\]** di origine, che specifica che un'interfaccia o un'interfaccia dispatch è in uscita, è l'unico altro attributo che può essere usato qui.

</dd> <dt>

*interface-name* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una [**coclasse**](coclass.md) può avere al massimo due **\[ membri \]** predefiniti. Una rappresenta l'interfaccia in uscita (di origine) o l'interfaccia dispatch e l'altra rappresenta l'interfaccia (sink) in ingresso o l'interfaccia dispatch. Se **\[ l'attributo \]** predefinito non viene specificato per alcun membro della **coclasse** o **del cotipo,** i primi membri in uscita e in ingresso che non dispongono dell'attributo con restrizioni vengono considerati **\[** [](restricted.md) **\]** come valori predefiniti.

### <a name="flags"></a>Flags

IMPLTYPEFLAG \_ FDEFAULT

## <a name="examples"></a>Esempi

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello Class"),appobject
]  
coclass Hello
{
    [default] interface IHello:IUnknown;
    interface IDispatch;
};
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Limitato**](restricted.md)
</dt> <dt>

[**fonte**](source.md)
</dt> </dl>

 

 