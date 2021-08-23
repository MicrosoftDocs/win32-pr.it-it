---
description: Un pacchetto di notifica Winlogon è una DLL che esporta funzioni che gestiscono eventi Winlogon. Ad esempio, quando un utente accede al sistema, Winlogon chiama la funzione del gestore eventi di accesso di ogni pacchetto di notifica per fornire informazioni sull'evento.
ms.assetid: a2a26bac-93b6-4d94-94fc-42c9821935a0
title: Creazione di un pacchetto di notifica Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84d0290f7afeba7a427f5c50caf1638fd88bfdb4b52ee513a9b1c0506aed9df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008869"
---
# <a name="creating-a-winlogon-notification-package"></a>Creazione di un pacchetto di notifica Winlogon

Un [*pacchetto di notifica Winlogon*](/windows/desktop/SecGloss/w-gly) è una DLL che esporta funzioni che gestiscono eventi Winlogon. Ad esempio, quando un utente accede al sistema, Winlogon chiama la funzione del gestore eventi di accesso di ogni pacchetto di notifica per fornire informazioni sull'evento.

I nomi delle funzioni del gestore eventi implementate in un pacchetto di notifica vengono lasciati allo sviluppatore; Winlogon controlla il Registro di sistema per ottenere i nomi delle funzioni del gestore eventi. Ad esempio, un pacchetto di notifica potrebbe implementare la funzione del gestore eventi di accesso come `WLEventLogon` mentre un altro potrebbe usare `HandleLogonEvent` .

Non è necessario implementare e registrare gestori eventi per ogni evento Winlogon, solo per gli eventi utili per l'applicazione. Ogni funzione del gestore eventi deve usare il prototipo di funzione descritto in [Prototipo di funzione del gestore eventi](event-handler-function-prototype.md). Questo prototipo ha un singolo parametro: una [**struttura WLX \_ NOTIFICATION \_ INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) che contiene i dettagli sull'evento.

Winlogon ignora l'output delle funzioni del gestore eventi. Se la gestione di un evento richiede l'interazione con Winlogon, usare le [funzioni di supporto di Winlogon](authentication-functions.md).

Per usare il pacchetto di notifica Winlogon, la DLL deve essere copiata nella cartella %SystemRoot% system32 e deve essere effettuato un aggiornamento del Registro di sistema per \\ il pacchetto di notifica. Per informazioni sull'aggiornamento del Registro di sistema, vedere [Registrazione di un pacchetto di notifica Winlogon](registering-a-winlogon-notification-package.md).

 

 
