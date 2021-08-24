---
title: Nozioni di base su Discompressore e Discompressore
description: Nozioni di base su Discompressore e Discompressore
ms.assetid: 49a958c1-1798-4c6c-913c-5bf5869f926b
keywords:
- gestione compressione video(VCM), apertura di file
- VCM (video compression manager),openings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1969748949aeb023f889bc651ccd028f19c3e18fe6cf1ba088b4f4ec29292f35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144994"
---
# <a name="compressor-and-decompressor-basics"></a>Nozioni di base su Discompressore e Discompressore

Per aprire e individuare un oggetto , è possibile usare le [**funzioni ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) [**e ICOpen.**](/windows/desktop/api/Vfw/nf-vfw-icopen) È possibile usare **ICLocate** per trovare un gruppo di un tipo specifico e per ottenere un handle per l'uso in altre funzioni di Gestione configurazione virtuale. Per aprire un oggetto , è possibile usare **ICOpen**. L'applicazione usa l'handle restituito da questa funzione per identificare l'oggetto aperto quando usa altre funzioni di Gestione configurazione virtuale.

Per aprire e individuare un decompressore, le applicazioni possono usare le macro [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) e [**ICDrawOpen.**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) Queste macro usano **ICLocate per** l'operazione.

Quando l'applicazione ha terminato di usare un dispositivo di compressione o decompressore, deve chiuderla per liberare tutte le risorse usate per la compressione o la decompressione. L'applicazione può usare [**la funzione ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) per chiudere l'oggetto o decompressore.

Inoltre, l'applicazione può enumerare gli elementi o i decompressori in un sistema usando la [**funzione ICInfo.**](/windows/desktop/api/Vfw/nf-vfw-icinfo)

> [!Note]  
> L'intestazione del flusso in un file AVI contiene informazioni sul tipo di flusso e sul gestore specifico per tale flusso. All'interno dell'intestazione del flusso, i membri **fccType** e **fccHandler** identificano il tipo di flusso e il gestore di flusso specificato per il flusso.

 

 

 




