---
title: Attributo id
description: L'attributo \ ID \ specifica un DISPID per una funzione membro, ovvero una proprietà o un metodo, in un'interfaccia o in un'interfaccia dispatch.
ms.assetid: 6f1be049-81b4-4aa2-a893-5dd79bb4d63c
keywords:
- attributo ID MIDL
topic_type:
- apiref
api_name:
- id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c57d8ea818bbd7b8fd5bd35816e6b7227eb917
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398883"
---
# <a name="id-attribute"></a>Attributo id

L'attributo **\[ ID \]** specifica un DISPID per una funzione membro, ovvero una proprietà o un metodo, in un'interfaccia o in un'interfaccia dispatch.

``` syntax
[id(id-num) [,optional-attribute-list]] return-type function-name(optional-parameter-list)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*ID-NUM* 
</dt> <dd>

DISPID per la funzione.

</dd> <dt>

*facoltativo-Attribute-List* 
</dt> <dd>

Specifica un elenco di zero o più attributi dell'interfaccia MIDL.

</dd> <dt>

*tipo restituito* 
</dt> <dd>

Specifica il tipo restituito della funzione.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della funzione nel file IDL.

</dd> <dt>

*facoltativo-parameter-list* 
</dt> <dd>

Zero o più parametri di funzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Utilizzare l'attributo **\[ \] ID** quando si desidera assegnare un DISPID standard ( \_ ad esempio, un valore DISPID, un DISPID NEWENUM e \_ così via) a un metodo o una proprietà oppure quando si implementa il proprio **IDispatch:: Invoke** anziché delegare a **DispInvoke** / **ITypeInfo:: Invoke**.

Se non si usa l'attributo **\[ ID \]** in un'interfaccia, il compilatore MIDL assegnerà un DISPID per l'utente. Tuttavia, quando si specifica un'interfaccia dispatch usando proprietà e metodi, è necessario specificare un DISPID per ogni proprietà e metodo.

*ID-NUM* è un valore integrale positivo a 32 bit. Gli ID negativi sono riservati per l'uso da automazione.

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

[**interfaccia**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 