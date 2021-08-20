---
title: requestedit (attributo)
description: L'attributo \ requestedit\ indica che la proprietà supporta la notifica OnRequestEdit.
ms.assetid: 63f38d83-596b-4031-bb6a-972374cd0c60
keywords:
- attributo requestedit MIDL
topic_type:
- apiref
api_name:
- requestedit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51a894e5d4a09e7535e10a73e1bd118245e5886e0cdbb23b0f0645e588ab4adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146354"
---
# <a name="requestedit-attribute"></a>requestedit (attributo)

**\[ L'attributo \] requestedit** indica che la proprietà supporta la **notifica OnRequestEdit.**

``` syntax
[requestedit [,optional-attributes]] return-type function-name(params)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*attributi facoltativi* 
</dt> <dd>

Zero o più attributi MIDL.

</dd> <dt>

*return-type* 
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

Il supporto **della notifica OnRequestEdit** significa che, prima che venga apportata una modifica, l'oggetto invierà al client una richiesta di autorizzazione per modificare una proprietà. Un oggetto può supportare data binding ma non dispone di questo attributo.

### <a name="flags"></a>Flags

FUNCFLAG \_ FREQUESTEDIT, VARFLAG \_ FREQUESTEDIT

## <a name="examples"></a>Esempi

``` syntax
properties:
    [propget, helpstring("A useful comment"), bindable, defaultbind,
     displaybind, requestedit] long Func1(void);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 