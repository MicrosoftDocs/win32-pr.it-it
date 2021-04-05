---
title: Gestione dei blocchi di dati tramite polling
description: Gestione dei blocchi di dati tramite polling
ms.assetid: 0a517f1d-4993-49b8-be86-bc63e5687cba
keywords:
- audio Waveform, blocchi di dati di polling
- blocchi di dati audio, polling
- polling di blocchi di dati audio
- Struttura WAVEHDR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e5580ff64425eae1bc6650268b065e60b90f43
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046605"
---
# <a name="managing-data-blocks-by-polling"></a>Gestione dei blocchi di dati tramite polling

Oltre a usare una funzione di callback, è possibile eseguire il polling del membro **dwFlags** di una struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) per determinare quando un dispositivo audio è terminato con un blocco di dati. A volte è preferibile eseguire il polling di **dwFlags** anziché attendere che un altro meccanismo riceva messaggi dai driver. Ad esempio, dopo aver chiamato la funzione [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) per rilasciare i blocchi di dati in sospeso, è possibile eseguire immediatamente il polling per assicurarsi che i blocchi di dati siano stati rilasciati prima di chiamare [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) e liberare la memoria per il blocco di dati.

È possibile utilizzare il \_ flag WHDR done per testare il membro **dwFlags** . Non appena il flag WHDR \_ Done viene impostato nel membro **dwFlags** della struttura **WAVEHDR** , il driver termina con il blocco di dati.

 

 