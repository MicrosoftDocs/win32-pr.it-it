---
description: La nozione di blocco in un ambiente Windows è stata storicamente molto importante.
ms.assetid: bd2ede96-34a4-4912-b9d2-ef11d37d2292
title: Operazioni di blocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8040865b4c6ededab925279e15d67cb89f7bc6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307039"
---
# <a name="blocking-operations"></a><span data-ttu-id="67493-103">Operazioni di blocco</span><span class="sxs-lookup"><span data-stu-id="67493-103">Blocking Operations</span></span>

<span data-ttu-id="67493-104">La nozione di blocco in un ambiente Windows è stata storicamente molto importante.</span><span class="sxs-lookup"><span data-stu-id="67493-104">The notion of blocking in a Windows environment has historically been a very important one.</span></span> <span data-ttu-id="67493-105">Negli ambienti Windows Sockets 1,1, le chiamate di blocco erano sconsigliate poiché tendevano a disabilitare l'interazione continuativa con il sistema.</span><span class="sxs-lookup"><span data-stu-id="67493-105">In Windows Sockets 1.1 environments, blocking calls were discouraged since they tended to disable ongoing interaction with the system.</span></span> <span data-ttu-id="67493-106">Inoltre, utilizzano una tecnica pseudoblocking che, per diversi motivi, non sempre funziona come previsto.</span><span class="sxs-lookup"><span data-stu-id="67493-106">Additionally, they employ a pseudoblocking technique which, for a variety of reasons, does not always work as intended.</span></span> <span data-ttu-id="67493-107">Tuttavia, negli ambienti Windows preventivamente pianificati, le chiamate di blocco sono molto più sensate, possono essere implementate dai servizi del sistema operativo nativo e sono in realtà un meccanismo preferenziale.</span><span class="sxs-lookup"><span data-stu-id="67493-107">However, in preemptively scheduled Windows environments, blocking calls make much more sense, can be implemented by native operating system services, and are in fact a generally preferred mechanism.</span></span> <span data-ttu-id="67493-108">L'API Winsock 2 non supporta più psuedoblocking, ma poiché gli shim di compatibilità di Windows Sockets 1,1 devono continuare a emulare questo comportamento, i provider di servizi devono supportare questo comportamento come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="67493-108">The Winsock 2 API no longer supports psuedoblocking, but because the Windows Sockets 1.1 compatibility shims must continue to emulate this behavior, service providers must support this as described in the following.</span></span>

 

 



