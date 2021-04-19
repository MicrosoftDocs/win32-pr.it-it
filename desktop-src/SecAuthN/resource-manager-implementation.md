---
description: Resource Manager viene eseguito come servizio attendibile in un singolo processo. Tutte le richieste per l'accesso tramite smart card vengono effettuate al gestore di risorse, che le instrada al lettore che contiene la scheda di destinazione.
ms.assetid: 4a62588a-14d9-43dc-9572-25a9cbcd0efd
title: Implementazione di Gestione risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ec653f999b74bb9851893b11e1fa49120a7bd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311611"
---
# <a name="resource-manager-implementation"></a><span data-ttu-id="e9401-104">Implementazione di Gestione risorse</span><span class="sxs-lookup"><span data-stu-id="e9401-104">Resource Manager Implementation</span></span>

<span data-ttu-id="e9401-105">[*Resource Manager*](../secgloss/r-gly.md) viene eseguito come servizio attendibile in un singolo processo.</span><span class="sxs-lookup"><span data-stu-id="e9401-105">The [*resource manager*](../secgloss/r-gly.md) runs as a trusted service in a single process.</span></span> <span data-ttu-id="e9401-106">Tutte le richieste per l'accesso tramite [*Smart Card*](../secgloss/s-gly.md) vengono effettuate al gestore di risorse, che le instrada al [*lettore*](../secgloss/r-gly.md) che contiene la scheda di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e9401-106">All requests for [*smart card*](../secgloss/s-gly.md) access are made to the resource manager, which routes them to the [*reader*](../secgloss/r-gly.md) that contains the targeted card.</span></span>

<span data-ttu-id="e9401-107">Le smart card vengono spesso utilizzate in combinazione con sicurezza e privacy personali.</span><span class="sxs-lookup"><span data-stu-id="e9401-107">Smart cards are often used in conjunction with security and personal privacy.</span></span> <span data-ttu-id="e9401-108">Laddove possibile, Resource Manager usa i meccanismi di sicurezza esistenti all'interno del sistema operativo sottostante durante l'accesso a un lettore o a una smart card.</span><span class="sxs-lookup"><span data-stu-id="e9401-108">Wherever possible, the resource manager uses the security mechanisms existing within the underlying operating system when accessing a reader or smart card.</span></span>

 

 
