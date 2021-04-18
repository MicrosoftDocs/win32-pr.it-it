---
title: Classificazioni
description: Classificazioni
ms.assetid: babc9db5-2782-4261-a571-acb7be4ea770
keywords:
- Interfacce di Windows Media Player Mobile, classificazioni
- interfacce, classificazioni
- riferimento per interfacce, classificazioni
- classificazioni in interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb90908c725fcb525e0be1547c27c588a4220c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298698"
---
# <a name="ratings"></a>Classificazioni

Quando si crea un'interfaccia personalizzata per Windows Media Player 10,1 Mobile, è possibile visualizzare la classificazione associata al contenuto basato su Windows Media Audio in corso di riproduzione. La classificazione viene visualizzata come stella con un numero. La stella sarà numerata da uno a cinque, indicando la classificazione corrente per quel contenuto. Se il contenuto non viene valutato, la stella sarà numerata zero.

La sezione classificazioni del file di definizione dell'interfaccia personalizzata inizia con questa riga:


```C++
[ Ratings ]

```



È quindi necessario aggiungere una riga che contiene informazioni sulle dimensioni e la posizione dell'icona di classificazione nell'interfaccia.


```C++
147, 3, 22, 21       ratings96S.gif

```



È possibile usare il modello seguente per la sezione ratings del file di definizione dell'interfaccia personalizzata:


```C++
// <Location>           <Image>
// ---------------      --------------------
```



È anche possibile assegnare un valore di classificazione a un elemento multimediale tramite l'interfaccia utente in Windows Media Player 10,1 mobile e alla successiva sincronizzazione del dispositivo con il computer, il nuovo valore delle classificazioni verrà propagato a tale elemento multimediale se risiede nella libreria di Windows Media Player 10.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento all'interfaccia**](skin-reference.md)
</dt> </dl>

 

 




