---
title: Creazione del file di area
description: Creazione del file di area
ms.assetid: e901dfa1-1e06-4136-b877-64be03107f6f
keywords:
- Windows Media Player Skin per dispositivi mobili, file di area
- skins, file di area
- creazione di skin, file di area
- File di area nelle skin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28d517f9df077c3a19a116392229f126c798e5321a2564075e58a554954d9d05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341249"
---
# <a name="creating-the-region-file"></a>Creazione del file di area

È necessario creare un file di area che mostra le aree che rispondono ai tocchi. È sufficiente copiare i livelli di base di ogni elemento in un nuovo livello e colorarli in modo che corrispondano ai numeri di colore che verranno utilizzati nel file di definizione dell'interfaccia. Assicurarsi che le immagini create in questo livello siano solide e che non siano applicati effetti. È probabile che si vogliano annotare i numeri di colore per ogni immagine. È possibile ottenere i numeri di colore dal Selezione colori. Si vogliono i numeri RGB, che sono tre numeri decimali. Ogni numero è compreso tra 0 e 255. Ad esempio, un rosso a tinta unita sarebbe 255, 0, 0.

> [!Note]  
> I file di area non vengono usati in Windows Media Player 10 skin per dispositivi mobili perché i tipi di pulsante non sono supportati in Windows Media Player 10 Mobile o versioni successive.

 

L'immagine seguente è il file Region.

![file di area](images/ceswmreg.png)

Questo file contiene solo quattro immagini perché solo i pulsanti PlayPause, Stop, Next e Prev sono pulsanti di tipo hit-type.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione dell'oggetto Art**](creating-the-art.md)
</dt> </dl>

 

 




