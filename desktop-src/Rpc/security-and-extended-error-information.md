---
title: Informazioni sulla sicurezza e sugli errori estesi
description: Le informazioni estese sugli errori offrono dati molto utili per la risoluzione di un problema RPC, ma tali dati sono molti considerati riservati dalle organizzazioni con consapevolezza della sicurezza.
ms.assetid: ca6ef213-e59d-4b4e-ae7e-f5b20d11fd01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b2029b40937dcef0622f6163e5e8f95b7006ade
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713552"
---
# <a name="security-and-extended-error-information"></a><span data-ttu-id="1da40-103">Informazioni sulla sicurezza e sugli errori estesi</span><span class="sxs-lookup"><span data-stu-id="1da40-103">Security and Extended Error Information</span></span>

<span data-ttu-id="1da40-104">Le informazioni estese sugli errori offrono dati molto utili per la risoluzione di un problema RPC, ma tali dati sono molti considerati riservati dalle organizzazioni con consapevolezza della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="1da40-104">Extended error information offers very useful data when troubleshooting an RPC problem, but such data many be considered confidential by security-conscious organizations.</span></span> <span data-ttu-id="1da40-105">In considerazione di questi problemi di sicurezza, le informazioni estese sugli errori sono disattivate per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1da40-105">In consideration of such security issues, extended error information is turned off by default.</span></span>

<span data-ttu-id="1da40-106">Le informazioni estese sugli errori vengono comunque generate quando le informazioni estese sugli errori sono disabilitate, ma le informazioni non vengono mai trasmesse tra i limiti del processo o del computer</span><span class="sxs-lookup"><span data-stu-id="1da40-106">Extended error information is still generated when extended error information is disabled, but the information is never transmitted across process or computer boundaries.</span></span> <span data-ttu-id="1da40-107">Questo approccio consente di usare le informazioni sugli errori per gli strumenti che hanno accesso allo spazio degli indirizzi del processo, ad esempio i debugger.</span><span class="sxs-lookup"><span data-stu-id="1da40-107">This approach enables error information to be used by tools that have access to the process address space, such as debuggers.</span></span> <span data-ttu-id="1da40-108">Se attivata, le informazioni estese sugli errori vengono generate e possono essere inviate attraverso i limiti del processo e del computer.</span><span class="sxs-lookup"><span data-stu-id="1da40-108">When turned on, extended error information is generated and can be sent across process and computer boundaries.</span></span> <span data-ttu-id="1da40-109">Attualmente, le informazioni sugli errori estesi vengono utilizzate per le sequenze di protocollo orientate alla connessione e RPC locale (LRPC).</span><span class="sxs-lookup"><span data-stu-id="1da40-109">Currently, extended error information is used for connection oriented protocol sequences and local RPC (LRPC).</span></span> <span data-ttu-id="1da40-110">È parzialmente implementato per datagrammi.</span><span class="sxs-lookup"><span data-stu-id="1da40-110">It is partially implemented for datagrams.</span></span>

 

 




