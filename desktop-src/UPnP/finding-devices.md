---
title: Ricerca di dispositivi
description: L'architettura UPnP è un'architettura di rete dinamica che consente ai dispositivi di aggiungersi e lasciare la rete in qualsiasi momento.
ms.assetid: b89d9ec3-ce1a-4162-bf82-b08a49207d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5b8feebd430252b118353681a90ce4cd683ee7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045179"
---
# <a name="finding-devices"></a><span data-ttu-id="9b69a-103">Ricerca di dispositivi</span><span class="sxs-lookup"><span data-stu-id="9b69a-103">Finding Devices</span></span>

<span data-ttu-id="9b69a-104">L'architettura UPnP è un'architettura di rete dinamica che consente ai dispositivi di aggiungersi e lasciare la rete in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="9b69a-104">The UPnP architecture is a dynamic network architecture that allows devices to join and leave the network at any time.</span></span> <span data-ttu-id="9b69a-105">Grazie a questa architettura dinamica, le applicazioni non possono basarsi su dispositivi specifici basati su UPnP per essere disponibili in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="9b69a-105">Because of this dynamic architecture, applications cannot rely on specific UPnP-based devices to be available at any given time.</span></span> <span data-ttu-id="9b69a-106">Per questo motivo, le applicazioni (o i punti di controllo) cercano la rete per individuare i dispositivi che soddisfano i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="9b69a-106">For this reason, applications (or control points) search the network to find devices that most closely match specified criteria.</span></span> <span data-ttu-id="9b69a-107">Le applicazioni attendono anche che i messaggi di annuncio del dispositivo che indicano la presenza di nuovi dispositivi siano stati aggiunti alla rete.</span><span class="sxs-lookup"><span data-stu-id="9b69a-107">Applications also wait for device advertisement messages that indicate new devices have been added to the network.</span></span>

<span data-ttu-id="9b69a-108">Di seguito sono riportati i criteri di ricerca validi per i dispositivi basati su UPnP:</span><span class="sxs-lookup"><span data-stu-id="9b69a-108">The following are valid search criteria for UPnP-based devices:</span></span>

-   <span data-ttu-id="9b69a-109">Tipo di dispositivo</span><span class="sxs-lookup"><span data-stu-id="9b69a-109">Device type</span></span>
-   <span data-ttu-id="9b69a-110">Tipo di servizio</span><span class="sxs-lookup"><span data-stu-id="9b69a-110">Service type</span></span>
-   <span data-ttu-id="9b69a-111">Nome univoco del dispositivo (UDN)</span><span class="sxs-lookup"><span data-stu-id="9b69a-111">Unique device name (UDN)</span></span>
-   <span data-ttu-id="9b69a-112">Tutti i dispositivi radice</span><span class="sxs-lookup"><span data-stu-id="9b69a-112">All root devices</span></span>

<span data-ttu-id="9b69a-113">Il tipo di dispositivo e le ricerche del tipo di servizio vengono in genere usate per trovare una classe di dispositivi con caratteristiche comuni.</span><span class="sxs-lookup"><span data-stu-id="9b69a-113">The device type and service type searches are typically used to find a class of devices with common characteristics.</span></span> <span data-ttu-id="9b69a-114">La ricerca UDN viene usata per trovare un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="9b69a-114">The UDN search is used to find a specific device.</span></span>

<span data-ttu-id="9b69a-115">Per cercare i dispositivi, un'applicazione deve prima creare un'istanza dell'oggetto di ricerca del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b69a-115">To search for devices, an application must first instantiate the Device Finder object.</span></span> <span data-ttu-id="9b69a-116">Questo oggetto espone l'interfaccia [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) ; i metodi eseguono le ricerche descritte in precedenza.</span><span class="sxs-lookup"><span data-stu-id="9b69a-116">This object exposes the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface; its methods perform the previously described searches.</span></span>

<span data-ttu-id="9b69a-117">Le sezioni seguenti descrivono il processo di ricerca dei dispositivi:</span><span class="sxs-lookup"><span data-stu-id="9b69a-117">The following sections describe the process of finding devices:</span></span>

-   [<span data-ttu-id="9b69a-118">Creazione del dispositivo di ricerca</span><span class="sxs-lookup"><span data-stu-id="9b69a-118">Creating the Device Finder</span></span>](creating-the-device-finder.md)
-   [<span data-ttu-id="9b69a-119">Ricerca asincrona</span><span class="sxs-lookup"><span data-stu-id="9b69a-119">Asynchronous Searching</span></span>](asynchronous-searching.md)
-   [<span data-ttu-id="9b69a-120">Ricerca sincrona</span><span class="sxs-lookup"><span data-stu-id="9b69a-120">Synchronous Searching</span></span>](synchronous-searching.md)
-   [<span data-ttu-id="9b69a-121">Raccolte di dispositivi restituite da ricerche sincrone</span><span class="sxs-lookup"><span data-stu-id="9b69a-121">Device Collections Returned By Synchronous Searches</span></span>](device-collections-returned-by-synchronous-searches.md)

 

 




