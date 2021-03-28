---
description: Il colore viene definito come una combinazione di tre colori primari rossi, verdi e blu.
ms.assetid: 6e44935c-2b3b-4062-8273-f1f3e70300d2
title: Valori dei colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e46cd7ee87871c660702bed120958e7096745d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130810"
---
# <a name="color-values"></a>Valori dei colori

Il colore viene definito come una combinazione di tre colori primari rossi, verdi e blu. il sistema identifica un colore assegnando un valore di colore (talvolta denominato tripletta RGB), che è costituito da valori a 3 8 bit che specificano le intensità dei relativi componenti colore. Il nero ha l'intensità minima per rosso, verde e blu, quindi il valore del colore per il nero è (0, 0, 0). Il bianco ha l'intensità massima per rosso, verde e blu, quindi il valore del colore è (255, 255, 255).

> [!Note]  
> Se è abilitata la corrispondenza dei colori dell'immagine, la definizione di colore e il significato di un valore di colore dipendono dal tipo di spazio dei colori attualmente impostato per il contesto di dispositivo.

 

Il sistema e le applicazioni usano parametri e variabili con il tipo [COLORREF](colorref.md) per passare e archiviare i valori dei colori. Ad esempio, la funzione [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) identifica il colore di ogni penna impostando il membro **lopnColor** in una struttura [**LOGPEN**](/windows/win32/api/wingdi/ns-wingdi-logpen) su un valore di colore. Le applicazioni possono estrarre i singoli valori dei componenti rosso, verde e blu da un valore di colore utilizzando rispettivamente le macro [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)e [**GetBValue**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) . Le applicazioni possono creare un valore di colore dai singoli valori dei componenti usando la macro [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) . Quando si crea o si esamina una tavolozza logica, un'applicazione usa la struttura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) per definire i valori dei colori ed esaminare i valori dei singoli componenti.

 

 



