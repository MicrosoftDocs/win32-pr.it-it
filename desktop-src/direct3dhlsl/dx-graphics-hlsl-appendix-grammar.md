---
title: Grammatica
description: Le istruzioni HLSL vengono costruite usando le regole seguenti per la grammatica.
ms.assetid: 683248e9-6fc7-451a-906b-6e0aab1b0c8c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b77f1050beaee2b269d12e69704018e3c5abee6e
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129849"
---
# <a name="grammar"></a>Grammatica

Le istruzioni HLSL vengono costruite usando le regole seguenti per la grammatica.

-   [Spazio vuoto](#whitespace)
-   [Numeri a virgola mobile](#floating-point-numbers)
-   [Numeri interi](#integer-numbers)
-   [Caratteri](#characters)
-   [Stringhe](#strings)
-   [Identificatori](#identifiers)
-   [Operatori](#operators)
-   [Argomenti correlati](#related-topics)

## <a name="whitespace"></a>Spazio vuoto

I caratteri seguenti vengono riconosciuti come spazi vuoti.

- SPACE
- TAB
- Eol
- Commenti in stile C (/ \* \* /)
- Commenti in stile C++ (//)

## <a name="floating-point-numbers"></a>Numeri a virgola mobile

I numeri a virgola mobile sono rappresentati in HLSL come segue:

-   fractional-constant exponent-part(opt) floating-suffix(opt)

    digit-sequence exponent-part floating-suffix(opt)

-   fractional-constant :

    digit-sequence(opt) . digit-sequence

    digit-sequence .

-   exponent-part :

    e sign(opt) digit-sequence

    E sign(opt) digit-sequence

-   sign : uno tra

    \+ -

-   digit-sequence :

    digit

    digit-sequence digit

-   floating-suffix : uno tra

    h H f F l L

    Usare il suffisso "L" per specificare un valore letterale a virgola mobile e precisione a 64 bit completo. Un valore letterale float a 32 bit è il valore predefinito.

    Ad esempio, il compilatore riconosce il valore letterale seguente come valore letterale a virgola mobile e precisione a 32 bit e ignora i bit inferiori:

    ```
    double x = -0.6473313946860445;
    ```

    

    Il compilatore riconosce il valore letterale seguente come valore letterale a virgola mobile e precisione a 64 bit:

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a>Numeri interi

I numeri interi sono rappresentati in HLSL come segue:

-   integer-constant integer-suffix(opt)
-   integer-constant: uno di

    \# (numero decimale)

    0 \# (numero ottale)

    0x \# (numero esadecimale)

-   integer-suffix può essere uno dei seguenti:

    u U l L

## <a name="characters"></a>Caratteri

I caratteri sono rappresentati in HLSL come indicato di seguito:



| Carattere                                          | Descrizione                                                                |
|-------------------------------------------|-----------------------------------------------------------------|
| 'c'                                       | (carattere)                                                     |
| \\'a' \\ 'b' \\ 'f' \\ 'b' \\ 'r' \\ 't' \\ 'v' | (caratteri di escape)                                                       |
| '\\\#\#\#'                                | (escape ottale, ognuno \# è una cifra ottale)                       |
| ' \\ x \# '                                   | (carattere di escape esadecimale, \# numero esadecimale, qualsiasi numero di cifre)            |
| \\'c'                                     | (c è un altro carattere, incluse la barra rovesciata e le virgolette) |



 

Gli escape non sono supportati nelle espressioni del preprocessore.

## <a name="strings"></a>Stringhe

Le stringhe sono rappresentate in HLSL come indicato di seguito:

"s" (s è qualsiasi stringa con caratteri di escape).

## <a name="identifiers"></a>Identificatori

Gli identificatori sono rappresentati in HLSL come segue:


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a>Operatori


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



Qualsiasi altro carattere singolo che non corrisponde a un'altra regola.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Appendice (DirectX HLSL)](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




