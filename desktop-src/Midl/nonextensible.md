---
title: Attributo nonextensible
description: L'attributo \ nonextensible\ specifica che l'implementazione di IDispatch include solo le proprietà e i metodi elencati nella descrizione dell'interfaccia e non può essere estesa con membri aggiuntivi in fase di esecuzione.
ms.assetid: 5fcffa65-4f0c-4180-a6c2-f68d63ff99ae
keywords:
- Attributo MIDL non estensibile
topic_type:
- apiref
api_name:
- nonextensible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96c4e55cf5cf2c05ff9c3619b19e7a9b0582f3cf64bc0f9a711fb1af274bfb9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066880"
---
# <a name="nonextensible-attribute"></a>Attributo nonextensible

**\[ L'attributo non \] estensibile** specifica che l'implementazione [**di IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) include solo le proprietà e i metodi elencati nella descrizione dell'interfaccia e non può essere estesa con membri aggiuntivi in fase di esecuzione. Per impostazione predefinita, Automazione presuppone che le interfacce possano aggiungere membri in fase di esecuzione, ovvero presuppone che siano estendibili.

``` syntax
[
    uuid(uuid-number), 
    nonextensible 
    [, optional-attribute-list]
] 
interface | dispinterface interface-name 
{
    interface-definition
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*uuid-number* 
</dt> <dd>

Specifica un numero di identificazione univoco universale per [**l'interfaccia**](interface.md).

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Specifica un elenco di zero o più attributi dell'interfaccia MIDL.

</dd> <dt>

*interface-name* 
</dt> <dd>

Specifica il nome dell'interfaccia [**o**](interface.md) [**dell'interfaccia dispatch.**](dispinterface.md)

</dd> <dt>

*interface-definition* 
</dt> <dd>

Specifica istruzioni IDL che formano la definizione [**dell'interfaccia o**](interface.md) [**dell'interfaccia dispatch.**](dispinterface.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile applicare **\[ l'attributo non estensibile \]** a un'interfaccia o a un'interfaccia dispatch. Tuttavia, un'interfaccia deve avere anche gli **\[** [**attributi dual**](dual.md) **\]** e **\[** [**oleautomation.**](oleautomation.md) **\]**

### <a name="flags"></a>Flags

TYPEFLAG \_ FNONEXTENSIBLE

## <a name="examples"></a>Esempi

``` syntax
library Hello
{
    [
        uuid(12345678-1234-1234-1234-123456789ABC), 
        helpstring("A helpful description."),
        oleautomation, 
        dual, 
        nonextensible
    ] 
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Contenuto di una libreria dei tipi](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**Dual**](dual.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Interfaccia**](interface.md)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 