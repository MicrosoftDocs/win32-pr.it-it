---
title: Terminologia pipe essenziale
description: Analogamente ad altri tipi di parametri per le chiamate a procedure remote, le pipe possono essere \ in \ o \ out \ Parameters.
ms.assetid: 377fb65a-e819-4e96-a5b7-9850afd97b73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df183d18d7962ad0c63ecaa0d350006a4144f23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517019"
---
# <a name="essential-pipe-terminology"></a><span data-ttu-id="dbe20-103">Terminologia pipe essenziale</span><span class="sxs-lookup"><span data-stu-id="dbe20-103">Essential Pipe Terminology</span></span>

<span data-ttu-id="dbe20-104">Analogamente ad altri tipi di parametri per le chiamate di procedure remote, le pipe possono essere \[ parametri [**in**](/windows/desktop/Midl/in) \] o \[ [**out**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="dbe20-104">Like other types of parameters to remote procedure calls, pipes can be \[ [**in**](/windows/desktop/Midl/in)\] or \[ [**out**](/windows/desktop/Midl/out-idl)\] parameters.</span></span> <span data-ttu-id="dbe20-105">Poiché il server controlla il trasferimento dei dati tramite una pipe, le pipe con l' \[  \] attributo in si dicono di eseguire il *pull* dei dati nel server.</span><span class="sxs-lookup"><span data-stu-id="dbe20-105">Since the server controls the transfer of data through a pipe, pipes with the \[**in**\] attribute are said to *pull* data to the server.</span></span> <span data-ttu-id="dbe20-106">Analogamente, le pipe di output effettuano il *push* dei dati dal server al client.</span><span class="sxs-lookup"><span data-stu-id="dbe20-106">Similarly, output pipes *push* data from the server to the client.</span></span> <span data-ttu-id="dbe20-107">Le procedure che eseguono il trasferimento dei dati sono denominate rispettivamente la *procedura pull* e la *procedura push*.</span><span class="sxs-lookup"><span data-stu-id="dbe20-107">The procedures that do the data transfer are called the *pull procedure* and the *push procedure*, respectively.</span></span>

<span data-ttu-id="dbe20-108">Il compilatore MIDL genera le procedure push e pull per il server.</span><span class="sxs-lookup"><span data-stu-id="dbe20-108">The MIDL compiler generates the push and pull procedures for the server.</span></span> <span data-ttu-id="dbe20-109">Inoltre, gestisce l'allocazione dei buffer di dati in memoria.</span><span class="sxs-lookup"><span data-stu-id="dbe20-109">In addition, it manages the allocation of data buffers in memory.</span></span> <span data-ttu-id="dbe20-110">Tuttavia, il client deve fornire le proprie procedure push e pull.</span><span class="sxs-lookup"><span data-stu-id="dbe20-110">However, the client must provide its own push and pull procedures.</span></span> <span data-ttu-id="dbe20-111">Deve inoltre fornire una procedura per l'allocazione dei buffer di memoria utilizzati dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="dbe20-111">It must also provide a procedure for allocating the memory buffers used by the pipe.</span></span> <span data-ttu-id="dbe20-112">Questi vengono chiamati automaticamente al momento appropriato dallo stub del client.</span><span class="sxs-lookup"><span data-stu-id="dbe20-112">These are automatically called at the appropriate time by the client stub.</span></span> <span data-ttu-id="dbe20-113">La procedura di allocazione è spesso denominata routine Alloc o funzione Alloc.</span><span class="sxs-lookup"><span data-stu-id="dbe20-113">The allocation procedure is often called the alloc procedure or the alloc function.</span></span>

 

 