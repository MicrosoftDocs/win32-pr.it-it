---
description: La combinazione di colori consente a un'applicazione di creare nuovi colori combinando il colore della penna o del pennello con i colori dell'immagine esistente.
ms.assetid: 4a5dff8c-f75f-41d2-8367-33d97d4fd010
title: Combinazione di colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa85f6ea449fa13f7b7120160915ea72a0e3dd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130814"
---
# <a name="color-mixing"></a>Combinazione di colori

La combinazione di colori consente a un'applicazione di creare nuovi colori combinando il colore della penna o del pennello con i colori dell'immagine esistente. L'applicazione può scegliere di disegnare la penna o il colore del pennello così come è (disegno efficace di qualsiasi immagine esistente) o di combinare il colore con i colori già presenti.

La modalità di combinazione di primo piano, talvolta chiamata operazione raster binaria, determina il modo in cui questi colori vengono combinati. Un'applicazione può unire i colori, mantenendo tutti i componenti di entrambi i colori; mascherare i colori, rimuovere o moderare i componenti che non sono comuni; o mascherano esclusivamente i colori, rimuovendo o moderando i componenti comuni. Questa operazione di combinazione di base prevede diverse varianti.

La combinazione di colori è soggetta all'approssimazione del colore. Se il risultato della combinazione di colori è un colore che il dispositivo non è in grado di generare, il sistema approssima il risultato, usando un colore che può generare. Se un'applicazione combina colori diversi, i singoli colori utilizzati per creare il colore con rethereing vengono combinati e i risultati sono soggetti a approssimazione dei colori.

Un'applicazione imposta la modalità di combinazione di primo piano usando la funzione [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) e recupera la modalità corrente usando la funzione [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) .

Sebbene sia disponibile una modalità di combinazione in background, questa modalità non controlla la combinazione di colori. Specifica invece se usare un colore di sfondo quando si disegnano linee con stile, pennelli tratteggiati e testo.

 

 



