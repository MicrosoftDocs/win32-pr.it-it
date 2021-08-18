---
title: Recupero dello stato di un'operazione di Gestione riavvio
description: Quando molti servizi e applicazioni devono essere arrestati o riavviati, l'operazione di Gestione riavvio può richiedere un lungo periodo di tempo. Il metodo seguente può essere utilizzato per ottenere lo stato dell'operazione corrente.
ms.assetid: 0df9de1f-df37-46a5-8010-6c8b34429376
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f96b7e247bdeb661e29d39cbb64bd8b7aaaa5caf9478bd1f1acc483c1dfbd614
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010189"
---
# <a name="getting-the-status-of-a-restart-manager-operation"></a>Recupero dello stato di un'operazione di Gestione riavvio

Quando molti servizi e applicazioni devono essere arrestati o riavviati, l'operazione di Gestione riavvio può richiedere un lungo periodo di tempo. Il metodo seguente può essere utilizzato per ottenere lo stato dell'operazione corrente.

**Per ottenere lo stato dell'operazione corrente di Gestione riavvio**

1.  Il programma di installazione deve implementare una funzione [**RM \_ WRITE STATUS \_ \_ CALLBACK**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) che determina lo stato delle applicazioni arrestate o riavviate. La funzione può fornire le informazioni all'interfaccia utente o al log.
2.  Il programma di installazione passa il puntatore alla funzione [**RM \_ WRITE STATUS \_ \_ CALLBACK**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) quando chiama la [**funzione RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) o [**RmRestart.**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart)

 

 