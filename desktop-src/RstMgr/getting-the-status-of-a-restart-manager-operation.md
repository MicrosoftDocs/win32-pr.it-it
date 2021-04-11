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
# <a name="getting-the-status-of-a-restart-manager-operation"></a><span data-ttu-id="1a2b0-104">Recupero dello stato di un'operazione di gestione riavvio</span><span class="sxs-lookup"><span data-stu-id="1a2b0-104">Getting the Status of a Restart Manager Operation</span></span>

<span data-ttu-id="1a2b0-105">Quando è necessario arrestare o riavviare molti servizi e applicazioni, l'operazione di gestione riavvio può richiedere un periodo di tempo prolungato.</span><span class="sxs-lookup"><span data-stu-id="1a2b0-105">When many applications and services must be shut down or restarted, the Restart Manager operation can take an extended period of time.</span></span> <span data-ttu-id="1a2b0-106">Il metodo seguente può essere utilizzato per ottenere lo stato dell'operazione corrente.</span><span class="sxs-lookup"><span data-stu-id="1a2b0-106">The following method can be used to obtain the status of the current operation.</span></span>

<span data-ttu-id="1a2b0-107">**Per ottenere lo stato dell'operazione corrente di gestione riavvio**</span><span class="sxs-lookup"><span data-stu-id="1a2b0-107">**To get the status of the current Restart Manager operation**</span></span>

1.  <span data-ttu-id="1a2b0-108">Il programma di installazione deve implementare una funzione di [**\_ callback di \_ stato \_ RM Write**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) che determina lo stato delle applicazioni che sono state arrestate o riavviate.</span><span class="sxs-lookup"><span data-stu-id="1a2b0-108">The installer should implement a [**RM\_WRITE\_STATUS\_CALLBACK**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) function that determines the status of the applications that have been shut down or restarted.</span></span> <span data-ttu-id="1a2b0-109">La funzione può fornire le informazioni all'interfaccia utente o al log.</span><span class="sxs-lookup"><span data-stu-id="1a2b0-109">The function can provide the information to the user interface or log.</span></span>
2.  <span data-ttu-id="1a2b0-110">Il programma di installazione passa il puntatore alla funzione di [**\_ \_ \_ callback dello stato RM Write**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) quando viene chiamata la funzione [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) o [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) .</span><span class="sxs-lookup"><span data-stu-id="1a2b0-110">The installer passes the pointer to the [**RM\_WRITE\_STATUS\_CALLBACK**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) function when calling the [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) or [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) function.</span></span>

 

 