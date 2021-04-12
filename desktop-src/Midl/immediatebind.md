---
title: immediatebind (attributo)
description: L'attributo \ immediatebind \ indica che il database riceverà immediatamente una notifica di tutte le modifiche apportate a una proprietà di un oggetto associato a dati.
ms.assetid: 1c08ddca-e273-43b3-a8f6-ed7f552e4e0e
keywords:
- attributo MIDL di immediatebind
topic_type:
- apiref
api_name:
- immediatebind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8a797514c15f8d4c46bb6161946d5d0b6bd10b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104223494"
---
# <a name="immediatebind-attribute"></a>immediatebind (attributo)

L'attributo **\[ immediatebind \]** indica che il database riceverà immediatamente una notifica di tutte le modifiche apportate a una proprietà di un oggetto associato a dati.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, immediatebind[, optional-attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Specifica un elenco di uno o più attributi che si applicano all'interfaccia nel suo complesso.

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

Specifica il nome dell' [**interfaccia**](interface.md) o dell'interfaccia [**Dispatch**](dispinterface.md).

</dd> <dt>

*facoltativo-Attribute-List* 
</dt> <dd>

Zero o più attributi di funzione.

</dd> <dt>

*returnType* 
</dt> <dd>

Specifica il tipo restituito della funzione.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della funzione nel file IDL.

</dd> <dt>

*params* 
</dt> <dd>

Zero o più parametri di funzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ immediatebind \]** consente ai controlli di distinguere tra le proprietà che devono notificare al database ogni modifica e quelle che non lo fanno. Ogni modifica apportata a un controllo CheckBox, ad esempio, deve essere inviata immediatamente al database sottostante, anche se il controllo non ha perso lo stato attivo. Tuttavia, per un controllo ListBox, viene apportata una modifica ogni volta che viene evidenziata un'altra selezione. La notifica al database di una modifica prima che il controllo perda lo stato attivo non è efficiente e non è necessario. L'attributo **\[ immediatebind \]** consente di specificare, impostando il bit immediatebind, singole proprietà in un form le cui modifiche devono essere segnalate immediatamente.

Anche le proprietà con l'attributo **\[ immediatebind \]** devono avere l' **\[** attributo [**associabile**](bindable.md) **\]** .

### <a name="flags"></a>Flags

FUNCFLAG \_ FIMMEDIATEBIND, VARFLAG \_ FIMMEDIATEBIND

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, immediatebind] long Size(void);

        [id(1), propput, bindable, 
         immediatebind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

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

 

 