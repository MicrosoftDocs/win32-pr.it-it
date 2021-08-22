---
description: Esecuzione automatica è una funzionalità del Windows operativo.
title: Creazione di un'applicazione CD-ROM abilitata per l'esecuzione automatica
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5c583c1d-a4eb-4291-a839-c1ca7c51342c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9b8bc1edad7fe49b996dd8471ae8ce081c36c71b7b7df48ca6296b07f8646ccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460931"
---
# <a name="creating-an-autorun-enabled-cd-rom-application"></a>Creazione di un'applicazione CD-ROM abilitata per l'esecuzione automatica

Esecuzione automatica è una funzionalità del Windows operativo. Automatizza le procedure per l'installazione e la configurazione di prodotti progettati Windows piattaforme basate su Windows distribuite su CD-ROM. Quando gli utenti inseriscono un compact disc abilitato per l'esecuzione automatica nell'unità CD-ROM, l'esecuzione automatica esegue automaticamente un'applicazione sul CD-ROM che installa, configura o esegue il prodotto selezionato.

L'esecuzione automatica può essere usata per installare ed eseguire applicazioni CD-ROM. Sebbene l'esecuzione automatica sia più comunemente usata per le applicazioni Windows, può essere usata anche per installare, configurare o eseguire applicazioni basate su MS-DOS in una sessione Windows Microsoft MS-DOS. È possibile configurare ogni applicazione basata su MS-DOS con una propria icona univoca, Config.sys file e Autoexec.bat file. Windows crea i file di configurazione corretti per l'applicazione basata su MS-DOS. L'applicazione di avvio avvia quindi l'applicazione basata su MS-DOS in una finestra.

> [!Note]  
> Per il funzionamento dell'esecuzione automatica, l'unità CD-ROM deve avere driver di dispositivo a 32 o 64 bit che rilevano quando un utente inserisce un compact disc e inviano una notifica al sistema.

 

Le sezioni seguenti illustrano come implementare un'applicazione CD-ROM abilitata per l'esecuzione automatica.

-   [Creazione di un'AutoRun-Enabled applicazione](autoplay-works.md)
-   [Voci di Autorun.inf](autorun-cmds.md)
-   [Abilitazione e disabilitazione dell'esecuzione automatica](autoplay-reg.md)

 

 



