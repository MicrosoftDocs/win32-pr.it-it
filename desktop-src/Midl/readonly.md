---
title: readonly (attributo)
description: L'attributo \ ReadOnly \ impedisce l'assegnazione a una variabile.
ms.assetid: b81064e6-e788-48d1-9958-203f1e3c7e4d
keywords:
- attributo di sola lettura MIDL
topic_type:
- apiref
api_name:
- readonly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4ef4ca5f32b96146ed5ab0ec085d32b24dca3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963034"
---
# <a name="readonly-attribute"></a>readonly (attributo)

L'attributo **\[ ReadOnly \]** impedisce l'assegnazione a una variabile.

``` syntax
[readonly [, optional-attributes]] data-type identifier
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*facoltativo-attributi* 
</dt> <dd>

Zero o più attributi MIDL.

</dd> <dt>

*tipo di dati* 
</dt> <dd>

Tipo di dati contenuti in base all' *identificatore*.

</dd> <dt>

*identifier* 
</dt> <dd>

Nome con cui il software può fare riferimento al percorso di archiviazione dei dati.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ ReadOnly \]** impedisce l'assegnazione a una variabile. **\[ ReadOnly \]** è supportato solo a livello di parametro, non a livello di metodo.

### <a name="flags"></a>Flags

\_FREADONLY VARFLAG

## <a name="examples"></a>Esempi

``` syntax
HRESULT Method3([in, readonly] int iMmutable);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 