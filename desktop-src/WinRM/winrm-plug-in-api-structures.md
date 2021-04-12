---
title: Strutture API del plug-in WinRM
description: Strutture API del plug-in WinRM
ms.assetid: 745619bc-c7b3-48fa-8212-cb1b5b9ed4db
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685bcf87ef8c634db367db62b3ec1472b50e3b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331279"
---
# <a name="winrm-plug-in-api-structures"></a><span data-ttu-id="7df44-103">Strutture API del plug-in WinRM</span><span class="sxs-lookup"><span data-stu-id="7df44-103">WinRM Plug-in API Structures</span></span>

<span data-ttu-id="7df44-104">Nella tabella seguente viene fornita una panoramica delle strutture nel plug-in di Gestione remota Windows (WinRM) Application Programming Interface (API).</span><span class="sxs-lookup"><span data-stu-id="7df44-104">The following table provides an overview of the structures in the Windows Remote Management (WinRM) plug-in application programming interface (API).</span></span>



| <span data-ttu-id="7df44-105">Struttura</span><span class="sxs-lookup"><span data-stu-id="7df44-105">Structure</span></span>                                                        | <span data-ttu-id="7df44-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7df44-106">Description</span></span>                                                                              |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7df44-107">**\_quota AUTHZ \_ WSMan**</span><span class="sxs-lookup"><span data-stu-id="7df44-107">**WSMAN\_AUTHZ\_QUOTA**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_authz_quota)                 | <span data-ttu-id="7df44-108">Definisce le informazioni sulla quota per ogni singolo utente.</span><span class="sxs-lookup"><span data-stu-id="7df44-108">Defines quota information on a per-user basis.</span></span>                                           |
| [<span data-ttu-id="7df44-109">**\_Dettagli del certificato WSMan \_**</span><span class="sxs-lookup"><span data-stu-id="7df44-109">**WSMAN\_CERTIFICATE\_DETAILS**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_certificate_details) | <span data-ttu-id="7df44-110">Rappresenta i campi all'interno del certificato client.</span><span class="sxs-lookup"><span data-stu-id="7df44-110">Represents the fields within the client certificate.</span></span>                                     |
| [<span data-ttu-id="7df44-111">**\_ \_ set arg del comando WSMan \_**</span><span class="sxs-lookup"><span data-stu-id="7df44-111">**WSMAN\_COMMAND\_ARG\_SET**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_command_arg_set)        | <span data-ttu-id="7df44-112">Rappresenta il set di argomenti passati alla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="7df44-112">Represents the set of arguments that are passed in to the command line.</span></span>                  |
| [<span data-ttu-id="7df44-113">**\_filtro WSMan**</span><span class="sxs-lookup"><span data-stu-id="7df44-113">**WSMAN\_FILTER**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_filter)                            | <span data-ttu-id="7df44-114">Definisce il filtro utilizzato per un'operazione.</span><span class="sxs-lookup"><span data-stu-id="7df44-114">Defines the filtering used for an operation.</span></span>                                             |
| [<span data-ttu-id="7df44-115">**\_frammento WSMan**</span><span class="sxs-lookup"><span data-stu-id="7df44-115">**WSMAN\_FRAGMENT**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_fragment)                        | <span data-ttu-id="7df44-116">Definisce le informazioni sul frammento per un'operazione.</span><span class="sxs-lookup"><span data-stu-id="7df44-116">Defines the fragment information for an operation.</span></span>                                       |
| [<span data-ttu-id="7df44-117">**\_informazioni sull'operazione WSMan \_**</span><span class="sxs-lookup"><span data-stu-id="7df44-117">**WSMAN\_OPERATION\_INFO**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_operation_info)           | <span data-ttu-id="7df44-118">Rappresenta uno specifico endpoint di risorsa per il quale il plug-in deve eseguire la richiesta.</span><span class="sxs-lookup"><span data-stu-id="7df44-118">Represents a specific resource end-point for which the plug-in must perform the request.</span></span> |
| [<span data-ttu-id="7df44-119">**\_richiesta di plug-in WSMan \_**</span><span class="sxs-lookup"><span data-stu-id="7df44-119">**WSMAN\_PLUGIN\_REQUEST**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request)           | <span data-ttu-id="7df44-120">Contiene informazioni sulla richiesta e viene passato a ogni operazione del plug-in.</span><span class="sxs-lookup"><span data-stu-id="7df44-120">Contains information about the request and is passed into every plug-in operation.</span></span>       |
| [<span data-ttu-id="7df44-121">**\_Dettagli mittente \_ WSMan**</span><span class="sxs-lookup"><span data-stu-id="7df44-121">**WSMAN\_SENDER\_DETAILS**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_sender_details)           | <span data-ttu-id="7df44-122">Specifica i dettagli del client per ogni richiesta in ingresso.</span><span class="sxs-lookup"><span data-stu-id="7df44-122">Specifies client details for every inbound request.</span></span>                                      |



 

 

 




