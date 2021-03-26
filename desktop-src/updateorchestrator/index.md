---
title: Aggiornare l'API dell'agente di orchestrazione
description: UpdateOrchestrator pianifica gli aggiornamenti software automatici tenendo presenti gli effetti dell'utente.
ms.date: 01/14/2021
ms.topic: overview
ms.openlocfilehash: a172cccdc56d2c645bb4e7d048066ca34aea07ba
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/21/2021
ms.locfileid: "103885875"
---
# <a name="updateorchestrator-api"></a>API UpdateOrchestrator

**UpdateOrchestrator** pianifica gli aggiornamenti software automatici tenendo presenti gli effetti dell'utente. Questa API consente di pianificare il download e le installazioni automatiche, insieme ai relativi requisiti, per eseguire gli aggiornamenti in un momento ottimale che riduca al minimo l'effetto della presenza dell'utente. Queste funzionalità sono particolarmente utili per ridurre i sistemi di prestazioni con risorse di calcolo limitate o più lente.

Windows 19H1 include una soluzione di prima generazione per i casi d'uso automatici di aggiornamenti software che sono stati approvati dagli aggiornamenti del sistema operativo e archiviano gli aggiornamenti delle app ed espone una versione iniziale di "accesso limitato" di questa API per un set di aggiornamenti selezionati di app "in modalità utente", come descritto di seguito.

## <a name="features"></a>Funzionalità

- Registra in modo dinamico gli aggiornamenti software
 
- Richiama gli aggiornamenti software registrati durante i tempi ottimali, ad esempio durante l'assenza dell'utente, per aggiornare "app in modalità utente".
    - Include la possibilità di "rimanere svegli" sull'alimentazione CA per ridurre ulteriormente l'effetto dell'utente.

- Opera su un modello di attendibilità che richiama solo gli aggiornamenti software registrati di terze parti attendibili
    - Esistono rischi sostanziali durante l'esposizione di UpdateOrchestrator a tutti i chiamanti, ad esempio l'aggiornamento del firmware o dei driver BIOS quando un utente non è presente.  UpdateOrchestrator include un modello di trust per attenuare questi rischi.

## <a name="developer-audience"></a>Sviluppatori

> [!IMPORTANT]
> L'API UpdateOrchestrator è attualmente una [funzionalità di accesso limitato](/uwp/api/windows.applicationmodel.limitedaccessfeatures). Questa API sarà disponibile pubblicamente in una versione futura.

Usare l'API UpdateOrchestrator se si dispone già di aggiornamenti software in background per le applicazioni ' user mode ' di Win32, ad esempio l'aggiornamento di Adobe per Acrobat Reader o Valve ' s Steam. Questa interfaccia non è necessaria per le applicazioni UWP/Store perché il Microsoft Store sfrutta già questa funzionalità per gli aggiornamenti software.

Per offrire la migliore esperienza utente, questa versione iniziale dell'API ha come ambito un set selezionato di aggiornamenti registrati che soddisfano i criteri seguenti:

- Aggiornamenti solo per le applicazioni ' user mode '
- Non coinvolgere BIOS/firmware/dispositivo o driver software
    - L'aggiornamento di driver BIOS, firmware o dispositivo/software che non hanno superato un criterio di qualità comune costituisce un rischio sostanziale, in particolare quando un utente non è presente. 
- La partecipazione all'uso di questa API comporta la possibilità di garantire la garanzia di tutti i contenuti scaricati e installati dagli aggiornamenti software in background nei sistemi degli utenti tramite i controlli. 

Questa API può essere modificata significativamente prima della versione pubblica.   Mentre l'API di UpdateOrchestrator è in fase di sviluppo, questa versione iniziale come funzionalità di accesso limitato è destinata solo agli aggiornamenti che soddisfano i criteri precedenti.

Il nostro obiettivo è migliorare le funzionalità di questa API e ridurre l'effetto di più aggiornamenti software automatici in Windows. Microsoft apprezzerà l'input grazie a questo [**breve sondaggio**](https://aka.ms/UOAPISurvey) per aiutare Microsoft a comprendere il modo in cui l'API UpdateOrchestrator può soddisfare al meglio le esigenze degli sviluppatori.

