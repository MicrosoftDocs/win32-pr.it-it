---
title: Configurazione (Windows Multimediali)
description: Informazioni su come un driver Windows Multimedia può consentire agli utenti di scegliere le impostazioni di configurazione visualizzando una finestra di dialogo di configurazione.
ms.assetid: d61d6c8b-8dba-45c2-ba99-0b2111a2d624
keywords:
- driver installabili, configurazione
- driver installabili, DRV_CONFIGURE messaggio
- DRV_CONFIGURE messaggio
- DRV_QUERYCONFIGURE messaggio
- Messaggio DRVCONFIGINFO
- configurazione di driver installabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1f5079878ba3da60484efb8afccc2effbbd8ec7212dfd339ab0cba5f43653a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144964"
---
# <a name="configuration-windows-multimedia"></a>Configurazione (Windows Multimediali)

Un driver installabile può consentire agli utenti di scegliere le impostazioni di configurazione per il driver e l'hardware associato visualizzando una finestra di dialogo di configurazione durante l'elaborazione [**del messaggio DRV \_ CONFIGURE.**](drv-configure.md) Il driver è responsabile della creazione e della gestione della finestra di dialogo, dell'elaborazione di qualsiasi input utente dalla finestra di dialogo e della modifica della configurazione del driver o dell'hardware come richiesto dall'utente. Il driver deve fornire una procedura separata per elaborare i messaggi della finestra per la finestra di dialogo e un modello di finestra di dialogo per definire l'aspetto e il contenuto della finestra di dialogo.

Prima di ricevere il messaggio DRV \_ CONFIGURE, un driver riceve il [**messaggio DRV \_ QUERYCONFIGURE.**](drv-queryconfigure.md) Il driver deve restituire un valore diverso da zero alla query per garantire la ricezione del messaggio DRV \_ CONFIGURE successivo.

Quando si inizializza la finestra di dialogo di configurazione, il driver recupera in genere le informazioni di configurazione dal Registro di sistema. Per facilitare l'individuazione di queste informazioni, il messaggio DRV CONFIGURE include in genere l'indirizzo di una \_ [**struttura DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) che contiene i nomi della chiave e del valore del Registro di sistema associati al driver. Se l'utente richiede modifiche alla configurazione, il driver deve aggiornare le informazioni di configurazione nel Registro di sistema.

 

 
