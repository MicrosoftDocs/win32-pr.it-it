---
description: Un singolo telefono potrebbe essere in grado di squillare con diverse modalità di anello.
ms.assetid: c5ddcb3c-183c-4f97-9429-977d5cc32668
title: Anello
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671aac6ead1938ff5b35ecb4996e4bc072a66d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967463"
---
# <a name="ring"></a><span data-ttu-id="d46db-103">Anello</span><span class="sxs-lookup"><span data-stu-id="d46db-103">Ring</span></span>

<span data-ttu-id="d46db-104">Un singolo telefono potrebbe essere in grado di squillare con diverse modalità di anello.</span><span class="sxs-lookup"><span data-stu-id="d46db-104">A single phone may be able to ring with different ring modes.</span></span> <span data-ttu-id="d46db-105">Data la vasta gamma di modalità anello disponibili, le modalità suoneria vengono identificate tramite il numero di modalità anello.</span><span class="sxs-lookup"><span data-stu-id="d46db-105">Given the wide variety of ring modes available, ring modes are identified by means of their ring mode number.</span></span> <span data-ttu-id="d46db-106">Un numero in modalità anello è compreso tra 0 e il numero di modalità suoneria disponibili meno uno.</span><span class="sxs-lookup"><span data-stu-id="d46db-106">A ring mode number ranges from zero to the number of available ring modes minus one.</span></span>

<span data-ttu-id="d46db-107">Le funzioni che un'applicazione utilizzerebbe per controllare le modalità anello di un dispositivo telefonico sono [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), che squilla un dispositivo telefonico aperto in base a una determinata modalità di anello e [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), che restituisce la modalità suoneria corrente di un dispositivo telefonico aperto.</span><span class="sxs-lookup"><span data-stu-id="d46db-107">The functions an application would use to control a phone device's ring modes are [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), which rings an open phone device according to a given ring mode, and [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), which returns the current ring mode of an opened phone device.</span></span>

<span data-ttu-id="d46db-108">Quando la modalità suoneria di un dispositivo telefonico viene modificata, all'applicazione viene inviato un messaggio di [**\_ stato telefonico**](phone-state.md) per notificare all'applicazione la modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="d46db-108">When the ring mode of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="d46db-109">I parametri di questo messaggio forniscono un'indicazione della modifica.</span><span class="sxs-lookup"><span data-stu-id="d46db-109">Parameters to this message provide an indication of the change.</span></span>

 

 



