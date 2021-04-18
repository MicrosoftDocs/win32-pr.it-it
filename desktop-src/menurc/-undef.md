---
title: " undef"
description: La direttiva \ undef rimuove la definizione corrente del nome specificato. Tutte le occorrenze successive del nome vengono elaborate senza sostituzione.
ms.assetid: c9a0b538-3030-4d39-bfc2-d158061967b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b14eeea18a05795cd8ebbb94d81d0aead6a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298243"
---
# <a name="undef"></a>\#undef

La direttiva **\# undef** rimuove la definizione corrente del nome specificato. Tutte le occorrenze successive del nome vengono elaborate senza sostituzione.

``` syntax
#undef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*nome*
</dt> <dd>

Nome da rimuovere. Questo valore è costituito da qualsiasi combinazione di lettere, cifre e punteggiatura valida per il preprocessore C/C++.

</dd> </dl>

## <a name="example"></a>Esempio

In questo esempio vengono rimosse le definizioni per i nomi diversi da zero e USERCLASS:

``` syntax
#undef     nonzero
#undef     USERCLASS
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direttive per il preprocessore](preprocessor-directives.md)
</dt> </dl>

 

 




