---
title: Appendice B supporto per gestione finestre di dialogo standard
description: Microsoft Active Accessibility fornisce il supporto completo per i controlli della finestra di dialogo Gestione finestre di dialogo standard (SDM).
ms.assetid: cdec2dbd-943b-4160-ae22-c16198cc192a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a710b7f35a242badbff6295d1af0d08cada13fa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710867"
---
# <a name="appendix-b-standard-dialog-manager-support"></a>Appendice B: supporto di gestione finestre di dialogo standard

Microsoft Active Accessibility fornisce il supporto completo per i controlli della finestra di dialogo Gestione finestre di dialogo standard (SDM). SDM è una libreria di codici Microsoft interna che fornisce alle applicazioni Microsoft un livello di indipendenza dalle differenze tra i sistemi operativi Macintosh e Microsoft Windows. SDM viene usato principalmente per le finestre di dialogo in Microsoft Excel e Microsoft Word.

SDM presenta problemi per gli strumenti di accessibilità perché usa implementazioni non standard delle finestre di dialogo. Ad esempio, i pulsanti della finestra di dialogo SDM non utilizzano gli handle di finestra in modo analogo agli elementi dell'interfaccia utente standard. Non è possibile inviare messaggi a pulsanti e pulsanti non inclusi nell'elenco di finestre. Un'applicazione che utilizza SDM comunica con il controllo tramite un'interfaccia privata.

Nella figura seguente viene illustrata una finestra di dialogo di esempio di Word. Sebbene sembri una normale finestra di dialogo di Windows che usa il controllo Tab, si tratta in realtà di una finestra di dialogo SDM.

![screenshot della finestra di dialogo Opzioni con la scheda Visualizza selezionata](images/dialog.gif)

 

 




