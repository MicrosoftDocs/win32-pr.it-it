---
title: Generazione di un formato non standard
description: Generazione di un formato non standard
ms.assetid: e9f80aec-d5dc-4c44-aea0-95220542e48d
keywords:
- Gestione compressione audio(ACM), formati non standard
- ACM (gestione compressione audio), formati non standard
- Esempi di ACM, formati non standard
- Funzione acmFormatSuggest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968dafae93cac419a0078989ab8786e02732cbaa942fd185969c5571c2e8237e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496341"
---
# <a name="generating-a-nonstandard-format"></a>Generazione di un formato non standard

A volte un'applicazione richiede un formato non standard. Ad esempio, un'applicazione potrebbe richiedere un file in formato ADPCM a 16 kHz. Poiché 16 kHz non è standard, le funzioni di enumerazione non genereranno questo formato. In realtà, a causa della codifica personalizzata degli algoritmi di formato nell'applicazione, non esiste un modo affidabile per generare un formato non standard. A volte, tuttavia, è possibile generare un formato analogo configurando un formato PCM valido con tutte le informazioni necessarie e quindi usando la [**funzione acmFormatSuggest.**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) Poiché i compressori e i decompressori tentano di suggerire un formato più vicino al formato desiderato, il numero di canali e la frequenza vengono in genere mantenuti.

 

 




