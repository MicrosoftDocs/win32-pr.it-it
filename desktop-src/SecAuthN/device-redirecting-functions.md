---
description: Le funzioni di reindirizzamento dispositivi rimandano i dispositivi MS-DOS standard, le lettere di unità e le porte LPT. Questo consente alle applicazioni in esecuzione nel sistema di usare i dispositivi e accedere alla rete in modo completamente trasparente.
ms.assetid: a61ab1e6-dad9-4dc0-a908-f8440619f610
title: Funzioni Device-Redirecting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577f8d108b6bfdeb01f786478cd736e6c84cc83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225904"
---
# <a name="device-redirecting-functions"></a><span data-ttu-id="676af-104">Funzioni Device-Redirecting</span><span class="sxs-lookup"><span data-stu-id="676af-104">Device-Redirecting Functions</span></span>

<span data-ttu-id="676af-105">Le funzioni di reindirizzamento dispositivi rimandano i dispositivi MS-DOS standard, le lettere di unità e le porte LPT.</span><span class="sxs-lookup"><span data-stu-id="676af-105">The device-redirecting functions redirect standard MS-DOS devices, drive letters and LPT ports.</span></span> <span data-ttu-id="676af-106">Questo consente alle applicazioni in esecuzione nel sistema di usare i dispositivi e accedere alla rete in modo completamente trasparente.</span><span class="sxs-lookup"><span data-stu-id="676af-106">This enables applications running on the system to use the devices and access the network in a totally transparent manner.</span></span>



| <span data-ttu-id="676af-107">Funzione</span><span class="sxs-lookup"><span data-stu-id="676af-107">Function</span></span>                                                         | <span data-ttu-id="676af-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="676af-108">Description</span></span>                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="676af-109">**NPAddConnection**</span><span class="sxs-lookup"><span data-stu-id="676af-109">**NPAddConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)                       | <span data-ttu-id="676af-110">Reindirizza o connette un dispositivo locale a una risorsa di rete.</span><span class="sxs-lookup"><span data-stu-id="676af-110">Redirects or connects a local device to a network resource.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="676af-111">**NPAddConnection3**</span><span class="sxs-lookup"><span data-stu-id="676af-111">**NPAddConnection3**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npaddconnection3)                     | <span data-ttu-id="676af-112">Esegue la stessa azione di [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection), ma consente all'utente di specificare quale finestra deve essere proprietaria di tutte le finestre di dialogo e il modo in cui deve essere stabilita la connessione.</span><span class="sxs-lookup"><span data-stu-id="676af-112">Performs the same action as [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection), but lets the user specify which window should own any dialog boxes and how the connection should be established.</span></span><br/> |
| [<span data-ttu-id="676af-113">**NPCancelConnection**</span><span class="sxs-lookup"><span data-stu-id="676af-113">**NPCancelConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npcancelconnection)                 | <span data-ttu-id="676af-114">Interrompe una connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="676af-114">Breaks a network connection.</span></span> <span data-ttu-id="676af-115">Le modifiche vengono memorizzate se un dispositivo viene disconnesso a meno che non si tratti di una connessione senza dispositivo.</span><span class="sxs-lookup"><span data-stu-id="676af-115">The changes are remembered if a device is disconnected unless the connection is a deviceless connection.</span></span><br/>                                                    |
| [<span data-ttu-id="676af-116">**NPGetConnection**</span><span class="sxs-lookup"><span data-stu-id="676af-116">**NPGetConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnection)                       | <span data-ttu-id="676af-117">Restituisce informazioni su una connessione.</span><span class="sxs-lookup"><span data-stu-id="676af-117">Returns information about a connection.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="676af-118">**NPGetConnection3**</span><span class="sxs-lookup"><span data-stu-id="676af-118">**NPGetConnection3**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnection3)                     | <span data-ttu-id="676af-119">Restituisce informazioni su una connessione, anche se la connessione è attualmente disconnessa.</span><span class="sxs-lookup"><span data-stu-id="676af-119">Returns information about a connection, even if the connection is currently disconnected.</span></span><br/>                                                                                                |
| [<span data-ttu-id="676af-120">**NPGetConnectionPerformance**</span><span class="sxs-lookup"><span data-stu-id="676af-120">**NPGetConnectionPerformance**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnectionperformance) | <span data-ttu-id="676af-121">Restituisce informazioni sulle prestazioni relative a una connessione.</span><span class="sxs-lookup"><span data-stu-id="676af-121">Returns performance information about a connection.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="676af-122">**NPGetUniversalName**</span><span class="sxs-lookup"><span data-stu-id="676af-122">**NPGetUniversalName**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetuniversalname)                 | <span data-ttu-id="676af-123">Restituisce il nome universale remoto o locale, nel formato specificato durante la chiamata di funzione.</span><span class="sxs-lookup"><span data-stu-id="676af-123">Returns the remote or local universal name, in the format specified during the function call.</span></span><br/>                                                                                            |



 

 

 




