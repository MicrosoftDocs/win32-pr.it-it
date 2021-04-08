---
title: Stazioni finestra
description: Una finestra di Windows contiene gli appunti, una tabella Atom e uno o più oggetti desktop. Ogni oggetto della stazione di finestra è un oggetto a protezione diretta. Quando viene creata, una stazione di finestra viene associata al processo chiamante e assegnata alla sessione corrente.
ms.assetid: 617661e2-3b0d-42a9-9769-2ba0957c31a8
keywords:
- oggetti Window Station
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee2048015e4b0c687932c4d01aafe31127e2141e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046916"
---
# <a name="window-stations"></a>Stazioni finestra

Una *finestra di Windows* contiene gli appunti, una tabella Atom e uno o più oggetti [Desktop](desktops.md) . Ogni oggetto della stazione di finestra è un oggetto a protezione diretta. Quando viene creata, una stazione di finestra viene associata al processo chiamante e assegnata alla sessione corrente.

*Interactive Window Station* è l'unica finestra che può visualizzare un'interfaccia utente o ricevere l'input dell'utente. Viene assegnato alla sessione di accesso dell'utente interattivo e contiene la tastiera, il mouse e il dispositivo di visualizzazione. Viene sempre denominato "WinSta0". Tutte le altre stazioni della finestra sono non interattive, il che significa che non possono visualizzare un'interfaccia utente o ricevere l'input dell'utente.

Quando un utente accede a un computer utilizzando Servizi Desktop remoto, viene avviata una sessione per l'utente. Ogni sessione è associata alla propria finestra interattiva denominata "WinSta0". Per ulteriori informazioni, vedere [Desktop remoto Sessions](/windows/desktop/TermServ/terminal-services-sessions).

Per ulteriori informazioni sulle stazioni della finestra, vedere gli argomenti seguenti:

-   [Creazione di finestre e desktop](window-station-and-desktop-creation.md)
-   [Elaborare la connessione a una stazione di finestra](process-connection-to-a-window-station.md)
-   [Diritti di accesso e sicurezza di Windows Station](window-station-security-and-access-rights.md)

 

 