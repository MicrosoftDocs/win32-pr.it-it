---
description: L'API WiFi nativa contiene funzioni, strutture ed enumerazioni che supportano la connettività di rete wireless e la gestione dei profili wireless.
ms.assetid: 686f9ccf-5040-44c5-8633-83f12dc46586
title: Informazioni sull'API WiFi nativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d4f656145430e34d79e05b88bc2bdeb54fe5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233702"
---
# <a name="about-the-native-wifi-api"></a><span data-ttu-id="969f0-103">Informazioni sull'API WiFi nativa</span><span class="sxs-lookup"><span data-stu-id="969f0-103">About the Native Wifi API</span></span>

<span data-ttu-id="969f0-104">L'API WiFi nativa contiene funzioni, strutture ed enumerazioni che supportano la connettività di rete wireless e la gestione dei profili wireless.</span><span class="sxs-lookup"><span data-stu-id="969f0-104">The Native Wifi API contains functions, structures, and enumerations that support wireless network connectivity and wireless profile management.</span></span> <span data-ttu-id="969f0-105">L'API può essere usata sia per le reti ad hoc che per l'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="969f0-105">The API can be used for both infrastructure and ad hoc networks.</span></span> <span data-ttu-id="969f0-106">L'API ad hoc wireless è un'interfaccia orientata a oggetti semplificata per la creazione, la gestione e l'utilizzo di reti ad hoc.</span><span class="sxs-lookup"><span data-stu-id="969f0-106">The Wireless Ad Hoc API is a simplified object-oriented interface for creating, managing, and using ad hoc networks.</span></span>

> [!Note]  
> <span data-ttu-id="969f0-107">La modalità ad hoc potrebbe non essere disponibile nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="969f0-107">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="969f0-108">A partire da Windows 8.1 e Windows Server 2012 R2, usare invece [Wi-Fi Direct](about-the-wi-fi-direct-api.md) .</span><span class="sxs-lookup"><span data-stu-id="969f0-108">Starting with Windows 8.1 and Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) instead.</span></span>

 

<span data-ttu-id="969f0-109">L'implementazione dell'API ad hoc usa l'API WiFi nativa.</span><span class="sxs-lookup"><span data-stu-id="969f0-109">The implementation of the Ad Hoc API uses the Native Wifi API.</span></span> <span data-ttu-id="969f0-110">Ciò significa che le chiamate API ad hoc possono attivare le notifiche Wi-Fi native e viceversa.</span><span class="sxs-lookup"><span data-stu-id="969f0-110">This means that Ad Hoc API calls can trigger Native Wifi notifications, and vice versa.</span></span>

<span data-ttu-id="969f0-111">La combinazione di chiamate API native Wi-Fi e chiamate API ad hoc wireless non è consigliata.</span><span class="sxs-lookup"><span data-stu-id="969f0-111">Mixing Native Wifi API calls and Wireless Ad Hoc API calls is not recommended.</span></span> <span data-ttu-id="969f0-112">Gli sviluppatori devono scegliere un approccio di programmazione prima di progettare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="969f0-112">Developers should choose a programming approach before designing an application.</span></span> <span data-ttu-id="969f0-113">Se l'applicazione USA o gestisce reti di infrastruttura, è necessario usare l'API WiFi nativa.</span><span class="sxs-lookup"><span data-stu-id="969f0-113">If your application uses or manages infrastructure networks, you should use the Native Wifi API.</span></span> <span data-ttu-id="969f0-114">Se l'applicazione richiede funzionalità di gestione del profilo, è necessario usare l'API WiFi nativa.</span><span class="sxs-lookup"><span data-stu-id="969f0-114">If your application requires profile management functionality, you should use the Native Wifi API.</span></span> <span data-ttu-id="969f0-115">In caso contrario, è consigliabile usare l'API ad hoc wireless.</span><span class="sxs-lookup"><span data-stu-id="969f0-115">Otherwise, you should use the Wireless Ad Hoc API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="969f0-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="969f0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="969f0-117">Informazioni sul Wi-Fi nativo</span><span class="sxs-lookup"><span data-stu-id="969f0-117">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="969f0-118">Supporto per le API WiFi native in Windows XP</span><span class="sxs-lookup"><span data-stu-id="969f0-118">Native Wifi API Support on Windows XP</span></span>](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> <dt>

[<span data-ttu-id="969f0-119">Autorizzazioni API WiFi Native</span><span class="sxs-lookup"><span data-stu-id="969f0-119">Native Wifi API Permissions</span></span>](native-wifi-api-permissions.md)
</dt> <dt>

[<span data-ttu-id="969f0-120">Informazioni sull'API ad hoc wireless</span><span class="sxs-lookup"><span data-stu-id="969f0-120">About the Wireless Ad Hoc API</span></span>](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[<span data-ttu-id="969f0-121">Scarica Windows Vista SDK</span><span class="sxs-lookup"><span data-stu-id="969f0-121">Download the Windows Vista SDK</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)
</dt> </dl>

 

 



