---
title: max_is (attributo)
description: L'attributo \ Max \_ is \ indica il valore massimo per un indice di matrice valido.
ms.assetid: 8d09f610-cae6-45f6-815c-5ba916d8a5e7
keywords:
- attributo max_is MIDL
topic_type:
- apiref
api_name:
- max_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f2e2040acbc0e8f65c02f4f4ec7c3ad329959b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337046"
---
# <a name="max_is-attribute"></a>\_attributo max is

L'attributo **\[ Max \_ is \]** indica il valore massimo per un indice di matrice valido.

``` syntax
[max_is(limited-expression-list )]
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*elenco di espressioni limitate* 
</dt> <dd>

Specifica una o più espressioni del linguaggio C. Ogni espressione restituisce un intero che rappresenta l'indice di matrice valido più alto. Il compilatore MIDL supporta le espressioni condizionali, le espressioni logiche, le espressioni relazionali e le espressioni aritmetiche. MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di incremento e decremento. Separare più espressioni con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ Max \_ is \]** non corrisponde necessariamente al numero di elementi nella matrice. Per una matrice di dimensioni *n* in C, dove il primo elemento della matrice è il numero di elemento zero, il valore massimo per un indice di matrice valido è *n*-1.

L'attributo **\[ Max \_ is \]** non può essere utilizzato come attributo di campo allo stesso tempo della **\[** [**dimensione \_**](size-is.md) **\]** Attribute.

Sebbene sia possibile utilizzare l'attributo **\[ Max \_ is \]** con un'espressione costante, questa operazione non è efficiente e non è necessaria. Ad esempio, usare una matrice a dimensione fissa:

``` syntax
/* transmits values of a[0]... a[MAX_SIZE-1] */ 
HRESULT Proc3([in] short Arr[MAX_SIZE]); 
```

invece di:

``` syntax
/* legal but marshaling code is much slower */ 
HRESULT Proc3([in max_is(MAX_SIZE-1)] short Arr[] );
```

## <a name="examples"></a>Esempi

``` syntax
/* if m = 10, there are 11 transmitted elements (a[0]...a[10])*/ 
HRESULT Proc1( 
    [in] short m, 
    [in, max_is(m)] short a[]);  
 
/* if m = 10, the valid range for b is b[0...10][20] */ 
HRESULT Proc2( 
    [in] short m, 
    [in, max_is(m)] short b[][20];
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Attributi di campo](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**min \_ è**](min-is.md)
</dt> <dt>

[**dimensioni \_**](size-is.md)
</dt> </dl>

 

 