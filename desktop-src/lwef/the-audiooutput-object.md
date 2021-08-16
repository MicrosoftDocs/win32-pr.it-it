---
title: Oggetto AudioOutput
description: Oggetto AudioOutput
ms.assetid: 7c1c6079-f445-4980-9559-8d26b6014e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07bfef883e5cb40d0a72ec4d848ad0d77f63f58aaeefd907f632e16798be4397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474951"
---
# <a name="the-audiooutput-object"></a>Oggetto AudioOutput

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Questo oggetto fornisce l'accesso alle proprietà di output audio gestite dal server. Le proprietà sono di sola lettura, ma l'utente può modificarle nella finestra delle proprietà di Microsoft Agent.

Se si dichiara una variabile oggetto di tipo [**IAgentCtlAudioObjectEx,**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**)non sarà possibile accedere a tutte le proprietà per [**l'oggetto AudioOutput.**](/windows/desktop/lwef/the-audiooutput-object) Anche se Agent supporta [**anche IAgentCtlAudioObject,**](https://www.bing.com/search?q=**IAgentCtlAudioObject**)quest'ultima interfaccia viene fornita solo per la compatibilità con le versioni precedenti e supporta solo tali proprietà nelle versioni precedenti.

-   [**Abilitato**](enabled-property-ao.md)
-   [**SoundEffects**](soundeffects-property.md)
-   [**Stato**](status-property.md)

 

 