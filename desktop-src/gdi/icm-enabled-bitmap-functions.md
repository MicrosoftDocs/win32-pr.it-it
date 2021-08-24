---
description: Gestione colori immagini Microsoft (ICM) garantisce che il rendering di un'immagine a colori, di un oggetto grafico o di un oggetto di testo sia il più possibile simile alla finalità originale in qualsiasi dispositivo, nonostante le differenze nelle tecnologie di creazione di immagini e nelle funzionalità di colore tra i dispositivi.
ms.assetid: 7b3cb9a4-ffd2-4867-85bd-0e663fdde6e3
title: ICM-Enabled funzioni bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38341851eb9ba2aed25cc93afbf7b869909430a30ecb626bf3a452883fdea97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831971"
---
# <a name="icm-enabled-bitmap-functions"></a>ICM-Enabled funzioni bitmap

Gestione colori immagini Microsoft (ICM) garantisce che il rendering di un'immagine a colori, di un oggetto grafico o di un oggetto di testo sia il più possibile simile alla finalità originale in qualsiasi dispositivo, nonostante le differenze nelle tecnologie di creazione di immagini e nelle funzionalità di colore tra i dispositivi. Se si esegue la scansione di un'immagine o di un altro elemento grafico in uno scanner a colori, lo si scarica tramite Internet, la visualizzazione o la modifica su schermo o la stampa su carta, film o altri supporti, ICM 2.0 consente di mantenere i colori coerenti e accurati. Per altre informazioni sui ICM, vedere Windows [Color System](/previous-versions//dd372446(v=vs.85)).

Nell'interfaccia GDI (Graphics Device Interface) sono disponibili varie funzioni che usano o operano sui dati dei colori. Le funzioni bitmap seguenti sono abilitate per l'uso con ICM:

-   [**Bitblt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)
-   [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)
-   [**CreateDIBSection**](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)
-   [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)
-   [**SetDIBColorTable**](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)
-   [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)
-   [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)
-   [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)
-   [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

 

 
