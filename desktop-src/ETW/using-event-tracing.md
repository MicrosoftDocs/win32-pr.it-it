---
description: Negli argomenti seguenti viene descritto come utilizzare l'API ETW per la traccia eventi.
ms.assetid: 7362874a-8206-4973-bb79-a9eaff55feb4
title: Utilizzo di traccia eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5141c19838796c0ec29f9eb20add689d56b97757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226359"
---
# <a name="using-event-tracing"></a>Utilizzo di traccia eventi

Negli argomenti seguenti viene descritto come utilizzare l'API ETW per la traccia eventi.



| Argomento                                                                          | Descrizione                                                                                                             |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Controllo delle sessioni di traccia eventi](controlling-event-tracing-sessions.md)   | Viene descritto come gestire le sessioni di traccia eventi.                                                                         |
| [Invio di eventi](providing-events.md)                                       | Viene descritto come registrare e instrumentare un provider di traccia eventi.                                                       |
| [Utilizzo di eventi](consuming-events.md)                                       | Viene descritto come implementare funzioni di callback utilizzate per utilizzare ed elaborare eventi da un file di log di traccia o in tempo reale. |
| [Preprocessore traccia software Windows](windows-software-trace-preprocessor.md) | Fornisce un meccanismo efficiente per registrare e utilizzare gli eventi che si verificano durante l'esecuzione di un'applicazione o di un driver.  |



 

Includere il file di intestazione Wmistr. h prima di includere il file di intestazione Evntrace. h.

 

 



