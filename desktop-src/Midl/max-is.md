---
title: max_is (attributo)
description: L'attributo \ max \_ is\ definisce il valore massimo per un indice di matrice valido.
ms.assetid: 8d09f610-cae6-45f6-815c-5ba916d8a5e7
keywords:
- max_is attributo MIDL
topic_type:
- apiref
api_name:
- max_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7dfa7e8cdc5b1df752a3a6eb442524157228d354079f262a27a5514860e335
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642967"
---
# <a name="max_is-attribute"></a>attributo max \_ is

**\[ L'attributo max \_ is \]** definisce il valore massimo per un indice di matrice valido.

``` syntax
[max_is(limited-expression-list )]
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*limited-expression-list* 
</dt> <dd>

Specifica una o più espressioni in linguaggio C. Ogni espressione restituisce un intero che rappresenta l'indice di matrice valido più alto. Il compilatore MIDL supporta espressioni condizionali, logiche, relazionali ed aritmetiche. MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di incremento e decremento. Separare più espressioni con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

**\[ \_ L'attributo \] max** is non corrisponde necessariamente al numero di elementi nella matrice. Per una matrice di dimensioni *n* in C, dove il primo elemento della matrice è il numero di elemento zero, il valore massimo per un indice di matrice valido *è n*-1.

**\[ L'attributo max \_ is \]** non può essere usato come attributo di campo contemporaneamente all'attributo **\[** [**\_ size.**](size-is.md) **\]**

Sebbene sia valido usare l'attributo **\[ max \_ is \]** con un'espressione costante, questa operazione è inefficiente e non necessaria. Ad esempio, usare una matrice di dimensioni fisse:

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

[**min \_ is**](min-is.md)
</dt> <dt>

[**size \_ è**](size-is.md)
</dt> </dl>

 

 