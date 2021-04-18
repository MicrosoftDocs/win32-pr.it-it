---
description: Se si forniscono contatori in un computer a 64 bit, è necessario installare nel computer entrambe le versioni a 32 e 64 bit del provider, se si desidera supportare consumer sia a 32 bit che a 64 bit.
ms.assetid: 2dba2c46-0185-4ce6-a7cc-27cdd9b19b70
title: Supporto a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e465529f35d8a9becb2583e9d5c00ac19a74d3be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312198"
---
# <a name="64-bit-support"></a>Supporto a 64 bit

Una DLL del provider di dati prestazioni a 64 bit non può essere eseguita in un processo consumer a 32 bit e una DLL del provider di dati sulle prestazioni a 32 bit non può essere eseguita in un processo a 64 bit. La registrazione del provider supporta solo un `Library` valore singolo per il percorso della dll del provider di dati sulle prestazioni, pertanto non è possibile specificare percorsi diversi che devono essere utilizzati da consumer a 32 bit e consumer a 64 bit.

Per supportare i provider v1 nei sistemi operativi a 64 bit sono disponibili le opzioni seguenti:

- **Consigliato:** Installare e registrare il percorso della versione a 32 bit della DLL del provider.
  - i consumer a 32 bit funzioneranno in modo nativo: caricherà la DLL del provider a 32 bit nel processo consumer a 32 bit.
  - i consumer a 64 bit funzioneranno indirettamente: non saranno in grado di caricare la DLL del provider a 32 bit nel processo di consumer a 64 bit, ma Windows eseguirà automaticamente il fallback alla creazione di un processo perfhost a 32 bit, al caricamento della DLL del provider a 32 bit nel processo perfhost e all'invio di dati sulle prestazioni dal processo perfhost a 32 bit al processo consumer a bit
- **solo 64 bit:** Installare e registrare il percorso della versione a 64 bit della DLL del provider.
  - i consumer a 32 bit avranno esito negativo: non saranno in grado di caricare la DLL del provider a 64 bit nel processo a 32 bit.
  - i consumer a 64 bit funzioneranno in modo nativo: caricherà la DLL del provider a 32 bit in-process.

> [!NOTE]
> Molti provider di dati prestazioni Windows predefiniti installano una DLL a 32 bit in `%systemroot%\syswow64` , installano una dll a 64 bit in `%systemroot%\system32` e registrano il `Library` percorso come `%systemroot%\system32\ProviderName.dll` , consentendo al reindirizzamento del file System di risolvere il percorso della DLL appropriata. Questa operazione è supportata solo per i provider di dati sulle prestazioni che fanno parte del sistema operativo Windows. I provider che non fanno parte del sistema operativo Windows non devono installare i file nella `Windows` cartella. I file non riconosciuti nella `Windows` cartella possono essere rimossi durante la manutenzione o l'aggiornamento.
