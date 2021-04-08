---
description: Le applicazioni possono restare in ascolto di eventi di sistema utilizzando l'oggetto InkCollector e in ascolto dell'evento SystemGesture.
ms.assetid: 141afdbe-b5a7-47dc-b505-46089a5eda75
title: Ascolto degli eventi di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1429e652140cc9624d324401edef7817dad40ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058284"
---
# <a name="listening-to-system-events"></a><span data-ttu-id="48cab-103">Ascolto degli eventi di sistema</span><span class="sxs-lookup"><span data-stu-id="48cab-103">Listening to System Events</span></span>

<span data-ttu-id="48cab-104">Le applicazioni possono restare in ascolto di eventi di sistema utilizzando l'oggetto [**InkCollector**](inkcollector-class.md) e in ascolto dell'evento [**SystemGesture**](inkcollector-systemgesture.md) .</span><span class="sxs-lookup"><span data-stu-id="48cab-104">Applications can listen to system events by using the [**InkCollector**](inkcollector-class.md) object and listening for the [**SystemGesture**](inkcollector-systemgesture.md) event on it.</span></span> <span data-ttu-id="48cab-105">È possibile impostare gli eventi a cui un'applicazione è in ascolto.</span><span class="sxs-lookup"><span data-stu-id="48cab-105">You can set which events an application listens to.</span></span> <span data-ttu-id="48cab-106">Quando si verifica un'azione della penna del tablet, l'evento **SystemGesture** corrispondente viene inviato all'applicazione nell'oggetto **InkCollector** .</span><span class="sxs-lookup"><span data-stu-id="48cab-106">When a tablet pen action occurs, the corresponding **SystemGesture** event is sent to the application on its **InkCollector** object.</span></span> <span data-ttu-id="48cab-107">Un'applicazione può annullare il messaggio del mouse corrispondente a un evento **SystemGesture** specificato quando riceve l'evento.</span><span class="sxs-lookup"><span data-stu-id="48cab-107">An application can cancel the mouse message that corresponds to a given **SystemGesture** event when it receives the event.</span></span> <span data-ttu-id="48cab-108">Per informazioni dettagliate sull'annullamento dei messaggi del mouse, vedere evento **SystemGesture** .</span><span class="sxs-lookup"><span data-stu-id="48cab-108">For details about canceling mouse messages, see **SystemGesture** event.</span></span>

 

 



