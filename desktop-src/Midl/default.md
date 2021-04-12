---
title: attributo default
description: L'attributo \ default \ indica che l'interfaccia o l'interfaccia dispatch, definita all'interno di una coclasse, rappresenta l'interfaccia di programmabilità predefinita. Questo attributo deve essere utilizzato dai linguaggi macro.
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
ms.openlocfilehash: 2171515bffc41abf2b5fe9a25826c2a71d3939c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472846"
---
# <a name="default-attribute"></a>attributo default

L'attributo **\[ \] default** indica che l' [**interfaccia**](interface.md) o l'interfaccia [**Dispatch**](dispinterface.md), definita all'interno di una [**coclasse**](coclass.md), rappresenta l'interfaccia di programmabilità predefinita. Questo attributo deve essere utilizzato dai linguaggi macro.

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

*UUID-numero* 
</dt> <dd>

Specifica un numero di identificazione univoco universale per la [**coclasse**](coclass.md).

</dd> <dt>

*elenco attributi* 
</dt> <dd>

Specifica attributi di [**coclasse**](coclass.md) aggiuntivi. Separare più attributi con virgole.

</dd> <dt>

*coclass-nome* 
</dt> <dd>

Specifica il nome con cui altri componenti software possono fare riferimento a questa [**coclasse**](coclass.md).

</dd> <dt>

*facoltativo-Interface-attribute* 
</dt> <dd>

L' **\[** attributo di [**origine**](source.md) **\]** , che specifica che un'interfaccia o un'interfaccia dispatch è in uscita, è l'unico altro attributo che può essere usato qui.

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una [**coclasse**](coclass.md) può avere al massimo due membri **\[ predefiniti \]** . Uno rappresenta l'interfaccia di uscita (di origine) o l'interfaccia dispatch e l'altra rappresenta l'interfaccia (sink) in ingresso o l'interfaccia dispatch. Se non viene specificato l'attributo **\[ default \]** per alcun membro della **coclasse** o del **tipo**, i primi membri in uscita e in ingresso che non dispongono dell' **\[** [**attributo Restricted**](restricted.md) **\]** vengono considerati come valori predefiniti.

### <a name="flags"></a>Flags

\_FDEFAULT IMPLTYPEFLAG

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

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**limitato**](restricted.md)
</dt> <dt>

[**origine**](source.md)
</dt> </dl>

 

 