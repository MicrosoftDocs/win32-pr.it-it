---
title: Implementazione di un provider di dispositivi
description: Per implementare un provider di dispositivi, creare un oggetto che espone l'interfaccia IUPnPDeviceProvider.
ms.assetid: 3ba1200d-68d4-4f03-805c-7fff2d76b16f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb8cd2bea433b884bf6ddf3828fb148c726cd867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471726"
---
# <a name="implementing-a-device-provider"></a><span data-ttu-id="ca809-103">Implementazione di un provider di dispositivi</span><span class="sxs-lookup"><span data-stu-id="ca809-103">Implementing a Device Provider</span></span>

<span data-ttu-id="ca809-104">Per implementare un provider di dispositivi, creare un oggetto che espone l'interfaccia [**IUPnPDeviceProvider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) .</span><span class="sxs-lookup"><span data-stu-id="ca809-104">To implement a device provider, create an object that exposes the [**IUPnPDeviceProvider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) interface.</span></span> <span data-ttu-id="ca809-105">Questo oggetto deve essere registrato con l'host del dispositivo usando il metodo [**IUPnPRegistrar:: RegisterDeviceProvider**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) .</span><span class="sxs-lookup"><span data-stu-id="ca809-105">This object must be registered with the device host using the [**IUPnPRegistrar::RegisterDeviceProvider**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) method.</span></span> <span data-ttu-id="ca809-106">Questo metodo accetta i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="ca809-106">This method takes the following parameters:</span></span>

-   <span data-ttu-id="ca809-107">Nome del provider, che deve essere univoco nel computer.</span><span class="sxs-lookup"><span data-stu-id="ca809-107">The name of the provider, which must be unique on the computer.</span></span>
-   <span data-ttu-id="ca809-108">ProgID della classe che implementa il provider del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca809-108">The ProgID of the class that implements the device provider.</span></span>
-   <span data-ttu-id="ca809-109">Stringa di inizializzazione che viene passata al provider di dispositivi quando viene avviata.</span><span class="sxs-lookup"><span data-stu-id="ca809-109">An initialization string that is passed to the device provider when it is started.</span></span>
-   <span data-ttu-id="ca809-110">ID del contenitore.</span><span class="sxs-lookup"><span data-stu-id="ca809-110">A container ID.</span></span> <span data-ttu-id="ca809-111">Un ID contenitore è una stringa che identifica il gruppo a cui appartiene il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca809-111">A container ID is a string that identifies the group to which the device belongs.</span></span> <span data-ttu-id="ca809-112">Tutti i dispositivi con lo stesso identificatore del contenitore sono ospitati nello stesso processo.</span><span class="sxs-lookup"><span data-stu-id="ca809-112">All devices with the same container identifier are hosted in the same process.</span></span>

 

 




