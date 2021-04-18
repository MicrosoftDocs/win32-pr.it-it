---
description: Di seguito sono riportate le funzioni COM+.
ms.assetid: fdeb70ff-17ae-4ee4-a8b1-7fffb65ba2b2
title: Funzioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f7ce33e729a12c37ff1f2dcef516ab13d9b69a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321096"
---
# <a name="com-functions"></a><span data-ttu-id="cce56-103">Funzioni COM+</span><span class="sxs-lookup"><span data-stu-id="cce56-103">COM+ Functions</span></span>

<span data-ttu-id="cce56-104">Di seguito sono riportate le funzioni COM+.</span><span class="sxs-lookup"><span data-stu-id="cce56-104">The following are the COM+ functions.</span></span>



| <span data-ttu-id="cce56-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="cce56-105">Function</span></span>                                                                 | <span data-ttu-id="cce56-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cce56-106">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cce56-107">**CoCreateActivity**</span><span class="sxs-lookup"><span data-stu-id="cce56-107">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)                             | <span data-ttu-id="cce56-108">Crea un'attività per eseguire operazioni batch sincrone e asincrone che possono utilizzare i servizi COM+ senza che sia necessario creare un componente COM+.</span><span class="sxs-lookup"><span data-stu-id="cce56-108">Creates an activity to do synchronous or asynchronous batch work that can use COM+ services without needing to create a COM+ component.</span></span> |
| [<span data-ttu-id="cce56-109">**CoEnterServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="cce56-109">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)                     | <span data-ttu-id="cce56-110">Utilizzato per immettere il codice che può utilizzare i servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="cce56-110">Used to enter code that can then use COM+ services.</span></span>                                                                                     |
| [<span data-ttu-id="cce56-111">**CoGetDefaultContext**</span><span class="sxs-lookup"><span data-stu-id="cce56-111">**CoGetDefaultContext**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetdefaultcontext)                       | <span data-ttu-id="cce56-112">Recupera un riferimento al contesto predefinito dell'Apartment specificato.</span><span class="sxs-lookup"><span data-stu-id="cce56-112">Retrieves a reference to the default context of the specified apartment.</span></span>                                                                |
| [<span data-ttu-id="cce56-113">**CoLeaveServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="cce56-113">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)                     | <span data-ttu-id="cce56-114">Utilizzato per lasciare il codice che utilizza i servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="cce56-114">Used to leave code that uses COM+ services.</span></span>                                                                                             |
| <span data-ttu-id="cce56-115">**ComPlusCompleteCbbSetup**</span><span class="sxs-lookup"><span data-stu-id="cce56-115">**ComPlusCompleteCbbSetup**</span></span>               | <span data-ttu-id="cce56-116">Completa una migrazione del catalogo nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cce56-116">Completes a catalog migration on the destination computer.</span></span>                                                                              |
| <span data-ttu-id="cce56-117">**GetComPlusPackageInstallStatus**</span><span class="sxs-lookup"><span data-stu-id="cce56-117">**GetComPlusPackageInstallStatus**</span></span> | <span data-ttu-id="cce56-118">Indica se è installato Common Language Runtime (CLR) a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="cce56-118">Indicates whether the 64-bit Common Language Runtime (CLR) is installed.</span></span>                                                                |
| [<span data-ttu-id="cce56-119">**GetDispenserManager**</span><span class="sxs-lookup"><span data-stu-id="cce56-119">**GetDispenserManager**</span></span>](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager)                       | <span data-ttu-id="cce56-120">Recupera l'interfaccia [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) del gestore del dispenser.</span><span class="sxs-lookup"><span data-stu-id="cce56-120">Retrieves the dispenser manager's [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) interface.</span></span>                                             |
| [<span data-ttu-id="cce56-121">**GetManagedExtensions**</span><span class="sxs-lookup"><span data-stu-id="cce56-121">**GetManagedExtensions**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-getmanagedextensions)                     | <span data-ttu-id="cce56-122">Determina se la versione installata di COM+ supporta funzionalità speciali fornite per gestire i componenti serviti (oggetti gestiti).</span><span class="sxs-lookup"><span data-stu-id="cce56-122">Determines whether the installed version of COM+ supports special features provided to manage serviced components (managed objects).</span></span>    |
| [<span data-ttu-id="cce56-123">**GetObjectContext**</span><span class="sxs-lookup"><span data-stu-id="cce56-123">**GetObjectContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext)                             | <span data-ttu-id="cce56-124">Recupera un riferimento al contesto associato all'oggetto COM+ corrente.</span><span class="sxs-lookup"><span data-stu-id="cce56-124">Retrieves a reference to the context that is associated with the current COM+ object.</span></span>                                                   |
| [<span data-ttu-id="cce56-125">**MTSCreateActivity**</span><span class="sxs-lookup"><span data-stu-id="cce56-125">**MTSCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-mtscreateactivity)                           | <span data-ttu-id="cce56-126">Crea un'attività in un Apartment a thread singolo per eseguire operazioni batch sincrone o asincrone.</span><span class="sxs-lookup"><span data-stu-id="cce56-126">Creates an activity in a single-threaded apartment to do synchronous or asynchronous batch work.</span></span>                                        |
| [<span data-ttu-id="cce56-127">**RecycleSurrogate**</span><span class="sxs-lookup"><span data-stu-id="cce56-127">**RecycleSurrogate**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-recyclesurrogate)                             | <span data-ttu-id="cce56-128">Ricicla il processo chiamante.</span><span class="sxs-lookup"><span data-stu-id="cce56-128">Recycles the calling process.</span></span>                                                                                                           |
| [<span data-ttu-id="cce56-129">**SafeRef**</span><span class="sxs-lookup"><span data-stu-id="cce56-129">**SafeRef**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef)                                               | <span data-ttu-id="cce56-130">Obsoleto Non usare.</span><span class="sxs-lookup"><span data-stu-id="cce56-130">Obsolete; do not use.</span></span>                                                                                                                   |



 

 

 



