---
title: readonly (attributo)
description: L'attributo \ readonly\ impedisce l'assegnazione a una variabile.
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
ms.openlocfilehash: 4d0d534efe8df1f4d05cd0b536a78094f903870d896114ee8b614511e067025b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013679"
---
# <a name="readonly-attribute"></a>readonly (attributo)

**\[ L'attributo \] readonly** impedisce l'assegnazione a una variabile.

``` syntax
[readonly [, optional-attributes]] data-type identifier
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*attributi facoltativi* 
</dt> <dd>

Zero o più attributi MIDL.

</dd> <dt>

*tipo di dati* 
</dt> <dd>

Tipo dei dati contenuti *nell'identificatore*.

</dd> <dt>

*identifier* 
</dt> <dd>

Nome con cui il software può fare riferimento alla posizione di archiviazione dei dati.

</dd> </dl>

## <a name="remarks"></a>Commenti

**\[ L'attributo \] readonly** impedisce l'assegnazione a una variabile. **\[ readonly \]** è supportato solo a livello di parametro, non a livello di metodo.

### <a name="flags"></a>Flags

VARFLAG \_ FREADONLY

## <a name="examples"></a>Esempi

``` syntax
HRESULT Method3([in, readonly] int iMmutable);
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

 

 