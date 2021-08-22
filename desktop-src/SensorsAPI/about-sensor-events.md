---
description: L'API Sensor può fornire notifiche degli eventi.
ms.assetid: 2400619c-ee9c-4662-ae57-6d4bc317e730
title: Informazioni sugli eventi dell'API Sensore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4af21bfed2a36c0c79fa46811221afbf2fcf87a4a5f15cf21adfbeaac8601f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003895"
---
# <a name="about-sensor-api-events"></a>Informazioni sugli eventi dell'API Sensore

L'API Sensor può fornire notifiche degli eventi.

Quando si esegue la registrazione per ricevere eventi tramite [**ISensor::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) o [**ISensorManager::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink), è necessario fornire un puntatore a un'interfaccia di callback. È necessario implementare i metodi dell'interfaccia di callback nel codice. L'API Sensor definisce le interfacce di callback seguenti:

-   [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents). Implementare questa interfaccia per ricevere eventi dai sensori. I sensori possono notificare all'applicazione nuovi dati, modifiche dello stato del sensore, disconnessione del sensore ed eventi personalizzati definiti dal produttore del sensore.
-   [**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents). Implementare questa interfaccia per ricevere eventi dal gestore dei sensori. Il gestore dei sensori può inviare una notifica all'applicazione quando un sensore si connette e può quindi essere disponibile per l'uso.

È possibile annullare le notifiche degli eventi chiamando [**nuovamente SetEventSink,**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) questa volta passando un **valore NULL** tramite il parametro .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso degli eventi dell'API Sensor](using-sensor-api-events.md)
</dt> </dl>

 

 
