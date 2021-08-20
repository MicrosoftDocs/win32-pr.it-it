---
title: Installazione (Windows Multimediali)
description: Informazioni sull Windows installazione multimediale, inclusa l'elaborazione DRV_INSTALL e DRV_REMOVE messaggi.
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
ms.openlocfilehash: a01ef47952f3d5a62c0dce246bf24689d37f11326f0f3ec251f7afc19c822fa9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140679"
---
# <a name="installation-windows-multimedia"></a>Installazione (Windows Multimediali)

Un driver installabile può eseguire attività di installazione specifiche del driver durante l'elaborazione dei messaggi [**DRV \_ INSTALL**](drv-install.md) e [**DRV \_ REMOVE.**](drv-remove.md) Un'applicazione di installazione, ad esempio Pannello di controllo, invia i messaggi al driver rispettivamente durante l'installazione o la rimozione del driver.

Quando si elabora il messaggio DRV INSTALL, il driver verifica in genere che l'hardware necessario sia presente e quindi visualizza la finestra di dialogo di configurazione per consentire all'utente di scegliere le impostazioni di configurazione iniziali per il driver e \_ l'hardware associato. Il messaggio include l'indirizzo di [**una struttura DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) che contiene i nomi della chiave e del valore del Registro di sistema associati al driver. il driver controlla il valore del Registro di sistema per le informazioni di configurazione predefinite. Infine, il driver crea anche eventuali chiavi e valori del Registro di sistema aggiuntivi necessari per il corretto funzionamento.

Quando si elabora il messaggio DRV REMOVE, il driver rimuove tutte le chiavi e i \_ valori del Registro di sistema creati.

 

 
