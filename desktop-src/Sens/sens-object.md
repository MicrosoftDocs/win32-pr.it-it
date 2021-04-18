---
description: Il servizio di notifica eventi di sistema (SENS) definisce la coclasse SENS come parte della libreria dei tipi SENS.
ms.assetid: b494808c-1116-47ac-8713-0d515b312368
title: Oggetto SENS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d0d5cd857063d6ac224de66610d2604db619d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316626"
---
# <a name="sens-object"></a><span data-ttu-id="ad564-103">Oggetto SENS</span><span class="sxs-lookup"><span data-stu-id="ad564-103">SENS Object</span></span>

<span data-ttu-id="ad564-104">Il servizio di notifica eventi di sistema (SENS) definisce la coclasse SENS come parte della libreria dei tipi SENS.</span><span class="sxs-lookup"><span data-stu-id="ad564-104">The System Event Notification Service (SENS) defines the SENS coclass as part of the SENS type library.</span></span>

## <a name="implementation"></a><span data-ttu-id="ad564-105">Implementazione</span><span class="sxs-lookup"><span data-stu-id="ad564-105">Implementation</span></span>

<span data-ttu-id="ad564-106">L'implementazione dell'oggetto SENS viene fornita dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ad564-106">The SENS object implementation is provided by the operating system.</span></span>

## <a name="creationaccess-functions"></a><span data-ttu-id="ad564-107">Funzioni di creazione/accesso</span><span class="sxs-lookup"><span data-stu-id="ad564-107">Creation/Access Functions</span></span>



| <span data-ttu-id="ad564-108">Funzione</span><span class="sxs-lookup"><span data-stu-id="ad564-108">Function</span></span>                                      | <span data-ttu-id="ad564-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad564-109">Description</span></span>                                             |
|-----------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="ad564-110">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="ad564-110">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) | <span data-ttu-id="ad564-111">Crea un'istanza dell'oggetto SENS utilizzando il relativo CLSID.</span><span class="sxs-lookup"><span data-stu-id="ad564-111">Creates an instance of the SENS object using its CLSID.</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="ad564-112">Interfacce</span><span class="sxs-lookup"><span data-stu-id="ad564-112">Interfaces</span></span>



| <span data-ttu-id="ad564-113">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="ad564-113">Interface</span></span>                            | <span data-ttu-id="ad564-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad564-114">Description</span></span>                                                                                         |
|--------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad564-115">**IsensNetwork**</span><span class="sxs-lookup"><span data-stu-id="ad564-115">**IsensNetwork**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork) | <span data-ttu-id="ad564-116">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ad564-116">Default.</span></span> <span data-ttu-id="ad564-117">Interfaccia in uscita implementata dall'oggetto sink nell'applicazione del Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="ad564-117">Outgoing interface implemented by sink object in subscriber application.</span></span>                   |
| [<span data-ttu-id="ad564-118">**IsensOnNow**</span><span class="sxs-lookup"><span data-stu-id="ad564-118">**IsensOnNow**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)     | <span data-ttu-id="ad564-119">Interfaccia in uscita implementata dall'oggetto sink nell'applicazione del Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="ad564-119">Outgoing interface implemented by sink object in subscriber application.</span></span>                            |
| [<span data-ttu-id="ad564-120">**IsensLogon**</span><span class="sxs-lookup"><span data-stu-id="ad564-120">**IsensLogon**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)     | <span data-ttu-id="ad564-121">Interfaccia in uscita implementata dall'oggetto sink nell'applicazione del Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="ad564-121">Outgoing interface implemented by sink object in subscriber application.</span></span>                            |
| [<span data-ttu-id="ad564-122">**IsensLogon2**</span><span class="sxs-lookup"><span data-stu-id="ad564-122">**IsensLogon2**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2)   | <span data-ttu-id="ad564-123">Interfaccia in uscita implementata dall'oggetto sink nell'applicazione del Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="ad564-123">Outgoing interface implemented by sink object in subscriber application.</span></span> <span data-ttu-id="ad564-124">Disponibile con Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ad564-124">Available with Windows XP.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ad564-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ad564-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad564-126">**ISensLogon**</span><span class="sxs-lookup"><span data-stu-id="ad564-126">**ISensLogon**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)
</dt> <dt>

[<span data-ttu-id="ad564-127">**ISensNetwork**</span><span class="sxs-lookup"><span data-stu-id="ad564-127">**ISensNetwork**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork)
</dt> <dt>

[<span data-ttu-id="ad564-128">**ISensOnNow**</span><span class="sxs-lookup"><span data-stu-id="ad564-128">**ISensOnNow**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)
</dt> <dt>

[<span data-ttu-id="ad564-129">Informazioni sul servizio di notifica eventi di sistema</span><span class="sxs-lookup"><span data-stu-id="ad564-129">About System Event Notification Service</span></span>](about-system-event-notification-service.md)
</dt> </dl>

 

 
