---
title: Appendice B Supporto di Dialog Manager Standard
description: Microsoft Active Accessibility supporto completo per i controlli della finestra di dialogo SDM (Standard Dialog Manager).
ms.assetid: cdec2dbd-943b-4160-ae22-c16198cc192a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b6500cabf4820fffe12b7ef160f2e494e43db067f6b96409dee02bbfd6119e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326823"
---
# <a name="appendix-b-standard-dialog-manager-support"></a>Appendice B: Supporto di Dialog Manager Standard

Microsoft Active Accessibility supporto completo per i controlli della finestra di dialogo SDM (Standard Dialog Manager). SDM è una libreria di codice Microsoft interna che offre alle applicazioni Microsoft un certo grado di indipendenza dalle differenze tra i sistemi operativi Macintosh e Microsoft Windows microsoft. SDM viene usato principalmente per le finestre di dialogo Microsoft Excel e Microsoft Word.

SDM presenta problemi per gli strumenti di accessibilità perché usa implementazioni non standard delle finestre di dialogo. Ad esempio, i pulsanti della finestra di dialogo SDM non usano gli handle di finestra come gli elementi dell'interfaccia utente standard. Non è possibile inviare messaggi ai pulsanti e i pulsanti non sono contenuti nell'elenco delle finestre. Un'applicazione che usa SDM comunica con il controllo tramite un'interfaccia privata.

La figura seguente mostra una finestra di dialogo di esempio di Word. Anche se è simile a una normale Windows che usa il controllo Struttura a schede, è in realtà una finestra di dialogo SDM.

![Screenshot della finestra di dialogo opzioni con la scheda Visualizza selezionata](images/dialog.gif)

 

 




