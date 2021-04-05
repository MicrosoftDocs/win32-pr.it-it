---
title: attributo Control
description: L'attributo \ Control \ identifica una coclasse o una libreria come controllo COM, da cui un sito contenitore deriverà librerie dei tipi aggiuntive o classi di oggetti componente.
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
ms.openlocfilehash: 982327d581ddb606f733e9efbbcb89e2f9972cf4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724954"
---
# <a name="control-attribute"></a>attributo Control

L'attributo **\[ Control \]** identifica una [**coclasse**](coclass.md) o una [**libreria**](library.md) come controllo com, da cui un sito contenitore deriverà librerie dei tipi aggiuntive o classi di oggetti componente.

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

*elenco attributi* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla [**libreria**](library.md) o all'istruzione [**coclasse**](coclass.md) . Separare più attributi con virgole.

</dd> <dt>

*lib-o-CoClassname* 
</dt> <dd>

Specifica il nome della [**libreria**](library.md) o della [**coclasse**](coclass.md).

</dd> <dt>

*definizioni* 
</dt> <dd>

Istruzioni MIDL che specificano i membri della [**libreria**](library.md) o della [**coclasse**](coclass.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo attributo consente di contrassegnare le librerie dei tipi che descrivono i controlli in modo che non vengano visualizzate nei browser dei tipi destinati agli oggetti non visivi.

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

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**libreria**](library.md)
</dt> </dl>

 

 