---
title: Attributo control
description: L'attributo \ control\ identifica una coclasse o una libreria come controllo COM, da cui un sito contenitore deriva librerie dei tipi aggiuntive o classi di oggetti componente.
ms.assetid: c39dd4b6-743f-4888-8954-8b83584bdea5
keywords:
- attributo di controllo MIDL
topic_type:
- apiref
api_name:
- control
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b6372ffb7f7d9f19769e419b12c0b109736a9867360224e023f1b622c653854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643680"
---
# <a name="control-attribute"></a>Attributo control

**\[ \] L'attributo** del controllo [](library.md) identifica [**una coclasse**](coclass.md) o una libreria come controllo COM, da cui un sito contenitore deriva librerie dei tipi aggiuntive o classi di oggetti componente.

``` syntax
[
    uuid, 
    control 
    [, attribute-list]
] 
library | coclass lib-or-coclassname 
{ 
    definitions 
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*attribute-list* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla libreria [**o**](library.md) all'istruzione [**coclasse.**](coclass.md) Separare più attributi con virgole.

</dd> <dt>

*lib-or-coclassname* 
</dt> <dd>

Specifica il nome della libreria [**o della**](library.md) [**coclasse**](coclass.md).

</dd> <dt>

*Definizioni* 
</dt> <dd>

Istruzioni MIDL che specificano i membri della libreria [**o**](library.md) [**della coclasse**](coclass.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo attributo consente di contrassegnare le librerie dei tipi che descrivono i controlli in modo che non siano visualizzati nei browser dei tipi destinati agli oggetti non visualizzati.

### <a name="flags"></a>Flags

TYPEFLAG \_ FCONTROL, LIBFLAG \_ FCONTROL

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("Hello 2.1 COM Control Library"), 
    control,version(2.1)
] 
library Hello 
{ 
    /* library definitions */
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**Libreria**](library.md)
</dt> </dl>

 

 