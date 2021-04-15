---
title: Chiusura di un dispositivo
description: Chiusura di un dispositivo
ms.assetid: eef40f23-2c58-4deb-a6f0-3563d9c30d10
keywords:
- Comando MCI_CLOSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824d156baa72ee404f29ae490d4d9816078f4d15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395383"
---
# <a name="closing-a-device"></a><span data-ttu-id="9425c-104">Chiusura di un dispositivo</span><span class="sxs-lookup"><span data-stu-id="9425c-104">Closing a Device</span></span>

<span data-ttu-id="9425c-105">Il comando [**Chiudi**](close.md) ([**MCI \_ Close**](mci-close.md)) rilascia l'accesso a un dispositivo o a un file.</span><span class="sxs-lookup"><span data-stu-id="9425c-105">The [**close**](close.md) ([**MCI\_CLOSE**](mci-close.md)) command releases access to a device or file.</span></span> <span data-ttu-id="9425c-106">MCI libera un dispositivo quando tutte le attività che usano un dispositivo lo hanno chiuso.</span><span class="sxs-lookup"><span data-stu-id="9425c-106">MCI frees a device when all tasks using a device have closed it.</span></span> <span data-ttu-id="9425c-107">Per consentire a MCI di gestire i dispositivi, l'applicazione deve chiudere ogni dispositivo o file al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="9425c-107">To help MCI manage the devices, your application must close each device or file when it is finished using it.</span></span>

<span data-ttu-id="9425c-108">Quando si chiude un dispositivo MCI esterno che usa i propri supporti anziché i file (ad esempio audio CD), il driver lascia il dispositivo alla modalità operativa corrente.</span><span class="sxs-lookup"><span data-stu-id="9425c-108">When you close an external MCI device that uses its own media instead of files (such as CD audio), the driver leaves the device in its current mode of operation.</span></span> <span data-ttu-id="9425c-109">Se quindi si chiude un dispositivo audio CD che esegue, anche se il driver di dispositivo viene rilasciato dalla memoria, il dispositivo audio CD continuerà a funzionare fino a quando non raggiunge la fine del contenuto.</span><span class="sxs-lookup"><span data-stu-id="9425c-109">Thus, if you close a CD audio device that is playing, even though the device driver is released from memory, the CD audio device will continue to play until it reaches the end of its content.</span></span>

> [!Note]  
> <span data-ttu-id="9425c-110">La chiusura di un'applicazione con i dispositivi Open MCI può impedire ad altre applicazioni di utilizzare tali dispositivi fino al riavvio di Windows.</span><span class="sxs-lookup"><span data-stu-id="9425c-110">Closing an application with open MCI devices can prevent other applications from using those devices until Windows is restarted.</span></span>

 

 

 




