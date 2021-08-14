---
title: helpfile (attributo)
description: L'attributo \helpfile\ imposta il nome del file della Guida per una libreria dei tipi. Tutti i tipi in una libreria condividono lo stesso file della Guida.
ms.assetid: caa248b1-a1a7-4c36-886a-079a66a01907
keywords:
- Attributo helpfile MIDL
topic_type:
- apiref
api_name:
- helpfile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1557d96f35913e5e1ed9b784bedfc430e6c4d77b65954583ca6923e4728af9a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384022"
---
# <a name="helpfile-attribute"></a>helpfile (attributo)

**\[ L'attributo \] helpfile** imposta il nome del file della Guida per una libreria dei tipi. Tutti i tipi in una libreria condividono lo stesso file della Guida.

``` syntax
[
    uuid(uuid-number), 
    helpfile("filename") 
    [, optional-attribute-list]
] 
library 
{
    library statements
};
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*uuid-number* 
</dt> <dd>

Specifica un numero di identificazione universalmente univoco per la [**libreria**](library.md).

</dd> <dt>

*Filename* 
</dt> <dd>

Specifica il nome del file contenente il testo della Guida.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Specifica zero o più attributi che verranno applicati dal compilatore MIDL alla [**libreria**](library.md).

</dd> <dt>

*istruzioni library* 
</dt> <dd>

Specifica una o più istruzioni MIDL che definiscono l'interfaccia della libreria.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare le **funzioni GetDocumentation** nelle **interfacce ITypeLib** e **ITypeInfo** per recuperare il nome del file.

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpfile("filename.hlp"),
    lcid(0x0409), 
    version(2.0)
]
library Hello
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Libreria**](library.md)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 