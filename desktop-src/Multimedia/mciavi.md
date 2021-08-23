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
ms.openlocfilehash: 6d4a7a6bc8da314cc5cb891846e46289396fefb6be60d92ddd38f17ab1aff0ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783430"
---
# <a name="mciavi"></a>MCIAVI

Un file AVI può contenere più di due flussi, ad esempio una sequenza video, una colonna sonora inglese e una colonna sonora francese. L'applicazione può usare un flusso indipendentemente dagli altri flussi nel file.

Il **tipo di dispositivo digitalvideo** controlla i file video. Per un elenco dei comandi MCI riconosciuti dai dispositivi digital-video, vedere [Set di comandi Digital-Video](digital-video-command-set.md).

Il driver MCIAVI riproduce sequenze video e altri flussi di dati sotto il controllo dei comandi MCI. I flussi di dati possono contenere immagini, audio e tavolozze. I dati dell'immagine possono essere costituiti da immagini con tavolozze dei colori o informazioni sul vero colore.

L'audio viene sincronizzato con il video entro un terzo di secondo. Se l'hardware audio non è disponibile, tuttavia, il driver riproduce solo il flusso video. Il driver MCIAVI può eliminare i fotogrammi video, se necessario, per riprodurre un flusso senza interruzioni audio.

L'applicazione può usare i servizi della classe finestra MCIWnd anziché l'interfaccia di comando MCI per controllare qualsiasi driver MCI. Questa classe finestra gestisce molti dei dettagli della gestione della finestra che supporta il dispositivo MCI e semplifica la programmazione necessaria per inviare i comandi MCI. L'applicazione può usare direttamente i servizi della libreria MCIWnd per controllare il dispositivo MCI oppure può avere MCIWnd visualizzare una barra degli strumenti, una barra di scorrimento e menu che consentono all'utente di controllare il dispositivo. Per altre informazioni sulla classe della finestra MCIWnd, vedere [McIWnd Window Class](mciwnd-window-class.md).

 

 




