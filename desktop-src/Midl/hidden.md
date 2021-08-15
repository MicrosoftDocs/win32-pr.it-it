---
title: hidden (attributo)
description: L'attributo \hidden\ indica che l'elemento esiste ma non deve essere visualizzato in un browser orientato all'utente.
ms.assetid: bf1f9270-fb93-4421-804e-d56e2c863bbd
keywords:
- attributo nascosto MIDL
topic_type:
- apiref
api_name:
- hidden
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a907a608376d9ad13f97427bd7a941b99221a0f14a6fa9fe35944ced10770b66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384046"
---
# <a name="hidden-attribute"></a>hidden (attributo)

**\[ L'attributo \]** nascosto indica che l'elemento esiste ma non deve essere visualizzato in un browser orientato all'utente.

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

*Elemento* 
</dt> <dd>

Una delle direttive seguenti: [**coclass,**](coclass.md) [**dispinterface,**](dispinterface.md) [**interface**](interface.md)o [**library**](library.md).

</dd> <dt>

*element-name* 
</dt> <dd>

Nome che altri componenti software possono usare per delineare l'elemento corrente.

</dd> <dt>

*Definizioni* 
</dt> <dd>

Specifica le istruzioni che costituiscono la definizione dell'elemento.

</dd> <dt>

*function-type* 
</dt> <dd>

Tipo restituito della funzione.

</dd> <dt>

*function-name* 
</dt> <dd>

Nome usato per richiamare la funzione.

</dd> <dt>

*optional-parameter-list* 
</dt> <dd>

Zero o più parametri di funzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

**\[ L'attributo \]** nascosto consente di rimuovere i membri dall'interfaccia (proteggendoli dall'ulteriore uso) mantenendo la compatibilità con il codice esistente. È possibile usare **\[ l'attributo \]** nascosto per proprietà, metodi e [**le istruzioni di coclasse**](coclass.md), interfaccia [**dispatch**](dispinterface.md) [**,**](interface.md)interfaccia [**e**](library.md) libreria.

Se specificato per una libreria, **\[ l'attributo nascosto \]** impedisce la visualizzazione dell'intera libreria. Questo utilizzo è pensato per i controlli. Gli host devono creare una nuova libreria dei tipi che esegue il wrapping del controllo con le proprietà estese.

### <a name="flags"></a>Flags

VARFLAG \_ FHIDDEN, FUNCFLAG \_ FHIDDEN, TYPEFLAG \_ FHIDDEN

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

[**Interfaccia**](interface.md)
</dt> <dt>

[**Libreria**](library.md)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> </dl>

 

 