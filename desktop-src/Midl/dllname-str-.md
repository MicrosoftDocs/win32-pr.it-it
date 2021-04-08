---
title: attributo dllname (STR)
description: L'attributo \ dllname \ definisce il nome della DLL che contiene i punti di ingresso per un modulo.
ms.assetid: dbf062ce-9dcc-4cc6-b7cd-cdc5945e399b
keywords:
- attributo MIDL di dllname (STR)
topic_type:
- apiref
api_name:
- dllname(str)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 990d277db855c2988021d19a0a756c49454546f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046729"
---
# <a name="dllnamestr-attribute"></a>attributo dllname (STR)

L'attributo **\[ dllname \]** definisce il nome della dll che contiene i punti di ingresso per un modulo.

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

*UUID-numero* 
</dt> <dd>

Specifica un numero di identificazione univoco universale per il [**modulo**](module.md).

</dd> <dt>

*filename* 
</dt> <dd>

Specifica una stringa a terminazione NULL che contiene il percorso completo del file dll.

</dd> <dt>

*facoltativo-Attribute-List* 
</dt> <dd>

Specifica un elenco di zero o più attributi dell'interfaccia MIDL.

</dd> <dt>

*moduleName* 
</dt> <dd>

Specifica il nome che altri componenti software possono usare per fare riferimento al modulo.

</dd> <dt>

*elemento element* 
</dt> <dd>

Specifica una o più istruzioni di definizione degli elementi del modulo.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ dllname \]** è obbligatorio in un modulo.

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

[**modulo**](module.md)
</dt> <dt>

[**voce**](entry.md)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 