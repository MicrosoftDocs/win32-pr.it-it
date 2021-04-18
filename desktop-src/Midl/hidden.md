---
title: hidden (attributo)
description: L'attributo \ Hidden \ indica che l'elemento esiste ma non deve essere visualizzato in un browser orientato all'utente.
ms.assetid: bf1f9270-fb93-4421-804e-d56e2c863bbd
keywords:
- attributo MIDL nascosto
topic_type:
- apiref
api_name:
- hidden
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1718351ef84199b60ba720ed2f3569cfa78a0a50
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299640"
---
# <a name="hidden-attribute"></a>hidden (attributo)

L'attributo **\[ Hidden \]** indica che l'elemento esiste ma non deve essere visualizzato in un browser orientato all'utente.

``` syntax
[
    other-attributes, 
    hidden
] 
element element-name
{
    definitions
}

[other-attributes, hidden] function-type function-name(optional-parameter-list);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*altri attributi* 
</dt> <dd>

Zero o più attributi MIDL facoltativi.

</dd> <dt>

*elemento* 
</dt> <dd>

Una delle direttive seguenti: [**coclasse**](coclass.md), interfaccia [**Dispatch**](dispinterface.md), [**interfaccia**](interface.md)o [**libreria**](library.md).

</dd> <dt>

*Nome elemento* 
</dt> <dd>

Nome che altri componenti software possono utilizzare per delineare l'elemento corrente.

</dd> <dt>

*definizioni* 
</dt> <dd>

Specifica le istruzioni che compongono la definizione dell'elemento.

</dd> <dt>

*tipo di funzione* 
</dt> <dd>

Tipo restituito della funzione.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Nome usato per richiamare la funzione.

</dd> <dt>

*facoltativo-parameter-list* 
</dt> <dd>

Zero o più parametri di funzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ Hidden \]** consente di rimuovere membri dall'interfaccia (mediante la schermatura da un ulteriore utilizzo) mantenendo la compatibilità con il codice esistente. È possibile usare l'attributo **\[ \] Hidden** per le proprietà, i metodi e le istruzioni [**coclass**](coclass.md), [**Dispatch**](dispinterface.md), [**Interface**](interface.md)e [**Library**](library.md) .

Quando viene specificato per una libreria, l'attributo **\[ Hidden \]** impedisce la visualizzazione dell'intera libreria. Questo utilizzo è pensato per i controlli. Gli host devono creare una nuova libreria dei tipi che esegue il wrapping del controllo con le proprietà estese.

### <a name="flags"></a>Flags

VARFLAG \_ FHIDDEN, FUNCFLAG \_ FHIDDEN, TypeFlag \_ FHIDDEN

## <a name="examples"></a>Esempi

``` syntax
[hidden, vararg] SAFEARRAY (int) SecretFunc(
    [in, out] SAFEARRAY (variant) *varP) ;

[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    hidden, 
    version (3.0)
] 
library HiddenLib 
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**interfaccia**](interface.md)
</dt> <dt>

[**libreria**](library.md)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> </dl>

 

 