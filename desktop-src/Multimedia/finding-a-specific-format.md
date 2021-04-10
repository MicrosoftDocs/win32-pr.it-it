---
title: Ricerca di un formato specifico
description: Ricerca di un formato specifico
ms.assetid: 0c892758-d409-4ed7-8f38-a24eee646b65
keywords:
- Gestione compressione audio (ACM), ricerca di formati
- ACM (Gestione compressione audio), ricerca di formati
- Esempi di ACM, ricerca di formati
- ricerca di formati
- acmFormatEnum (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c148c075df09cb702caf6b1d192fe8ce41b48ad0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955737"
---
# <a name="finding-a-specific-format"></a>Ricerca di un formato specifico

Un'applicazione potrebbe avere solo una specifica parziale per un formato quando è necessaria la specifica completa. Ad esempio, la specifica può prevedere un formato ADPCM mono a 4 bit a 11 kHz, ma non il numero medio di byte al secondo. L'applicazione può ottenere il formato completo senza l'intervento dell'utente tramite la funzione [**acmFormatEnum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum) e specificando flag nel parametro *fdwEnum* .

 

 




