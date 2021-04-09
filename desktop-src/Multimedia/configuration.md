---
title: Configurazione (Windows Multimedia)
description: Configurazione
ms.assetid: d61d6c8b-8dba-45c2-ba99-0b2111a2d624
keywords:
- driver installabili, configurazione
- driver installabili, messaggio DRV_CONFIGURE
- Messaggio DRV_CONFIGURE
- Messaggio DRV_QUERYCONFIGURE
- Messaggio DRVCONFIGINFO
- configurazione dei driver installabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a248f992a857b88b723bd54c771f1af5709d97
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047718"
---
# <a name="configuration-windows-multimedia"></a>Configurazione (Windows Multimedia)

Un driver installabile può consentire agli utenti di scegliere le impostazioni di configurazione per il driver e l'hardware associato visualizzando una finestra di dialogo di configurazione durante l'elaborazione del messaggio di configurazione di [**drv \_**](drv-configure.md) . Il driver è responsabile della creazione e della gestione della finestra di dialogo, dell'elaborazione di qualsiasi input utente dalla finestra di dialogo e della modifica della configurazione del driver o dell'hardware come richiesto dall'utente. Il driver deve fornire una routine della finestra di dialogo separata per elaborare i messaggi di finestra per la finestra di dialogo e un modello di finestra di dialogo per definire l'aspetto e il contenuto della finestra di dialogo.

Prima di ricevere il \_ messaggio di configurazione di DRV, un driver riceve il messaggio [**drv \_ QUERYCONFIGURE**](drv-queryconfigure.md) . Il driver deve restituire un valore diverso da zero alla query per garantire la ricezione del messaggio di \_ configurazione DRV successivo.

Quando si inizializza la finestra di dialogo configurazione, il driver recupera in genere le informazioni di configurazione dal registro di sistema. Per facilitare l'individuazione di queste informazioni, il messaggio di configurazione di DRV \_ include in genere l'indirizzo di una struttura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) che contiene i nomi della chiave del registro di sistema e il valore associato al driver. Se l'utente richiede modifiche alla configurazione, il driver deve aggiornare le informazioni di configurazione nel registro di sistema.

 

 
