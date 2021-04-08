---
description: 'Altre informazioni su: riferimento gestito del motore di archiviazione estendibile'
title: Riferimento gestito del motore di archiviazione estendibile
TOCTitle: Extensible Storage Engine Managed Reference
ms:assetid: b6dc69d0-82be-478d-b47f-37d7569cd200
ms:mtpsurl: https://msdn.microsoft.com/library/Dn375980(v=EXCHG.10)
ms:contentKeyID: 56355772
ms.date: 09/02/2015
ms.topic: article
ms.openlocfilehash: a1323d662cc7252ff6bda1eda53108751d3aedfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049672"
---
# <a name="extensible-storage-engine-managed-reference"></a><span data-ttu-id="71b46-103">Riferimento gestito del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="71b46-103">Extensible Storage Engine Managed Reference</span></span>

<span data-ttu-id="71b46-104">Trovare le informazioni di riferimento per la libreria ManagedESENT.</span><span class="sxs-lookup"><span data-stu-id="71b46-104">Find reference information for the ManagedESENT library.</span></span> <span data-ttu-id="71b46-105">La libreria ManagedESENT fornisce l'accesso gestito a ESENT, il motore di database incorporabile nativo di Windows.</span><span class="sxs-lookup"><span data-stu-id="71b46-105">The ManagedESENT library provides managed access to ESENT, the embeddable database engine that is native to Windows.</span></span>


<span data-ttu-id="71b46-106">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="71b46-106">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="71b46-107">**In questo articolo**</span><span class="sxs-lookup"><span data-stu-id="71b46-107">**In this article**</span></span>  
<span data-ttu-id="71b46-108">In che modo la libreria ManagedESENT è diversa da ESENT?</span><span class="sxs-lookup"><span data-stu-id="71b46-108">How is the ManagedESENT library different than ESENT?</span></span>  
<span data-ttu-id="71b46-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71b46-109">Requirements</span></span>  
<span data-ttu-id="71b46-110">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="71b46-110">In this section</span></span>  

## <a name="how-is-the-managedesent-library-different-than-esent"></a><span data-ttu-id="71b46-111">In che modo la libreria ManagedESENT è diversa da ESENT?</span><span class="sxs-lookup"><span data-stu-id="71b46-111">How is the ManagedESENT library different than ESENT?</span></span>

<span data-ttu-id="71b46-112">ESENT è un motore di database transazionale incorporabile che consente di creare applicazioni personalizzate che richiedono un'archiviazione dei dati affidabile, a prestazioni elevate e con sovraccarico ridotto.</span><span class="sxs-lookup"><span data-stu-id="71b46-112">ESENT is an embeddable, transactional database engine that allows you to create custom applications that need reliable, high-performance, low-overhead storage of data.</span></span> <span data-ttu-id="71b46-113">Il motore ESENT può aiutare a soddisfare le esigenze dei dati che variano da qualcosa di semplice come una tabella hash troppo grande per l'archiviazione in memoria, in un elemento più complesso, ad esempio un'applicazione con tabelle, colonne e indici.</span><span class="sxs-lookup"><span data-stu-id="71b46-113">The ESENT engine can help with data needs that range from something as simple as a hash table that is too large to store in memory, to something more complex, such as an application with tables, columns, and indexes.</span></span> <span data-ttu-id="71b46-114">Per creare un'applicazione con ESENT, è possibile usare la DLL esent.dll che fa parte del sistema operativo Windows e scrivere il codice con C/C++.</span><span class="sxs-lookup"><span data-stu-id="71b46-114">To create an application with ESENT, you use the esent.dll DLL that is part of the Windows operating system and write your code with C/C++.</span></span> <span data-ttu-id="71b46-115">Per altre informazioni su ESENT, vedere informazioni di [riferimento sul motore di archiviazione estensibile](./extensible-storage-engine-reference.md).</span><span class="sxs-lookup"><span data-stu-id="71b46-115">For more information about ESENT, see [Extensible Storage Engine Reference](./extensible-storage-engine-reference.md).</span></span>

<span data-ttu-id="71b46-116">ManagedESENT si basa su esent.dll, che fa parte di Windows, quindi non sono presenti file binari non gestiti aggiuntivi da scaricare e installare.</span><span class="sxs-lookup"><span data-stu-id="71b46-116">ManagedESENT is built on top of esent.dll, which is part of Windows, so there are no extra unmanaged binaries to download and install.</span></span> <span data-ttu-id="71b46-117">Con la libreria ManagedESENT è possibile creare l'applicazione usando un linguaggio gestito, ad esempio C \# anziché c/C++.</span><span class="sxs-lookup"><span data-stu-id="71b46-117">With the ManagedESENT library, you can create your application by using a managed language such as C\# instead of C/C++.</span></span> <span data-ttu-id="71b46-118">La libreria usa lo stesso tipo e i nomi di membro per esporre l'API ESE, quindi se si ha già familiarità con la struttura di questa API, è possibile passare facilmente a questa libreria gestita.</span><span class="sxs-lookup"><span data-stu-id="71b46-118">The library uses the same type and member names to expose the ESE API, so if you are already familiar with the structure of this API, you can easily transition to this managed library.</span></span>

## <a name="requirements"></a><span data-ttu-id="71b46-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71b46-119">Requirements</span></span>

<span data-ttu-id="71b46-120">Questa libreria gestita richiede gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="71b46-120">This managed library requires the following:</span></span>

  - <span data-ttu-id="71b46-121">Un computer che esegue una versione di Windows a partire da Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71b46-121">A computer running a version of Windows starting with Windows Vista</span></span>

  - <span data-ttu-id="71b46-122">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="71b46-122">Visual Studio 2012</span></span>

  - <span data-ttu-id="71b46-123">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="71b46-123">The .NET Framework 4.5</span></span>

## <a name="in-this-section"></a><span data-ttu-id="71b46-124">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="71b46-124">In this section</span></span>

  - [<span data-ttu-id="71b46-125">Microsoft. ISAM. ESENT</span><span class="sxs-lookup"><span data-stu-id="71b46-125">Microsoft.Isam.Esent</span></span>](./microsoft.isam.esent-namespace.md)

  - [<span data-ttu-id="71b46-126">Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="71b46-126">Microsoft.Isam.Esent.Interop</span></span>](./microsoft.isam.esent.interop-namespace.md)

  - [<span data-ttu-id="71b46-127">Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="71b46-127">Microsoft.Isam.Esent.Interop.Server2003</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)

  - [<span data-ttu-id="71b46-128">Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="71b46-128">Microsoft.Isam.Esent.Interop.Vista</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)

  - [<span data-ttu-id="71b46-129">Microsoft. ISAM. esent. Interop. Windows7</span><span class="sxs-lookup"><span data-stu-id="71b46-129">Microsoft.Isam.Esent.Interop.Windows7</span></span>](./microsoft.isam.esent.interop.windows7-namespace.md)

  - [<span data-ttu-id="71b46-130">Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="71b46-130">Microsoft.Isam.Esent.Interop.Windows8</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
