---
description: Un pacchetto di notifica Winlogon è una DLL che esporta funzioni che gestiscono gli eventi Winlogon. Ad esempio, quando un utente accede al sistema, Winlogon chiama ogni funzione del gestore eventi di accesso del pacchetto di notifica per fornire informazioni sull'evento.
ms.assetid: a2a26bac-93b6-4d94-94fc-42c9821935a0
title: Creazione di un pacchetto di notifica Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0127674967ee3155d42e143a1b142d8c83137c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311941"
---
# <a name="creating-a-winlogon-notification-package"></a>Creazione di un pacchetto di notifica Winlogon

Un pacchetto di notifica [*Winlogon*](/windows/desktop/SecGloss/w-gly) è una dll che esporta funzioni che gestiscono gli eventi Winlogon. Ad esempio, quando un utente accede al sistema, Winlogon chiama ogni funzione del gestore eventi di accesso del pacchetto di notifica per fornire informazioni sull'evento.

I nomi delle funzioni del gestore eventi implementati in un pacchetto di notifica vengono lasciati allo sviluppatore; Winlogon controlla il registro di sistema per ottenere i nomi delle funzioni del gestore eventi. Ad esempio, un pacchetto di notifica può implementare la funzione del gestore eventi di accesso come se `WLEventLogon` fosse un altro a usare `HandleLogonEvent` .

Non è necessario implementare e registrare i gestori eventi per ogni evento Winlogon, solo per gli eventi che risultano utili per l'applicazione. Ogni funzione del gestore eventi deve usare il prototipo di funzione descritto nel [prototipo di funzione del gestore eventi](event-handler-function-prototype.md). Questo prototipo ha un solo parametro: una struttura di [**\_ \_ informazioni di notifica di WLX**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) che contiene i dettagli sull'evento.

Winlogon ignora l'output delle funzioni del gestore eventi. Se la gestione di un evento richiede l'interazione con Winlogon, usare le [funzioni di supporto di Winlogon](authentication-functions.md).

Per usare il pacchetto di notifiche Winlogon, la DLL deve essere copiata nella cartella% SystemRoot% \\ system32 ed è necessario eseguire un aggiornamento del registro di sistema per il pacchetto di notifica. Per informazioni sull'aggiornamento del registro di sistema, vedere la pagina relativa alla [registrazione di un pacchetto di notifica Winlogon](registering-a-winlogon-notification-package.md).

 

 
