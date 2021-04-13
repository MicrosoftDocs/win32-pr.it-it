---
title: Oggetto AudioOutput
description: Oggetto AudioOutput
ms.assetid: 7c1c6079-f445-4980-9559-8d26b6014e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919b435edf31b6ae24a8b5c6977d5aed542efac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104399021"
---
# <a name="the-audiooutput-object"></a>Oggetto AudioOutput

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Questo oggetto fornisce l'accesso alle proprietà di output audio gestite dal server. Le proprietà sono di sola lettura, ma l'utente può modificarle nella finestra delle proprietà di Microsoft Agent.

Se si dichiara una variabile oggetto di tipo [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**), non sarà possibile accedere a tutte le proprietà per l'oggetto [**AudioOutput**](/windows/desktop/lwef/the-audiooutput-object) . Mentre Agent supporta anche [**IAgentCtlAudioObject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**), quest'ultima interfaccia viene fornita solo per compatibilità con le versioni precedenti e supporta solo le proprietà nelle versioni precedenti.

-   [**Abilitato**](enabled-property-ao.md)
-   [**SoundEffects**](soundeffects-property.md)
-   [**Stato**](status-property.md)

 

 