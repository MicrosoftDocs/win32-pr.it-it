---
title: " define"
description: La direttiva \ define assegna il valore specificato al nome specificato. Tutte le occorrenze successive del nome vengono sostituite dal valore.
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557c6b486d9c2bd07b0b012c17e806f5d9eaae91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711950"
---
# <a name="define"></a>\#definire

La direttiva **\# define** assegna il valore specificato al nome specificato. Tutte le occorrenze successive del nome vengono sostituite dal valore.

``` syntax
#define name value
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*nome*
</dt> <dd>

Nome da definire. Questo valore è costituito da qualsiasi combinazione di lettere, cifre e punteggiatura valida per il preprocessore C/C++.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*valore*
</dt> <dd>

Integer, stringa di caratteri o riga di testo.

</dd> </dl>

## <a name="example"></a>Esempio

In questo esempio i valori vengono assegnati ai nomi diversi da ZERO e USERCLASS:

``` syntax
#define     NONZERO     1
#define     USERCLASS   "MyControlClass"
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direttive per il preprocessore](preprocessor-directives.md)
</dt> </dl>

 

 




