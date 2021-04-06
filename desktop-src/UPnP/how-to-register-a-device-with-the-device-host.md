---
title: Come registrare un dispositivo con l'host del dispositivo
description: È possibile registrare un dispositivo in esecuzione o un dispositivo non in esecuzione.
ms.assetid: 40e30881-d5fb-4cf9-8dd7-0d50d2621d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3be1561d82741ce33e7eb05e63b015d5cb38f52
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044753"
---
# <a name="how-to-register-a-device-with-the-device-host"></a><span data-ttu-id="7c9d3-103">Come registrare un dispositivo con l'host del dispositivo</span><span class="sxs-lookup"><span data-stu-id="7c9d3-103">How to Register a Device with the Device Host</span></span>

<span data-ttu-id="7c9d3-104">È possibile registrare un dispositivo in esecuzione o un dispositivo non in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-104">You can register either a running device or a non-running device.</span></span>

## <a name="registering-a-running-device"></a><span data-ttu-id="7c9d3-105">Registrazione di un dispositivo in esecuzione</span><span class="sxs-lookup"><span data-stu-id="7c9d3-105">Registering a Running Device</span></span>

<span data-ttu-id="7c9d3-106">I dispositivi vengono registrati usando l'interfaccia [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) .</span><span class="sxs-lookup"><span data-stu-id="7c9d3-106">Devices are registered using the [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) interface.</span></span> <span data-ttu-id="7c9d3-107">Solo gli amministratori possono registrare i dispositivi in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-107">Only administrators are allowed to register running devices.</span></span> <span data-ttu-id="7c9d3-108">Per registrare un dispositivo che dispone di un oggetto controllo dispositivo in esecuzione, un'applicazione deve richiamare [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), passando quanto segue:</span><span class="sxs-lookup"><span data-stu-id="7c9d3-108">To register a device that has a running device control object, an application must invoke [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), passing the following:</span></span>

-   <span data-ttu-id="7c9d3-109">Testo della descrizione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-109">The text of the device's description.</span></span>
-   <span data-ttu-id="7c9d3-110">Puntatore **IUnknown** all'oggetto controllo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-110">An **IUnknown** pointer to the device control object.</span></span>
-   <span data-ttu-id="7c9d3-111">Una stringa di inizializzazione che viene passata al metodo [**IUPnPDeviceControl:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) dell'oggetto controllo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-111">An initialization string that is passed to the device control object's [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method.</span></span>
-   <span data-ttu-id="7c9d3-112">Percorso della directory delle risorse.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-112">The location of the resource directory.</span></span>
-   <span data-ttu-id="7c9d3-113">Durata del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-113">The lifetime of the device.</span></span>
-   <span data-ttu-id="7c9d3-114">Il parametro ID dispositivo (un parametro OUT), ovvero il valore restituito di questa chiamata; un puntatore all'ID dispositivo viene restituito in C++.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-114">The Device ID parameter (an OUT parameter), which is the return value of this call; a pointer to the Device ID is returned in C++.</span></span>

## <a name="registering-a-non-running-device"></a><span data-ttu-id="7c9d3-115">Registrazione di un dispositivo non in esecuzione</span><span class="sxs-lookup"><span data-stu-id="7c9d3-115">Registering a Non-Running Device</span></span>

<span data-ttu-id="7c9d3-116">Per impostazione predefinita, solo gli amministratori e gli utenti interattivi possono registrare dispositivi non in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-116">By default, only administrators and interactive users are allowed to register non-running devices.</span></span> <span data-ttu-id="7c9d3-117">Per registrare un dispositivo con un oggetto controllo dispositivo che non è in esecuzione, l'applicazione usa il metodo [**IUPnPRegistrar:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) .</span><span class="sxs-lookup"><span data-stu-id="7c9d3-117">To register a device with a device control object that is not running, the application uses the [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) method.</span></span>

<span data-ttu-id="7c9d3-118">Per registrare a livello di codice un dispositivo con un oggetto controllo dispositivo non in esecuzione, l'applicazione deve richiamare [**IUPnPRegistrar:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) e passare i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="7c9d3-118">To programmatically register a device with a non-running device control object, the application must invoke [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) and pass it the following parameters:</span></span>

-   <span data-ttu-id="7c9d3-119">Testo della descrizione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-119">The text of the device's description.</span></span>
-   <span data-ttu-id="7c9d3-120">ProgID dell'oggetto controllo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-120">The ProgID of the device control object.</span></span>
-   <span data-ttu-id="7c9d3-121">Una stringa di inizializzazione che viene passata al metodo [**IUPnPDeviceControl:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) dell'oggetto controllo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-121">An initialization string that is passed to the device control object's [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method.</span></span>
-   <span data-ttu-id="7c9d3-122">ID del contenitore.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-122">A container ID.</span></span>
-   <span data-ttu-id="7c9d3-123">Percorso della directory delle risorse.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-123">The location of the resource directory.</span></span>
-   <span data-ttu-id="7c9d3-124">Durata del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-124">The lifetime of the device.</span></span>
-   <span data-ttu-id="7c9d3-125">Il parametro ID dispositivo (un parametro OUT), ovvero il valore restituito di questa chiamata; un puntatore all'ID dispositivo viene restituito in C++.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-125">The Device ID parameter (an OUT parameter), which is the return value of this call; a pointer to the Device ID is returned in C++.</span></span>

<span data-ttu-id="7c9d3-126">Le registrazioni dei dispositivi non in esecuzione possono essere configurate in modo da renderle permanente tra gli avvii del sistema (i dispositivi non vengono pubblicati durante la fase di arresto).</span><span class="sxs-lookup"><span data-stu-id="7c9d3-126">The registrations of non-running devices can be configured to persist across system boots (the devices are unpublished during the shutdown phase).</span></span> <span data-ttu-id="7c9d3-127">Se pertanto sono configurati in questo modo, i dispositivi vengono pubblicati e annunciati ogni volta che il computer viene avviato.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-127">Therefore, if they are configured this way, devices are published and announced every time the computer is booted.</span></span>

 

 




