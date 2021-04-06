---
title: " elif"
description: La direttiva \ Elif contrassegna una clausola facoltativa di un blocco di compilazione condizionale definito da una direttiva \ ifdef, \ ifndef o \ if.
ms.assetid: 432b8543-7e1a-411a-8191-cc0f0e4a2e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a548cff74151dadf4a83a1e7d91ceedeafe07e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044849"
---
# <a name="elif"></a>\#elif

La direttiva **\# Elif** contrassegna una clausola facoltativa di un blocco di compilazione condizionale definito da una direttiva **\# ifdef**, **\# ifndef** o **\# if** . La direttiva controlla la compilazione condizionale del file di risorse controllando l'espressione costante specificata. Se l'espressione costante è diversa da zero, **\# Elif** indica al compilatore di continuare l'elaborazione delle istruzioni fino alla successiva direttiva **\# endif**, **\# else** o **\# Elif** e quindi di passare all'istruzione dopo **\# endif**. Se l'espressione costante è zero, **\# Elif** indica al compilatore di passare alla successiva direttiva **\# endif**, **\# else** o **\# Elif** . È possibile utilizzare un numero qualsiasi di direttive **\# Elif** in un blocco condizionale.

``` syntax
#elif constant-expression
```

<dl> <dt>

<span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*espressione costante*
</dt> <dd>

Espressione da controllare. Questo valore è un nome definito, una costante Integer o un'espressione costituita da nomi, numeri interi e operatori aritmetici e relazionali.

</dd> </dl>

## <a name="example"></a>Esempio

In questo esempio, **\# Elif** indica al compilatore di elaborare la seconda istruzione [**bitmap**](bitmap-resource.md) solo se il valore assegnato alla versione del nome è minore di 7. La direttiva **\# Elif** viene elaborata solo se Version è maggiore o uguale a 3.

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#elif Version < 7
BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direttive per il preprocessore](preprocessor-directives.md)
</dt> </dl>

 

 




