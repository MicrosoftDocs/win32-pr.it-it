---
title: Gestione dei blocchi di dati tramite polling
description: Gestione dei blocchi di dati tramite polling
ms.assetid: 0a517f1d-4993-49b8-be86-bc63e5687cba
keywords:
- audio waveform, polling di blocchi di dati
- blocchi di dati audio, polling
- polling di blocchi di dati audio
- Struttura WAVEHDR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c84e75eccaf34ef16ccadefb4dae42931854a0c6c4278003fb5c01b0c551f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139167"
---
# <a name="managing-data-blocks-by-polling"></a>Gestione dei blocchi di dati tramite polling

Oltre a usare una funzione di callback, è possibile eseguire il polling del membro **dwFlags** di una struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) per determinare quando un dispositivo audio termina con un blocco di dati. A volte è meglio eseguire il **polling di dwFlags** anziché attendere che un altro meccanismo riceva messaggi dai driver. Ad esempio, dopo aver chiamato la funzione [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) per rilasciare i blocchi di dati in sospeso, è possibile eseguire immediatamente il polling per assicurarsi che i blocchi di dati siano stati rilasciati prima di chiamare [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) e liberare la memoria per il blocco di dati.

È possibile usare il flag WHDR \_ DONE per testare **il membro dwFlags.** Non appena il flag WHDR DONE viene impostato nel membro \_ **dwFlags** della struttura **WAVEHDR,** il driver termina con il blocco di dati.

 

 