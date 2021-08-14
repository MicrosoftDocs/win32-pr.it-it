---
title: Stazioni finestra
description: Una stazione finestra contiene gli Appunti, una tabella atom e uno o più oggetti desktop. Ogni oggetto stazione finestra è un oggetto a protezione diretta. Quando viene creata, una stazione finestra viene associata al processo chiamante e assegnata alla sessione corrente.
ms.assetid: 617661e2-3b0d-42a9-9769-2ba0957c31a8
keywords:
- oggetti window station
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d55e43a0db21b23a6704949f0d72a184c9034f625689b800814ac8a93891b7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199692"
---
# <a name="window-stations"></a>Stazioni finestra

Una *stazione finestra* contiene gli Appunti, una tabella atom e uno o più oggetti [desktop.](desktops.md) Ogni oggetto stazione finestra è un oggetto a protezione diretta. Quando viene creata, una stazione finestra viene associata al processo chiamante e assegnata alla sessione corrente.

La *stazione finestra interattiva è* l'unica stazione finestra in grado di visualizzare un'interfaccia utente o ricevere l'input dell'utente. Viene assegnato alla sessione di accesso dell'utente interattivo e contiene la tastiera, il mouse e il dispositivo di visualizzazione. Viene sempre denominato "WinSta0". Tutte le altre stazioni finestra non sono interattive, ovvero non possono visualizzare un'interfaccia utente o ricevere l'input dell'utente.

Quando un utente accede a un computer usando Servizi Desktop remoto, viene avviata una sessione per l'utente. Ogni sessione è associata alla propria stazione finestra interattiva denominata "WinSta0". Per altre informazioni, vedere [Desktop remoto Sessions](/windows/desktop/TermServ/terminal-services-sessions).

Per altre informazioni sulle stazioni finestra, vedere gli argomenti seguenti:

-   [Creazione di window station e desktop](window-station-and-desktop-creation.md)
-   [Elaborare la connessione a una stazione finestra](process-connection-to-a-window-station.md)
-   [Sicurezza e diritti di accesso di Window Station](window-station-security-and-access-rights.md)

 

 