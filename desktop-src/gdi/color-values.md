---
description: Il colore è definito come una combinazione di tre colori principali, rosso, verde e blu.
ms.assetid: 6e44935c-2b3b-4062-8273-f1f3e70300d2
title: Valori di colore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b1518060e1ad4af7ada1c244ecdcac742f27a36133080f31199714dd8059d5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761931"
---
# <a name="color-values"></a>Valori di colore

Il colore è definito come una combinazione di tre colori principali, rosso, verde e blu. il sistema identifica un colore specificando un valore di colore (talvolta chiamato tripletta RGB), costituito da tre valori a 8 bit che specificano l'intensità dei componenti del colore. Il nero ha l'intensità minima per rosso, verde e blu, quindi il valore del colore per il nero è (0, 0, 0). Il bianco ha l'intensità massima per rosso, verde e blu, quindi il valore del colore è (255, 255, 255).

> [!Note]  
> Se la corrispondenza dei colori delle immagini è abilitata, la definizione del colore e il significato di un valore di colore dipendono dal tipo di spazio colore attualmente impostato per il contesto di dispositivo.

 

Il sistema e le applicazioni usano parametri e variabili con il [tipo COLORREF](colorref.md) per passare e archiviare i valori dei colori. Ad esempio, la [**funzione EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) identifica il colore di ogni penna impostando il membro **lopnColor** in una struttura [**LOGPEN**](/windows/win32/api/wingdi/ns-wingdi-logpen) su un valore di colore. Le applicazioni possono estrarre i singoli valori dei componenti rosso, verde e blu da un valore di colore usando rispettivamente le macro [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)e [**GetBValue.**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) Le applicazioni possono creare un valore di colore dai valori dei singoli componenti usando la macro [**RGB.**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) Quando si crea o si esamina una tavolozza logica, un'applicazione usa la [**struttura RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) per definire i valori dei colori ed esaminare i valori dei singoli componenti.

 

 



