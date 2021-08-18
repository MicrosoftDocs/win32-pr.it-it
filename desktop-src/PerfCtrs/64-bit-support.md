---
description: Se si forniscono contatori in un computer a 64 bit, è necessario installare sia la versione a 32 bit che la versione a 64 bit del provider nel computer se si desidera supportare consumer sia a 32 bit che a 64 bit.
ms.assetid: 2dba2c46-0185-4ce6-a7cc-27cdd9b19b70
title: Supporto a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9756a6eaf95097c881368bc3f150422f494dac04e503da5060f27355827a653c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011429"
---
# <a name="64-bit-support"></a>Supporto a 64 bit

Una DLL del provider di dati delle prestazioni a 64 bit non può essere eseguita in un processo consumer a 32 bit e una DLL del provider di dati delle prestazioni a 32 bit non può essere eseguita in un processo a 64 bit. La registrazione del provider supporta solo un singolo valore per il percorso della DLL del provider di dati sulle prestazioni, pertanto non è possibile specificare percorsi diversi da usare dai consumer a 32 bit e dai consumer `Library` a 64 bit.

Per supportare i provider V1 nei sistemi operativi a 64 bit sono disponibili le opzioni seguenti:

- **Consigliato:** Installare e registrare il percorso della versione a 32 bit della DLL del provider.
  - I consumer a 32 bit funzioneranno in modo nativo: caricano la DLL del provider a 32 bit nel processo consumer a 32 bit.
  - I consumer a 64 bit funzioneranno in modo indiretto: non saranno in grado di caricare la DLL del provider a 32 bit nel processo consumer a 64 bit, ma Windows si tornerà automaticamente alla creazione di un processo perfhost a 32 bit, al caricamento della DLL del provider a 32 bit nel processo perfhost e all'invio di dati sulle prestazioni dal processo perfhost a 32 bit al processo consumer a 64 bit.
- **Solo a 64 bit:** Installare e registrare il percorso della versione a 64 bit della DLL del provider.
  - I consumer a 32 bit avranno esito negativo: non saranno in grado di caricare la DLL del provider a 64 bit nel processo a 32 bit.
  - I consumer a 64 bit funzioneranno in modo nativo: caricano la DLL del provider a 32 bit in-process.

> [!NOTE]
> Diversi provider di dati delle prestazioni Windows predefiniti installano una DLL a 32 bit in , installano una DLL a 64 bit in e registrano il percorso come , consentendo al reindirizzamento del file system di risolvere il percorso della `%systemroot%\syswow64` `%systemroot%\system32` DLL `Library` `%systemroot%\system32\ProviderName.dll` appropriata. Questa opzione è supportata solo per i provider di dati delle prestazioni che fanno parte del Windows operativo. I provider che non fanno parte del Windows sistema operativo non devono installare file nella `Windows` cartella . I file non riconosciuti nella cartella possono `Windows` essere rimossi durante la manutenzione o l'aggiornamento.
