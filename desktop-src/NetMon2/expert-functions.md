---
description: Le funzioni di supporto seguenti possono essere chiamate solo da esperti che esportano la funzione Run o Configure.
ms.assetid: 6890087c-7c94-41ff-bb5c-4bf88a4e07cc
title: Funzioni di esperti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7441289008c7dcd647775c2932e210ccd09b24bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878670"
---
# <a name="expert-functions"></a>Funzioni di esperti

Le funzioni di supporto seguenti possono essere chiamate solo da esperti che esportano la funzione [Run](run.md) o [Configure](configure.md) .



| Funzione                                         | Descrizione                                                                             |
|--------------------------------------------------|-----------------------------------------------------------------------------------------|
| [ExpertGetFrame](expertgetframe.md)             | Recupera un frame specificato dall'acquisizione.                                               |
| [ExpertIndicateStatus](expertindicatestatus.md) | Indica la percentuale di completamento dell'analisi dell'acquisizione dell'esperto.             |
| [ExpertGetStartupInfo](expertgetstartupinfo.md) | Recupera le informazioni di avvio per l'esperto.                                       |
| [ExpertMemorySize](expertmemorysize.md)         | Recupera le dimensioni della memoria allocata da una chiamata alla funzione **ExpertAllocMemory** . |
| [ExpertSubmitEvent](expertsubmitevent.md)       | Indica un problema e recupera le informazioni sul problema, se disponibile.          |
| [ExpertAllocMemory](expertallocmemory.md)       | Alloca memoria per l'esperto.                                                        |
| [ExpertReallocMemory](expertreallocmemory.md)   | Modifica le dimensioni della memoria allocata dalla funzione **ExpertAllocMemory** .         |
| [ExpertFreeMemory](expertfreememory.md)         | Libera la memoria allocata dall'esperto.                                                   |



 

Per informazioni sulle funzioni di esportazione, le funzioni di supporto che possono essere chiamate da esperti e analizzatori, strutture ed enumerazioni, vedere gli argomenti seguenti:



| Per informazioni su                                             | Vedere                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| Funzioni esportate da esperti                            | [Funzioni di esportazione DLL di esperti](expert-dll-export-functions.md)               |
| Strutture utilizzate dalle funzioni di esperti                      | [Strutture di esperti](expert-structures.md)                                   |
| Enumerazioni utilizzate da funzioni e strutture di esperti              | [Enumerazioni di esperti](expert-enumerations.md)                               |
| Funzioni di supporto comuni che possono essere chiamate da esperti e analizzatori | [Funzioni comuni di esperti e parser](expert-and-parser-common-functions.md) |



 

 

 



