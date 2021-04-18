---
title: last_is (attributo)
description: Il campo attributo \ Last \_ is \ specifica l'indice dell'ultimo elemento della matrice da trasmettere. Quando l'indice specificato è zero o negativo, non viene trasmesso alcun elemento della matrice.
ms.assetid: 42a5cb0d-0887-4aa7-b34f-2fbad0f4c8ab
keywords:
- attributo last_is MIDL
topic_type:
- apiref
api_name:
- last_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 453a51109452f3cdacb1a48e67b76ccbc9f2e257
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516774"
---
# <a name="last_is-attribute"></a>\_attributo Last is

L'attributo Field **\[ Last \_ viene \]** specificato l'indice dell'ultimo elemento della matrice da trasmettere. Quando l'indice specificato è zero o negativo, non viene trasmesso alcun elemento della matrice.

``` syntax
[last_is( limited-expression-list )]
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*elenco di espressioni limitate* 
</dt> <dd>

Specifica una o più espressioni del linguaggio C. Ogni espressione restituisce un intero che rappresenta l'indice della matrice dell'ultimo elemento della matrice da trasmettere. Il compilatore MIDL supporta le espressioni condizionali, le espressioni logiche, le espressioni relazionali e le espressioni aritmetiche. MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di incremento e decremento. Separare più espressioni con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ Last \_ is \]** determina che il valore dell'indice della matrice corrispondente alla **\[** [**\_**](length-is.md) **\]** **\[ \_ \]** lunghezza è Attribute quando length non è specificato. La relazione tra questi indici di matrice è la seguente: length = Last-First + 1.

Se il valore dell'indice della matrice specificato da **\[** [**First \_**](first-is.md) è **\]** maggiore del valore specificato da **\[ Last \_ \] è**, verranno trasmessi zero elementi.

L'attributo **\[ Last \_ is \]** non può essere utilizzato come attributo di campo nello stesso momento in cui la **\[** [**lunghezza \_ è**](length-is.md) **\]** Attribute o l' **\[** attributo [**String**](string.md) **\]** .

L'utilizzo di un'espressione costante con l'attributo **\[ Last \_ è \]** un utilizzo non appropriato dell'attributo. È valido, ma inefficiente, e comporterà il codice di marshalling più lento.

Se il valore specificato da **\[** [**Max \_ è**](max-is.md) **\]** uguale a o maggiore di zero, deve essere true la relazione seguente: 0 <= Last \_ è <= Max \_ è.

## <a name="examples"></a>Esempi

``` syntax
proc1(
    [in] short Last,
    [in, last_is(Last)] short asNumbers[MAXSIZE]);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Attributi di campo](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**il primo \_ è**](first-is.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**lunghezza \_**](length-is.md)
</dt> <dt>

[**Max \_ è**](max-is.md)
</dt> <dt>

[**dimensioni \_**](size-is.md)
</dt> </dl>

 

 