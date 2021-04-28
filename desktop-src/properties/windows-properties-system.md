---
description: Sistema di proprietà Windows
ms.assetid: c2094bbe-a4ca-4f30-b16e-14dced2912bc
title: Sistema di proprietà Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49e44c988d3a91572be1b42d5fbaf75e664d7f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089879"
---
# <a name="windows-property-system"></a><span data-ttu-id="bf5d1-103">Sistema di proprietà Windows</span><span class="sxs-lookup"><span data-stu-id="bf5d1-103">Windows Property System</span></span>

## <a name="purpose"></a><span data-ttu-id="bf5d1-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="bf5d1-104">Purpose</span></span>

<span data-ttu-id="bf5d1-105">Il Sistema di proprietà Windows è un sistema estendibile di lettura/scrittura di definizioni di dati che fornisce un modo uniforme per esprimere i metadati sugli elementi della shell.</span><span class="sxs-lookup"><span data-stu-id="bf5d1-105">The Windows Property System is an extensible read/write system of data definitions that provides a uniform way of expressing metadata about Shell items.</span></span> <span data-ttu-id="bf5d1-106">Il sistema di proprietà di Windows in Windows Vista e versioni successive consente di archiviare e recuperare i metadati per gli elementi della shell.</span><span class="sxs-lookup"><span data-stu-id="bf5d1-106">The Windows Property system in Windows Vista and later enables you to store and retrieve metadata for Shell items.</span></span> <span data-ttu-id="bf5d1-107">Un elemento della shell è un singolo contenuto, ad esempio un file, una cartella, un messaggio di posta elettronica o un contatto.</span><span class="sxs-lookup"><span data-stu-id="bf5d1-107">A Shell item is any single piece of content, such as a file, folder, email, or contact.</span></span> <span data-ttu-id="bf5d1-108">Una proprietà è una singola parte di metadati associata a un elemento della shell.</span><span class="sxs-lookup"><span data-stu-id="bf5d1-108">A property is an individual piece of metadata associated with a Shell item.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="bf5d1-109">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="bf5d1-109">Developer audience</span></span>

<span data-ttu-id="bf5d1-110">Prima di iniziare a leggere la documentazione Sistema di proprietà Windows SDK, è necessario avere una conoscenza di base degli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="bf5d1-110">Before you start reading the Windows Property System SDK documentation, you should have a fundamental understanding of the following:</span></span>

-   <span data-ttu-id="bf5d1-111">Component Object Model (COM)</span><span class="sxs-lookup"><span data-stu-id="bf5d1-111">Component Object Model (COM)</span></span>
-   <span data-ttu-id="bf5d1-112">Programmazione dello spazio dei nomi della shell</span><span class="sxs-lookup"><span data-stu-id="bf5d1-112">Shell Namespace programming</span></span>

<span data-ttu-id="bf5d1-113">Per un'introduzione a COM, vedere [Nozioni fondamentali su COM.](../com/com-fundamentals.md)</span><span class="sxs-lookup"><span data-stu-id="bf5d1-113">For an introduction to COM, see [COM Fundamentals](../com/com-fundamentals.md).</span></span> <span data-ttu-id="bf5d1-114">Per un'introduzione alla programmazione dello spazio dei nomi della shell, [vedere Attività iniziali con lo spazio dei nomi della shell](../shell/namespace-intro.md).</span><span class="sxs-lookup"><span data-stu-id="bf5d1-114">For an introduction to Shell Namespace programming, see [Getting Started with the Shell Namespace](../shell/namespace-intro.md).</span></span>

<span data-ttu-id="bf5d1-115">Per gli usi del Sistema di proprietà Windows, vedere [Cenni preliminari sul sistema di proprietà: scenari di sviluppo.](property-system-overview.md)</span><span class="sxs-lookup"><span data-stu-id="bf5d1-115">For uses of the Windows Property System, see [Property System Overview: Development Scenarios](property-system-overview.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="bf5d1-116">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="bf5d1-116">Run-time requirements</span></span>

<span data-ttu-id="bf5d1-117">L'ambiente di run-time supportato per l'Sistema di proprietà Windows è Windows Vista o versione successiva e Windows Software Development Kit (Windows SDK) (SDK).</span><span class="sxs-lookup"><span data-stu-id="bf5d1-117">The supported run-time environment for using the Windows Property System is Windows Vista or later and the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bf5d1-118">Windows XP e Microsoft Windows Desktop Search (WDS) 3.0 o versioni successive includono anche un subset del Sistema di proprietà Windows.</span><span class="sxs-lookup"><span data-stu-id="bf5d1-118">Windows XP and Microsoft Windows Desktop Search (WDS) 3.0 or later also include a subset of the Windows Property System.</span></span> <span data-ttu-id="bf5d1-119">Per il download di Windows 7 o Windows Vista SDK aggiornato, vedere [il](https://msdn.microsoft.com/windowsvista/bb980924.aspx)Windows SDK .</span><span class="sxs-lookup"><span data-stu-id="bf5d1-119">For the Windows 7 or updated Windows Vista SDK download, see the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bf5d1-120">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="bf5d1-120">In this section</span></span>

-   [<span data-ttu-id="bf5d1-121">Panoramica del sistema di proprietà</span><span class="sxs-lookup"><span data-stu-id="bf5d1-121">Property System Overview</span></span>](property-system-overview.md)
-   [<span data-ttu-id="bf5d1-122">Sistema di proprietà Windows per sviluppatori</span><span class="sxs-lookup"><span data-stu-id="bf5d1-122">Windows Property System Developer's Guide</span></span>](property-system-developer-s-guide.md)
-   [<span data-ttu-id="bf5d1-123">Riferimento al sistema di proprietà</span><span class="sxs-lookup"><span data-stu-id="bf5d1-123">Property System Reference</span></span>](property-system-reference.md)
-   [<span data-ttu-id="bf5d1-124">Esempi di codice del sistema di proprietà</span><span class="sxs-lookup"><span data-stu-id="bf5d1-124">Property System Code Samples</span></span>](property-system-code-samples.md)

 

 
