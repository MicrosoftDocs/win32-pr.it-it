---
description: Eseguire il backup dei volumi mentre le applicazioni in un sistema continuano a scrivere nei volumi. Ridurre al minimo i tempi di inattività dell'applicazione creando rapidamente uno snapshot (copia shadow) di un volume che duplica tutti i dati. Eseguire il backup multivolume.
ms.assetid: 1eca1e3e-fc86-44b5-b3c4-bcee41bc5a43
title: Servizio Copia Shadow del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438ef32f1cbbc5fc82878486d9ad35b549f4535a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307172"
---
# <a name="volume-shadow-copy-service"></a><span data-ttu-id="a64c6-105">Servizio Copia Shadow del volume</span><span class="sxs-lookup"><span data-stu-id="a64c6-105">Volume Shadow Copy Service</span></span>

## <a name="purpose"></a><span data-ttu-id="a64c6-106">Scopo</span><span class="sxs-lookup"><span data-stu-id="a64c6-106">Purpose</span></span>

<span data-ttu-id="a64c6-107">Il Servizio Copia Shadow del volume (VSS) è un set di interfacce COM che implementa un Framework per consentire l'esecuzione dei backup del volume mentre le applicazioni in un sistema continuano a scrivere nei volumi.</span><span class="sxs-lookup"><span data-stu-id="a64c6-107">The Volume Shadow Copy Service (VSS) is a set of COM interfaces that implements a framework to allow volume backups to be performed while applications on a system continue to write to the volumes.</span></span>

<span data-ttu-id="a64c6-108">Per un'introduzione a VSS per gli amministratori di sistema, vedere [servizio Copia Shadow del volume](/windows-server/storage/file-server/volume-shadow-copy-service) nella libreria TechNet.</span><span class="sxs-lookup"><span data-stu-id="a64c6-108">For an introduction to VSS for system administrators, see [Volume Shadow Copy Service](/windows-server/storage/file-server/volume-shadow-copy-service) in the TechNet Library.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a64c6-109">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="a64c6-109">Run-time requirements</span></span>

<span data-ttu-id="a64c6-110">VSS è supportato in Microsoft Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a64c6-110">VSS is supported on Microsoft Windows XP and later.</span></span> <span data-ttu-id="a64c6-111">Per informazioni sui requisiti della fase di esecuzione per un particolare elemento di programmazione, vedere la sezione requisiti della documentazione relativa a tale elemento.</span><span class="sxs-lookup"><span data-stu-id="a64c6-111">For information about run-time requirements for a particular programming element, see the Requirements section of the documentation for that element.</span></span>

<span data-ttu-id="a64c6-112">Tutte le applicazioni VSS a 32 bit, ovvero i richiedenti, i provider e i writer, devono essere eseguite come applicazioni native a 32 bit o 64 bit.</span><span class="sxs-lookup"><span data-stu-id="a64c6-112">All 32-bit VSS applications (requesters, providers, and writers) must run as native 32-bit or 64-bit applications.</span></span> <span data-ttu-id="a64c6-113">L'esecuzione in WOW64 non è supportata.</span><span class="sxs-lookup"><span data-stu-id="a64c6-113">Running them under WOW64 is not supported.</span></span> <span data-ttu-id="a64c6-114">Per ulteriori informazioni, vedere [configurazioni e restrizioni supportate](usage-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="a64c6-114">For more information, see [Supported Configurations and Restrictions](usage-conventions.md).</span></span>

<span data-ttu-id="a64c6-115">**Windows Server 2003 e Windows XP:** L'esecuzione di richiedenti VSS a 32 bit in WOW64 è supportata, ma non per i backup dello stato del sistema.</span><span class="sxs-lookup"><span data-stu-id="a64c6-115">**Windows Server 2003 and Windows XP:** Running 32-bit VSS requesters under WOW64 is supported, but not for system-state backups.</span></span> <span data-ttu-id="a64c6-116">L'esecuzione di provider e writer VSS a 32 bit in WOW64 non è supportata.</span><span class="sxs-lookup"><span data-stu-id="a64c6-116">Running 32-bit VSS providers and writers under WOW64 is not supported.</span></span> <span data-ttu-id="a64c6-117">Il supporto per l'esecuzione di richiedenti a 32 bit in WOW64 è stato rimosso in Windows Vista e nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a64c6-117">Support for running 32-bit requesters under WOW64 was removed in Windows Vista and subsequent versions.</span></span>

> [!Note]  
> <span data-ttu-id="a64c6-118">Non è possibile usare una copia shadow creata in Windows Server 2003 R2 o Windows Server 2003 in un computer che esegue Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a64c6-118">A shadow copy that was created on Windows Server 2003 R2 or Windows Server 2003 cannot be used on a computer that is running Windows Server 2008 R2 or Windows Server 2008.</span></span> <span data-ttu-id="a64c6-119">Non è possibile usare una copia shadow creata in Windows Server 2008 R2 o Windows Server 2008 in un computer che esegue Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a64c6-119">A shadow copy that was created on Windows Server 2008 R2 or Windows Server 2008 cannot be used on a computer that is running Windows Server 2003.</span></span> <span data-ttu-id="a64c6-120">Tuttavia, una copia shadow creata in Windows Server 2008 può essere usata in un computer che esegue Windows Server 2008 R2 e viceversa.</span><span class="sxs-lookup"><span data-stu-id="a64c6-120">However, a shadow copy that was created on Windows Server 2008 can be used on a computer that is running Windows Server 2008 R2, and vice versa.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="a64c6-121">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="a64c6-121">In this section</span></span>



| <span data-ttu-id="a64c6-122">Argomento</span><span class="sxs-lookup"><span data-stu-id="a64c6-122">Topic</span></span>                                                          | <span data-ttu-id="a64c6-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a64c6-123">Description</span></span>                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a64c6-124">Overview</span><span class="sxs-lookup"><span data-stu-id="a64c6-124">Overview</span></span>](volume-shadow-copy-service-overview.md)<br/> | <span data-ttu-id="a64c6-125">Descrive il modello a oggetti VSS, le strategie di backup e ripristino e come creare provider VSS, richiedenti e writer.</span><span class="sxs-lookup"><span data-stu-id="a64c6-125">Describes the VSS object model, backup and restore strategies, and how to create VSS providers, requesters, and writers.</span></span><br/> |
| [<span data-ttu-id="a64c6-126">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a64c6-126">Reference</span></span>](volume-shadow-copy-reference.md)<br/>       | <span data-ttu-id="a64c6-127">Descrive le classi VSS, i tipi di dati, le enumerazioni, le funzioni, le interfacce e le strutture.</span><span class="sxs-lookup"><span data-stu-id="a64c6-127">Describes VSS classes, data types, enumerations, functions, interfaces, and structures.</span></span><br/>                                  |



 

## <a name="additional-resources"></a><span data-ttu-id="a64c6-128">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="a64c6-128">Additional resources</span></span>



|                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a64c6-129">Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="a64c6-129">Windows Vista and later</span></span>            | <span data-ttu-id="a64c6-130">VSS è disponibile nel Software Development Kit (SDK) di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a64c6-130">VSS is available in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a64c6-131">È possibile installare l'SDK per Windows 7 e Windows Server 2008 R2 dall' [area download di Windows](https://www.microsoft.com/download/details.aspx?id=8279).</span><span class="sxs-lookup"><span data-stu-id="a64c6-131">You can install the SDK for Windows 7 and Windows Server 2008 R2 from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).</span></span> <span data-ttu-id="a64c6-132">È anche possibile scaricare la [versione ISO](https://www.microsoft.com/download/details.aspx?id=8442) dell'SDK dall'area download di Windows.</span><span class="sxs-lookup"><span data-stu-id="a64c6-132">You can also download the [ISO version](https://www.microsoft.com/download/details.aspx?id=8442) of the SDK from the Windows Download Center.</span></span> <span data-ttu-id="a64c6-133">Le versioni precedenti dell'SDK possono essere scaricate dalla [pagina di Download Windows SDK](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a64c6-133">Previous versions of the SDK can be downloaded from the [Windows SDK Download Page](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span> |
| <span data-ttu-id="a64c6-134">Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="a64c6-134">Windows Server 2003 and Windows XP</span></span> | <span data-ttu-id="a64c6-135">VSS è disponibile nell'SDK Servizio Copia Shadow del volume 7,2, che è possibile scaricare dall' [area download di Windows](https://www.microsoft.com/download/details.aspx?id=23490).</span><span class="sxs-lookup"><span data-stu-id="a64c6-135">VSS is available in the Volume Shadow Copy Service 7.2 SDK, which you can download from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=23490).</span></span> <span data-ttu-id="a64c6-136">Si noti che i file vssapi. lib a 64 bit nelle directory sotto la \\ directory Win2003 obj possono essere usati per le versioni a 64 bit di Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a64c6-136">Note that the 64-bit vssapi.lib files in the directories under the Win2003\\Obj directory can be used for the 64-bit versions of Windows Server 2003 and Windows XP.</span></span>                                                                                                                                                                 |



 

 

 
