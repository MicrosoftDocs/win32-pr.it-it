---
description: L'API del sensore può fornire notifiche degli eventi.
ms.assetid: 2400619c-ee9c-4662-ae57-6d4bc317e730
title: Informazioni sugli eventi dell'API del sensore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e941dca86d5b7ec3aa9922220c1232b10429f60a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884265"
---
# <a name="about-sensor-api-events"></a>Informazioni sugli eventi dell'API del sensore

L'API del sensore può fornire notifiche degli eventi.

Quando si esegue la registrazione per ricevere eventi, tramite [**ISensor:: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) o [**ISensorManager:: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink)è necessario fornire un puntatore a un'interfaccia di callback. È necessario implementare i metodi dell'interfaccia di callback nel codice. L'API del sensore definisce le interfacce di callback seguenti:

-   [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents). Implementare questa interfaccia per ricevere eventi dai sensori. I sensori possono notificare all'applicazione i nuovi dati, le modifiche allo stato del sensore, la disconnessione del sensore e gli eventi personalizzati definiti dal produttore del sensore.
-   [**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents). Implementare questa interfaccia per ricevere eventi da Gestione sensori. Gestione sensori può inviare una notifica all'applicazione quando si connette un sensore e pertanto può essere disponibile per l'utilizzo.

È possibile annullare le notifiche degli eventi chiamando di nuovo [**SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) , questa volta passando un valore **null** tramite il parametro.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso degli eventi dell'API del sensore](using-sensor-api-events.md)
</dt> </dl>

 

 
