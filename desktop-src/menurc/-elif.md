---
title: " elif"
description: La direttiva \ elif contrassegna una clausola facoltativa di un blocco di compilazione condizionale definita da una direttiva \ ifdef, \ ifndef o \ if.
ms.assetid: 432b8543-7e1a-411a-8191-cc0f0e4a2e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e131d40648bcda75025087717798ceb2ad1262d680877512dbb85a451fc86e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720901"
---
# <a name="elif"></a>\#Elif

La **\# direttiva elif** contrassegna una clausola facoltativa di un blocco di compilazione condizionale definita da una direttiva **\# ifdef**, **\# ifndef** o **\# if.** La direttiva controlla la compilazione condizionale del file di risorse controllando l'espressione costante specificata. Se l'espressione costante è diversa da zero, **\# elif** indica al compilatore di continuare a elaborare le istruzioni fino alla successiva direttiva **\# endif**, **\# else** o **\# elif** e quindi di passare all'istruzione dopo **\# endif**. Se l'espressione costante è zero, **\# elif** indica al compilatore di passare alla direttiva **\# endif**, **\# else** o **\# elif** successiva. È possibile usare qualsiasi numero di **\# direttive elif** in un blocco condizionale.

``` syntax
#elif constant-expression
```

<dl> <dt>

<span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*
</dt> <dd>

Espressione da controllare. Questo valore è un nome definito, una costante integer o un'espressione costituita da nomi, numeri interi e operatori aritmetici e relazionali.

</dd> </dl>

## <a name="example"></a>Esempio

In questo esempio elif indica al **\# compilatore** di elaborare la seconda [**istruzione BITMAP**](bitmap-resource.md) solo se il valore assegnato al nome Version è minore di 7. La **\# direttiva elif** viene elaborata solo se Version è maggiore o uguale a 3.

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

 

 




