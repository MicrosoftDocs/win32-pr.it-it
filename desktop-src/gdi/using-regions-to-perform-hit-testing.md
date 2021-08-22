---
description: L'esempio in Pennelli usa aree per simulare un oggetto &\# 0034;zoom&0034; visualizzazione di una bitmap monocromatica da \# 8x8 pixel.
ms.assetid: a8e0cbfe-f05b-46ae-b420-ae34a5efbff3
title: Uso di aree per eseguire l'hit testing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d553eeaf37b954d0ec9d0b8897df98cf1a513d7ca7212ca82bc376afe1fc7163
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558121"
---
# <a name="using-regions-to-perform-hit-testing"></a>Uso di aree per eseguire l'hit testing

L'esempio in [Pennelli](brushes.md) usa le aree per simulare una visualizzazione "ingrandita" di una bitmap monocromatica da 8x8 pixel. Facendo clic sui pixel in questa bitmap, l'utente crea un pennello personalizzato adatto per le operazioni di disegno. L'esempio illustra come usare la funzione [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) per eseguire l'hit testing e la [**funzione InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) per invertire i colori in un'area.

 

 



