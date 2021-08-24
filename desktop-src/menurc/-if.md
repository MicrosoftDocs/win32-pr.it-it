---
title: " if"
description: La direttiva \ if controlla la compilazione condizionale del file di risorse controllando l'espressione costante specificata.
ms.assetid: 4d0f26a0-1a2d-4fad-b5ce-b9441397d2c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d898d0089ab6abeefb8c11e3a781446e498ed7c0f490545189987ec4857f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599712"
---
# <a name="if"></a>\#Se

La **\# direttiva if** controlla la compilazione condizionale del file di risorse controllando l'espressione costante specificata. Se l'espressione costante è diversa da **\# zero,** se indica al compilatore di continuare l'elaborazione delle istruzioni fino alla successiva direttiva **\# endif**, **\# else** o **\# elif** e quindi passare all'istruzione dopo la **\# direttiva endif.** Se l'espressione costante è zero, **\# se** indica al compilatore di passare alla direttiva **\# endif**, **\# else** **\# o elif** successiva.

``` syntax
#if constant-expression
```

<dl> <dt>

<span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*
</dt> <dd>

Espressione da controllare. Questo valore è un nome definito, una costante integer o un'espressione costituita da nomi, numeri interi e operatori aritmetici e relazionali.

</dd> </dl>

## <a name="example"></a>Esempio

Questo esempio compila [**l'istruzione BITMAP**](bitmap-resource.md) solo se il valore version assegnato è minore di 3:

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direttive per il preprocessore](preprocessor-directives.md)
</dt> </dl>

 

 




