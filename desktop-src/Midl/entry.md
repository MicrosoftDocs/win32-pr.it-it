---
title: entry (attributo)
description: L'attributo \ entry\ specifica una funzione o una costante esportata in un modulo identificando il punto di ingresso nella DLL.
ms.assetid: 1d2d6429-d828-44ec-8b0a-cefb64c6e706
keywords:
- Attributo entry MIDL
topic_type:
- apiref
api_name:
- entry
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f6dab1681cb04adbd48c4a27c14a359c87624870a43c118c6dd1a589689c00f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013929"
---
# <a name="entry-attribute"></a>entry (attributo)

**\[ L'attributo \]** entry specifica una funzione o una costante esportata in un modulo identificando il punto di ingresso nella DLL.

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

*uuid-number* 
</dt> <dd>

Specifica un numero di identificazione universalmente univoco per il [**modulo**](module.md).

</dd> <dt>

*id voce* 
</dt> <dd>

Specifica il nome della funzione del punto di ingresso del modulo o il numero di identificazione intero.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Specifica zero o più attributi per il compilatore MIDL da applicare al [**modulo**](module.md).

</dd> <dt>

*Modulename* 
</dt> <dd>

Specifica il nome utilizzato da altri componenti software per indicare il [**modulo**](module.md).

</dd> <dt>

*elementlist* 
</dt> <dd>

Specifica una o più istruzioni di definizione degli elementi del modulo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se la *variabile entryid* dell'attributo **\[ \] entry** è una stringa, si tratta di un punto di ingresso denominato. Se *entryid* è un numero, il punto di ingresso è definito da un ordinale. Questo attributo consente di ottenere l'indirizzo di una funzione in un modulo.

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

[**Dllname**](dllname-str-.md)
</dt> <dt>

[**Modulo**](module.md)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 