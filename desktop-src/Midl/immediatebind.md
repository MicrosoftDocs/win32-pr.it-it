---
title: immediatebind (attributo)
description: L'attributo \ immediatebind\ indica che il database riceverà immediatamente una notifica di tutte le modifiche apportate a una proprietà di un oggetto associato a dati.
ms.assetid: 1c08ddca-e273-43b3-a8f6-ed7f552e4e0e
keywords:
- Attributo immediatebind MIDL
topic_type:
- apiref
api_name:
- immediatebind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40396343177da07a2747c79473cdc52f2d665fea8411f4d6f117a5032d66707a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642977"
---
# <a name="immediatebind-attribute"></a>immediatebind (attributo)

**\[ L'attributo \] immediatebind** indica che il database riceverà immediatamente una notifica di tutte le modifiche apportate a una proprietà di un oggetto associato a dati.

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

*interface-attribute-list* 
</dt> <dd>

Specifica un elenco di uno o più attributi che si applicano all'intera interfaccia.

</dd> <dt>

*interface-name* 
</dt> <dd>

Specifica il nome dell'interfaccia [**o**](interface.md) [**dell'interfaccia dispatch.**](dispinterface.md)

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Zero o più attributi di funzione.

</dd> <dt>

*Returntype* 
</dt> <dd>

Specifica il tipo restituito della funzione.

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della funzione nel file IDL.

</dd> <dt>

*params* 
</dt> <dd>

Zero o più parametri di funzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

**\[ L'attributo \] immediatebind** consente ai controlli di distinguere tra le proprietà che devono notificare al database ogni modifica e quelle che non lo fanno. Ad esempio, ogni modifica a un controllo casella di controllo deve essere inviata immediatamente al database sottostante, anche se il controllo non ha perso lo stato attivo. Tuttavia, per un controllo casella di riepilogo, viene apportata una modifica ogni volta che viene evidenziata una selezione diversa. Notificare al database una modifica prima che il controllo perda lo stato attivo sarebbe inefficiente e superfluo. **\[ L'attributo \] immediatebind** consente di specificare, impostando il bit ImmediateBind, singole proprietà in un form le cui modifiche devono essere segnalate immediatamente.

Anche le proprietà con **\[ l'attributo immediatebind \]** devono avere l'attributo **\[** [**associabile.**](bindable.md) **\]**

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

 

 