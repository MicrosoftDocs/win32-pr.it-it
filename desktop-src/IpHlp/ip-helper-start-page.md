---
description: L'API helper protocollo Internet (helper IP) consente il recupero e la modifica delle impostazioni di configurazione di rete per il computer locale.
ms.assetid: 4896a9f8-0486-4380-bf49-d1c9ef114acc
title: Helper IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d50153e1ad890063f33a473058f6a850a9f171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879090"
---
# <a name="ip-helper"></a><span data-ttu-id="12a66-103">Helper IP</span><span class="sxs-lookup"><span data-stu-id="12a66-103">IP Helper</span></span>

## <a name="purpose"></a><span data-ttu-id="12a66-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="12a66-104">Purpose</span></span>

<span data-ttu-id="12a66-105">L'API helper protocollo Internet (helper IP) consente il recupero e la modifica delle impostazioni di configurazione di rete per il computer locale.</span><span class="sxs-lookup"><span data-stu-id="12a66-105">The Internet Protocol Helper (IP Helper) API enables the retrieval and modification of network configuration settings for the local computer.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="12a66-106">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="12a66-106">Where applicable</span></span>

<span data-ttu-id="12a66-107">L'API helper IP è applicabile in qualsiasi ambiente informatico in cui è utile modificare a livello di codice la rete e la configurazione TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="12a66-107">The IP Helper API is applicable in any computing environment where programmatically manipulating network and TCP/IP configuration is useful.</span></span> <span data-ttu-id="12a66-108">Le applicazioni tipiche includono i protocolli di routing IP e gli agenti Simple Network Management Protocol (SNMP).</span><span class="sxs-lookup"><span data-stu-id="12a66-108">Typical applications include IP routing protocols and Simple Network Management Protocol (SNMP) agents.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="12a66-109">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="12a66-109">Developer audience</span></span>

<span data-ttu-id="12a66-110">L'API helper IP è progettata per l'uso da parte dei programmatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="12a66-110">The IP Helper API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="12a66-111">I programmatori devono inoltre acquisire familiarità con i concetti relativi alla rete Windows e TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="12a66-111">Programmers should also be familiar with Windows networking and TCP/IP networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="12a66-112">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="12a66-112">Run-time requirements</span></span>

<span data-ttu-id="12a66-113">L'API helper IP può essere usata in tutte le piattaforme Windows.</span><span class="sxs-lookup"><span data-stu-id="12a66-113">The IP Helper API can be used on all Windows platforms.</span></span> <span data-ttu-id="12a66-114">Non tutti i sistemi operativi supportano tutte le funzioni.</span><span class="sxs-lookup"><span data-stu-id="12a66-114">Not all operating systems support all functions.</span></span> <span data-ttu-id="12a66-115">Laddove sono presenti alcune implementazioni o funzionalità delle restrizioni della piattaforma Windows Sockets 2, sono chiaramente indicate nella documentazione.</span><span class="sxs-lookup"><span data-stu-id="12a66-115">Where certain implementations or capabilities of Windows Sockets 2 platform restrictions do exist, they are clearly noted in the documentation.</span></span> <span data-ttu-id="12a66-116">Se una funzione helper IP viene chiamata su una piattaforma che non supporta la funzione, \_ viene restituito l'errore non \_ supportato.</span><span class="sxs-lookup"><span data-stu-id="12a66-116">If an IP Helper function is called on a platform that does not support the function, ERROR\_NOT\_SUPPORTED is returned.</span></span> <span data-ttu-id="12a66-117">Per informazioni più specifiche sui sistemi operativi che supportano una particolare funzione, vedere le sezioni requisiti nella documentazione.</span><span class="sxs-lookup"><span data-stu-id="12a66-117">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="12a66-118">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="12a66-118">In this section</span></span>



| <span data-ttu-id="12a66-119">Argomento</span><span class="sxs-lookup"><span data-stu-id="12a66-119">Topic</span></span>                                                              | <span data-ttu-id="12a66-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12a66-120">Description</span></span>                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12a66-121">Novità dell'helper IP</span><span class="sxs-lookup"><span data-stu-id="12a66-121">What's New in IP Helper</span></span>](what-s-new-in-ip-helper.md)<br/>  | <span data-ttu-id="12a66-122">Informazioni sulle nuove funzionalità per l'helper IP.</span><span class="sxs-lookup"><span data-stu-id="12a66-122">Information on new features for IP Helper.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="12a66-123">Informazioni su helper IP</span><span class="sxs-lookup"><span data-stu-id="12a66-123">About IP Helper</span></span>](about-ip-helper.md)<br/>                  | <span data-ttu-id="12a66-124">Informazioni generali sulle funzionalità e le considerazioni sulla programmazione dell'helper IP disponibili per gli sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="12a66-124">General information about IP Helper programming considerations and capabilities available to developers.</span></span><br/>                                                                                               |
| [<span data-ttu-id="12a66-125">Uso dell'helper IP</span><span class="sxs-lookup"><span data-stu-id="12a66-125">Using IP Helper</span></span>](using-ip-helper.md)<br/>                  | <span data-ttu-id="12a66-126">Procedure e tecniche di programmazione utilizzate con l'helper IP.</span><span class="sxs-lookup"><span data-stu-id="12a66-126">Procedures and programming techniques used with IP Helper.</span></span> <span data-ttu-id="12a66-127">Questa sezione include tecniche di programmazione di base per l'helper IP, ad esempio [Introduzione con l'helper IP](getting-started-with-ip-helper.md).</span><span class="sxs-lookup"><span data-stu-id="12a66-127">This section includes basic IP Helper programming techniques, such as [Getting Started With IP Helper](getting-started-with-ip-helper.md).</span></span><br/> |
| [<span data-ttu-id="12a66-128">Riferimento dell'helper IP</span><span class="sxs-lookup"><span data-stu-id="12a66-128">IP Helper reference</span></span>](ip-helper-function-reference.md)<br/> | <span data-ttu-id="12a66-129">Documentazione di riferimento per le funzioni di supporto IP, le strutture e le enumerazioni.</span><span class="sxs-lookup"><span data-stu-id="12a66-129">Reference documentation for the IP Helper functions, structures, and enumerations.</span></span><br/>                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="12a66-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="12a66-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12a66-131">Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="12a66-131">Windows Sockets 2</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="12a66-132">Routing and Remote Access Service</span><span class="sxs-lookup"><span data-stu-id="12a66-132">Routing and Remote Access Service</span></span>](../rras/routing-start-page.md)
</dt> </dl>

 

