---
description: Nuovi Low-Level binari
ms.assetid: 8c883462-29d8-46c4-b1c6-3ae8b8d3b397
title: Nuovi Low-Level binari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c84601fd1394c9e31123415953e87ef1beb69e173d2744368daf58e9f79355f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994891"
---
# <a name="new-low-level-binaries"></a>Nuovi Low-Level binari

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** - Windows 7  
**Server** - Windows Server 2008 R2  









## <a name="feature-impact"></a>Impatto sulle funzionalità

**Gravità** - Media  
**Frequenza** - Alta  











## <a name="description"></a>Descrizione

Per migliorare l'efficienza di progettazione interna e migliorare le basi per il lavoro futuro, alcune funzionalità sono state rilocate in nuovi file binari di basso livello. Questo refactoring consente a installazioni future di Windows di fornire subset di funzionalità per ridurre la superficie di attacco (requisiti di disco e memoria, manutenzione e superficie di attacco).

## <a name="manifestation-of-impact"></a>Impatto significativo

Come esempio di funzionalità che sono stati spostati in file binari di basso livello, kernelbase.dll funzionalità da kernel32.dll e advapi32.dll. Ciò significa che il file binario esistente ora inoltra le chiamate al nuovo file binario anziché gestirle direttamente. L'inoltro può essere statico (la tabella di esportazione mostra il reindirizzamento) o runtime (la DLL ha una routine stub che chiama il nuovo file binario). Ciò inciderà sulle applicazioni di basso livello, ad esempio le applicazioni di sicurezza e di backup che dipendono da API interne e offset.

## <a name="solution"></a>Soluzione

L'unico impatto è sul codice che fa supposizioni quando si tenta di esaminare il kernel32.dll o la tabella di esportazione advapi32.dll in memoria, ad esempio un'applicazione antivirus. Usare le API pubblicate e non i dettagli dell'implementazione. Questo è solo un esempio di implementazione di in base a un dettaglio di implementazione per un'API.

 

 



