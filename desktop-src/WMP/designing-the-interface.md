---
title: Progettazione dell'interfaccia
description: Progettazione dell'interfaccia
ms.assetid: 7b87bab4-8246-461a-a9cd-2d348e7f0d48
keywords:
- Interfacce utente di Windows Media Player Mobile, interfacce utente
- interfacce, interfacce utente
- creazione di interfacce, interfacce utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8070ef6fd4589f762624d7a0b5ee1d380a264066
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116889"
---
# <a name="designing-the-interface"></a>Progettazione dell'interfaccia

Una volta scelte le funzioni, è possibile progettare l'interfaccia. È stata scelta una semplice interfaccia per corrispondere alla funzionalità. I simboli per i controlli sono stati scelti dai controlli VCR standard.

L'immagine seguente mostra l'aspetto dell'interfaccia.

![interfaccia di esempio](images/ceswmful.png)

-   **Pulsante come playpause o PlayPauseStop.** L'utente sta toccando più questo, quindi è possibile considerare un pulsante più grande. L'angolo superiore destro costituisce una buona posizione che l'utente può trovare rapidamente. Viene usata una freccia a tinta unita per indicare la riproduzione e due barre verticali (non mostrate qui) per indicare la pausa.
    > [!Note]  
    > Il pulsante PlayPauseStop può essere usato solo quando si crea un'interfaccia per Windows Media Player 10 mobile o versione successiva.

     

-   **Pulsante Arresta.** Per facilitarne l'individuazione, è posizionata nell'angolo superiore sinistro. Un quadrato viene usato per indicare l'arresto. Se si sta creando un'interfaccia per Windows Media Player 10 mobile o versione successiva, il pulsante PlayPauseStop fornisce già questa funzionalità.
-   **Pulsanti avanti e indietro.** Poiché questi non verranno usati con la stessa frequenza, verranno posizionati a sinistra. Il successivo è sopra il pulsante indietro, perché è più probabile che si desideri procedere in una playlist. I simboli a doppia freccia vengono usati perché sono simili in funzione a un controllo di avanzamento rapido.
-   **TrackBar del volume.** Questa posizione viene posizionata nella parte inferiore della schermata ed è una linea semplice con un pulsante Thumb.
-   **Casella di testo Marquee.** Si trova sotto il pulsante come playpause o PlayPauseStop in modo che sia facile da vedere.

Si consiglia di disegnare questo primo e sperimentare la posizione di ogni elemento dell'interfaccia utente. Il progetto illustrato qui è stato scelto per semplicità e semplicità d'uso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida all'interfaccia**](skin-guide.md)
</dt> </dl>

 

 




