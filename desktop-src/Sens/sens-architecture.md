---
description: Il servizio di notifica eventi di sistema funziona con il sistema di eventi COM+.
ms.assetid: c51d1f61-6087-4480-b989-31241829781b
title: Architettura SENS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32976a716ab0ba5651ce6605fe524d639820696
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316627"
---
# <a name="sens-architecture"></a>Architettura SENS

Il servizio di notifica eventi di sistema funziona con il sistema di eventi COM+. SENS è un autore di eventi per le classi di eventi monitorati: eventi di rete, di accesso e di alimentazione/batteria. L'applicazione che riceve una notifica viene chiamata Sottoscrittore di eventi.

Quando un'applicazione sottoscrive la ricezione di notifiche, può specificare anche i filtri associati agli eventi sottoscritti. Gli eventi SENS e COM+ utilizzano i filtri per determinare ulteriormente quando l'applicazione deve ricevere notifiche.

Le notifiche sono asincrone, quindi l'applicazione che riceve la notifica non deve essere attiva quando viene inviata la notifica. Quando un'applicazione sottoscrive la ricezione di notifiche, può specificare se deve essere attivata quando si verifica l'evento o se viene inviata una notifica in un secondo momento quando è attiva.

La sottoscrizione può essere temporanea e valida solo fino a quando l'applicazione non viene arrestata oppure può essere persistente e valida fino a quando l'applicazione non viene rimossa dal sistema.

Un archivio dati degli eventi COM+ contiene informazioni su server Publisher (SENS), sottoscrittori di eventi e filtri. SENS definisce anche un'interfaccia in uscita per ogni classe di evento in una libreria dei tipi.



| classe di evento    | GUID                          | Interfaccia    |
|----------------|-------------------------------|--------------|
| Eventi di rete | \_rete EVENTCLASS \_ SENSGUID | ISensNetwork |
| Eventi di accesso   | \_accesso EVENTCLASS di SENSGUID \_   | ISensLogon   |
| Eventi di alimentazione   | SENSGUID \_ EVENTCLASS \_ ONNOW   | ISensOnNow   |



 

Per ricevere notifiche per uno di questi eventi, l'applicazione deve eseguire due operazioni:

-   Sottoscrivere gli eventi SENS che interessano. Per sottoscrivere un evento, utilizzare le interfacce **IEventSubscription** e **IEVENTSYSTEM** negli eventi com+. È necessario specificare un identificatore per le classi di evento e l'identificatore del server di pubblicazione SENS, SENSGUID \_ Publisher. Le sottoscrizioni sono a livello di ogni evento, quindi l'applicazione di sottoscrizione deve specificare anche gli eventi di interesse della classe. Ogni evento corrisponde a un metodo nell'interfaccia corrispondente alla relativa classe di evento.
-   Creare un oggetto sink con un'implementazione per ogni interfaccia gestita. Vedere [**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork), [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)e [**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) per ulteriori informazioni su queste interfacce e sugli eventi supportati in ognuno di essi.

Quando si verifica uno degli eventi monitorati, SENS elabora ogni sottoscrizione con tutti i filtri associati e invia una notifica ai sottoscrittori tramite il sistema di eventi COM+.

 

 



