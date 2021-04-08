---
description: Quando non sono necessari privilegi elevati per installare un pacchetto di Windows Installer, l'autore del pacchetto può disattivare la finestra di dialogo visualizzata da controllo dell'account utente per richiedere l'autorizzazione dell'amministratore.
ms.assetid: cab30f95-cc93-46db-aba5-741b44adb6de
title: Creazione di pacchetti senza la finestra di dialogo controllo dell'account utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dcd44bf7d2250e12e7cafde46b57978b48cceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756230"
---
# <a name="authoring-packages-without-the-uac-dialog-box"></a>Creazione di pacchetti senza la finestra di dialogo controllo dell'account utente

Quando non sono necessari privilegi elevati per installare un pacchetto di Windows Installer, l'autore del pacchetto può disattivare la finestra di dialogo visualizzata da [*controllo dell'account utente*](u-gly.md) per richiedere l'autorizzazione dell'amministratore.

Per evitare la visualizzazione della finestra di dialogo controllo dell'account utente durante l'installazione dell'applicazione, l'autore del pacchetto deve eseguire le operazioni seguenti:

-   Installare l'applicazione utilizzando Windows Installer 4,0 o versioni successive in Windows Vista.
-   Non dipendere dall'utilizzo di privilegi di sistema elevati per installare l'applicazione nel computer.
-   Installare l'applicazione nel contesto per utente e impostarla come contesto di installazione predefinito del pacchetto. Se la proprietà [**ALLUSERS**](allusers.md) non è impostata, il programma di installazione installa il pacchetto nel contesto per singolo utente. Se non si include la proprietà **ALLUSERS** nella tabella delle [Proprietà](property-table.md), il programma di installazione non imposta questa proprietà e l'installazione per utente diventa il contesto di installazione predefinito. È possibile eseguire l'override di questa impostazione predefinita impostando la proprietà **ALLUSERS** nella riga di comando.
-   Impostare il bit 3 nella proprietà [**riepilogo Conteggio parole**](word-count-summary.md) per indicare che non sono necessari privilegi elevati per installare l'applicazione.

 

 



