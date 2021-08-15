---
title: Creazione di una finestra di dialogo per la selezione di formati con restrizioni
description: Creazione di una finestra di dialogo per la selezione di formati con restrizioni
ms.assetid: 486ba928-e06d-4ab0-a642-ba0fe16c8291
keywords:
- Gestione compressione audio,creazione di finestre di dialogo
- ACM (Gestione compressione audio), creazione di finestre di dialogo
- Esempi di ACM, creazione di finestre di dialogo
- creazione di finestre di dialogo
- Funzione acmFormatChoose
- Gestione compressione audio(ACM), selezione di formati con restrizioni
- ACM (Gestione compressione audio), selezione dei formati con restrizioni
- Esempi di ACM, selezione di formati con restrizioni
- selezione di formati con restrizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994fffa7ef13f6febe41eb766b4ecaef7eb735f11f58d36f37adfccbb152bffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802041"
---
# <a name="producing-a-dialog-box-for-selecting-restricted-formats"></a>Creazione di una finestra di dialogo per la selezione di formati con restrizioni

È possibile usare la finestra di dialogo creata dalla [**funzione acmFormatChoose,**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) ma limitare o controllare i formati nella finestra di dialogo. A tale scopo, usare il flag ACMFORMATCHOOSE \_ STYLEF \_ ENABLEHOOK per associare la procedura di dialogo. L'applicazione può quindi filtrare i formati rispondendo al messaggio [**MM \_ ACM \_ FORMATCHOOSE**](mm-acm-formatchoose.md) nella procedura del messaggio per la finestra di dialogo.

 

 




