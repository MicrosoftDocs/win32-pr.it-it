---
title: Ottenere informazioni sui compressori e i decompressori
description: Ottenere informazioni sui compressori e i decompressori
ms.assetid: bb9773dc-a706-40e6-8703-1cd47101992c
keywords:
- Gestione compressione video (VCM), recupero di informazioni sui commediatori
- VCM (Video Compression Manager), recupero di informazioni sui commediatori
- ICGetInfo (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c619d13559d99b570af200298f29fcd8238c7d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955515"
---
# <a name="getting-information-about-compressors-and-decompressors"></a>Ottenere informazioni sui compressori e i decompressori

Per ottenere informazioni generali su un compressore o un decompressore, l'applicazione può usare la funzione [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) . Questa funzione riempie una struttura [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) con le informazioni sul compressore o il decompressore. L'applicazione deve allocare la memoria per la struttura **ICINFO** e passarvi un puntatore in **ICGetInfo**. A meno che l'applicazione non cerchi un compressore o un decompressore particolare, i flag nella struttura **ICINFO** forniscono le informazioni più utili sulle funzionalità di un compressore o di un decompressore.

Per ottenere la frequenza dei fotogrammi chiave predefinita e il valore di qualità predefinito di un compressore o di un decompressore, l'applicazione può inviare i messaggi [**MCI \_ GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) e [**ICM \_ GETDEFAULTQUALITY**](icm-getdefaultquality.md) (o usare le macro [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) e [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) ).

Per determinare il formato di visualizzazione migliore di un compressore o di un decompressore, l'applicazione può usare la funzione [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) .

Per determinare se un compressore o un decompressore può visualizzare una finestra di dialogo informazioni su, inviare il messaggio [**ICM \_ About**](icm-about.md) (usare la macro [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) ). È anche possibile visualizzare la finestra di dialogo informazioni su di un commutatore o un decompressore inviando il \_ messaggio ICM about e modificando il valore del parametro *wParam* (o usando la macro [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) ).

 

 




