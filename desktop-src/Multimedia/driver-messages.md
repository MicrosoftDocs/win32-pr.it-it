---
title: Messaggi driver
description: Messaggi driver
ms.assetid: ed3748ac-08e6-418e-b345-30c796fa38f3
keywords:
- driver installabili, messaggi
- driver installabili, messaggi personalizzati
- messaggi driver
- messaggi di driver personalizzati
- driver installabili, funzione DriverProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25e03f9d68254752655be8abe9040a17d44dc0ff
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046608"
---
# <a name="driver-messages"></a>Messaggi driver

Ogni messaggio di driver è costituito da un identificatore di messaggio e da parametri a 2 32 bit. L'identificatore del messaggio è un valore univoco che la funzione [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) controlla per determinare l'azione da eseguire. Il significato dei parametri del messaggio dipende dal messaggio. I parametri possono rappresentare valori o indirizzi. In molti casi, i parametri non vengono usati e sono impostati su zero.

I messaggi del driver possono essere standard o personalizzati. Windows invia messaggi di driver standard, ad esempio [**drv \_ Open**](drv-open.md), [**drv \_ Close**](drv-close.md)e [**drv \_ Configure**](drv-configure.md), a un driver installabile in risposta a una richiesta di apertura, chiusura o configurazione del driver. I messaggi standard indirizzano il driver installabile per caricare o scaricare le risorse, abilitare o disabilitare l'operazione, aprire o chiudere un'istanza del driver e visualizzare una finestra di dialogo di configurazione. Alcuni messaggi standard, ad esempio [**drv \_ Power**](drv-power.md) e [**drv \_ EXITSESSION**](drv-exitsession.md), notificano al driver gli eventi a livello di sistema che influiscono sul funzionamento del driver o di qualsiasi hardware correlato.

Le applicazioni e le dll inviano messaggi di driver personalizzati per indirizzare un driver installabile per eseguire azioni specifiche del driver. I driver installabili che supportano messaggi personalizzati devono includere l'elaborazione appropriata nella funzione **DriverProc** . Per evitare conflitti tra i messaggi di driver personalizzati e standard, gli identificatori di messaggio personalizzati devono avere valori compresi tra DRV \_ riservato all' \_ utente DRV. I messaggi personalizzati passati alla funzione [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) vengono ignorati.

 

 