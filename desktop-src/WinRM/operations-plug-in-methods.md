---
title: Metodi del plug-in per le operazioni
description: Metodi del plug-in per le operazioni
ms.assetid: 81fe751f-51fd-4da6-b44a-0af9007eea9a
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff64a53c4c63b9e552efe90ac057b8a31d603b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955046"
---
# <a name="operations-plug-in-methods"></a><span data-ttu-id="f770a-103">Metodi del plug-in per le operazioni</span><span class="sxs-lookup"><span data-stu-id="f770a-103">Operations Plug-in Methods</span></span>

<span data-ttu-id="f770a-104">Tutti i punti di ingresso del plug-in per le operazioni hanno un meccanismo di callback per segnalare l'esito positivo o negativo della chiamata.</span><span class="sxs-lookup"><span data-stu-id="f770a-104">All operations plug-in entry points have a callback mechanism to report the success or failure of the call.</span></span> <span data-ttu-id="f770a-105">Alcuni meccanismi di callback vengono chiamati più volte, fino a quando non vengono restituiti tutti i risultati.</span><span class="sxs-lookup"><span data-stu-id="f770a-105">Some callback mechanisms are called multiple times, until all of the results are reported.</span></span>

<span data-ttu-id="f770a-106">Nella tabella seguente viene fornita una panoramica dei metodi di callback delle operazioni.</span><span class="sxs-lookup"><span data-stu-id="f770a-106">The following table provides an overview of the operations callback methods.</span></span>



| <span data-ttu-id="f770a-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="f770a-107">Method</span></span>                                                                         | <span data-ttu-id="f770a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f770a-108">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f770a-109">**WSManPluginFreeRequestDetails**</span><span class="sxs-lookup"><span data-stu-id="f770a-109">**WSManPluginFreeRequestDetails**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginfreerequestdetails)         | <span data-ttu-id="f770a-110">Rilascia la memoria allocata per la struttura della [**\_ \_ richiesta del plug**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) -in WSMan.</span><span class="sxs-lookup"><span data-stu-id="f770a-110">Releases memory that is allocated for the [**WSMAN\_PLUGIN\_REQUEST**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) structure.</span></span>                                          |
| [<span data-ttu-id="f770a-111">**WSManPluginGetOperationParameters**</span><span class="sxs-lookup"><span data-stu-id="f770a-111">**WSManPluginGetOperationParameters**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanplugingetoperationparameters) | <span data-ttu-id="f770a-112">Ottiene informazioni operative, ad esempio timeout e restrizioni dei dati associate a un'operazione.</span><span class="sxs-lookup"><span data-stu-id="f770a-112">Gets operational information, such as time-outs and data restrictions that are associated with an operation.</span></span>                                         |
| [<span data-ttu-id="f770a-113">**WSManPluginOperationComplete**</span><span class="sxs-lookup"><span data-stu-id="f770a-113">**WSManPluginOperationComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginoperationcomplete)           | <span data-ttu-id="f770a-114">Registra il completamento di un'operazione.</span><span class="sxs-lookup"><span data-stu-id="f770a-114">Records the completion of an operation.</span></span>                                                                                                              |
| [<span data-ttu-id="f770a-115">**WSManPluginReceiveResult**</span><span class="sxs-lookup"><span data-stu-id="f770a-115">**WSManPluginReceiveResult**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreceiveresult)                   | <span data-ttu-id="f770a-116">Segnala i risultati ai plug-in di Gestione remota Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="f770a-116">Reports results to Windows Remote Management (WinRM) plug-ins.</span></span>                                                                                       |
| [<span data-ttu-id="f770a-117">**WSManPluginReportContext**</span><span class="sxs-lookup"><span data-stu-id="f770a-117">**WSManPluginReportContext**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreportcontext)                   | <span data-ttu-id="f770a-118">Segnala la shell e il contesto dei comandi all'infrastruttura WinRM in modo che sia possibile eseguire ulteriori operazioni sulla shell e/o sul comando.</span><span class="sxs-lookup"><span data-stu-id="f770a-118">Reports the shell and command context back to the WinRM infrastructure so that further operations can be performed against the shell and/or command.</span></span> |



 

 

 




