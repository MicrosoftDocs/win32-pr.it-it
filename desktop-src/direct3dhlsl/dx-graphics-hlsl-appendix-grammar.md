---
title: Grammatica
description: Le istruzioni HLSL vengono create usando le regole seguenti per la grammatica.
ms.assetid: 683248e9-6fc7-451a-906b-6e0aab1b0c8c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d2346e1ca2302f80c796558b4aa2bbdce016d494
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516519"
---
# <a name="grammar"></a>Grammatica

Le istruzioni HLSL vengono create usando le regole seguenti per la grammatica.

-   [Whitespace](#whitespace)
-   [Numeri a virgola mobile](#floating-point-numbers)
-   [Numeri interi](#integer-numbers)
-   [Caratteri](#characters)
-   [Stringhe](#strings)
-   [Identificatori](#identifiers)
-   [Operatori](#operators)
-   [Argomenti correlati](#related-topics)

## <a name="whitespace"></a>Spazi vuoti

I caratteri seguenti sono riconosciuti come spazi vuoti.



|                            |
|----------------------------|
| SPACE                      |
| TAB                        |
| FINE riga                        |
| Commenti in stile C (/ \* \* /) |
| Commenti in stile C++ (//)    |



 

## <a name="floating-point-numbers"></a>Numeri a virgola mobile

I numeri a virgola mobile sono rappresentati in HLSL, come indicato di seguito:

-   frazionario: suffisso a virgola mobile (opt) a virgola mobile (opt)

    cifre-sequenza esponente-parte a virgola mobile (opt)

-   costante frazionaria:

    digit-Sequence (opt). digit-sequence

    sequenza numerica.

-   parte esponente:

    segno e (opt) digit-Sequence

    Segno E (opt) digit-Sequence

-   sign : uno tra

    \+ -

-   sequenza numerica:

    digit

    digit-sequence digit

-   floating-suffix : uno tra

    h H f l L

    Usare il suffisso "L" per specificare un valore letterale a virgola mobile con precisione a 64 bit completo. Il valore predefinito è un valore letterale float a 32 bit.

    Il compilatore, ad esempio, riconosce il valore letterale seguente come valore letterale a virgola mobile con precisione a 32 bit e ignora i bit inferiori:

    ```
    double x = -0.6473313946860445;
    ```

    

    Il compilatore riconosce il valore letterale seguente come valore letterale a virgola mobile con precisione a 64 bit:

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a>Numeri interi

I numeri interi sono rappresentati in HLSL, come indicato di seguito:

-   Integer-Constant Integer-suffisso (opt)
-   costante Integer: uno tra

    \# (numero decimale)

    0 \# (numero ottale)

    0x \# (numero esadecimale)

-   il suffisso Integer può essere uno dei seguenti:

    u U l

## <a name="characters"></a>Caratteri

I caratteri sono rappresentati in HLSL, come indicato di seguito:



|                                           |                                                                 |
|-------------------------------------------|-----------------------------------------------------------------|
| c                                       | carattere                                                     |
| ' \\ a' \\ b '' \\ f '' \\ b '' \\ r '' T'' \\ \\ v' | Escape                                                       |
| '\\\#\#\#'                                | (escape ottale, ognuno \# è una cifra ottale)                       |
| ' \\ x \# '                                   | (escape esadecimale, \# è un numero esadecimale, un numero qualsiasi di cifre)            |
| ' \\ c'                                     | (c è un altro carattere, incluse la barra rovesciata e le virgolette) |



 

Le espressioni di escape non sono supportate nelle espressioni del preprocessore.

## <a name="strings"></a>Stringhe

Le stringhe sono rappresentate in HLSL, come indicato di seguito:

"s" (s è qualsiasi stringa con caratteri di escape).

## <a name="identifiers"></a>Identificatori

Gli identificatori sono rappresentati in HLSL, come indicato di seguito:


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a>Operatori


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



Anche qualsiasi altro carattere singolo che non corrisponde a un'altra regola.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Appendice (DirectX HLSL)](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




