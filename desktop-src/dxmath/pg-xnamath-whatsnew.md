---
description: La libreria DirectXMath si basa sulla libreria XNA Math C++ SIMD versione 2. x. Qui viene descritto come DirectXMath differisce da XNA Math e come le versioni di DirectXMath sono diverse.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Novità (DirectXMath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb9fa8c7ee0600ce0b0fa5eade3a3e111e5edbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309244"
---
# <a name="whats-new-directxmath"></a><span data-ttu-id="6726f-104">Novità (DirectXMath)</span><span class="sxs-lookup"><span data-stu-id="6726f-104">What's New (DirectXMath)</span></span>

<span data-ttu-id="6726f-105">La libreria DirectXMath si basa sulla [libreria XNA Math C++ SIMD della versione 2,04](https://walbourn.github.io/).</span><span class="sxs-lookup"><span data-stu-id="6726f-105">The DirectXMath library is based on the [XNA Math C++ SIMD library version 2.04](https://walbourn.github.io/).</span></span> <span data-ttu-id="6726f-106">Qui viene descritto come DirectXMath differisce da XNA Math e come le versioni di DirectXMath sono diverse.</span><span class="sxs-lookup"><span data-stu-id="6726f-106">Here we describe how DirectXMath differs from XNA Math and how DirectXMath versions differ.</span></span>

-   [<span data-ttu-id="6726f-107">Cronologia Rlease</span><span class="sxs-lookup"><span data-stu-id="6726f-107">Rlease history</span></span>](#release-history)
-   [<span data-ttu-id="6726f-108">Differenze DirectXMath da XNA Math</span><span class="sxs-lookup"><span data-stu-id="6726f-108">DirectXMath differences from XNA Math</span></span>](#directxmath-differences-from-xna-math)
-   [<span data-ttu-id="6726f-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6726f-109">Related topics</span></span>](#related-topics)

## <a name="release-history"></a><span data-ttu-id="6726f-110">Cronologia delle versioni</span><span class="sxs-lookup"><span data-stu-id="6726f-110">Release history</span></span>

<table>
 <tr>
  <td><span data-ttu-id="6726f-111">SDK di aggiornamento di Windows 10 maggio 2020</span><span class="sxs-lookup"><span data-stu-id="6726f-111">Windows 10 May 2020 Update SDK</span></span></td><td><span data-ttu-id="6726f-112">DirectXMath 3,14</span><span class="sxs-lookup"><span data-stu-id="6726f-112">DirectXMath 3.14</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="6726f-113">SDK di aggiornamento di Windows 10 ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="6726f-113">Windows 10 October 2018 Update SDK</span></span></td><td><span data-ttu-id="6726f-114">DirectXMath 3,13</span><span class="sxs-lookup"><span data-stu-id="6726f-114">DirectXMath 3.13</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="6726f-115">SDK di aggiornamento di Windows 10 aprile 2018</span><span class="sxs-lookup"><span data-stu-id="6726f-115">Windows 10 April 2018 Update SDK</span></span><br /><span data-ttu-id="6726f-116">Windows 10 Fall Creators Update SDK</span><span class="sxs-lookup"><span data-stu-id="6726f-116">Windows 10 Fall Creators Update SDK</span></span></td><td><span data-ttu-id="6726f-117">DirectXMath 3,11</span><span class="sxs-lookup"><span data-stu-id="6726f-117">DirectXMath 3.11</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="6726f-118">SDK di Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="6726f-118">Windows 10 Creators Update SDK</span></span></td><td><span data-ttu-id="6726f-119">DirectXMath 3,10</span><span class="sxs-lookup"><span data-stu-id="6726f-119">DirectXMath 3.10</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="6726f-120">Windows 10 Anniversary SDK</span><span class="sxs-lookup"><span data-stu-id="6726f-120">Windows 10 Anniversary SDK</span></span></td><td><span data-ttu-id="6726f-121">DirectXMath 3,09</span><span class="sxs-lookup"><span data-stu-id="6726f-121">DirectXMath 3.09</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="6726f-122">Windows 10 SDK (2015 novembre)</span><span class="sxs-lookup"><span data-stu-id="6726f-122">Windows 10 SDK (November 2015)</span></span></td><td><span data-ttu-id="6726f-123">DirectXMath 3,08</span><span class="sxs-lookup"><span data-stu-id="6726f-123">DirectXMath 3.08</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="6726f-124">Windows SDK per Windows 8.1 (Spring 2015)</span><span class="sxs-lookup"><span data-stu-id="6726f-124">Windows SDK for Windows 8.1 (Spring 2015)</span></span></td><td><span data-ttu-id="6726f-125">DirectXMath 3,07</span><span class="sxs-lookup"><span data-stu-id="6726f-125">DirectXMath 3.07</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="6726f-126">Windows SDK per Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6726f-126">Windows SDK for Windows 8.1</span></span></td><td><span data-ttu-id="6726f-127">DirectXMath 3,06</span><span class="sxs-lookup"><span data-stu-id="6726f-127">DirectXMath 3.06</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="6726f-128">Windows SDK per Windows 8</span><span class="sxs-lookup"><span data-stu-id="6726f-128">Windows SDK for Windows 8</span></span></td><td><span data-ttu-id="6726f-129">DirectXMath 3,03</span><span class="sxs-lookup"><span data-stu-id="6726f-129">DirectXMath 3.03</span></span></td>
 </tr>
</table>

<span data-ttu-id="6726f-130">Per ulteriori informazioni, vedere [DirectXMath releases](https://github.com/Microsoft/DirectXMath/releases) .</span><span class="sxs-lookup"><span data-stu-id="6726f-130">See [DirectXMath releases](https://github.com/Microsoft/DirectXMath/releases) for more information.</span></span>

## <a name="directxmath-differences-from-xna-math"></a><span data-ttu-id="6726f-131">Differenze DirectXMath da XNA Math</span><span class="sxs-lookup"><span data-stu-id="6726f-131">DirectXMath differences from XNA Math</span></span>

<span data-ttu-id="6726f-132">Ecco come la libreria DirectXMath differisce principalmente dalla libreria matematica XNA:</span><span class="sxs-lookup"><span data-stu-id="6726f-132">Here is how the DirectXMath library primarily differs from the XNA Math library:</span></span>

-   <span data-ttu-id="6726f-133">DirectXMath è solo C++ (spazi dei nomi, overload, nuovi modelli e così via).</span><span class="sxs-lookup"><span data-stu-id="6726f-133">DirectXMath is C++ only (namespaces, overloads, new templates, and so on).</span></span>
-   <span data-ttu-id="6726f-134">Richiede il supporto della libreria standard C++ 11, ovvero stdint. h e così via.</span><span class="sxs-lookup"><span data-stu-id="6726f-134">Requires C++11 standard library support (that is, stdint.h, and so on).</span></span>
-   <span data-ttu-id="6726f-135">ARM-NEON intrinseci supporto per la piattaforma Windows RT.</span><span class="sxs-lookup"><span data-stu-id="6726f-135">ARM-NEON intrinsics support for the Windows RT platform.</span></span>
-   <span data-ttu-id="6726f-136">Nuova funzionalità per i colori (conversioni dello spazio dei colori, costanti di colore .NET).</span><span class="sxs-lookup"><span data-stu-id="6726f-136">New color functionality (color space conversions, .NET color constants).</span></span>
-   <span data-ttu-id="6726f-137">Tipi di volumi di delimitazione (una versione di che in precedenza era presente nell'intestazione XNACollision nell'esempio di conflitto di DirectX SDK).</span><span class="sxs-lookup"><span data-stu-id="6726f-137">Bounding volume types (a version of which was previously in the XNACollision header in the DirectX SDK Collision sample).</span></span>
-   <span data-ttu-id="6726f-138">Nessuna versione di Xbox 360 disponibile.</span><span class="sxs-lookup"><span data-stu-id="6726f-138">No Xbox 360 version is available.</span></span> <span data-ttu-id="6726f-139">Il XDK di Xbox 360 continua a spedire XNAMath V2. x; rimozione dei tipi di dati e delle varianti di funzione specifici di Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="6726f-139">The Xbox 360 XDK continues to ship XNAMath v2.x; removal of Xbox 360 specific data types and function variants.</span></span>
-   <span data-ttu-id="6726f-140">[**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) rilavorato per ottimizzare l'ottimizzazione per le funzioni intrinseche SSE e ARM-Neon.</span><span class="sxs-lookup"><span data-stu-id="6726f-140">Reworked [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) for improved optimization for SSE and ARM-NEON intrinsics.</span></span>
-   <span data-ttu-id="6726f-141">Il tipo [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) è completamente opaco.</span><span class="sxs-lookup"><span data-stu-id="6726f-141">The [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) type is fully opaque.</span></span> <span data-ttu-id="6726f-142">Per accedere ai singoli elementi di **XMMATRIX**, usare altri tipi, ad esempio [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span><span class="sxs-lookup"><span data-stu-id="6726f-142">To access individual elements of **XMMATRIX**, use other types such as [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6726f-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6726f-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6726f-144">Guida alla programmazione di DirectXMath</span><span class="sxs-lookup"><span data-stu-id="6726f-144">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> <dt>

[<span data-ttu-id="6726f-145">Versioni di DirectXMath</span><span class="sxs-lookup"><span data-stu-id="6726f-145">DirectXMath releases</span></span>](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
