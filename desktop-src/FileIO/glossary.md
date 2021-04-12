---
description: Terminologia utilizzata per descrivere Transactional NTFS (TxF).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44cb060c-e6a6-48d6-bbcf-d8dc1ae8ceb2
title: Glossario TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee17e9c53b804995e7ef3491b68e963e9311a37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233516"
---
# <a name="txf-glossary"></a><span data-ttu-id="7ecbd-103">Glossario TxF</span><span class="sxs-lookup"><span data-stu-id="7ecbd-103">TxF Glossary</span></span>

<dl> <dt>

<span data-ttu-id="7ecbd-104"><span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**disponibilità**</span><span class="sxs-lookup"><span data-stu-id="7ecbd-104"><span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**availability**</span></span>
</dt> <dd>

<span data-ttu-id="7ecbd-105">La disponibilità indica che un gestore di risorse interrompe le transazioni anche se la coerenza viene interrotta in modo che il sistema possa continuare a eseguire nuove attività.</span><span class="sxs-lookup"><span data-stu-id="7ecbd-105">Availability means that a resource manager will abort transactions even if that would break consistency so that the system can continue to do new work.</span></span> <span data-ttu-id="7ecbd-106">Il gestore di risorse predefinito impone la disponibilità nel volume di sistema.</span><span class="sxs-lookup"><span data-stu-id="7ecbd-106">The default resource manager forces availability on the system volume.</span></span> <span data-ttu-id="7ecbd-107">Se, ad esempio, il log delle transazioni è pieno, non è possibile aggiungere nuovi spazi di log delle transazioni e una transazione precedente che verrebbe interrotta richiede il recapito di un risultato da un gestore di risorse superiore per il completamento di una transazione distribuita, il gestore di risorse non attenderà la gestione transazioni superiore e interromperà la transazione, anche se ciò potrebbe interrompere la coerenza.</span><span class="sxs-lookup"><span data-stu-id="7ecbd-107">For example, if the transaction log is full, new transaction log space cannot be added, and an older transaction that would be aborted requires an outcome to be delivered from a superior resource manager in order for a distributed transaction to complete, the resource manager will not wait for the superior transaction manager and abort that transaction even though that potentially breaks consistency.</span></span>

</dd> <dt>

<span data-ttu-id="7ecbd-108"><span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**coerenza**</span><span class="sxs-lookup"><span data-stu-id="7ecbd-108"><span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**consistency**</span></span>
</dt> <dd>

<span data-ttu-id="7ecbd-109">La coerenza indica che un gestore di risorse non riuscirà a eseguire nuove transazioni se non è in grado di avanzare.</span><span class="sxs-lookup"><span data-stu-id="7ecbd-109">Consistency means that a resource manager will fail new transactions if it cannot make forward progress.</span></span> <span data-ttu-id="7ecbd-110">Se, ad esempio, il log delle transazioni è pieno, non è possibile aggiungere nuovi spazi di log delle transazioni e una transazione meno recente che verrebbe interrotta richiede il recapito di un risultato da un gestore di risorse superiore affinché una transazione distribuita venga completata, il gestore di risorse attenderà tale risultato.</span><span class="sxs-lookup"><span data-stu-id="7ecbd-110">For example, if the transaction log is full, new transaction log space cannot be added, and an older transaction that would be aborted requires an outcome to be delivered from a superior resource manager in order for a distributed transaction to complete, the resource manager will wait for that outcome.</span></span>

</dd> <dt>

<span data-ttu-id="7ecbd-111"><span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**miniversione**</span><span class="sxs-lookup"><span data-stu-id="7ecbd-111"><span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**miniversion**</span></span>
</dt> <dd>

<span data-ttu-id="7ecbd-112">Un miniversione è una versione di un file creato da un writer transazionale durante una transazione.</span><span class="sxs-lookup"><span data-stu-id="7ecbd-112">A miniversion is a version of a file that a transacted writer creates during a transaction.</span></span> <span data-ttu-id="7ecbd-113">Miniversione può essere aperto in un secondo momento nella transazione con accesso in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="7ecbd-113">The miniversion can be opened later in the transaction with read-only access.</span></span>

</dd> <dt>

<span data-ttu-id="7ecbd-114"><span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**lettore sottoposto a transazione**</span><span class="sxs-lookup"><span data-stu-id="7ecbd-114"><span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**transacted reader**</span></span>
</dt> <dd>

<span data-ttu-id="7ecbd-115">Un reader transazionale è un handle di file transazionale aperto con qualsiasi autorizzazione che fa parte di un accesso in lettura generico, ma non fa parte di un accesso in scrittura generico.</span><span class="sxs-lookup"><span data-stu-id="7ecbd-115">A transacted reader is a transacted file handle opened with any permission that is a part of generic read access, but is not part of generic write access.</span></span>

</dd> <dt>

<span data-ttu-id="7ecbd-116"><span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**Writer transazionale**</span><span class="sxs-lookup"><span data-stu-id="7ecbd-116"><span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**transacted writer**</span></span>
</dt> <dd>

<span data-ttu-id="7ecbd-117">Un writer transazionale è un handle di file transazionale aperto con qualsiasi autorizzazione che non fa parte di un accesso in lettura generico, ma fa parte di un accesso in scrittura generico.</span><span class="sxs-lookup"><span data-stu-id="7ecbd-117">A transacted writer is a transacted file handle opened with any permission that is not part of generic read access, but is part of generic write access.</span></span>

</dd> </dl>

 

 



