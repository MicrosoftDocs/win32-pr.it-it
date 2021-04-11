---
title: entry (attributo)
description: L'attributo \ entry \ specifica una funzione o una costante esportata in un modulo identificando il punto di ingresso nella DLL.
ms.assetid: 1d2d6429-d828-44ec-8b0a-cefb64c6e706
keywords:
- attributo voce MIDL
topic_type:
- apiref
api_name:
- entry
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e596284a83c48bcfc84ef4f7985aed7c33ba7da
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336951"
---
# <a name="entry-attribute"></a>entry (attributo)

L'attributo **\[ entry \]** specifica una funzione o una costante esportata in un modulo identificando il punto di ingresso nella dll.

``` syntax
[
    uuid(uuid-number), 
    entry(entry-id)
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

*ID di ingresso* 
</dt> <dd>

Specifica il nome della funzione del punto di ingresso del modulo o il numero di identificazione intero.

</dd> <dt>

*facoltativo-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi per il compilatore MIDL da applicare al [**modulo**](module.md).

</dd> <dt>

*moduleName* 
</dt> <dd>

Specifica il nome usato da altri componenti software per indicare il [**modulo**](module.md).

</dd> <dt>

*elemento element* 
</dt> <dd>

Specifica una o più istruzioni di definizione degli elementi del modulo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se la variabile *EntryID* dell'attributo **\[ entry \]** è una stringa, si tratta di un punto di ingresso denominato. Se *EntryID* è un numero, il punto di ingresso viene definito da un ordinale. Questo attributo fornisce un modo per ottenere l'indirizzo di una funzione in un modulo.

## <a name="examples"></a>Esempi

``` syntax
[
    dllname("MyAppsFirst.dll")
] 
module MyModule
{
    [entry(20), bindable, requestedit, 
     propputref, defaultbind ] HRESULT Func1(
         [in]IUnknown * Param1, 
         [out] MyType * Param2);
    [entry("TwentyOne"), hidden, vararg] SAFEARRAY (int) Func2(
        [in, out] SAFEARRAY (variant) *varP) ;
    [entry(22)] Float Func3(
        [in] lpstr pName, [in] double dLevel,
        [out] short * sByte) ;
    } ;
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**DllName**](dllname-str-.md)
</dt> <dt>

[**modulo**](module.md)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 