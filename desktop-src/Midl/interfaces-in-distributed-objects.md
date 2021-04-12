---
title: Interfacce negli oggetti distribuiti
description: Nell'elaborazione distribuita un'interfaccia è una raccolta di definizioni e funzioni remote che consente a due o più programmi di interagire tra contesti diversi.
ms.assetid: d7cd6bf3-58ec-426d-850a-9c5456ed816d
keywords:
- interfacce MIDL, in oggetti distribuiti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cbee13dcbab9ccaa6ef6ad3ad3880daa9b14ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337286"
---
# <a name="interfaces-in-distributed-objects"></a><span data-ttu-id="42b51-104">Interfacce negli oggetti distribuiti</span><span class="sxs-lookup"><span data-stu-id="42b51-104">Interfaces in Distributed Objects</span></span>

<span data-ttu-id="42b51-105">Nell'elaborazione distribuita un'interfaccia è una raccolta di definizioni e funzioni remote che consente a due o più programmi di interagire tra contesti diversi.</span><span class="sxs-lookup"><span data-stu-id="42b51-105">In distributed computing, an interface is a collection of definitions and remote functions that enables two or more programs to interoperate between different contexts.</span></span> <span data-ttu-id="42b51-106">In un'applicazione RPC, un'interfaccia specifica:</span><span class="sxs-lookup"><span data-stu-id="42b51-106">In an RPC application, an interface specifies:</span></span>

-   <span data-ttu-id="42b51-107">Modo in cui le applicazioni client e server si identificano tra loro.</span><span class="sxs-lookup"><span data-stu-id="42b51-107">How client and server applications identify themselves to each other.</span></span>
-   <span data-ttu-id="42b51-108">Modalità di trasmissione dei dati tra client e server.</span><span class="sxs-lookup"><span data-stu-id="42b51-108">How data is transmitted between client and server.</span></span>
-   <span data-ttu-id="42b51-109">Procedure remote che l'applicazione client può chiamare.</span><span class="sxs-lookup"><span data-stu-id="42b51-109">Remote procedures that the client application can call.</span></span>
-   <span data-ttu-id="42b51-110">Tipi di dati per i parametri e valori restituiti delle procedure remote.</span><span class="sxs-lookup"><span data-stu-id="42b51-110">Data types for the parameters and return values of the remote procedures.</span></span>

<span data-ttu-id="42b51-111">Il Microsoft Interface Definition Language (MIDL) è per l'implementazione di interfacce utilizzate nelle applicazioni distribuite.</span><span class="sxs-lookup"><span data-stu-id="42b51-111">The Microsoft Interface Definition Language (MIDL) is for implementing interfaces used in distributed applications.</span></span> <span data-ttu-id="42b51-112">Con MIDL, un'applicazione può disporre di un'interfaccia o di molti.</span><span class="sxs-lookup"><span data-stu-id="42b51-112">With MIDL, an application can have one interface or many.</span></span> <span data-ttu-id="42b51-113">Ogni interfaccia specifica un contratto distribuito univoco tra i programmi client e server.</span><span class="sxs-lookup"><span data-stu-id="42b51-113">Each interface specifies a unique distributed contract between the client and server programs.</span></span> <span data-ttu-id="42b51-114">Le applicazioni basate su RPC (Remote Procedure Call), Component Object Model (COM) e Distributed Component Object Model (DCOM) specificano le interfacce usando MIDL.</span><span class="sxs-lookup"><span data-stu-id="42b51-114">Applications based on remote procedure calls (RPC), Component Object Model (COM), and Distributed Component Object Model (DCOM) specify their interfaces using MIDL.</span></span>

<span data-ttu-id="42b51-115">MIDL è simile a C e C++ in molti modi.</span><span class="sxs-lookup"><span data-stu-id="42b51-115">MIDL resembles C and C++ in many ways.</span></span> <span data-ttu-id="42b51-116">Per una panoramica sulla scrittura di interfacce MIDL, vedere [sviluppo dell'interfaccia](/windows/desktop/Rpc/developing-the-interface).</span><span class="sxs-lookup"><span data-stu-id="42b51-116">For an overview of writing MIDL interfaces, see [Developing the Interface](/windows/desktop/Rpc/developing-the-interface).</span></span>

 

 