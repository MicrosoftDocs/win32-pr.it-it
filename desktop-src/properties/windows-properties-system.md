---
description: .
ms.assetid: c2094bbe-a4ca-4f30-b16e-14dced2912bc
title: Sistema di proprietà di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e96f931d37ef698339f9219a0dc8db43a6003e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306195"
---
# <a name="windows-property-system"></a><span data-ttu-id="a69c8-103">Sistema di proprietà di Windows</span><span class="sxs-lookup"><span data-stu-id="a69c8-103">Windows Property System</span></span>

## <a name="purpose"></a><span data-ttu-id="a69c8-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="a69c8-104">Purpose</span></span>

<span data-ttu-id="a69c8-105">Il sistema di proprietà di Windows è un sistema di lettura/scrittura estendibile di definizioni dei dati che fornisce un modo uniforme per esprimere i metadati sugli elementi della shell.</span><span class="sxs-lookup"><span data-stu-id="a69c8-105">The Windows Property System is an extensible read/write system of data definitions that provides a uniform way of expressing metadata about Shell items.</span></span> <span data-ttu-id="a69c8-106">Il sistema di proprietà di Windows in Windows Vista e versioni successive consente di archiviare e recuperare metadati per gli elementi della shell.</span><span class="sxs-lookup"><span data-stu-id="a69c8-106">The Windows Property system in Windows Vista and later enables you to store and retrieve metadata for Shell items.</span></span> <span data-ttu-id="a69c8-107">Un elemento della shell è costituito da qualsiasi singolo contenuto, ad esempio un file, una cartella, un messaggio di posta elettronica o un contatto.</span><span class="sxs-lookup"><span data-stu-id="a69c8-107">A Shell item is any single piece of content, such as a file, folder, email, or contact.</span></span> <span data-ttu-id="a69c8-108">Una proprietà è una singola parte di metadati associata a un elemento della shell.</span><span class="sxs-lookup"><span data-stu-id="a69c8-108">A property is an individual piece of metadata associated with a Shell item.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a69c8-109">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="a69c8-109">Developer audience</span></span>

<span data-ttu-id="a69c8-110">Prima di iniziare a leggere la documentazione relativa all'SDK del sistema di proprietà di Windows, è necessario avere una conoscenza di base dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="a69c8-110">Before you start reading the Windows Property System SDK documentation, you should have a fundamental understanding of the following:</span></span>

-   <span data-ttu-id="a69c8-111">Component Object Model (COM)</span><span class="sxs-lookup"><span data-stu-id="a69c8-111">Component Object Model (COM)</span></span>
-   <span data-ttu-id="a69c8-112">Programmazione dello spazio dei nomi della shell</span><span class="sxs-lookup"><span data-stu-id="a69c8-112">Shell Namespace programming</span></span>

<span data-ttu-id="a69c8-113">Per un'introduzione a COM, vedere [nozioni fondamentali su com](../com/com-fundamentals.md).</span><span class="sxs-lookup"><span data-stu-id="a69c8-113">For an introduction to COM, see [COM Fundamentals](../com/com-fundamentals.md).</span></span> <span data-ttu-id="a69c8-114">Per un'introduzione alla programmazione dello spazio dei nomi della shell, vedere [Introduzione con lo spazio dei nomi della shell](../shell/namespace-intro.md).</span><span class="sxs-lookup"><span data-stu-id="a69c8-114">For an introduction to Shell Namespace programming, see [Getting Started with the Shell Namespace](../shell/namespace-intro.md).</span></span>

<span data-ttu-id="a69c8-115">Per gli usi del sistema di proprietà di Windows, vedere [Panoramica del sistema di proprietà: scenari di sviluppo](property-system-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a69c8-115">For uses of the Windows Property System, see [Property System Overview: Development Scenarios](property-system-overview.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a69c8-116">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="a69c8-116">Run-time requirements</span></span>

<span data-ttu-id="a69c8-117">L'ambiente di runtime supportato per l'utilizzo del sistema di proprietà di Windows è Windows Vista o versione successiva e Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="a69c8-117">The supported run-time environment for using the Windows Property System is Windows Vista or later and the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a69c8-118">Windows XP e Microsoft Windows Desktop Search (WDS) 3,0 o versioni successive includono anche un subset del sistema di proprietà di Windows.</span><span class="sxs-lookup"><span data-stu-id="a69c8-118">Windows XP and Microsoft Windows Desktop Search (WDS) 3.0 or later also include a subset of the Windows Property System.</span></span> <span data-ttu-id="a69c8-119">Per il download di Windows 7 o Windows Vista SDK aggiornato, vedere la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a69c8-119">For the Windows 7 or updated Windows Vista SDK download, see the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a69c8-120">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="a69c8-120">In this section</span></span>

-   [<span data-ttu-id="a69c8-121">Panoramica del sistema di proprietà</span><span class="sxs-lookup"><span data-stu-id="a69c8-121">Property System Overview</span></span>](property-system-overview.md)
-   [<span data-ttu-id="a69c8-122">Guida per gli sviluppatori del sistema di proprietà di Windows</span><span class="sxs-lookup"><span data-stu-id="a69c8-122">Windows Property System Developer's Guide</span></span>](property-system-developer-s-guide.md)
-   [<span data-ttu-id="a69c8-123">Riferimento al sistema di proprietà</span><span class="sxs-lookup"><span data-stu-id="a69c8-123">Property System Reference</span></span>](property-system-reference.md)
-   [<span data-ttu-id="a69c8-124">Esempi di codice del sistema di proprietà</span><span class="sxs-lookup"><span data-stu-id="a69c8-124">Property System Code Samples</span></span>](property-system-code-samples.md)

 

 
