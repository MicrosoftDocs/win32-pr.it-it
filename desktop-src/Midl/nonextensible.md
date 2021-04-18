---
title: Attributo nonextensible
description: L'attributo \ nonextensible \ specifica che l'implementazione di IDispatch include solo le proprietà e i metodi elencati nella descrizione dell'interfaccia e non può essere estesa con membri aggiuntivi in fase di esecuzione.
ms.assetid: 5fcffa65-4f0c-4180-a6c2-f68d63ff99ae
keywords:
- attributo MIDL non estendibile
topic_type:
- apiref
api_name:
- nonextensible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e591ea4ab0647449ca9296b3b14a4aab9fff6991
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299635"
---
# <a name="nonextensible-attribute"></a>Attributo nonextensible

L'attributo non **\[ \] estendibile** specifica che l'implementazione di [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) include solo le proprietà e i metodi elencati nella descrizione dell'interfaccia e non può essere estesa con membri aggiuntivi in fase di esecuzione. Per impostazione predefinita, l'automazione presuppone che le interfacce possano aggiungere membri in fase di esecuzione, ovvero presuppone che siano estendibili.

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

*UUID-numero* 
</dt> <dd>

Specifica un numero di identificazione univoco universale per l' [**interfaccia**](interface.md).

</dd> <dt>

*facoltativo-Attribute-List* 
</dt> <dd>

Specifica un elenco di zero o più attributi dell'interfaccia MIDL.

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

Specifica il nome dell' [**interfaccia**](interface.md) o dell'interfaccia [**Dispatch**](dispinterface.md).

</dd> <dt>

*interfaccia-definizione* 
</dt> <dd>

Specifica le istruzioni IDL che formano la definizione dell' [**interfaccia**](interface.md) o dell'interfaccia [**Dispatch**](dispinterface.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile applicare l'attributo non **\[ estendibile \]** a un'interfaccia o a un'interfaccia dispatch. Tuttavia, un'interfaccia deve avere anche gli **\[** attributi [**Dual**](dual.md) **\]** e **\[** [**oleautomation**](oleautomation.md) **\]** .

### <a name="flags"></a>Flags

\_FNONEXTENSIBLE TYPEFLAG

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

[**interfaccia**](interface.md)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 