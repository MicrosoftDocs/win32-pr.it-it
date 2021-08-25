---
description: Diverse funzioni usano il pennello attualmente selezionato in un contesto di dispositivo per eseguire operazioni bitmap.
ms.assetid: 98fb2fd5-9cf4-4016-9e30-ec724e77cebc
title: Bitmap come pennelli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee8e218180ab646de1c9c8ff622be1bcc268df73f6f4bb0b6df82482c9a2c851
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944251"
---
# <a name="bitmaps-as-brushes"></a>Bitmap come pennelli

Diverse funzioni usano il pennello attualmente selezionato in un contesto di dispositivo per eseguire operazioni bitmap. Ad esempio, la funzione [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) replica il pennello in un'area rettangolare all'interno di una finestra e la [**funzione FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) replica il pennello all'interno di un'area in una finestra delimitata dal colore specificato (a differenza di **PatBlt**, **FloodFill** riempie forme non rettangolari).

La [**funzione FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) replica il pennello all'interno di un'area delimitata da un colore specificato. Tuttavia, a differenza [**della funzione PatBlt,**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) **FloodFill** non combina i dati di colore per il pennello con i dati di colore per i pixel sullo schermo; imposta semplicemente il colore di tutti i pixel all'interno dell'area racchiusa sullo schermo sul colore del pennello attualmente selezionato nel contesto di dispositivo.

 

 



