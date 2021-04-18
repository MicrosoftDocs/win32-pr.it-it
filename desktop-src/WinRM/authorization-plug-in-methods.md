---
title: Metodi plug-in di autorizzazione
description: Tutti i punti di ingresso del plug-in di autorizzazione hanno un meccanismo di callback per segnalare l'esito positivo o negativo della chiamata. Alcuni meccanismi di callback vengono chiamati più volte fino a quando non vengono restituiti tutti i risultati.
ms.assetid: 6d7c1c54-fab5-431b-b123-eee6fd4dfb92
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9253267b87a30c5cc2781440b0ecd430f244e90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298311"
---
# <a name="authorization-plug-in-methods"></a><span data-ttu-id="594cd-104">Metodi plug-in di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="594cd-104">Authorization Plug-in Methods</span></span>

<span data-ttu-id="594cd-105">Tutti i punti di ingresso del plug-in di autorizzazione hanno un meccanismo di callback per segnalare l'esito positivo o negativo della chiamata.</span><span class="sxs-lookup"><span data-stu-id="594cd-105">All authorization plug-in entry points have a callback mechanism to report the success or failure of the call.</span></span> <span data-ttu-id="594cd-106">Alcuni meccanismi di callback vengono chiamati più volte fino a quando non vengono restituiti tutti i risultati.</span><span class="sxs-lookup"><span data-stu-id="594cd-106">Some callback mechanisms are called multiple times until all of the results are reported.</span></span>

<span data-ttu-id="594cd-107">Nella tabella seguente viene fornita una panoramica dei metodi di callback di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="594cd-107">The following table provides an overview of the authorization callback methods.</span></span>



| <span data-ttu-id="594cd-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="594cd-108">Method</span></span>                                                                           | <span data-ttu-id="594cd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="594cd-109">Description</span></span>                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="594cd-110">**WSManPluginAuthzOperationComplete**</span><span class="sxs-lookup"><span data-stu-id="594cd-110">**WSManPluginAuthzOperationComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete)   | <span data-ttu-id="594cd-111">Segnala un'operazione utente riuscita o non riuscita.</span><span class="sxs-lookup"><span data-stu-id="594cd-111">Reports either a successful or failed user operation.</span></span>                |
| [<span data-ttu-id="594cd-112">**WSManPluginAuthzQueryQuotaComplete**</span><span class="sxs-lookup"><span data-stu-id="594cd-112">**WSManPluginAuthzQueryQuotaComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzqueryquotacomplete) | <span data-ttu-id="594cd-113">Segnala i dettagli della quota rilevanti per l'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="594cd-113">Reports quota details that are relevant for the specified user.</span></span>      |
| [<span data-ttu-id="594cd-114">**WSManPluginAuthzUserComplete**</span><span class="sxs-lookup"><span data-stu-id="594cd-114">**WSManPluginAuthzUserComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete)             | <span data-ttu-id="594cd-115">Segnala un'autorizzazione di connessione utente riuscita o non riuscita.</span><span class="sxs-lookup"><span data-stu-id="594cd-115">Reports either a successful or failed user connection authorization.</span></span> |



 

 

 




