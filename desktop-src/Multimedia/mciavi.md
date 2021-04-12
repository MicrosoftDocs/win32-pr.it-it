---
title: MCIAVI
description: MCIAVI
ms.assetid: 68639f35-bc20-457d-b937-760af8323dce
keywords:
- Dispositivi MCI, driver MCIAVI
- Comandi MCI, driver MCIAVI
- Driver MCIAVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be2e69cf2b0fd9ee71650c56b0d7d9efb50a46e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471470"
---
# <a name="mciavi"></a>MCIAVI

Un file AVI può contenere più di due flussi, ad esempio una sequenza video, una colonna della lingua inglese e una colonna musicale francese. L'applicazione può usare un flusso indipendentemente dagli altri flussi del file.

Il tipo di dispositivo **digitalvideo** controlla i file video. Per un elenco dei comandi MCI riconosciuti dai dispositivi digitali video, vedere [set di comandi Digital-video](digital-video-command-set.md).

Il driver MCIAVI riproduce sequenze video e altri flussi di dati sotto il controllo dei comandi MCI. I flussi di dati possono contenere immagini, audio e tavolozze. I dati dell'immagine possono essere costituiti da immagini con tavolozze dei colori o informazioni sui colori reali.

L'audio viene sincronizzato con il video entro un trentesimo di secondo. Se l'hardware audio non è disponibile, tuttavia, il driver riproduce solo il flusso video. Se necessario, il driver MCIAVI può eliminare i fotogrammi video per riprodurre un flusso senza interruzioni audio.

L'applicazione può usare i servizi della classe MCIWnd della finestra anziché l'interfaccia del comando MCI per controllare qualsiasi driver MCI. Questa classe di finestra gestisce molti dei dettagli relativi alla gestione della finestra che supporta il dispositivo MCI e semplifica la programmazione necessaria per inviare i comandi MCI. L'applicazione può usare direttamente i servizi di libreria MCIWnd per controllare il dispositivo MCI oppure MCIWnd visualizzare una barra degli strumenti, una barra di scorrimento e i menu che consentono all'utente di controllare il dispositivo. Per ulteriori informazioni sulla classe della finestra MCIWnd, vedere [classe della finestra MCIWnd](mciwnd-window-class.md).

 

 




