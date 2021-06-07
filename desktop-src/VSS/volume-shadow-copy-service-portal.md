---
description: Eseguire il backup dei volumi mentre le applicazioni in un sistema continuano a scrivere nei volumi. Ridurre al minimo i tempi di inattività dell'applicazione creando rapidamente uno snapshot (copia shadow) di un volume che duplica tutti i dati. Eseguire il backup multivolume.
ms.assetid: 1eca1e3e-fc86-44b5-b3c4-bcee41bc5a43
title: Servizio Copia Shadow del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2159d39f407f7ae5dbde454ab6cf3562307d892c
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443082"
---
# <a name="volume-shadow-copy-service"></a><span data-ttu-id="ff123-105">Servizio Copia Shadow del volume</span><span class="sxs-lookup"><span data-stu-id="ff123-105">Volume Shadow Copy Service</span></span>

## <a name="purpose"></a><span data-ttu-id="ff123-106">Scopo</span><span class="sxs-lookup"><span data-stu-id="ff123-106">Purpose</span></span>

<span data-ttu-id="ff123-107">Il Servizio Copia Shadow del volume (VSS) è un set di interfacce COM che implementa un framework per consentire l'esecuzione di backup dei volumi mentre le applicazioni in un sistema continuano a scrivere nei volumi.</span><span class="sxs-lookup"><span data-stu-id="ff123-107">The Volume Shadow Copy Service (VSS) is a set of COM interfaces that implements a framework to allow volume backups to be performed while applications on a system continue to write to the volumes.</span></span>

<span data-ttu-id="ff123-108">Per un'introduzione a VSS per gli amministratori di sistema, [Servizio Copia Shadow del volume](/windows-server/storage/file-server/volume-shadow-copy-service) nella libreria TechNet.</span><span class="sxs-lookup"><span data-stu-id="ff123-108">For an introduction to VSS for system administrators, see [Volume Shadow Copy Service](/windows-server/storage/file-server/volume-shadow-copy-service) in the TechNet Library.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="ff123-109">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="ff123-109">Run-time requirements</span></span>

<span data-ttu-id="ff123-110">VSS è supportato in Microsoft Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ff123-110">VSS is supported on Microsoft Windows XP and later.</span></span> <span data-ttu-id="ff123-111">Per informazioni sui requisiti di run-time per un particolare elemento di programmazione, vedere la sezione Requisiti della documentazione relativa a tale elemento.</span><span class="sxs-lookup"><span data-stu-id="ff123-111">For information about run-time requirements for a particular programming element, see the Requirements section of the documentation for that element.</span></span>

<span data-ttu-id="ff123-112">Tutte le applicazioni VSS a 32 bit (richiedenti, provider e writer) devono essere eseguite come applicazioni native a 32 bit o a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="ff123-112">All 32-bit VSS applications (requesters, providers, and writers) must run as native 32-bit or 64-bit applications.</span></span> <span data-ttu-id="ff123-113">L'esecuzione in WOW64 non è supportata.</span><span class="sxs-lookup"><span data-stu-id="ff123-113">Running them under WOW64 is not supported.</span></span> <span data-ttu-id="ff123-114">Per altre informazioni, vedere [Configurazioni e restrizioni supportate.](usage-conventions.md)</span><span class="sxs-lookup"><span data-stu-id="ff123-114">For more information, see [Supported Configurations and Restrictions](usage-conventions.md).</span></span>

<span data-ttu-id="ff123-115">**Windows Server 2003 e Windows XP:** L'esecuzione di richiedenti VSS a 32 bit in WOW64 è supportata, ma non per i backup dello stato del sistema.</span><span class="sxs-lookup"><span data-stu-id="ff123-115">**Windows Server 2003 and Windows XP:** Running 32-bit VSS requesters under WOW64 is supported, but not for system-state backups.</span></span> <span data-ttu-id="ff123-116">L'esecuzione di provider e writer VSS a 32 bit in WOW64 non è supportata.</span><span class="sxs-lookup"><span data-stu-id="ff123-116">Running 32-bit VSS providers and writers under WOW64 is not supported.</span></span> <span data-ttu-id="ff123-117">Il supporto per l'esecuzione di richiedenti a 32 bit in WOW64 è stato rimosso in Windows Vista e nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ff123-117">Support for running 32-bit requesters under WOW64 was removed in Windows Vista and subsequent versions.</span></span>

> [!Note]  
> <span data-ttu-id="ff123-118">Una copia shadow creata in Windows Server 2003 R2 o Windows Server 2003 non può essere usata in un computer che esegue Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ff123-118">A shadow copy that was created on Windows Server 2003 R2 or Windows Server 2003 cannot be used on a computer that is running Windows Server 2008 R2 or Windows Server 2008.</span></span> <span data-ttu-id="ff123-119">Una copia shadow creata in Windows Server 2008 R2 o Windows Server 2008 non può essere usata in un computer che esegue Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ff123-119">A shadow copy that was created on Windows Server 2008 R2 or Windows Server 2008 cannot be used on a computer that is running Windows Server 2003.</span></span> <span data-ttu-id="ff123-120">Tuttavia, una copia shadow creata in Windows Server 2008 può essere utilizzata in un computer che esegue Windows Server 2008 R2 e viceversa.</span><span class="sxs-lookup"><span data-stu-id="ff123-120">However, a shadow copy that was created on Windows Server 2008 can be used on a computer that is running Windows Server 2008 R2, and vice versa.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="ff123-121">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="ff123-121">In this section</span></span>



| <span data-ttu-id="ff123-122">Argomento</span><span class="sxs-lookup"><span data-stu-id="ff123-122">Topic</span></span>                                                          | <span data-ttu-id="ff123-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff123-123">Description</span></span>                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff123-124">Panoramica</span><span class="sxs-lookup"><span data-stu-id="ff123-124">Overview</span></span>](volume-shadow-copy-service-overview.md)<br/> | <span data-ttu-id="ff123-125">Descrive il modello a oggetti vss, le strategie di backup e ripristino e come creare provider, richiedenti e writer vss.</span><span class="sxs-lookup"><span data-stu-id="ff123-125">Describes the VSS object model, backup and restore strategies, and how to create VSS providers, requesters, and writers.</span></span><br/> |
| [<span data-ttu-id="ff123-126">Riferimento</span><span class="sxs-lookup"><span data-stu-id="ff123-126">Reference</span></span>](volume-shadow-copy-reference.md)<br/>       | <span data-ttu-id="ff123-127">Descrive le classi, i tipi di dati, le enumerazioni, le funzioni, le interfacce e le strutture vss.</span><span class="sxs-lookup"><span data-stu-id="ff123-127">Describes VSS classes, data types, enumerations, functions, interfaces, and structures.</span></span><br/>                                  |



 

## <a name="additional-resources"></a><span data-ttu-id="ff123-128">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="ff123-128">Additional resources</span></span>



|   <span data-ttu-id="ff123-129">Risorsa</span><span class="sxs-lookup"><span data-stu-id="ff123-129">Resource</span></span>                                 |   <span data-ttu-id="ff123-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff123-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff123-131">Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="ff123-131">Windows Vista and later</span></span>            | <span data-ttu-id="ff123-132">VSS è disponibile in Microsoft Windows Software Development Kit (Windows SDK) (SDK).</span><span class="sxs-lookup"><span data-stu-id="ff123-132">VSS is available in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ff123-133">È possibile installare l'SDK per Windows 7 e Windows Server 2008 R2 [dall'Area download Windows.](https://www.microsoft.com/download/details.aspx?id=8279)</span><span class="sxs-lookup"><span data-stu-id="ff123-133">You can install the SDK for Windows 7 and Windows Server 2008 R2 from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).</span></span> <span data-ttu-id="ff123-134">È anche possibile scaricare la [versione ISO dell'SDK](https://www.microsoft.com/download/details.aspx?id=8442) dall'Area download Windows.</span><span class="sxs-lookup"><span data-stu-id="ff123-134">You can also download the [ISO version](https://www.microsoft.com/download/details.aspx?id=8442) of the SDK from the Windows Download Center.</span></span> <span data-ttu-id="ff123-135">Le versioni precedenti dell'SDK possono essere scaricate dalla [Windows SDK download.](https://msdn.microsoft.com/windows/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff123-135">Previous versions of the SDK can be downloaded from the [Windows SDK Download Page](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span> |
| <span data-ttu-id="ff123-136">Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="ff123-136">Windows Server 2003 and Windows XP</span></span> | <span data-ttu-id="ff123-137">VSS è disponibile in Servizio Copia Shadow del volume 7.2 SDK, che è possibile scaricare [dall'Area download Windows.](https://www.microsoft.com/download/details.aspx?id=23490)</span><span class="sxs-lookup"><span data-stu-id="ff123-137">VSS is available in the Volume Shadow Copy Service 7.2 SDK, which you can download from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=23490).</span></span> <span data-ttu-id="ff123-138">Si noti che i file vssapi.lib a 64 bit nelle directory nella directory Obj di Win2003 possono essere usati per le versioni a \\ 64 bit di Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ff123-138">Note that the 64-bit vssapi.lib files in the directories under the Win2003\\Obj directory can be used for the 64-bit versions of Windows Server 2003 and Windows XP.</span></span>                                                                                                                                                                 |



 

 

 
