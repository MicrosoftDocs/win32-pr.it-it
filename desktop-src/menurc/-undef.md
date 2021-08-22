---
title: " undef"
description: La direttiva \ undef rimuove la definizione corrente del nome specificato. Tutte le occorrenze successive del nome vengono elaborate senza sostituzione.
ms.assetid: c9a0b538-3030-4d39-bfc2-d158061967b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3adf208ecca3f130aefc99de8d2926028f25bcd46be46d42e4cbf92e708fa0b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118473061"
---
# <a name="undef"></a>\#undef

La **\# direttiva undef** rimuove la definizione corrente del nome specificato. Tutte le occorrenze successive del nome vengono elaborate senza sostituzione.

``` syntax
#undef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Nome*
</dt> <dd>

Nome da rimuovere. Questo valore è qualsiasi combinazione di lettere, cifre e punteggiatura valida per il preprocessore C/C++.

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

 

 




