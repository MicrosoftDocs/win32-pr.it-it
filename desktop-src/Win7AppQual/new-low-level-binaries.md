---
description: .
ms.assetid: 8c883462-29d8-46c4-b1c6-3ae8b8d3b397
title: Nuovi file binari di Low-Level
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b6e197f22df9fb3d6e12aeeff3c5f4a2a0e41c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232916"
---
# <a name="new-low-level-binaries"></a>Nuovi file binari di Low-Level

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Effetto sulle funzionalità

**Gravità** -medio  
**Frequenza** -alta  











## <a name="description"></a>Descrizione

Per migliorare l'efficienza di progettazione interna e migliorare le fondamenta per il lavoro futuro, abbiamo rilocato alcune funzionalità per i nuovi file binari di basso livello. Questo refactoring renderà possibile l'installazione futura di Windows per fornire subset di funzionalità per ridurre la superficie di attacco (requisiti di disco e memoria, manutenzione e superficie di attacco).

## <a name="manifestation-of-impact"></a>Manifesto di effetto

Come esempio di funzionalità che siamo passati a file binari di basso livello, kernelbase.dll ottiene la funzionalità da kernel32.dll e advapi32.dll. Ciò significa che il file binario esistente ora esegue le chiamate al nuovo file binario anziché gestirli direttamente; l'invio può essere statico (la tabella di esportazione Mostra il reindirizzamento) o il runtime (la dll ha una routine stub che chiama il nuovo binario). Questo influirà sulle applicazioni di basso livello, ad esempio le applicazioni di sicurezza e di backup che dipendono da API e offset interni.

## <a name="solution"></a>Soluzione

L'unico effetto è il codice che fa supposizioni quando si tenta di esaminare la kernel32.dll o la tabella di esportazione advapi32.dll in memoria, ad esempio un'applicazione antivirus. Usare le API pubblicate e non i dettagli relativi all'implementazione. Questo è solo un esempio di implementazione di in un dettaglio di implementazione per un'API.

 

 



