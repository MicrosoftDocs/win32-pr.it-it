---
description: Microsoft Image Color Management (ICM) assicura che un'immagine di colore, un oggetto grafico o un oggetto testo venga sottoposto al rendering il più vicino possibile alla finalità originale su qualsiasi dispositivo, nonostante le differenze nelle tecnologie di imaging e nelle funzionalità cromatiche tra i dispositivi.
ms.assetid: 7b3cb9a4-ffd2-4867-85bd-0e663fdde6e3
title: Funzioni bitmap ICM-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b89dac569aafad1ef94b066bc97f588bac62c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880282"
---
# <a name="icm-enabled-bitmap-functions"></a>Funzioni bitmap ICM-Enabled

Microsoft Image Color Management (ICM) assicura che un'immagine di colore, un oggetto grafico o un oggetto testo venga sottoposto al rendering il più vicino possibile alla finalità originale su qualsiasi dispositivo, nonostante le differenze nelle tecnologie di imaging e nelle funzionalità cromatiche tra i dispositivi. Se si sta eseguendo la scansione di un'immagine o di un altro elemento grafico su uno scanner di colori, lo si scarica su Internet, lo si visualizza o lo si modifica sullo schermo oppure lo si stampa su carta, film o altri supporti, ICM 2,0 consente di garantire la coerenza e l'accuratezza dei colori. Per ulteriori informazioni su ICM, vedere [Windows Color System](/previous-versions//dd372446(v=vs.85)).

Sono disponibili varie funzioni nell'interfaccia GDI (Graphics Device Interface) che usano o operano sui dati di colore. Le funzioni bitmap seguenti sono abilitate per l'uso con ICM:

-   [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)
-   [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)
-   [**CreateDIBSection**](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)
-   [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)
-   [**SetDIBColorTable**](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)
-   [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)
-   [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)
-   [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)
-   [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

 

 
