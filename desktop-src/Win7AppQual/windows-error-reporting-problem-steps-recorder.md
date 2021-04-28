---
description: Segnalazione errori Windows Registrazione azioni utente
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Segnalazione errori Windows Registrazione azioni utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46abb8adf545152e34c2b2100022068291e3571f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084159"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a>Segnalazione errori Windows Registrazione azioni utente

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** - Windows 7  
**Server** - Windows Server 2008 R2  


## <a name="description"></a>Descrizione

Prima di Windows 7, Segnalazione errori Windows (WER) raccoglieva segnalazioni di errori che indicava problemi che doveva essere ripristinati. Queste segnalazioni di errore contengono informazioni utili che descrivono la natura generale di un problema, ma non informazioni sufficienti per determinarne la causa radice. A tale scopo, gli sviluppatori necessitano di uno strumento per riprodurre lo scenario di arresto anomalo/blocco per il debug.

Una nuova applicazione, Registrazione azioni utente (PSR.exe), è disponibile in tutte le build di Windows 7. Questa funzionalità consente la raccolta delle azioni eseguite da un utente durante l'arresto anomalo del sistema, in modo che tester e sviluppatori possano riprodurre la situazione per l'analisi e il debug.

## <a name="usage"></a>Utilizzo

Attualmente, uno sviluppatore Segnalazione errori Windows servizio deve richiedere l'abilitazione di PSR per un'applicazione. Le organizzazioni di supporto Tecnico Microsoft usano anche questo strumento durante la risoluzione dei problemi con gli utenti finali. Sono disponibili piani per rendere disponibile PSR in Windows Quality Online Services (Winqual) dopo il rilascio di Windows 7.

**Nota:** Con PSR abilitato per un'applicazione, è possibile che si sia verificata una riduzione delle prestazioni dell'applicazione.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Segnalazione errori Windows di blog](/archive/blogs/wer/)
-   [Windows Quality Online Services (Winqual)](https://winqual.microsoft.com)

 

 
