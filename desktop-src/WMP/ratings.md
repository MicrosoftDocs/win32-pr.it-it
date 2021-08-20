---
title: Classificazioni
description: Classificazioni
ms.assetid: babc9db5-2782-4261-a571-acb7be4ea770
keywords:
- Windows Media Player Interfaccia per dispositivi mobili, classificazioni
- skins,ratings
- informazioni di riferimento per le interfaccia, le classificazioni
- classificazioni nelle interfaccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eec9b28ef77c59b4ca2303c96426009f34b817c65e853071febc76507c3aac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934092"
---
# <a name="ratings"></a>Classificazioni

Quando si crea un'interfaccia per Windows Media Player 10.1 Mobile, è possibile visualizzare la classificazione associata al contenuto basato su Windows Media Audio attualmente in riproduzione. La classificazione viene visualizzata come stella con un numero. La stella verrà numerata da uno a cinque, indicando la classificazione corrente per tale contenuto. Se il contenuto non viene valutato, la stella sarà numerata zero.

La sezione Ratings del file di definizione dell'interfaccia inizia con questa riga:


```C++
[ Ratings ]

```



È quindi necessario aggiungere una riga contenente informazioni sulle dimensioni e sulla posizione dell'icona delle classificazioni nell'interfaccia.


```C++
147, 3, 22, 21       ratings96S.gif

```



È possibile usare il modello seguente per la sezione Ratings del file di definizione dell'interfaccia:


```C++
// <Location>           <Image>
// ---------------      --------------------
```



È anche possibile assegnare un valore ratings a un elemento multimediale tramite l'interfaccia utente di Windows Media Player 10.1 Mobile e alla successiva sincronizzazione del dispositivo con un computer, il nuovo valore ratings verrà propagato a tale elemento multimediale se si trova nella libreria di Windows Media Player 10.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento per l'interfaccia**](skin-reference.md)
</dt> </dl>

 

 




