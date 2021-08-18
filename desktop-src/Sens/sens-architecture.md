---
description: Il servizio di notifica degli eventi di sistema funziona con il sistema di eventi COM+.
ms.assetid: c51d1f61-6087-4480-b989-31241829781b
title: Architettura SENS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586ad8ae9c5ec50f4f36c07ed592599cf5e09775bd7f450844c83cc42a4c580f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890410"
---
# <a name="sens-architecture"></a>Architettura SENS

Il servizio di notifica degli eventi di sistema funziona con il sistema di eventi COM+. SENS è un editore di eventi per le classi di eventi monitorati: eventi di rete, accesso ed eventi di alimentazione/batteria. L'applicazione che riceve una notifica è denominata sottoscrittore di eventi.

Quando un'applicazione esegue la sottoscrizione per ricevere notifiche, può anche specificare filtri associati agli eventi sottoscritti. Gli eventi SENS e COM+ usano i filtri per determinare ulteriormente quando l'applicazione deve ricevere una notifica.

Le notifiche sono asincrone, pertanto l'applicazione che riceve la notifica non deve essere attiva quando viene inviata la notifica. Quando un'applicazione sottoscrive la ricezione di notifiche, può specificare se deve essere attivata quando si verifica l'evento o riceve una notifica in un secondo momento quando è attiva.

La sottoscrizione può essere temporanea e valida solo fino a quando l'applicazione non viene arrestata oppure può essere persistente e valida fino a quando l'applicazione non viene rimossa dal sistema.

Un archivio dati com+ Events contiene informazioni sull'editore eventi (SENS), sui sottoscrittori di eventi e sui filtri. SENS predistina anche un'interfaccia in uscita per ogni classe di evento in una libreria dei tipi.



| classe di evento    | GUID                          | Interfaccia    |
|----------------|-------------------------------|--------------|
| Eventi di rete | RETE EVENTCLASS SENSGUID \_ \_ | ISensNetwork |
| Eventi di accesso   | SENSGUID \_ EVENTCLASS \_ LOGON   | ISensLogon   |
| Eventi di alimentazione   | SENSGUID \_ EVENTCLASS \_ ONNOW   | ISensOnNow   |



 

Per ricevere notifiche per uno di questi eventi, l'applicazione deve eseguire due operazioni:

-   Sottoscrivere gli eventi SENS di interesse. Per sottoscrivere un evento, usare **le interfacce IEventSubscription** e **IEventSystem** negli eventi COM+. È necessario fornire un identificatore per le classi di evento e l'identificatore dell'editore SENS, SENSGUID \_ PUBLISHER. Le sottoscrizioni sono a livello di evento, quindi l'applicazione di sottoscrizione deve anche specificare gli eventi all'interno della classe di interesse. Ogni evento corrisponde a un metodo nell'interfaccia corrispondente alla relativa classe di evento.
-   Creare un oggetto sink con un'implementazione per ogni interfaccia gestita. Per altre informazioni su queste interfacce e sugli eventi supportati in ognuna, vedere [**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork), [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)e [**ISensOnNow.**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)

Quando si verifica uno degli eventi monitorati, SENS elabora ogni sottoscrizione con eventuali filtri associati e invia una notifica ai sottoscrittori tramite il sistema di eventi COM+.

 

 



