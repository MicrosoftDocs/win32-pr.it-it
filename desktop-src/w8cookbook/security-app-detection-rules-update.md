---
title: Aggiornamento delle regole di rilevamento delle app di sicurezza
description: Aggiornamento delle regole di rilevamento delle app di sicurezza
ms.assetid: A272C09B-A777-4119-BAB9-F91ABC03717A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242c6f9da8d474c16fab7573e216d3157f93b014
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104047493"
---
# <a name="security-app-detection-rules-update"></a>Aggiornamento delle regole di rilevamento delle app di sicurezza

## <a name="platforms"></a>Piattaforme

**Client** -Windows 8  
**Server** : Windows Server 2012  


### <a name="description"></a>Descrizione

Le app di Windows Store aggiunte in Windows 8 vengono installate in un percorso comune in "programmi" (% ProgramFiles%) denominato \\ file di programma \\ WindowsApps.

### <a name="manifestation"></a>Manifestazione

Questo può causare conflitti con le configurazioni esistenti e alcuni rilevatori antivirus/antimalware vedono questo percorso come una posizione potenziale che rappresenta una fonte di preoccupazione.

### <a name="mitigation"></a>Strategia di riduzione del rischio

Le raccomandazioni correnti sono:

-   Allontanarsi dai \\ file di programma \\ WindowsApps per archiviare le app personalizzate
-   I fornitori di antivirus/antimalware devono aggiornare le proprie euristiche in modo da non identificare la località come una località di malware

 

 




