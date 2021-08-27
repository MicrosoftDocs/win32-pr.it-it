---
description: Un'applicazione può convertire un percorso in un'area chiamando la funzione PathToRegion.
ms.assetid: c4261516-7872-4118-99e2-138f0ac3c38a
title: Conversione di percorsi in aree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d404aa50669fe2349b3e39f172dd652ef765c9de8c615cde446e8540e6051bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062461"
---
# <a name="conversion-of-paths-to-regions"></a>Conversione di percorsi in aree

Un'applicazione può convertire un percorso in un'area chiamando la [**funzione PathToRegion.**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) Come [**SelectClipPath,**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) **PathToRegion** è utile nella creazione di effetti grafici speciali. Ad esempio, non esistono funzioni che consentono a un'applicazione di eseguire l'offset di un percorso. Tuttavia, esiste una funzione che consente a un'applicazione di eseguire l'offset di un'area ([**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)). Usando **PathToRegion,** un'applicazione può creare l'effetto di animare una forma complessa creando un tracciato che definisce la forma, convertendo il percorso in un'area (chiamando **PathToRegion**) e quindi disegnando, spostando e cancellando ripetutamente l'area (chiamando funzioni in una sequenza, ad esempio [**FillRgn,**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) **OffsetRgn** e **FillRgn).**

 

 



