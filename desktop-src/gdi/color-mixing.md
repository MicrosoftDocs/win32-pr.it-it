---
description: La combinazione di colori consente a un'applicazione di creare nuovi colori combinando il colore della penna o del pennello con i colori nell'immagine esistente.
ms.assetid: 4a5dff8c-f75f-41d2-8367-33d97d4fd010
title: Combinazione di colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed1adde68360d7050e0cebb6e7d5ac073b36a3c18c3687990c1f2aea6a5719f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105730"
---
# <a name="color-mixing"></a>Combinazione di colori

La combinazione di colori consente a un'applicazione di creare nuovi colori combinando il colore della penna o del pennello con i colori nell'immagine esistente. L'applicazione può scegliere di disegnare il colore della penna o del pennello così come è (disegnando in modo efficace su qualsiasi immagine esistente) o di combinare il colore con i colori già presenti.

La modalità di combinazione in primo piano, talvolta denominata operazione raster binaria, determina la modalità di combinazione di questi colori. Un'applicazione può unire i colori, mantenendo tutti i componenti di entrambi i colori; mascherare i colori, rimuovere o moderare i componenti che non sono comuni; o mascherare esclusivamente i colori, rimuovendo o moderando i componenti comuni. Esistono diverse variazioni in queste operazioni di combinazione di base.

La combinazione di colori è soggetta all'approssimazione del colore. Se il risultato della combinazione di colori è un colore che il dispositivo non può generare, il sistema approssima il risultato, usando un colore che può generare. Se un'applicazione combina colori dithering, i singoli colori usati per creare il colore dithering vengono misti e i risultati sono soggetti all'approssimazione del colore.

Un'applicazione imposta la modalità di combinazione in primo piano usando la [**funzione SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) e recupera la modalità corrente usando la [**funzione GetROP2.**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)

Anche se è presente una modalità di combinazione di sfondo, tale modalità non controlla la combinazione di colori. Specifica invece se viene usato un colore di sfondo quando si disegnano linee con stile, pennelli tratteggiati e testo.

 

 



