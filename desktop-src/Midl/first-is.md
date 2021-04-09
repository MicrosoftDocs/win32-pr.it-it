---
title: first_is (attributo)
description: L'attributo \ First \_ is \ specifica l'indice del primo elemento della matrice da trasmettere.
ms.assetid: 1de7821c-19e7-4b2c-98fc-2fae3563831c
keywords:
- attributo first_is MIDL
topic_type:
- apiref
api_name:
- first_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1d8d1be33299354e77ef92d885bb3b092cccfb6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872518"
---
# <a name="first_is-attribute"></a>primo \_ attributo

Il \[ **primo attributo \_ è** \] che specifica l'indice del primo elemento di matrice da trasmettere.

``` syntax
first_is(limited-expression-list)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*elenco di espressioni limitate* 
</dt> <dd>

Specifica una o più espressioni del linguaggio C. Ogni espressione restituisce un intero che rappresenta l'indice della matrice del primo elemento di matrice da trasmettere. Il compilatore MIDL supporta le espressioni condizionali, le espressioni logiche, le espressioni relazionali e le espressioni aritmetiche. MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di incremento e decremento. Separare più espressioni con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se il **\[ primo \_ \]** attributo non è presente o se l'indice specificato è un numero negativo, l'elemento della matrice zero è il primo elemento trasmesso.

Il **\[ primo \_ attributo \] è** anche in grado di determinare i valori degli indici della matrice corrispondenti all' **\[** [**ultimo \_**](last-is.md) oggetto **\]** o la **\[** [**lunghezza \_ è**](length-is.md) **\]** attributo quando questi attributi non sono specificati. La relazione tra gli indici di matrice è la seguente:

``` syntax
length = last - first + 1
```

È inoltre necessario che la relazione seguente contenga:

``` syntax
0 <= first_is <= max_is
```

È necessario che la relazione seguente venga mantenuta quando **\[** [**Max \_ è**](max-is.md) **\] <= 0:**

``` syntax
first_is == 0
```

Il **\[ primo \_ attributo \] is** non può essere utilizzato contemporaneamente all' **\[** attributo [**String**](string.md) **\]** .

L'utilizzo di un'espressione costante con il **\[ primo attributo \_ è \]** un utilizzo non appropriato dell'attributo. È valido, ma inefficiente, e comporterà il codice di marshalling più lento.

## <a name="examples"></a>Esempi

``` syntax
HRESULT Proc1(
    [in] short First,
    [first_is(First)] Arr[10]);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[attributi di campo \_](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ultimo \_ è**](last-is.md)
</dt> <dt>

[**lunghezza \_**](length-is.md)
</dt> <dt>

[**Max \_ è**](max-is.md)
</dt> <dt>

[**min \_ è**](min-is.md)
</dt> <dt>

[**dimensioni \_**](size-is.md)
</dt> <dt>

[**string**](string.md)
</dt> </dl>

 

 