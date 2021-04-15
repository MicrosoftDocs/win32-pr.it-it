---
title: Interfaccia utente delle versioni precedenti rimosse per i volumi locali
description: Interfaccia utente delle versioni precedenti rimosse per i volumi locali
ms.assetid: 0BD3D046-EB06-4C9A-952C-306AC99396C6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25d898be8d079ee713e0fa3e508e552b3cd4009
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104474486"
---
# <a name="previous-versions-ui-removed-for-local-volumes"></a><span data-ttu-id="8ba59-103">Interfaccia utente delle versioni precedenti rimosse per i volumi locali</span><span class="sxs-lookup"><span data-stu-id="8ba59-103">Previous versions UI removed for local volumes</span></span>

## <a name="platform"></a><span data-ttu-id="8ba59-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="8ba59-104">Platform</span></span>

<span data-ttu-id="8ba59-105">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="8ba59-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="8ba59-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ba59-106">Description</span></span>

<span data-ttu-id="8ba59-107">Nelle versioni precedenti di Windows gli utenti potevano ripristinare le versioni precedenti dei singoli file dalle "copie shadow" dei volumi locali.</span><span class="sxs-lookup"><span data-stu-id="8ba59-107">Earlier versions of Windows allowed users to restore previous versions of individual files from “shadow copies” of local volumes.</span></span> <span data-ttu-id="8ba59-108">Queste copie shadow vengono create dalla funzionalità "versioni precedenti" tramite il servizio Copia Shadow del volume (VSS).</span><span class="sxs-lookup"><span data-stu-id="8ba59-108">These shadow copies are created by the “Previous Versions” feature through Volume Shadow Copy service (VSS).</span></span> <span data-ttu-id="8ba59-109">In Windows 7, gli utenti possono configurare e pianificare le copie shadow in interfaccia utente di protezione del sistema disponibili tramite le proprietà del sistema.</span><span class="sxs-lookup"><span data-stu-id="8ba59-109">In Windows 7, users could configure and schedule shadow copies in System Protection UI available through System Properties.</span></span>

<span data-ttu-id="8ba59-110">Tuttavia, le versioni precedenti sono state usate raramente e hanno comportato un impatto negativo sulle prestazioni complessive di Windows. di conseguenza la funzionalità è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="8ba59-110">However, Previous Versions were rarely used and negatively impacted the overall Windows performance; as a result the feature was removed.</span></span> <span data-ttu-id="8ba59-111">In Windows 8 queste funzionalità non sono più disponibili:</span><span class="sxs-lookup"><span data-stu-id="8ba59-111">In Windows 8, these features are no longer available:</span></span>

-   <span data-ttu-id="8ba59-112">Possibilità di esplorare, cercare o ripristinare versioni precedenti dei file tramite l'interfaccia utente di versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="8ba59-112">The ability to browse, search or restore previous versions of files through Previous Versions UI</span></span>
-   <span data-ttu-id="8ba59-113">La possibilità di configurare o pianificare versioni precedenti dei file tramite l'interfaccia utente di protezione del sistema</span><span class="sxs-lookup"><span data-stu-id="8ba59-113">The ability to configure or schedule previous versions of files through System Protection UI</span></span>

<span data-ttu-id="8ba59-114">Tuttavia, gli utenti possono comunque utilizzare la scheda versioni precedenti quando si accede a condivisioni file in un server Windows.</span><span class="sxs-lookup"><span data-stu-id="8ba59-114">However, users can still use the Previous Versions tab when accessing file shares on a Windows server.</span></span>

## <a name="manifestation"></a><span data-ttu-id="8ba59-115">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="8ba59-115">Manifestation</span></span>

<span data-ttu-id="8ba59-116">L'opzione versioni precedenti non è più disponibile per i volumi locali nel menu proprietà di Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="8ba59-116">The Previous Versions option is no longer available for local volumes in the Windows Explorer Properties menu.</span></span>

## <a name="solution"></a><span data-ttu-id="8ba59-117">Soluzione</span><span class="sxs-lookup"><span data-stu-id="8ba59-117">Solution</span></span>

<span data-ttu-id="8ba59-118">Gli sviluppatori che hanno la necessità di creare copie shadow dei volumi locali possono comunque eseguire questa operazione chiamando le API VSS nel codice personalizzato.</span><span class="sxs-lookup"><span data-stu-id="8ba59-118">Developers who need to create shadow copies of local volumes can still do so by calling VSS APIs in custom code.</span></span>

 

 




