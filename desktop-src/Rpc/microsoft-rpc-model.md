---
title: Modello RPC
description: La chiamata RPC (Remote Procedure Call) per i linguaggi di programmazione C e C++ è progettata per soddisfare le esigenze degli sviluppatori che lavorano alla prossima generazione di software per i sistemi operativi Windows.
ms.assetid: ebab41a5-e841-4e0f-8acd-d0aab94f01c1
keywords:
- RPC (Remote Procedure Call), descritto, modello RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e72048b12329133fcc8ce4ee82bce266ed29162
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729415"
---
# <a name="the-rpc-model"></a><span data-ttu-id="b3d52-104">Modello RPC</span><span class="sxs-lookup"><span data-stu-id="b3d52-104">The RPC Model</span></span>

<span data-ttu-id="b3d52-105">La chiamata RPC (Remote Procedure Call) per i linguaggi di programmazione C e C++ è progettata per soddisfare le esigenze degli sviluppatori che lavorano alla prossima generazione di software per i sistemi operativi Windows.</span><span class="sxs-lookup"><span data-stu-id="b3d52-105">Remote Procedure Call (RPC) for the C and C++ programming languages is designed to help meet the needs of developers working on the next generation of software for Windows operating systems.</span></span>

<span data-ttu-id="b3d52-106">RPC è un meccanismo di comunicazione interprocesso potente, affidabile, efficiente e sicuro che consente lo scambio di dati e la chiamata di funzionalità che risiedono in un processo diverso.</span><span class="sxs-lookup"><span data-stu-id="b3d52-106">RPC is a powerful, robust, efficient, and secure interprocess communication (IPC) mechanism that enables data exchange and invocation of functionality residing in a different process.</span></span> <span data-ttu-id="b3d52-107">Il processo diverso può trovarsi nello stesso computer, nella rete locale o in Internet.</span><span class="sxs-lookup"><span data-stu-id="b3d52-107">That different process can be on the same machine, on the local area network, or across the Internet.</span></span> <span data-ttu-id="b3d52-108">In questa sezione vengono illustrati il modello di programmazione RPC e il modello per i sistemi distribuiti che possono essere implementati tramite RPC.</span><span class="sxs-lookup"><span data-stu-id="b3d52-108">This section explains the RPC programming model and the model for distributed systems that can be implemented using RPC.</span></span>

<span data-ttu-id="b3d52-109">RPC supporta completamente Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b3d52-109">RPC fully supports 64-bit Windows.</span></span> <span data-ttu-id="b3d52-110">Esistono tre tipi di processi: processi a 32 bit nativi, processi a 64 bit nativi e processi a 32 bit in esecuzione nell'emulatore di processi a 32 bit in un sistema a 64 bit (spesso definito processi WOW64).</span><span class="sxs-lookup"><span data-stu-id="b3d52-110">There are three types of processes: native 32-bit processes, native 64-bit processes, and 32-bit processes running under the 32-bit process emulator on a 64-bit system (often referred to as WOW64 processes).</span></span> <span data-ttu-id="b3d52-111">Per ulteriori informazioni su WOW64, vedere [esecuzione di applicazioni a 32 bit](/windows/desktop/WinProg64/running-32-bit-applications).</span><span class="sxs-lookup"><span data-stu-id="b3d52-111">For more information about WOW64, see [Running 32-bit Applications](/windows/desktop/WinProg64/running-32-bit-applications).</span></span> <span data-ttu-id="b3d52-112">Utilizzando RPC, gli sviluppatori possono comunicare in modo trasparente tra diversi tipi di processo. RPC gestisce automaticamente le differenze di processo dietro le quinte.</span><span class="sxs-lookup"><span data-stu-id="b3d52-112">Using RPC, developers can transparently communicate between different types of process; RPC automatically manages process differences behind the scenes.</span></span>

<span data-ttu-id="b3d52-113">Inizialmente RPC è stato sviluppato come estensione per la RPC OSF.</span><span class="sxs-lookup"><span data-stu-id="b3d52-113">RPC was initially developed as an extension to OSF RPC.</span></span> <span data-ttu-id="b3d52-114">Ad eccezione di alcune funzionalità avanzate, RPC è interoperativo con le implementazioni di altri fornitori di OSF RPC.</span><span class="sxs-lookup"><span data-stu-id="b3d52-114">With the exception of some of its advanced features, RPC is interoperable with other vendors' implementations of OSF RPC.</span></span>

<span data-ttu-id="b3d52-115">In questa sezione viene inoltre fornita una panoramica dei componenti RPC e del relativo funzionamento.</span><span class="sxs-lookup"><span data-stu-id="b3d52-115">This section also provides an overview of RPC components and their operation.</span></span> <span data-ttu-id="b3d52-116">Le informazioni vengono presentate negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3d52-116">The information is presented in the following topics:</span></span>

-   [<span data-ttu-id="b3d52-117">Modello di programmazione</span><span class="sxs-lookup"><span data-stu-id="b3d52-117">The Programming Model</span></span>](the-programming-model.md)
-   [<span data-ttu-id="b3d52-118">Modello per sistemi distribuiti</span><span class="sxs-lookup"><span data-stu-id="b3d52-118">The Model for Distributed Systems</span></span>](the-model-for-distributed-systems.md)
-   [<span data-ttu-id="b3d52-119">Funzionamento di RPC</span><span class="sxs-lookup"><span data-stu-id="b3d52-119">How RPC Works</span></span>](how-rpc-works.md)
-   [<span data-ttu-id="b3d52-120">Componenti RPC Microsoft</span><span class="sxs-lookup"><span data-stu-id="b3d52-120">Microsoft RPC Components</span></span>](microsoft-rpc-components.md)

 

 