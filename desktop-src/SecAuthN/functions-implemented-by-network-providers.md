---
description: Le funzioni seguenti sono implementate da una DLL del provider di rete per comunicare con il router multi-provider (MPR).
ms.assetid: ebdaec3d-6335-4bdf-b150-91e538068f2b
title: Funzioni implementate dai provider di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8122d8e06e92f66958f597c8fbe26f8e1c7abdd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968300"
---
# <a name="functions-implemented-by-network-providers"></a><span data-ttu-id="e282f-103">Funzioni implementate dai provider di rete</span><span class="sxs-lookup"><span data-stu-id="e282f-103">Functions Implemented by Network Providers</span></span>

<span data-ttu-id="e282f-104">Le funzioni seguenti sono implementate da una DLL del provider di rete per comunicare con il [*router multi-provider*](/windows/desktop/SecGloss/m-gly) (MPR).</span><span class="sxs-lookup"><span data-stu-id="e282f-104">The following functions are implemented by a network provider DLL to communicate with the [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR).</span></span> <span data-ttu-id="e282f-105">Si noti che solo le [funzioni delle funzionalità](capabilities-functions.md) devono essere implementate da un provider di rete.</span><span class="sxs-lookup"><span data-stu-id="e282f-105">Note that only the [Capabilities Functions](capabilities-functions.md) must be implemented by a network provider.</span></span> <span data-ttu-id="e282f-106">L'implementazione degli altri tipi di funzioni è facoltativa e dipende dai requisiti del provider di rete.</span><span class="sxs-lookup"><span data-stu-id="e282f-106">Implementation of the other types of functions is optional and depends on the requirements of the network provider.</span></span>



| <span data-ttu-id="e282f-107">Set di funzioni</span><span class="sxs-lookup"><span data-stu-id="e282f-107">Function set</span></span>                                                                                    | <span data-ttu-id="e282f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e282f-108">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e282f-109">Funzioni funzionalità</span><span class="sxs-lookup"><span data-stu-id="e282f-109">Capabilities Functions</span></span>](capabilities-functions.md)<br/>                                 | <span data-ttu-id="e282f-110">Consente al chiamante di determinare le funzionalità del provider di rete.</span><span class="sxs-lookup"><span data-stu-id="e282f-110">Allows the caller to determine the capabilities of the network provider.</span></span><br/>                                                                |
| [<span data-ttu-id="e282f-111">Funzioni nome utente</span><span class="sxs-lookup"><span data-stu-id="e282f-111">User Name Functions</span></span>](user-name-functions.md)<br/>                                       | <span data-ttu-id="e282f-112">Richiede al provider di rete il nome utente associato a una connessione.</span><span class="sxs-lookup"><span data-stu-id="e282f-112">Prompts the network provider for the user name associated with a connection.</span></span><br/>                                                            |
| [<span data-ttu-id="e282f-113">Funzioni di reindirizzamento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="e282f-113">Device-Redirecting Functions</span></span>](device-redirecting-functions.md)<br/>                     | <span data-ttu-id="e282f-114">Consente a un provider di rete di reindirizzare i dispositivi, le lettere di unità e le porte LPT standard nel sistema operativo Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="e282f-114">Allows a network provider to redirect devices, drive letters, and LPT ports that are standard on the Microsoft MS-DOS operating system.</span></span><br/> |
| [<span data-ttu-id="e282f-115">Funzioni della finestra di dialogo specifiche del provider</span><span class="sxs-lookup"><span data-stu-id="e282f-115">Provider-Specific Dialog Box Functions</span></span>](provider-specific-dialog-box-functions.md)<br/> | <span data-ttu-id="e282f-116">Consente a un provider di rete di visualizzare o agire su informazioni specifiche della rete.</span><span class="sxs-lookup"><span data-stu-id="e282f-116">Allows a network provider to display or act on network-specific information.</span></span><br/>                                                            |
| [<span data-ttu-id="e282f-117">Funzioni amministrative</span><span class="sxs-lookup"><span data-stu-id="e282f-117">Administrative Functions</span></span>](administrative-functions.md)<br/>                             | <span data-ttu-id="e282f-118">Consente a un provider di rete di visualizzare o agire su directory di rete speciali.</span><span class="sxs-lookup"><span data-stu-id="e282f-118">Allows a network provider to display or act on special network directories.</span></span><br/>                                                             |
| [<span data-ttu-id="e282f-119">Funzioni di enumerazione</span><span class="sxs-lookup"><span data-stu-id="e282f-119">Enumeration Functions</span></span>](enumeration-functions.md)<br/>                                   | <span data-ttu-id="e282f-120">Consente all'utente di accedere alle risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="e282f-120">Allows the user to browse network resources.</span></span><br/>                                                                                            |



 

<span data-ttu-id="e282f-121">Per ulteriori informazioni su come creare e registrare un provider di rete, vedere [implementazione di un provider di rete](implementing-a-network-provider.md) e [registrazione di provider di rete e gestione credenziali](registering-network-providers-and-credential-managers.md).</span><span class="sxs-lookup"><span data-stu-id="e282f-121">For more information about how to create and register a network provider, see [Implementing a Network Provider](implementing-a-network-provider.md) and [Registering Network Providers and Credential Managers](registering-network-providers-and-credential-managers.md).</span></span>

 

