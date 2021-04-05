---
title: API dispositivo software
description: È possibile usare l'API del dispositivo software per creare un dispositivo PnP da un'app.
ms.assetid: 203abb2c-526f-4995-95de-4eb0ecee63d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e011d806ea21310fccc6ca96517a5465cb41add1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729706"
---
# <a name="software-device-api"></a><span data-ttu-id="6df16-103">API dispositivo software</span><span class="sxs-lookup"><span data-stu-id="6df16-103">Software Device API</span></span>

## <a name="purpose"></a><span data-ttu-id="6df16-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="6df16-104">Purpose</span></span>

<span data-ttu-id="6df16-105">È possibile usare l'API del dispositivo software per creare un dispositivo PnP da un'app.</span><span class="sxs-lookup"><span data-stu-id="6df16-105">You can use the Software Device API to create a PnP device from an app.</span></span> <span data-ttu-id="6df16-106">L'API consente di enumerare il dispositivo come figlio di qualsiasi dispositivo padre esistente.</span><span class="sxs-lookup"><span data-stu-id="6df16-106">The API lets you enumerate the device as a child of any existing parent device.</span></span> <span data-ttu-id="6df16-107">L'API consente inoltre di registrare le interfacce del dispositivo sui dispositivi enumerati e impostare le proprietà per i dispositivi e le interfacce.</span><span class="sxs-lookup"><span data-stu-id="6df16-107">The API also lets you register device interfaces against the enumerated devices and set properties for the devices and interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6df16-108">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="6df16-108">In this section</span></span>



| <span data-ttu-id="6df16-109">Argomento</span><span class="sxs-lookup"><span data-stu-id="6df16-109">Topic</span></span>                                                                                         | <span data-ttu-id="6df16-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6df16-110">Description</span></span>                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6df16-111">[Guida alla programmazione dell'API del dispositivo software](/previous-versions/windows/hardware/drivers/dn315034(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6df16-111">[Software Device API Programming Guide](/previous-versions/windows/hardware/drivers/dn315034(v=vs.85))</span></span><br/> | <span data-ttu-id="6df16-112">Questa guida contiene informazioni su come usare l'API del dispositivo software per enumerare i dispositivi PnP.</span><span class="sxs-lookup"><span data-stu-id="6df16-112">This guide contains info on how to use the Software Device API to enumerate PnP devices.</span></span> <br/>                                                                               |
| [<span data-ttu-id="6df16-113">Informazioni di riferimento sulle API dei dispositivi software</span><span class="sxs-lookup"><span data-stu-id="6df16-113">Software Device API Reference</span></span>](software-device-api-reference.md)<br/>                 | <span data-ttu-id="6df16-114">Questo riferimento descrive le funzioni API del dispositivo software che un'app client chiama e una funzione di callback implementata da un'app client e le strutture API del dispositivo software.</span><span class="sxs-lookup"><span data-stu-id="6df16-114">This reference describes Software Device API functions that a client app calls and a callback function that a client app implements and Software Device API structures.</span></span><br/> |



 

## <a name="developer-audience"></a><span data-ttu-id="6df16-115">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="6df16-115">Developer audience</span></span>

<span data-ttu-id="6df16-116">L'API del dispositivo software è progettata per l'uso da parte degli sviluppatori che desiderano pubblicare le funzionalità del dispositivo nella "directory" PnP o caricare un driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6df16-116">The Software Device API is designed for use by developers who want to publish device functionality in the PnP "directory" or to load a device driver.</span></span>

 

 

[<span data-ttu-id="6df16-117">Invia commenti su questo argomento a Microsoft</span><span class="sxs-lookup"><span data-stu-id="6df16-117">Send comments about this topic to Microsoft</span></span>](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bswdevice\swdevice%5D:%20Software%20Device%20API%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Invia commenti su questo argomento a Microsoft")