---
description: Quando non sono necessari privilegi elevati per installare un pacchetto del programma di installazione di Windows, l'autore del pacchetto può eliminare la finestra di dialogo visualizzata da Controllo dell'account utente per richiedere agli utenti l'autorizzazione dell'amministratore.
ms.assetid: cab30f95-cc93-46db-aba5-741b44adb6de
title: Creazione di pacchetti senza la finestra di dialogo Controllo dell'account utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5064589a49327db263158b10ff9377e0f7b69232b0e3679d5bd86c7bd2f2e3f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066091"
---
# <a name="authoring-packages-without-the-uac-dialog-box"></a>Creazione di pacchetti senza la finestra di dialogo Controllo dell'account utente

Quando non sono necessari privilegi elevati per installare un pacchetto del programma di installazione [](u-gly.md) di Windows, l'autore del pacchetto può eliminare la finestra di dialogo visualizzata da Controllo dell'account utente per richiedere agli utenti l'autorizzazione dell'amministratore.

Per evitare la visualizzazione della finestra di dialogo Controllo dell'account utente durante l'installazione dell'applicazione, l'autore del pacchetto deve eseguire le operazioni seguenti:

-   Installare l'applicazione usando Windows Installer 4.0 o versione successiva in Windows Vista.
-   Non dipendere dall'uso di privilegi di sistema elevati per installare l'applicazione nel computer.
-   Installare l'applicazione nel contesto per utente e renderla il contesto di installazione predefinito del pacchetto. Se la [**proprietà ALLUSERS**](allusers.md) non è impostata, il programma di installazione installa il pacchetto nel contesto per utente. Se non si include la proprietà **ALLUSERS** nella tabella [Property](property-table.md), il programma di installazione non imposta questa proprietà e quindi l'installazione per utente diventa il contesto di installazione predefinito. È possibile eseguire l'override di questa impostazione predefinita impostando **la proprietà ALLUSERS** nella riga di comando.
-   Impostare il bit 3 nella [**proprietà Riepilogo conteggio**](word-count-summary.md) parole per indicare che non sono necessari privilegi elevati per installare l'applicazione.

 

 



