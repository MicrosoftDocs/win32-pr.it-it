---
title: Query del dispositivo mixer
description: Query del dispositivo mixer
ms.assetid: 3b453802-954b-4356-9ad5-0f8376b6199d
keywords:
- audio multimediale, query del dispositivo mixer
- audio, query del dispositivo mixer
- mixer audio, query sul dispositivo
- mixer, query del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02acc3d5c7e418d14412c60a2e28e32849497c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046683"
---
# <a name="mixer-device-queries"></a><span data-ttu-id="44e05-107">Query del dispositivo mixer</span><span class="sxs-lookup"><span data-stu-id="44e05-107">Mixer Device Queries</span></span>

<span data-ttu-id="44e05-108">I servizi mixer forniscono funzioni per determinare il numero di dispositivi mixer presenti nel sistema e le funzionalità dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="44e05-108">The mixer services provide functions for determining the number of mixer devices present in the system and the capabilities of the devices.</span></span> <span data-ttu-id="44e05-109">È anche possibile usare una funzione di servizi mixer per determinare l'identificatore del dispositivo per un dispositivo mixer.</span><span class="sxs-lookup"><span data-stu-id="44e05-109">You can also use a mixer services function to determine the device identifier for a mixer device.</span></span>

<span data-ttu-id="44e05-110">È possibile usare la funzione [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) per determinare il numero di dispositivi mixer presenti nel sistema.</span><span class="sxs-lookup"><span data-stu-id="44e05-110">You can use the [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) function to determine how many mixer devices are present in the system.</span></span> <span data-ttu-id="44e05-111">I dispositivi mixer sono identificati da un identificatore di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44e05-111">Mixer devices are identified by a device identifier.</span></span> <span data-ttu-id="44e05-112">Gli identificatori di dispositivo sono determinati in modo implicito dal numero di dispositivi presenti in un determinato sistema.</span><span class="sxs-lookup"><span data-stu-id="44e05-112">Device identifiers are determined implicitly from the number of devices present in a given system.</span></span> <span data-ttu-id="44e05-113">Sono compresi tra zero e uno inferiore al numero di dispositivi presenti.</span><span class="sxs-lookup"><span data-stu-id="44e05-113">They range from zero through one less than the number of devices present.</span></span>

<span data-ttu-id="44e05-114">Prima di usare un dispositivo mixer, è necessario determinarne le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="44e05-114">Before using a mixer device, you must determine its capabilities.</span></span> <span data-ttu-id="44e05-115">Le funzionalità audio possono variare da un computer multimediale a un altro, quindi le applicazioni devono usare un'ampia gamma di hardware audio.</span><span class="sxs-lookup"><span data-stu-id="44e05-115">Audio capabilities can vary from one multimedia computer to another, so applications need to work with a variety of audio hardware.</span></span>

<span data-ttu-id="44e05-116">È possibile usare la funzione [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps) per determinare le funzionalità dei dispositivi mixer.</span><span class="sxs-lookup"><span data-stu-id="44e05-116">You can use the [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps) function to determine the capabilities of mixer devices.</span></span> <span data-ttu-id="44e05-117">Questa funzione riempie una struttura [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps) con informazioni sulle funzionalità di un dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="44e05-117">This function fills a [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps) structure with information about the capabilities of a specified device.</span></span>

<span data-ttu-id="44e05-118">La funzione [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid) recupera l'identificatore del dispositivo mixer audio associato a un handle di dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="44e05-118">The [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid) function retrieves the audio mixer device identifier associated with a specified device handle.</span></span> <span data-ttu-id="44e05-119">Ad esempio, è possibile usare questa funzione per recuperare l'identificatore del dispositivo per un mixer audio e quindi usare l'identificatore del dispositivo per regolare il volume o per visualizzare un altro controllo.</span><span class="sxs-lookup"><span data-stu-id="44e05-119">For example, you could use this function to retrieve the device identifier for an audio mixer and then use the device identifier to adjust the volume or to display another control.</span></span>

 

 