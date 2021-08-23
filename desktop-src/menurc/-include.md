---
title: " include"
description: La direttiva \ include fa in modo che il compilatore di risorse eelaborare il file specificato nel parametro filename.
ms.assetid: 9a3505c6-c19f-4c4f-85a4-94fbcfc0f9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bf5d6fa40e45073ca7ccb5f97dd3ddb0d13dfdfced965d5c83332183da421e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599720"
---
# <a name="-include"></a>'include'

La **\# direttiva include** fa in modo che il compilatore di risorse eelaborare il file specificato nel parametro *filename.* Questo file deve essere un file di intestazione che definisce le costanti usate nel file di definizione delle risorse. Il file può usare caratteri a byte singolo, a byte doppio o Unicode.

``` syntax
#include filename
```

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Filename*
</dt> <dd>

Nome del file da includere. Se il file si trova nella directory corrente, la stringa deve essere racchiusa tra virgolette doppie. Se il file si trova nella directory specificata dalla variabile di ambiente INCLUDE, la stringa deve essere racchiusa tra caratteri minore di e maggiore di (<>). È necessario specificare un percorso completo racchiuso tra virgolette doppie (") se il file non si trova nella directory corrente o nella directory specificata dalla variabile di ambiente INCLUDE.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare l'istruzione seguente nel file di intestazione per racchiudere le istruzioni che possono essere compilate da un compilatore C ma non da RC:

``` syntax
#ifndef RC_INVOKED
```

In questo modo, è possibile usare gli stessi file di inclusione nei file con estensione c e rc.

## <a name="example"></a>Esempio

Questo esempio elabora i file di intestazione Windows.h e MyDefs.h durante la compilazione del file di definizione della risorsa:

``` syntax
#include <windows.h>
#include "headers\mydefs.h"
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direttive per il preprocessore](preprocessor-directives.md)
</dt> </dl>

 

 




