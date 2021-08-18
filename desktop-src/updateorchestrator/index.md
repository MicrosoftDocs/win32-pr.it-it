---
title: Aggiornare l'API di Orchestrator
description: UpdateOrchestrator pianifica gli aggiornamenti software automatici in base all'impatto dell'utente.
ms.date: 01/14/2021
ms.topic: overview
ms.openlocfilehash: 6460446397af168a4098a7203179d5587d4dcd9a3cea813991648a5083d07334
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966107"
---
# <a name="updateorchestrator-api"></a>UpdateOrchestrator API

**UpdateOrchestrator pianifica** gli aggiornamenti software automatici in base all'impatto dell'utente. Questa API consente di pianificare il download e le installazioni automatici, insieme ai relativi requisiti, per eseguire gli aggiornamenti in un momento ottimale che riduce al minimo l'impatto sugli utenti presenti. Queste funzionalità sono particolarmente utili per i sistemi con prestazioni inferiori con risorse di calcolo limitate o lente.

Windows 19H1 include una soluzione di prima generazione per i casi d'uso degli aggiornamenti software automatici adottati dagli aggiornamenti del sistema operativo e dagli aggiornamenti delle app dello Store ed espone una versione iniziale "Accesso limitato" di questa API per un set selezionato di aggiornamenti delle app in modalità utente, come descritto di seguito.

## <a name="features"></a>Funzionalità

- Registra dinamicamente gli aggiornamenti software
 
- Richiama gli strumenti di aggiornamento software registrati durante i periodi ottimali, ad esempio durante l'assenza dell'utente, per aggiornare le "app in modalità utente".
    - Include la possibilità di "rimanere attivo" sull'alimentazione CA per ridurre ulteriormente l'impatto a distanza dell'utente.

- Opera su un modello di attendibilità che richiama solo strumenti di aggiornamento software registrati di terze parti attendibili
    - Esistono rischi sostanziali quando si espone UpdateOrchestrator a tutti i chiamanti, ad esempio l'aggiornamento del firmware o dei driver BIOS quando un utente non è presente.  UpdateOrchestrator include un modello di attendibilità per attenuare questi rischi.

## <a name="developer-audience"></a>Sviluppatori

> [!IMPORTANT]
> L'API UpdateOrchestrator è attualmente una [funzionalità ad accesso limitato.](/uwp/api/windows.applicationmodel.limitedaccessfeatures) Questa API diventerà disponibile pubblicamente in una versione futura.

Usare l'API UpdateOrchestrator se si dispone già di strumenti di aggiornamento software in background per le applicazioni Win32 in modalità utente, ad esempio lo strumento di aggiornamento di Adobe per Acrobat Reader o Valve's Steam. Questa interfaccia non è necessaria per le applicazioni UWP/Store perché il Microsoft Store già sfrutta questa funzionalità per gli aggiornamenti software.

Per offrire la migliore esperienza del cliente, questa versione iniziale dell'API ha come ambito un set selezionato di aggiornamenti registrati che soddisfano i criteri seguenti:

- Aggiornamenti solo per le applicazioni in modalità utente
- Non coinvolgere BIOS/firmware/dispositivo o driver software
    - L'aggiornamento di BIOS, firmware o driver di dispositivo/software che non hanno superato criteri di qualità comuni costituisce un rischio significativo, in particolare quando un utente non è presente. 
- La partecipazione all'utilizzo di questa API comporta la possibilità di garantire tutto il contenuto scaricato e installato dagli aggiornamenti software in background nei sistemi degli utenti tramite controlli. 

Questa API può essere modificata in modo significativo prima del rilascio pubblico.   Mentre l'API UpdateOrchestrator è in fase di sviluppo, questa versione iniziale come funzionalità di accesso limitato è solo per gli aggiornamenti che al momento soddisfano i criteri precedenti.

L'obiettivo è migliorare le funzionalità di questa API e ridurre l'impatto di più aggiornamenti software automatici Windows. Questo breve sondaggio ci aiuta [**a**](https://aka.ms/UOAPISurvey) comprendere in che modo l'API UpdateOrchestrator può soddisfare meglio le esigenze degli sviluppatori.

