---
title: Gestione delle eccezioni in WOW64
description: WOW64 usa eccezioni x64, ia64 o ARM64 native come trasporto per le eccezioni x86. Pertanto, in un'applicazione a 32 bit in esecuzione in WOW64, le eccezioni non rilevate si comportano come eccezioni native a 64 bit.
ms.assetid: 2EE1A1F3-A691-4ee6-9587-7FF7C4F9DD98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7d461a809ac35a4742f9bdbbaeb461eb6d7365075d9c4b57334a94f434c1e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561527"
---
# <a name="exception-handling-under-wow64"></a>Gestione delle eccezioni in WOW64

WOW64 usa eccezioni x64, ia64 o ARM64 native come trasporto per le eccezioni x86. Pertanto, in un'applicazione a 32 bit in esecuzione in WOW64, le eccezioni non rilevate si comportano come eccezioni native a 64 bit.

In un'applicazione in esecuzione in una versione a 32 bit di Windows, le eccezioni non rilevate vengono passate ai gestori eccezioni di livello superiore dell'applicazione, se disponibili. Nella stessa applicazione a 32 bit in esecuzione in WOW64, il sistema può eliminare le eccezioni non rilevate.

**Windows Vista, Windows Server 2003 e Windows XP:** Nella stessa applicazione a 32 bit in esecuzione in WOW64, il sistema chiama i filtri delle eccezioni, ma può eliminare le eccezioni non rilevate senza richiamare i gestori associati. Questo comportamento è cambiato a partire da Windows Vista con Service Pack 1 (SP1).

Per altre informazioni sulle eccezioni non rilevate nelle routine della finestra, vedere la [funzione WindowProc.](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

 

 