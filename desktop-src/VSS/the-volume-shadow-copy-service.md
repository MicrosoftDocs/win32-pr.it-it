---
description: Il Servizio Copia Shadow del volume (VSS) fornisce l'infrastruttura di sistema per l'esecuzione di applicazioni VSS in sistemi basati su Windows.
ms.assetid: 237b2729-1e9b-4d0e-9c59-990e047a0360
title: Servizio Copia Shadow del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274e1e561b702dc2e69782fa5e9c2b47e6ea6a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751602"
---
# <a name="the-volume-shadow-copy-service"></a><span data-ttu-id="d8b3c-103">Servizio Copia Shadow del volume</span><span class="sxs-lookup"><span data-stu-id="d8b3c-103">The Volume Shadow Copy Service</span></span>

<span data-ttu-id="d8b3c-104">Il Servizio Copia Shadow del volume (VSS) fornisce l'infrastruttura di sistema per l'esecuzione di applicazioni VSS in sistemi basati su Windows.</span><span class="sxs-lookup"><span data-stu-id="d8b3c-104">The Volume Shadow Copy Service (VSS) provides the system infrastructure for running VSS applications on Windows-based systems.</span></span>

<span data-ttu-id="d8b3c-105">Sebbene in gran parte trasparente per utenti e sviluppatori, VSS esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d8b3c-105">Though largely transparent to user and developer, VSS does the following:</span></span>

-   <span data-ttu-id="d8b3c-106">Coordina le attività di provider, writer e richiedenti nella creazione e nell'uso di copie shadow</span><span class="sxs-lookup"><span data-stu-id="d8b3c-106">Coordinates activities of providers, writers, and requesters in the creation and use of shadow copies</span></span>
-   <span data-ttu-id="d8b3c-107">Fornisce il provider di sistema predefinito</span><span class="sxs-lookup"><span data-stu-id="d8b3c-107">Furnishes the default system provider</span></span>
-   <span data-ttu-id="d8b3c-108">Implementa la funzionalità di driver di basso livello necessaria per il funzionamento di qualsiasi provider</span><span class="sxs-lookup"><span data-stu-id="d8b3c-108">Implements low-level driver functionality necessary for any provider to work</span></span>

<span data-ttu-id="d8b3c-109">Il Servizio viene avviato on demand, quindi, perché le operazioni del Servizio Copia Shadow del volume abbiano esito positivo, questo servizio deve essere abilitato.</span><span class="sxs-lookup"><span data-stu-id="d8b3c-109">The VSS service starts on demand; therefore, for VSS operations to be successful, this service must be enabled.</span></span>

 

 



