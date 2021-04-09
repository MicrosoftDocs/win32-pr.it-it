---
description: In questa sezione vengono descritte le funzioni di supporto che è possibile utilizzare per sviluppare monitoraggi personalizzati.
ms.assetid: 2c019183-9823-4e34-bb41-cf35f2731b8f
title: Funzioni di monitoraggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9391927104196e282d4438c0b047e233d61f3619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879498"
---
# <a name="monitor-functions"></a><span data-ttu-id="70f71-103">Funzioni di monitoraggio</span><span class="sxs-lookup"><span data-stu-id="70f71-103">Monitor Functions</span></span>

<span data-ttu-id="70f71-104">In questa sezione vengono descritte le funzioni di supporto che è possibile utilizzare per sviluppare monitoraggi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="70f71-104">This section describes the helper functions you can use to develop custom monitors.</span></span>



| <span data-ttu-id="70f71-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="70f71-105">Function</span></span>                                       | <span data-ttu-id="70f71-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70f71-106">Description</span></span>                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70f71-107">DllGetMonitorObject</span><span class="sxs-lookup"><span data-stu-id="70f71-107">DllGetMonitorObject</span></span>](dllgetmonitorobject.md) | <span data-ttu-id="70f71-108">Crea un'istanza del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="70f71-108">Creates an instance of the monitor.</span></span>                                                                                                                              |
| [<span data-ttu-id="70f71-109">HTMLValueToUnicode</span><span class="sxs-lookup"><span data-stu-id="70f71-109">HTMLValueToUnicode</span></span>](htmlvaluetounicode.md)   | <span data-ttu-id="70f71-110">Converte una \_ stringa di versione HTML CP UTF8 in Unicode.</span><span class="sxs-lookup"><span data-stu-id="70f71-110">Converts an HTML CP\_UTF8 version string to Unicode.</span></span>                                                                                                             |
| [<span data-ttu-id="70f71-111">LoadDWORD</span><span class="sxs-lookup"><span data-stu-id="70f71-111">LoadDWORD</span></span>](loaddword.md)                     | <span data-ttu-id="70f71-112">Carica un **valore DWORD** da una stringa di configurazione HTML.</span><span class="sxs-lookup"><span data-stu-id="70f71-112">Loads a **DWORD** from an HTML configuration string.</span></span>                                                                                                             |
| [<span data-ttu-id="70f71-113">LoadIPAddresses</span><span class="sxs-lookup"><span data-stu-id="70f71-113">LoadIPAddresses</span></span>](loadipaddresses.md)         | <span data-ttu-id="70f71-114">Carica un elenco di indirizzi IP da una stringa di configurazione HTML TEXTAREA.</span><span class="sxs-lookup"><span data-stu-id="70f71-114">Loads an IP address list from an HTML TEXTAREA configuration string.</span></span>                                                                                             |
| [<span data-ttu-id="70f71-115">LoadIPXAddresses</span><span class="sxs-lookup"><span data-stu-id="70f71-115">LoadIPXAddresses</span></span>](loadipxaddresses.md)       | <span data-ttu-id="70f71-116">Carica un elenco di indirizzi IPX da una stringa di configurazione HTML TEXTAREA.</span><span class="sxs-lookup"><span data-stu-id="70f71-116">Loads an IPX address list from an HTML TEXTAREA configuration string.</span></span>                                                                                            |
| [<span data-ttu-id="70f71-117">LoadMACAddresses</span><span class="sxs-lookup"><span data-stu-id="70f71-117">LoadMACAddresses</span></span>](loadmacaddresses.md)       | <span data-ttu-id="70f71-118">Carica un elenco di indirizzi MAC da una stringa di configurazione HTML TEXTAREA.</span><span class="sxs-lookup"><span data-stu-id="70f71-118">Loads a MAC address list from an HTML TEXTAREA configuration string.</span></span>                                                                                             |
| [<span data-ttu-id="70f71-119">LoadStringAddr</span><span class="sxs-lookup"><span data-stu-id="70f71-119">LoadStringAddr</span></span>](loadstringaddr.md)           | <span data-ttu-id="70f71-120">Trasforma una stringa (ad esempio "157.54.32.45") in un indirizzo **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="70f71-120">Transforms a string (such as "157.54.32.45") to a **DWORD** address.</span></span>                                                                                             |
| [<span data-ttu-id="70f71-121">LoadTCHAR</span><span class="sxs-lookup"><span data-stu-id="70f71-121">LoadTCHAR</span></span>](loadtchar.md)                     | <span data-ttu-id="70f71-122">Cerca un nome di variabile richiesto nella stringa di configurazione e alloca spazio sufficiente (usando **HeapAllocMemory**) per archiviare, copiare e restituire l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70f71-122">Searches for a requested variable name in the configuration string, and allocates sufficient space (by using **HeapAllocMemory**) to store, copy, and return it.</span></span> |
| [<span data-ttu-id="70f71-123">OnLoadingDLL</span><span class="sxs-lookup"><span data-stu-id="70f71-123">OnLoadingDLL</span></span>](onloadingdll.md)               | <span data-ttu-id="70f71-124">Indica che il caricamento della DLL è iniziato.</span><span class="sxs-lookup"><span data-stu-id="70f71-124">Indicates that the DLL has begun to load.</span></span> <span data-ttu-id="70f71-125">MCSVC chiama questa funzione quando carica la DLL di monitoraggio per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="70f71-125">The MCSVC calls this function when it first loads the monitor DLL.</span></span>                                                     |



 

 

 



