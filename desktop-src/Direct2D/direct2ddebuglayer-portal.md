---
title: Livello di debug Direct2D
description: Estensione di runtime per Direct2D che offre messaggi di errore descrittivi, rilevamento delle perdite di oggetti, notifiche sulle prestazioni e altri suggerimenti per la creazione di app Direct2D.
ms.assetid: 23b522d4-0733-4892-b93d-28f899fa0f17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f71b1364e645859059fb090634cbdae6f8c084e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395458"
---
# <a name="direct2d-debug-layer"></a>Livello di debug Direct2D

## <a name="purpose"></a>Scopo

Il livello di debug Direct2D, implementato separatamente da Direct2D nella propria DLL denominata d2d1debug.dll, fornisce messaggi di debug in fase di progettazione per ridurre al minimo l'errore dell'applicazione di Runtime. I messaggi di debug spesso derivano da violazioni dei contratti API, ad esempio parametri non validi (potrebbe essere correlato a Direct3D), risorse non valide, violazioni del threading e altri problemi di prestazioni, ad esempio l'utilizzo di un livello quando il clip sarebbe sufficiente.

Per decidere la quantità di informazioni tracciate dal livello di debug, il livello di debug offre tre livelli di debug: informazioni, avviso ed errore. Questi tre livelli sono interpretati nel modo seguente:

-   **Errore:** Direct2D invia messaggi di errore gravi al livello di debug. Se ad esempio si interrompe un vincolo di threading, verrà generato un errore grave.

    Inoltre, un messaggio di errore di livello attiva il punto di interruzione per facilitare il debug.

-   **Avviso:** Direct2D invia messaggi di errore e avvisi al livello di debug in modo che sia possibile risolvere uno di questi messaggi.

-   **Informazioni:** Direct2D invia messaggi di errore, avvisi e informazioni di diagnostica aggiuntive al livello di debug. Ad esempio, i messaggi di miglioramento delle prestazioni verranno inviati a questo livello di debug.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Installazione del livello di debug Direct2D](installing-the-direct2d-debug-layer.md)<br/> | Viene descritto come installare il livello di debug Direct2D.<br/>      |
| [Panoramica del livello di debug Direct2D](direct2ddebuglayer-overview.md)<br/>               |                                                                    |
| [Messaggi di debug](direct2ddebuglayer-debugmessages.md)<br/>                         | Elenca i messaggi di debug dal livello di debug Direct2D.<br/> |



 

 

 





