---
description: .
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Registrazione passaggi Segnalazione errori Windows problema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25fb70acef867b878063bd6011fde6867f7f0e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759785"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a>Registrazione passaggi Segnalazione errori Windows problema

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** -Windows 7  
**Server** : Windows Server 2008 R2  


## <a name="description"></a>Descrizione

Prima di Windows 7, Segnalazione errori Windows (WER) raccoglieva segnalazioni di errori che indicavano problemi che necessitano di riparazione. Queste segnalazioni di errori contengono informazioni utili che descrivono la natura generale di un problema, ma non informazioni sufficienti per determinarne la causa principale. Per questo, gli sviluppatori hanno bisogno di uno strumento per riprodurre lo scenario di arresto anomalo/blocco per il debug.

Una nuova applicazione, registrazione passaggi problema (PSR.exe), viene fornita in tutte le build di Windows 7. Questa funzionalità consente la raccolta delle azioni eseguite da un utente in caso di arresto anomalo, in modo che i tester e gli sviluppatori possano riprodurre la situazione per l'analisi e il debug.

## <a name="usage"></a>Utilizzo

Attualmente, uno sviluppatore di servizi di Segnalazione errori Windows deve richiedere l'abilitazione di PSR per un'applicazione; Le organizzazioni del supporto tecnico Microsoft usano questo strumento anche durante la risoluzione dei problemi con gli utenti finali. Sono previsti piani per rendere PSR disponibile in Windows Quality Online Services (Winqual) dopo il rilascio di Windows 7.

**Nota:** Con la funzionalità PSR abilitata per un'applicazione, è possibile che si verifichi una riduzione delle prestazioni dell'applicazione.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Intervento di Segnalazione errori Windows Blog](/archive/blogs/wer/)
-   [Servizi online di qualità Windows (Winqual)](https://winqual.microsoft.com)

 

 
