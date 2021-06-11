---
title: Installazione (Windows Multimedia)
description: Informazioni sull'installazione di Windows Multimedia, inclusa l'elaborazione DRV_INSTALL e DRV_REMOVE messaggi.
ms.assetid: 1f0e23ad-4db7-4f32-98d9-e672370db559
keywords:
- driver installabili, installazione
- driver installabili, DRV_INSTALL messaggio
- driver installabili, DRV_REMOVE messaggio
- DRV_INSTALL messaggio
- DRV_REMOVE messaggio
- Messaggio DRVCONFIGINFO
- installazione di driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f82a23a781e62553d6488331b2c832104fd770
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989036"
---
# <a name="installation-windows-multimedia"></a>Installazione (Windows Multimedia)

Un driver installabile può eseguire attività di installazione specifiche del driver durante l'elaborazione dei messaggi [**\_ DRV INSTALL**](drv-install.md) [**e DRV \_ REMOVE.**](drv-remove.md) Un'applicazione di installazione, ad esempio Pannello di controllo, invia i messaggi al driver rispettivamente durante l'installazione o la rimozione del driver.

Durante l'elaborazione del messaggio DRV INSTALL, il driver verifica in genere che l'hardware necessario sia presente e quindi visualizza la finestra di dialogo di configurazione per consentire all'utente di scegliere le impostazioni di configurazione iniziali per il driver e \_ l'hardware associato. Il messaggio include l'indirizzo di una [**struttura DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) che contiene i nomi della chiave e del valore del Registro di sistema associati al driver. Il driver controlla il valore del Registro di sistema per le informazioni di configurazione predefinite. Infine, il driver crea anche eventuali chiavi e valori del Registro di sistema aggiuntivi necessari per il corretto funzionamento.

Durante l'elaborazione del messaggio DRV REMOVE, il driver rimuove le chiavi e i valori \_ del Registro di sistema che potrebbero essere stati creati.

 

 
