---
title: Recupero di informazioni su affollamenti e decompressori
description: Recupero di informazioni su affollamenti e decompressori
ms.assetid: bb9773dc-a706-40e6-8703-1cd47101992c
keywords:
- gestione compressione video(VCM), recupero di informazioni sui dispositivi
- VCM (Video Compression Manager), recupero di informazioni sui dispositivi
- Funzione ICGetInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404b6acacd97b514edcf0328a8127f97152554015694eba3f8e5bf3b76214de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678612"
---
# <a name="getting-information-about-compressors-and-decompressors"></a>Recupero di informazioni su affollamenti e decompressori

Per ottenere informazioni generali su un oggetto o un decompressore, l'applicazione può usare la [**funzione ICGetInfo.**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) Questa funzione riempie una [**struttura ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) con informazioni sull'oggetto o sul decompressore. L'applicazione deve allocare la memoria per **la struttura ICINFO** e passare un puntatore a essa in **ICGetInfo.** A meno che l'applicazione non eserviti la ricerca di un particolare comune o decompressore, i flag nella struttura **ICINFO** forniscono le informazioni più utili sulle funzionalità di un oggetto o di un decompressore.

Per ottenere la frequenza dei fotogrammi chiave predefinita e il valore di qualità predefinito di un dispositivo di compressione o decompressore, l'applicazione può inviare i messaggi [**ICM \_ GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) e [**ICM \_ GETDEFAULTQUALITY**](icm-getdefaultquality.md) oppure usare le macro [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) e [**ICGetDefaultQuality.**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality)

Per determinare il formato di visualizzazione migliore di un formattatore o un decompressore, l'applicazione può usare la [**funzione ICGetDisplayFormat.**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)

Per determinare se un piccolo o decompressore può visualizzare una finestra di dialogo Informazioni su, inviare il messaggio [**ICM \_ ABOUT**](icm-about.md) (o usare la macro [**ICQueryAbout).**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) È anche possibile visualizzare la finestra di dialogo Informazioni su di un dispositivo di decompressione inviando il messaggio ICM ABOUT e modificando il valore del parametro \_ *wParam* (o usando la macro [**ICAbout).**](/windows/desktop/api/Vfw/nf-vfw-icabout)

 

 




