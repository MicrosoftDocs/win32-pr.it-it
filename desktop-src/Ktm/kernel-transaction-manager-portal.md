---
description: Implementare il registro di sistema transazionale NTFS (TxF) e transazionale (TxR). TxF consente operazioni transazionali file system all'interno di NTFS. TxR consente operazioni del registro di sistema transazionali. Coordinare file system e le operazioni del registro di sistema con una transazione.
ms.assetid: 2f601994-db1e-4aac-8db1-9a36c702664b
title: Gestione transazioni kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281050461163d5fd0cde64af79e70569d613888e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317139"
---
# <a name="kernel-transaction-manager"></a><span data-ttu-id="c9199-106">Gestione transazioni kernel</span><span class="sxs-lookup"><span data-stu-id="c9199-106">Kernel Transaction Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="c9199-107">Scopo</span><span class="sxs-lookup"><span data-stu-id="c9199-107">Purpose</span></span>

<span data-ttu-id="c9199-108">Gestione transazioni kernel consente lo sviluppo di applicazioni che utilizzano transazioni.</span><span class="sxs-lookup"><span data-stu-id="c9199-108">The Kernel Transaction Manager (KTM) enables the development of applications that use transactions.</span></span> <span data-ttu-id="c9199-109">Il motore di transazione stesso si trova all'interno del kernel, ma è possibile sviluppare transazioni per transazioni in modalità kernel o utente e all'interno di un singolo host o tra host distribuiti.</span><span class="sxs-lookup"><span data-stu-id="c9199-109">The transaction engine itself is within the kernel, but transactions can be developed for kernel- or user-mode transactions, and within a single host or among distributed hosts.</span></span>

<span data-ttu-id="c9199-110">La KTM viene utilizzata per implementare il registro di sistema transazionale NTFS (TxF) e transazionale (TxR).</span><span class="sxs-lookup"><span data-stu-id="c9199-110">The KTM is used to implement Transactional NTFS (TxF) and Transactional Registry (TxR).</span></span> <span data-ttu-id="c9199-111">TxF consente operazioni transazionali file system all'interno del file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="c9199-111">TxF allows transacted file system operations within the NTFS file system.</span></span> <span data-ttu-id="c9199-112">TxR consente operazioni del registro di sistema transazionali.</span><span class="sxs-lookup"><span data-stu-id="c9199-112">TxR allows transacted registry operations.</span></span> <span data-ttu-id="c9199-113">KTM consente alle applicazioni client di coordinare file system e operazioni del registro di sistema con una transazione.</span><span class="sxs-lookup"><span data-stu-id="c9199-113">KTM enables client applications to coordinate file system and registry operations with a transaction.</span></span>

<span data-ttu-id="c9199-114">Per sviluppare un'applicazione che coordina le transazioni con risorse diverse da TxF o TxR, è necessario innanzitutto sviluppare un servizio in grado di riconoscere le transazioni Win32, detto anche Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="c9199-114">To develop an application that coordinates transactions with resources other than TxF or TxR, you must first develop a Win32 transaction-aware service, also called a resource manager.</span></span>

<span data-ttu-id="c9199-115">Le applicazioni gestite e COM+ devono usare i relativi gestori transazioni nativi.</span><span class="sxs-lookup"><span data-stu-id="c9199-115">Managed and COM+ applications should use their native transaction managers.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="c9199-116">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="c9199-116">Where applicable</span></span>

<span data-ttu-id="c9199-117">È possibile utilizzare KTM con le applicazioni e i gestori di risorse ospitati in Windows Vista o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c9199-117">KTM can be used with applications and resource managers hosted on Windows Vista or Windows Server 2008.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="c9199-118">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="c9199-118">Developer audience</span></span>

<span data-ttu-id="c9199-119">L'API KTM è progettata per l'uso da parte dei programmatori C e C++.</span><span class="sxs-lookup"><span data-stu-id="c9199-119">The KTM API is designed for use by C and C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c9199-120">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="c9199-120">Run-time requirements</span></span>

<span data-ttu-id="c9199-121">KTM è supportato a partire da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c9199-121">KTM is supported starting with Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c9199-122">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="c9199-122">In this section</span></span>



| <span data-ttu-id="c9199-123">Argomento</span><span class="sxs-lookup"><span data-stu-id="c9199-123">Topic</span></span>                                     | <span data-ttu-id="c9199-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9199-124">Description</span></span>                                                                                                       |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9199-125">Informazioni</span><span class="sxs-lookup"><span data-stu-id="c9199-125">About</span></span>](about-ktm.md)<br/>         | <span data-ttu-id="c9199-126">Informazioni generali sulle transazioni e sulle funzionalità fornite da KTM.</span><span class="sxs-lookup"><span data-stu-id="c9199-126">General information about transactions and the capabilities provided by KTM.</span></span><br/>                           |
| [<span data-ttu-id="c9199-127">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c9199-127">Reference</span></span>](ktm-reference.md)<br/> | <span data-ttu-id="c9199-128">Documentazione per le funzioni, le strutture dei dati, le enumerazioni e altri elementi di programmazione di KTM.</span><span class="sxs-lookup"><span data-stu-id="c9199-128">Documentation for the functions, data structures, enumerations, and other programming elements of KTM.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="c9199-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c9199-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9199-130">Common Log File System</span><span class="sxs-lookup"><span data-stu-id="c9199-130">Common Log File System</span></span>](/previous-versions/windows/desktop/clfs/common-log-file-system-portal)
</dt> <dt>

[<span data-ttu-id="c9199-131">Transactional NTFS (TxF)</span><span class="sxs-lookup"><span data-stu-id="c9199-131">Transactional NTFS (TxF)</span></span>](/windows/desktop/FileIO/transactional-ntfs-portal)
</dt> <dt>

<span data-ttu-id="c9199-132">[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c9199-132">[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))</span></span>
</dt> </dl>

 

