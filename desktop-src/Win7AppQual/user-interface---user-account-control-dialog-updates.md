---
description: .
ms.assetid: f2d4b82d-a84a-4fc1-b7ad-cdc92a24f889
title: Interfaccia utente-aggiornamenti della finestra di dialogo controllo dell'account utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5711f8bbed029102bea81e0f4cfcbd4649b5a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319826"
---
# <a name="user-interface---user-account-control-dialog-updates"></a>Interfaccia utente-aggiornamenti della finestra di dialogo controllo dell'account utente

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Effetto sulle funzionalità

**Gravità** -bassa  
**Frequenza** -media  











## <a name="description"></a>Descrizione

In Windows 7 sono state standardizzate le opzioni della finestra di dialogo controllo dell'account utente. In precedenza, gli utenti dovevano scegliere tra più opzioni, ad esempio "continua", "Annulla" e così via. Ora tutte le finestre di dialogo forniscono agli utenti un semplice "Sì" o "No". Il layout della finestra di dialogo ora Mostra anche il nome del programma, l'autore e l'origine.

## <a name="leveraging-feature-capabilities"></a>Sfruttando le funzionalità

I requisiti di sviluppo delle applicazioni in Windows 7 per la compatibilità con il controllo dell'account utente sono identici a quelli di Windows Vista. Le applicazioni compatibili con Windows Vista interagiranno con UAC in Windows 7 senza alcuna modifica. Per informazioni su come fare in modo che le applicazioni Windows XP funzionino correttamente in Windows 7, vedere gli argomenti relativi al controllo dell'account utente in *Windows Vista Application Compatibility Cookbook* . Sebbene i miglioramenti apportati all'UAC per Windows 7 avranno un effetto sull'esperienza dell'utente, non avranno alcun effetto sull'interfaccia dell'applicazione. Tuttavia, se è presente un contenuto della guida collegato alle finestre di dialogo del controllo dell'account utente, potrebbe essere necessario aggiornare le schermate.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Cookbook per la compatibilità delle applicazioni di Windows Vista](/previous-versions/bb757005(v=msdn.10))
-   [Download di Application Compatibility Toolkit](/windows-hardware/get-started/adk-install)
-   [Analizzatore utente standard](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))

> [!Note]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi/aree geografiche.

 

 

 
