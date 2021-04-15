---
title: " include"
description: La direttiva \ include fa in modo che il compilatore di risorse elabori il file specificato nel parametro filename.
ms.assetid: 9a3505c6-c19f-4c4f-85a4-94fbcfc0f9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8d36f1d0ae24f3dc21d67eec57056872aabdbd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400178"
---
# <a name="-include"></a>includere

La direttiva **\# include** fa in modo che il compilatore di risorse elabori il file specificato nel parametro *filename* . Questo file deve essere un file di intestazione che definisce le costanti usate nel file di definizione delle risorse. Il file può utilizzare caratteri a byte singolo, a doppio byte o Unicode.

``` syntax
#include filename
```

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*filename*
</dt> <dd>

Nome del file da includere. Se il file si trova nella directory corrente, la stringa deve essere racchiusa tra virgolette doppie. Se il file si trova nella directory specificata dalla variabile di ambiente INCLUDE, la stringa deve essere racchiusa tra caratteri minore di e maggiore di (<>). È necessario fornire un percorso completo racchiuso tra virgolette doppie (") se il file non si trova nella directory corrente o nella directory specificata dalla variabile di ambiente INCLUDE.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare l'istruzione seguente nel file di intestazione per racchiudere le istruzioni che possono essere compilate da un compilatore C ma non da RC:

``` syntax
#ifndef RC_INVOKED
```

In questo modo, è possibile usare gli stessi file di inclusione nei file con estensione c e RC.

## <a name="example"></a>Esempio

Questo esempio elabora i file di intestazione Windows. h e MyDefs. h durante la compilazione del file di definizione delle risorse:

``` syntax
#include <windows.h>
#include "headers\mydefs.h"
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direttive per il preprocessore](preprocessor-directives.md)
</dt> </dl>

 

 




