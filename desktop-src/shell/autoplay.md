---
description: AutoRun è una funzionalità del sistema operativo Windows.
title: Creazione di un'applicazione CD-ROM abilitata per l'AutoRun
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5c583c1d-a4eb-4291-a839-c1ca7c51342c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 33f3ccc0a253690cd377cad908f87b43ac1ea304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225938"
---
# <a name="creating-an-autorun-enabled-cd-rom-application"></a>Creazione di un'applicazione CD-ROM abilitata per l'AutoRun

AutoRun è una funzionalità del sistema operativo Windows. Consente di automatizzare le procedure per l'installazione e la configurazione di prodotti progettati per piattaforme basate su Windows distribuite su CD-ROM. Quando gli utenti inseriscono un disco Compact abilitato per l'AutoRun nell'unità CD-ROM, l'esecuzione automatica esegue automaticamente un'applicazione nel CD-ROM che installa, configura o esegue il prodotto selezionato.

AutoRun può essere usato per installare ed eseguire applicazioni CD-ROM. Sebbene l'esecuzione automatica sia più comunemente usata per le applicazioni Windows, può essere usata anche per installare, configurare o eseguire applicazioni basate su MS-DOS in una sessione Microsoft MS-DOS di Windows. È possibile configurare ogni applicazione basata su MS-DOS con una propria icona univoca, un file di Config.sys e un file di Autoexec.bat. Windows crea i file di configurazione corretti per l'applicazione basata su MS-DOS. L'applicazione di avvio avvia quindi l'applicazione basata su MS-DOS in una finestra.

> [!Note]  
> Per il funzionamento dell'avvio automatico, l'unità CD-ROM deve avere driver di dispositivo 32 o 64 bit che rilevano quando un utente inserisce un disco compatto e invia una notifica al sistema.

 

Le sezioni seguenti illustrano come implementare un'applicazione CD-ROM abilitata per l'esecuzione automatica.

-   [Creazione di un'applicazione AutoRun-Enabled](autoplay-works.md)
-   [Voci Autorun. inf](autorun-cmds.md)
-   [Abilitazione e disabilitazione dell'esecuzione automatica](autoplay-reg.md)

 

 



