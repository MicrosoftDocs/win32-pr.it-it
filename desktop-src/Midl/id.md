---
title: Attributo id
description: L'attributo \ id\ specifica un DISPID per una funzione membro (una proprietà o un metodo, in un'interfaccia o interfaccia dispatch).
ms.assetid: 6f1be049-81b4-4aa2-a893-5dd79bb4d63c
keywords:
- Attributo ID MIDL
topic_type:
- apiref
api_name:
- id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a4d783265ebfcf9dca454c80c39031dc0c37dfb63a8749b4d0e6299a510d91a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643067"
---
# <a name="id-attribute"></a>Attributo id

**\[ L'attributo id \]** specifica un DISPID per una funzione membro (una proprietà o un metodo, in un'interfaccia o in un'interfaccia dispatch).

``` syntax
[id(id-num) [,optional-attribute-list]] return-type function-name(optional-parameter-list)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*id-num* 
</dt> <dd>

DISPID per la funzione.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Specifica un elenco di zero o più attributi dell'interfaccia MIDL.

</dd> <dt>

*return-type* 
</dt> <dd>

Specifica il tipo restituito della funzione.

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della funzione nel file IDL.

</dd> <dt>

*optional-parameter-list* 
</dt> <dd>

Zero o più parametri di funzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare l'attributo **\[ id \]** quando si vuole assegnare un DISPID standard (ad esempio, DISPID VALUE, DISPID NEWENUM e così via) a un metodo o a una proprietà oppure quando si implementa il proprio IDispatch::Invoke anziché delegare a \_ \_ **DispInvoke**  / **ITypeInfo::Invoke**.

Se non si usa **\[ l'attributo id \]** in un'interfaccia, il compilatore MIDL assegna automaticamente un DISPID. Tuttavia, quando si specifica un'interfaccia dispatch usando proprietà e metodi, è necessario specificare un DISPID per ogni proprietà e metodo.

*id-num è* un valore integrale positivo a 32 bit. Gli ID negativi sono riservati per l'uso da parte di Automazione.

## <a name="examples"></a>Esempi

``` syntax
interface IKnown : IUnknown
{
    properties:
        [id(90), propget, 
         helpstring("A meaningful comment."] long Func1(void);

    /* Other interface statements */
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Interfaccia**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 