---
title: " if"
description: La direttiva \ if controlla la compilazione condizionale del file di risorse controllando l'espressione costante specificata.
ms.assetid: 4d0f26a0-1a2d-4fad-b5ce-b9441397d2c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364d6f5eb818813f61f6428446effb4793b96b2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298246"
---
# <a name="if"></a>\#Se

La direttiva **\# if** controlla la compilazione condizionale del file di risorse controllando l'espressione costante specificata. Se l'espressione costante è diversa da zero, **\# se** indica al compilatore di continuare a elaborare istruzioni fino alla direttiva **\# endif**, **\# else** o **\# Elif** successiva e quindi di passare all'istruzione dopo la direttiva **\# endif** . Se l'espressione costante è zero, **\# se** indica al compilatore di ignorare la direttiva **\# endif**, **\# else** o **\# Elif** successiva.

``` syntax
#if constant-expression
```

<dl> <dt>

<span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*espressione costante*
</dt> <dd>

Espressione da controllare. Questo valore è un nome definito, una costante Integer o un'espressione costituita da nomi, numeri interi e operatori aritmetici e relazionali.

</dd> </dl>

## <a name="example"></a>Esempio

In questo esempio viene compilata l'istruzione [**bitmap**](bitmap-resource.md) solo se la versione assegnata al valore è minore di 3:

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direttive per il preprocessore](preprocessor-directives.md)
</dt> </dl>

 

 




