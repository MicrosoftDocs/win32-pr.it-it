---
description: I certificati possono essere richiesti e distribuiti tramite qualsiasi meccanismo di trasporto.
ms.assetid: 2cbd0cdb-eefa-4434-893d-20e8b34f4cfe
title: Indipendenza del trasporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed8d68b8f6312495c242f6b2bd2ea75301f802c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308648"
---
# <a name="transport-independence"></a><span data-ttu-id="413fb-103">Indipendenza del trasporto</span><span class="sxs-lookup"><span data-stu-id="413fb-103">Transport Independence</span></span>

<span data-ttu-id="413fb-104">I certificati possono essere richiesti e distribuiti tramite qualsiasi meccanismo di trasporto.</span><span class="sxs-lookup"><span data-stu-id="413fb-104">Certificates can be requested and distributed through any transport mechanism.</span></span> <span data-ttu-id="413fb-105">Servizi certificati accetta [*richieste di certificati*](../secgloss/c-gly.md) da un richiedente tramite http, DCOM, RPC, file su disco o trasporto personalizzato.</span><span class="sxs-lookup"><span data-stu-id="413fb-105">Certificate Services accepts [*certificate requests*](../secgloss/c-gly.md) from an applicant through HTTP, DCOM, RPC, disk file, or by custom transport.</span></span> <span data-ttu-id="413fb-106">Servizi certificati invia certificati al richiedente tramite HTTP, DCOM, RPC, file su disco o trasporto personalizzato.</span><span class="sxs-lookup"><span data-stu-id="413fb-106">Certificate Services posts certificates to the applicant through HTTP, DCOM, RPC, disk file, or custom transport.</span></span>

<span data-ttu-id="413fb-107">I trasporti sono supportati dalle applicazioni intermedie e dalle DLL dei moduli di uscita, in genere scritte in C/C++.</span><span class="sxs-lookup"><span data-stu-id="413fb-107">Transports are supported by intermediary applications and exit module DLLs, usually written in C/C++.</span></span> <span data-ttu-id="413fb-108">Le applicazioni intermedie e i moduli di uscita isolano le funzioni di Servizi certificati dalla comunicazione con un trasporto specifico.</span><span class="sxs-lookup"><span data-stu-id="413fb-108">The intermediary applications and exit modules isolate Certificate Services functions from communicating with any specific transport.</span></span>

 

 
