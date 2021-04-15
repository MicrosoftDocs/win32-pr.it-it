---
title: Installazione (Windows Multimedia)
description: Installazione
ms.assetid: 1f0e23ad-4db7-4f32-98d9-e672370db559
keywords:
- driver installabili, installazione
- driver installabili, messaggio DRV_INSTALL
- driver installabili, messaggio DRV_REMOVE
- Messaggio DRV_INSTALL
- Messaggio DRV_REMOVE
- Messaggio DRVCONFIGINFO
- installazione dei driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ebebd090c7499698c59c325d1ac0d487902454
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400111"
---
# <a name="installation-windows-multimedia"></a>Installazione (Windows Multimedia)

Un driver installabile può eseguire attività di installazione specifiche del driver quando si elaborano i messaggi [**drv \_ Install**](drv-install.md) e [**drv \_ Remove**](drv-remove.md) . Un'applicazione di installazione, ad esempio un'applicazione del pannello di controllo, invia i messaggi al driver rispettivamente durante l'installazione o la rimozione del driver.

Quando si elabora il \_ messaggio di installazione di DRV, il driver verifica in genere che l'hardware necessario sia presente e quindi Visualizza la finestra di dialogo di configurazione per consentire all'utente di scegliere le impostazioni di configurazione iniziali per il driver e l'hardware associato. Il messaggio include l'indirizzo di una struttura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) che contiene i nomi della chiave del registro di sistema e il valore associato al driver; il driver controlla il valore del registro di sistema per le informazioni di configurazione predefinite. Infine, il driver crea anche le chiavi del registro di sistema e i valori aggiuntivi necessari per l'operazione riuscita.

Quando si elabora il \_ messaggio di rimozione di DRV, il driver rimuove le chiavi del registro di sistema e i valori che potrebbero essere stati creati.

 

 
