---
description: Un'applicazione può convertire un percorso in un'area chiamando la funzione PathToRegion.
ms.assetid: c4261516-7872-4118-99e2-138f0ac3c38a
title: Conversione dei percorsi in aree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3a576f04035f6e29bb37a23de956322639daf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754474"
---
# <a name="conversion-of-paths-to-regions"></a>Conversione dei percorsi in aree

Un'applicazione può convertire un percorso in un'area chiamando la funzione [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) . Analogamente a [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath), **PathToRegion** è utile per la creazione di speciali effetti grafici. Non sono ad esempio disponibili funzioni che consentono a un'applicazione di eseguire l'offset di un percorso. Tuttavia, esiste una funzione che consente a un'applicazione di eseguire l'offset di un'area ([**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)). Usando **PathToRegion** , un'applicazione può creare l'effetto dell'animazione di una forma complessa creando un percorso che definisce la forma, convertendo il percorso in un'area (chiamando **PathToRegion**), quindi disegnando ripetutamente, spostando e cancellando l'area (chiamando le funzioni in una sequenza, ad esempio [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn), **OffsetRgn** e **FillRgn**).

 

 



