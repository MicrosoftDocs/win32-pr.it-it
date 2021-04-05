---
description: Le lampade su un dispositivo telefonico possono essere accese in un'ampia gamma di diverse modalità di illuminazione.
ms.assetid: d8e8ef57-9faa-4122-b99a-3956362cd9d8
title: Lampade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01005c282b7a86b4b8c8ee27348ba4cf8d43db9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058062"
---
# <a name="lamps"></a><span data-ttu-id="1a451-103">Lampade</span><span class="sxs-lookup"><span data-stu-id="1a451-103">Lamps</span></span>

<span data-ttu-id="1a451-104">Le lampade su un dispositivo telefonico possono essere accese in un'ampia gamma di diverse modalità di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="1a451-104">The lamps on a phone device can be lit in a variety of different lighting modes.</span></span> <span data-ttu-id="1a451-105">A differenza dei modelli di suoneria, le modalità Lamp sono più uniformi tra set di telefoni di fornitori diversi.</span><span class="sxs-lookup"><span data-stu-id="1a451-105">Unlike ringing patterns, lamp modes are more uniform across phone sets of different vendors.</span></span> <span data-ttu-id="1a451-106">Un set comune di modalità lampada viene definito dall'API.</span><span class="sxs-lookup"><span data-stu-id="1a451-106">A common set of lamp modes is defined by the API.</span></span> <span data-ttu-id="1a451-107">Una lampada identificata dall'identificatore del pulsante della lampada può essere accesa in una determinata modalità lampada.</span><span class="sxs-lookup"><span data-stu-id="1a451-107">A lamp identified by its lamp-button identifier can be lit in a given lamp mode.</span></span> <span data-ttu-id="1a451-108">È anche possibile eseguire una query su una lampada per la modalità lampada corrente.</span><span class="sxs-lookup"><span data-stu-id="1a451-108">A lamp can also be queried for its current lamp mode.</span></span>

<span data-ttu-id="1a451-109">Le funzioni TAPI usate per le lampade sono [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), che illumina una lampada su un dispositivo telefonico aperto specificato in una determinata modalità di illuminazione LAMP e [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), che restituisce la modalità corrente della lampada specificata.</span><span class="sxs-lookup"><span data-stu-id="1a451-109">The TAPI functions used for lamps are [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), which lights a lamp on a specified open phone device in a given lamp lighting mode, and [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), which returns the current lamp mode of the specified lamp.</span></span>

<span data-ttu-id="1a451-110">Quando viene modificata una lampada di un dispositivo telefonico, all'applicazione viene inviato un messaggio di [**\_ stato telefonico**](phone-state.md) per notificare all'applicazione la modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="1a451-110">When a lamp of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="1a451-111">I parametri di questo messaggio forniscono un'indicazione della modifica.</span><span class="sxs-lookup"><span data-stu-id="1a451-111">Parameters to this message provide an indication of the change.</span></span>

 

 



