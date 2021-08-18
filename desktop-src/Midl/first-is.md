---
title: first_is (attributo)
description: L'attributo \ \_ first is\ specifica l'indice del primo elemento della matrice da trasmettere.
ms.assetid: 1de7821c-19e7-4b2c-98fc-2fae3563831c
keywords:
- first_is attributo MIDL
topic_type:
- apiref
api_name:
- first_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d08be3ce14074c126a35272ede1b670121634f75d0b3d6cfb0db34e4f305760
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067281"
---
# <a name="first_is-attribute"></a>first \_ è attribute

Il \[ **primo \_ è** l'attributo che specifica l'indice del primo elemento della matrice \] da trasmettere.

``` syntax
first_is(limited-expression-list)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*limited-expression-list* 
</dt> <dd>

Specifica una o più espressioni in linguaggio C. Ogni espressione restituisce un intero che rappresenta l'indice di matrice del primo elemento della matrice da trasmettere. Il compilatore MIDL supporta espressioni condizionali, espressioni logiche, espressioni relazionali ed espressioni aritmetiche. MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di incremento e decremento. Separare più espressioni con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se il **\[ primo \_ è \]** l'attributo non è presente o se l'indice specificato è un numero negativo, l'elemento della matrice zero è il primo elemento trasmesso.

Il **\[ primo \_ è \]** attribute può anche aiutare a determinare i valori degli indici di matrice corrispondenti all'ultimo è o length è attribute quando questi attributi non **\[** [**\_**](last-is.md) sono **\]** **\[** [**\_**](length-is.md) **\]** specificati. La relazione tra questi indici di matrice è:

``` syntax
length = last - first + 1
```

Anche la relazione seguente deve contenere:

``` syntax
0 <= first_is <= max_is
```

La relazione seguente deve contenere **\[** [**quando max \_ è**](max-is.md) **\] <= 0:**

``` syntax
first_is == 0
```

Il **\[ primo \_ è \]** l'attributo non può essere usato contemporaneamente all'attributo **\[** [](string.md) **\]** stringa.

L'uso di un'espressione costante **\[ con il primo \_ attributo \]** è un uso non appropriato dell'attributo . È legale, ma inefficiente e comporta un marshalling più lento del codice.

## <a name="examples"></a>Esempi

``` syntax
HRESULT Proc1(
    [in] short First,
    [first_is(First)] Arr[10]);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[attributi \_ di campo](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**\_l'ultimo è**](last-is.md)
</dt> <dt>

[**length \_ è**](length-is.md)
</dt> <dt>

[**max \_ è**](max-is.md)
</dt> <dt>

[**min \_ è**](min-is.md)
</dt> <dt>

[**size \_ è**](size-is.md)
</dt> <dt>

[**string**](string.md)
</dt> </dl>

 

 