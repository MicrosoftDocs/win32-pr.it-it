---
title: helpfile (attributo)
description: L'attributo \ fileguide \ imposta il nome del file della Guida per una libreria dei tipi. Tutti i tipi in una libreria condividono lo stesso file della guida.
ms.assetid: caa248b1-a1a7-4c36-886a-079a66a01907
keywords:
- attributo filelima MIDL
topic_type:
- apiref
api_name:
- helpfile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b4283b0285631a710af774d364a01b82c9d44b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725162"
---
# <a name="helpfile-attribute"></a>helpfile (attributo)

L'attributo **\[ filelima \]** imposta il nome del file della Guida per una libreria dei tipi. Tutti i tipi in una libreria condividono lo stesso file della guida.

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

*UUID-numero* 
</dt> <dd>

Specifica un numero di identificazione univoco universale per la [**libreria**](library.md).

</dd> <dt>

*filename* 
</dt> <dd>

Specifica il nome del file contenente il testo della guida.

</dd> <dt>

*facoltativo-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi che verranno applicati al compilatore MIDL alla [**libreria**](library.md).

</dd> <dt>

*istruzioni Library* 
</dt> <dd>

Specifica una o più istruzioni MIDL che definiscono l'interfaccia della libreria.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare le funzioni **GetDocumentation** nelle interfacce **ITypeLib** e **ITypeInfo** per recuperare il nome del file.

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

[**libreria**](library.md)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 