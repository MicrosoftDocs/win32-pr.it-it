---
description: Registrazione e segnalazione errori
ms.assetid: 162ce34b-cc82-40bb-8422-a639152aee25
title: Registrazione e segnalazione errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdc29d32ae26429f2fe23fe88762fabf82185c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305213"
---
# <a name="logging-and-error-reporting"></a><span data-ttu-id="0f48c-103">Registrazione e segnalazione errori</span><span class="sxs-lookup"><span data-stu-id="0f48c-103">Logging and Error Reporting</span></span>

## <a name="log-file"></a><span data-ttu-id="0f48c-104">File di registro</span><span class="sxs-lookup"><span data-stu-id="0f48c-104">Log file</span></span>

<span data-ttu-id="0f48c-105">COMREPL genera un file di log contenente i messaggi di stato e di errore.</span><span class="sxs-lookup"><span data-stu-id="0f48c-105">COMREPL generates a log file containing status and error messages.</span></span> <span data-ttu-id="0f48c-106">Questo file è archiviato nel computer in cui COMREPL è stato avviato in% systemdir% \\ com \\ Replication \\ comrepl. log.</span><span class="sxs-lookup"><span data-stu-id="0f48c-106">This file is stored on the computer where COMREPL was launched in %systemdir%\\com\\replication\\ComRepl.log.</span></span>

<span data-ttu-id="0f48c-107">Questo file di log viene cancellato quando viene avviata una fase di copia.</span><span class="sxs-lookup"><span data-stu-id="0f48c-107">This log file is cleared when a copy phase is started.</span></span> <span data-ttu-id="0f48c-108">L'installazione successiva nelle destinazioni viene aggiunta al file.</span><span class="sxs-lookup"><span data-stu-id="0f48c-108">Subsequent installation on targets will append to the file.</span></span>

## <a name="error-handling"></a><span data-ttu-id="0f48c-109">Gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="0f48c-109">Error handling</span></span>

<span data-ttu-id="0f48c-110">Gli errori sono indicati nel file di log descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="0f48c-110">Errors are noted in the log file described above.</span></span> <span data-ttu-id="0f48c-111">Per informazioni dettagliate sull'errore, vedere il registro eventi nei computer di origine o di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0f48c-111">Detailed error information may also be found in the event log on source or target computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f48c-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0f48c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f48c-113">Gestione dei file</span><span class="sxs-lookup"><span data-stu-id="0f48c-113">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="0f48c-114">Fasi di replica</span><span class="sxs-lookup"><span data-stu-id="0f48c-114">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="0f48c-115">Uso di COMREPL</span><span class="sxs-lookup"><span data-stu-id="0f48c-115">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="0f48c-116">Cosa viene replicato</span><span class="sxs-lookup"><span data-stu-id="0f48c-116">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



