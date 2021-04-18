---
title: Informazioni sull'API host del dispositivo
description: L'API host del dispositivo con tecnologia UPnP è un Framework per l'implementazione della funzionalità dei dispositivi basati su UPnP sulla piattaforma Windows.
ms.assetid: fa716c59-d3f0-4cd4-b92d-939b258b0102
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c751328696d6524208dc95a0b7961829f8ee231c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396655"
---
# <a name="about-the-device-host-api"></a><span data-ttu-id="768e7-103">Informazioni sull'API host del dispositivo</span><span class="sxs-lookup"><span data-stu-id="768e7-103">About the Device Host API</span></span>

<span data-ttu-id="768e7-104">L'API host del dispositivo con tecnologia UPnP è un Framework per l'implementazione della funzionalità dei dispositivi basati su UPnP sulla piattaforma Windows.</span><span class="sxs-lookup"><span data-stu-id="768e7-104">The Device Host API with UPnP technology is a framework for implementing UPnP-based device functionality on the Windows platform.</span></span> <span data-ttu-id="768e7-105">Gli sviluppatori che creano dispositivi usando l'API host del dispositivo con la tecnologia UPnP (detti [*dispositivi ospitati*](h-gly.md)) devono implementare solo le funzionalità di base del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="768e7-105">Developers who are creating devices by using the Device Host API with UPnP technology (referred to as [*hosted devices*](h-gly.md)) need only implement the device's core functionality.</span></span> <span data-ttu-id="768e7-106">Gli sviluppatori possono affidarsi all'host del dispositivo per gestire i dettagli specifici di UPnP di individuazione, descrizione, controllo, eventi e presentazione.</span><span class="sxs-lookup"><span data-stu-id="768e7-106">Developers can rely on the device host to handle the UPnP-specific details of discovery, description, control, eventing, and presentation.</span></span> <span data-ttu-id="768e7-107">L'host del dispositivo convalida i dati in arrivo dai client basati su UPnP e formatta tutti i dati in uscita dai dispositivi ospitati in base all'architettura del dispositivo UPnP.</span><span class="sxs-lookup"><span data-stu-id="768e7-107">The device host validates incoming data from UPnP-based clients and formats all outgoing data from hosted devices according to the UPnP device architecture.</span></span>

<span data-ttu-id="768e7-108">Le sezioni seguenti illustrano, in generale, il funzionamento dell'host del dispositivo UPnP:</span><span class="sxs-lookup"><span data-stu-id="768e7-108">The following sections explain, in general, how the UPnP device host works:</span></span>

-   [<span data-ttu-id="768e7-109">Implementazione di un dispositivo ospitato</span><span class="sxs-lookup"><span data-stu-id="768e7-109">Implementing a Hosted Device</span></span>](implementing-a-hosted-device.md)
-   [<span data-ttu-id="768e7-110">Registrazione di un dispositivo ospitato con l'host del dispositivo</span><span class="sxs-lookup"><span data-stu-id="768e7-110">Registering a Hosted Device with the Device Host</span></span>](registering-a-hosted-device-with-the-device-host.md)
-   [<span data-ttu-id="768e7-111">Provider di dispositivi</span><span class="sxs-lookup"><span data-stu-id="768e7-111">Device Providers</span></span>](device-providers.md)
-   [<span data-ttu-id="768e7-112">Gestione eventi</span><span class="sxs-lookup"><span data-stu-id="768e7-112">Eventing</span></span>](eventing.md)
-   [<span data-ttu-id="768e7-113">Presentazione</span><span class="sxs-lookup"><span data-stu-id="768e7-113">Presentation</span></span>](presentation.md)

 

 




