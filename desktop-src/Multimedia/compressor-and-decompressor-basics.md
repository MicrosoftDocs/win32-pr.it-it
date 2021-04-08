---
title: Nozioni di base compressore e decompressore
description: Nozioni di base compressore e decompressore
ms.assetid: 49a958c1-1798-4c6c-913c-5bf5869f926b
keywords:
- Gestione compressione video (VCM), apertura di compressatori
- VCM (Gestione compressione video), apertura di comprimeri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b51e0221c495d5e2d0782f4e56e0778c0d2462
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856053"
---
# <a name="compressor-and-decompressor-basics"></a>Nozioni di base compressore e decompressore

Per aprire e individuare un compressore, è possibile usare le funzioni [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) e [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) . È possibile usare **ICLocate** per trovare un compressore di un tipo specifico e per ottenerne un handle da usare in altre funzioni di VCM. Per aprire un compressore, è possibile usare **ICOpen**. L'applicazione usa l'handle restituito da questa funzione per identificare il compressore aperto quando usa altre funzioni VCM.

Per aprire e individuare un decompressore, le applicazioni possono usare le macro [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) e [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) . Queste macro usano **ICLocate** per Operation.

Quando l'applicazione ha terminato di usare un comprimetore o un decompressore, è necessario chiuderlo per liberare le risorse usate per la compressione o la decompressione. L'applicazione può usare la funzione [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) per chiudere il compressore o il decompressore.

Inoltre, l'applicazione può enumerare i compressori o i decompressori in un sistema tramite la funzione [**ICInfo**](/windows/desktop/api/Vfw/nf-vfw-icinfo) .

> [!Note]  
> L'intestazione del flusso in un file AVI contiene informazioni sul tipo di flusso e sul gestore specifico per tale flusso. All'interno dell'intestazione del flusso, i membri **fccType** e **fccHandler** identificano il tipo di flusso e il gestore di flusso specificato per il flusso.

 

 

 




