---
title: Messaggi del driver
description: Messaggi del driver
ms.assetid: ed3748ac-08e6-418e-b345-30c796fa38f3
keywords:
- driver installabili, messaggi
- driver installabili,messaggi personalizzati
- messaggi del driver
- messaggi di driver personalizzati
- driver installabili, funzione DriverProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9fb6c741cf782f620d9234f431a248fb47a8362ddcd55cf84205d8faee5800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526331"
---
# <a name="driver-messages"></a>Messaggi del driver

Ogni messaggio del driver è costituito da un identificatore di messaggio e da due parametri a 32 bit. L'identificatore del messaggio è un valore univoco che [la funzione DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) controlla per determinare quale azione eseguire. Il significato dei parametri del messaggio dipende dal messaggio. I parametri possono rappresentare valori o indirizzi. In molti casi, i parametri non vengono usati e sono impostati su zero.

I messaggi del driver possono essere standard o personalizzati. Windows invia messaggi di driver standard, ad esempio [**DRV \_ OPEN,**](drv-open.md) [**DRV \_ CLOSE**](drv-close.md)e [**DRV \_ CONFIGURE,**](drv-configure.md)a un driver installabile in risposta a una richiesta di apertura, chiusura o configurazione del driver. I messaggi standard indirizzano il driver installabile a caricare o scaricare le risorse, abilitarne o disabilitarne il funzionamento, aprire o chiudere un'istanza del driver e visualizzare una finestra di dialogo di configurazione. Alcuni messaggi standard, ad esempio [**DRV \_ POWER**](drv-power.md) e [**DRV \_ EXITSESSION,**](drv-exitsession.md)notificano al driver gli eventi a livello di sistema che influiscono sul funzionamento del driver o su qualsiasi hardware correlato.

Le applicazioni e le DLL inviano messaggi di driver personalizzati per indirizzare un driver installabile per eseguire azioni specifiche del driver. I driver installabili che supportano messaggi personalizzati devono includere l'elaborazione appropriata nella **funzione DriverProc.** Per evitare conflitti tra messaggi di driver personalizzati e standard, gli identificatori di messaggio personalizzati devono avere valori compresi tra DRV \_ RESERVED e DRV \_ USER. I messaggi personalizzati passati alla [funzione DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) vengono ignorati.

 

 