---
description: Per eseguire operazioni bitmap, un numero di funzioni usa il pennello attualmente selezionato in un contesto di dispositivo.
ms.assetid: 98fb2fd5-9cf4-4016-9e30-ec724e77cebc
title: Bitmap come pennelli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c693e3c144dec2d26eccca1f1b628252dea187c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226709"
---
# <a name="bitmaps-as-brushes"></a>Bitmap come pennelli

Per eseguire operazioni bitmap, un numero di funzioni usa il pennello attualmente selezionato in un contesto di dispositivo. Ad esempio, la funzione [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) replica il pennello in un'area rettangolare all'interno di una finestra e la funzione [**FLOODFILL**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) replica il pennello all'interno di un'area in una finestra delimitata dal colore specificato (a differenza di **PatBlt**, **FLOODFILL** riempie forme non rettangolari).

La funzione [**FLOODFILL**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) replica il pennello all'interno di un'area delimitata da un colore specificato. Tuttavia, a differenza della funzione [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) , **FLOODFILL** non combina i dati relativi al colore per il pennello con i dati relativi al colore per i pixel sullo schermo; imposta semplicemente il colore di tutti i pixel all'interno dell'area racchiusa sullo schermo sul colore del pennello attualmente selezionato nel contesto di dispositivo.

 

 



