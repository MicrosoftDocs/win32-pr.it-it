---
title: Attributo dllname(str)
description: L'attributo \ dllname\ definisce il nome della DLL che contiene i punti di ingresso per un modulo.
ms.assetid: dbf062ce-9dcc-4cc6-b7cd-cdc5945e399b
keywords:
- Attributo DLLname(str) MIDL
topic_type:
- apiref
api_name:
- dllname(str)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db6f70fb65822a63bd2bf0f9919ac1b9554a664d1ac7ec9775c611b5b4e7f73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067291"
---
# <a name="dllnamestr-attribute"></a>Attributo dllname(str)

**\[ L'attributo \] dllname** definisce il nome della DLL che contiene i punti di ingresso per un modulo.

``` syntax
[
    uuid(uuid-number), 
    dllname("filename")
    [, optional-attribute-list]
]
module modulename
{
    elementlist
};
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*uuid-number* 
</dt> <dd>

Specifica un numero di identificazione univoco universale per il [**modulo**](module.md).

</dd> <dt>

*Filename* 
</dt> <dd>

Specifica una stringa con terminazione NULL che contiene il percorso completo del file DLL.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Specifica un elenco di zero o più attributi dell'interfaccia MIDL.

</dd> <dt>

*Modulename* 
</dt> <dd>

Specifica il nome che altri componenti software possono usare per fare riferimento al modulo.

</dd> <dt>

*elementlist* 
</dt> <dd>

Specifica una o più istruzioni di definizione degli elementi del modulo.

</dd> </dl>

## <a name="remarks"></a>Commenti

**\[ L'attributo \] dllname** è obbligatorio in un modulo.

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("A meaningful comment"),   
    dllname("HANDY.DLL")
] 
module HandyStuff
{
    /* Module content definitions */
};
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Modulo**](module.md)
</dt> <dt>

[**Voce**](entry.md)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 