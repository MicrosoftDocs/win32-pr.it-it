---
title: Progettazione dell'interfaccia
description: Progettazione dell'interfaccia
ms.assetid: 7b87bab4-8246-461a-a9cd-2d348e7f0d48
keywords:
- Windows Media Player Interfacce per dispositivi mobili, interfacce utente
- interfacce, interfacce utente
- creazione di interfacce, interfacce utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b11dee2a6236f2a279756644a88d69e267c5da93240b5e12c19c32d86e30a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749863"
---
# <a name="designing-the-interface"></a>Progettazione dell'interfaccia

Dopo aver scelto le funzioni, l'interfaccia può essere progettata. È stata scelta un'interfaccia semplice che corrisponde alla funzionalità. I simboli per i controlli sono stati scelti dai controlli vcr standard.

L'immagine seguente mostra l'aspetto dell'interfaccia.

![interfaccia di esempio](images/ceswmful.png)

-   **Pulsante PlayPause o PlayPauseStop.** L'utente lo tocca di più, quindi è possibile prendere in considerazione un pulsante più grande. L'angolo superiore destro rappresenta una posizione che l'utente può trovare rapidamente. Viene usata una freccia a tinta unita per indicare il gioco e due barre verticali (non mostrate qui) per indicare la sospensione.
    > [!Note]  
    > Il pulsante PlayPauseStop può essere usato solo quando si crea un'interfaccia per Windows Media Player 10 Mobile o versione successiva.

     

-   **Pulsante Arresta.** Per semplificare l'individuazione, viene posizionato nell'angolo superiore sinistro. Viene usato un quadrato per indicare l'arresto. Se si crea un'interfaccia per Windows Media Player 10 Mobile o versione successiva, il pulsante PlayPauseStop fornisce già questa funzionalità.
-   **Pulsanti Avanti e Prev.** Poiché non verranno usati con la frequenza, vengono posizionati a sinistra. Il pulsante Avanti è sopra il pulsante Prev perché è più probabile che gli utenti vogliano procedere in una playlist. I simboli a doppia freccia vengono usati perché sono simili nella funzione a un controllo di avanzamento rapido.
-   **Trackbar del volume.** Si trova nella parte inferiore dello schermo ed è una linea semplice con un pulsante a forma di pollice sopra.
-   **Casella di testo Selezione.** Si trova sotto il pulsante PlayPause o PlayPauseStop in modo che sia facile da vedere.

È possibile creare un disegno per primo e sperimentare la posizione di ogni elemento dell'interfaccia utente. La progettazione illustrata qui è stata scelta per semplicità e semplicità d'uso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida all'interfaccia**](skin-guide.md)
</dt> </dl>

 

 




