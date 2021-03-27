---
description: L'esempio nei pennelli usa le aree per simulare un &\# 0034; zoom&\# 0034; vista di una bitmap a 8 pixel monocromatico.
ms.assetid: a8e0cbfe-f05b-46ae-b420-ae34a5efbff3
title: Uso delle aree per eseguire l'hit testing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb50ca1f837213b85619af381b86c2bd76efcbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227141"
---
# <a name="using-regions-to-perform-hit-testing"></a>Uso delle aree per eseguire l'hit testing

L'esempio nei [pennelli](brushes.md) usa le aree per simulare una visualizzazione "con zoom" di una bitmap 8 per 8 pixel monocromatico. Facendo clic sui pixel in questa bitmap, l'utente crea un pennello personalizzato adatto per le operazioni di disegno. Nell'esempio viene illustrato come utilizzare la funzione [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) per eseguire hit testing e la funzione [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) per invertire i colori in un'area.

 

 



