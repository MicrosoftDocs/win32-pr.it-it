---
title: Livello di debug Direct2D
description: Estensione di runtime per Direct2D che offre messaggi di errore descrittivi, rilevamento di perdite di oggetti, avvisi sulle prestazioni e altri segnali per la creazione di app Direct2D.
ms.assetid: 23b522d4-0733-4892-b93d-28f899fa0f17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29cb01c2f8f4f4b14694da94262847ae0def0817a13ffffc48f5c414a8eacda7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044361"
---
# <a name="direct2d-debug-layer"></a>Livello di debug Direct2D

## <a name="purpose"></a>Scopo

Il livello di debug Direct2D, implementato separatamente da Direct2D nella propria DLL denominata d2d1debug.dll, fornisce messaggi di debug in fase di progettazione per ridurre al minimo gli errori dell'applicazione di runtime. I messaggi di debug spesso derivano da violazioni dei contratti API, ad esempio parametri non validi (potrebbero essere correlati a Direct3D), risorse non valide, violazioni di threading e altri problemi di prestazioni, ad esempio l'uso di un livello quando una clip è sufficiente.

Per decidere la quantità di informazioni tracciate dal livello di debug, il livello di debug offre tre livelli di debug: informazioni, avviso ed errore. Questi tre livelli vengono interpretati come segue:

-   **Errore:** Direct2D invia messaggi di errore gravi al livello di debug. Ad esempio, l'interruzione di un vincolo di threading genererà un errore grave.

    Inoltre, un messaggio di errore di livello attiva il punto di interruzione per facilitare il debug.

-   **Avviso:** Direct2D invia messaggi di errore e avvisi al livello di debug in modo che sia possibile risolvere uno di questi messaggi.

-   **Informazioni:** Direct2D invia messaggi di errore, avvisi e informazioni di diagnostica aggiuntive al livello di debug. Ad esempio, i messaggi di miglioramento delle prestazioni verranno inviati a questo livello di debug.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Installazione del livello di debug Direct2D](installing-the-direct2d-debug-layer.md)<br/> | Descrive come installare il livello di debug Direct2D.<br/>      |
| [Panoramica del livello di debug Direct2D](direct2ddebuglayer-overview.md)<br/>               |                                                                    |
| [Messaggi di debug](direct2ddebuglayer-debugmessages.md)<br/>                         | Elenca i messaggi di debug dal livello di debug Direct2D.<br/> |



 

 

 





