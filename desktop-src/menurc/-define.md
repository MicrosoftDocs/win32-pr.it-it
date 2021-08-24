---
title: " define"
description: La direttiva \ define assegna il valore specificato al nome specificato. Tutte le occorrenze successive del nome vengono sostituite dal valore .
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8e8f99dc592eefb1fb79201883e8a32837633814b79d7819e84d283709a46f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826051"
---
# <a name="define"></a>\#Definire

La **\# direttiva define** assegna il valore specificato al nome specificato. Tutte le occorrenze successive del nome vengono sostituite dal valore .

``` syntax
#define name value
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Nome*
</dt> <dd>

Nome da definire. Questo valore è qualsiasi combinazione di lettere, cifre e punteggiatura valida per il preprocessore C/C++.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*Valore*
</dt> <dd>

Integer, stringa di caratteri o riga di testo.

</dd> </dl>

## <a name="example"></a>Esempio

In questo esempio vengono assegnati valori ai nomi NONZERO e USERCLASS:

``` syntax
#define     NONZERO     1
#define     USERCLASS   "MyControlClass"
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direttive per il preprocessore](preprocessor-directives.md)
</dt> </dl>

 

 




