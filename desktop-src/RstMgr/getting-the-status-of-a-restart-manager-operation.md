---
title: Recupero dello stato di un'operazione di gestione riavvio
description: Quando è necessario arrestare o riavviare molti servizi e applicazioni, l'operazione di gestione riavvio può richiedere un periodo di tempo prolungato. Il metodo seguente può essere utilizzato per ottenere lo stato dell'operazione corrente.
ms.assetid: 0df9de1f-df37-46a5-8010-6c8b34429376
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afa5f329a8f21aa625c5c7b61a3e65b2c907bbf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118286"
---
# <a name="getting-the-status-of-a-restart-manager-operation"></a>Recupero dello stato di un'operazione di gestione riavvio

Quando è necessario arrestare o riavviare molti servizi e applicazioni, l'operazione di gestione riavvio può richiedere un periodo di tempo prolungato. Il metodo seguente può essere utilizzato per ottenere lo stato dell'operazione corrente.

**Per ottenere lo stato dell'operazione corrente di gestione riavvio**

1.  Il programma di installazione deve implementare una funzione di [**\_ callback di \_ stato \_ RM Write**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) che determina lo stato delle applicazioni che sono state arrestate o riavviate. La funzione può fornire le informazioni all'interfaccia utente o al log.
2.  Il programma di installazione passa il puntatore alla funzione di [**\_ \_ \_ callback dello stato RM Write**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) quando viene chiamata la funzione [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) o [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) .

 

 