---
description: La libreria DirectXMath è basata sulla libreria SIMD XNA Math C++ versione 2.x. Di seguito viene descritto come DirectXMath differisce da XNA Math e come differiscono le versioni di DirectXMath.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Novità (DirectXMath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df1e7f25789ca6f58205ce9f45482e0a49540d1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827627"
---
# <a name="whats-new-directxmath"></a><span data-ttu-id="4f46e-104">Novità (DirectXMath)</span><span class="sxs-lookup"><span data-stu-id="4f46e-104">What's New (DirectXMath)</span></span>

<span data-ttu-id="4f46e-105">La libreria DirectXMath è basata sulla libreria [SIMD XNA Math C++ versione 2.04.](https://walbourn.github.io/xna-math-version-2-04/)</span><span class="sxs-lookup"><span data-stu-id="4f46e-105">The DirectXMath library is based on the [XNA Math C++ SIMD library version 2.04](https://walbourn.github.io/xna-math-version-2-04/).</span></span> <span data-ttu-id="4f46e-106">Di seguito viene descritto come DirectXMath differisce da XNA Math e come differiscono le versioni di DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="4f46e-106">Here we describe how DirectXMath differs from XNA Math and how DirectXMath versions differ.</span></span>

-   [<span data-ttu-id="4f46e-107">Cronologia di Rlease</span><span class="sxs-lookup"><span data-stu-id="4f46e-107">Rlease history</span></span>](#release-history)
-   [<span data-ttu-id="4f46e-108">Differenze di DirectXMath rispetto a XNA Math</span><span class="sxs-lookup"><span data-stu-id="4f46e-108">DirectXMath differences from XNA Math</span></span>](#directxmath-differences-from-xna-math)
-   [<span data-ttu-id="4f46e-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4f46e-109">Related topics</span></span>](#related-topics)

## <a name="release-history"></a><span data-ttu-id="4f46e-110">Cronologia delle versioni</span><span class="sxs-lookup"><span data-stu-id="4f46e-110">Release history</span></span>

<table>
 <tr>
  <td><span data-ttu-id="4f46e-111">Windows 10 SDK (20348), versione 2104</span><span class="sxs-lookup"><span data-stu-id="4f46e-111">Windows 10 SDK (20348), version 2104</span></span></td><td><span data-ttu-id="4f46e-112">DirectXMath 3.16</span><span class="sxs-lookup"><span data-stu-id="4f46e-112">DirectXMath 3.16</span></span></td>
 </td>
 <tr>
  <td><span data-ttu-id="4f46e-113">Windows 10 sdk di aggiornamento di maggio 2020</span><span class="sxs-lookup"><span data-stu-id="4f46e-113">Windows 10 May 2020 Update SDK</span></span></td><td><span data-ttu-id="4f46e-114">DirectXMath 3.14</span><span class="sxs-lookup"><span data-stu-id="4f46e-114">DirectXMath 3.14</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4f46e-115">Aggiornamento di Windows 10 (ottobre 2018) SDK</span><span class="sxs-lookup"><span data-stu-id="4f46e-115">Windows 10 October 2018 Update SDK</span></span></td><td><span data-ttu-id="4f46e-116">DirectXMath 3.13</span><span class="sxs-lookup"><span data-stu-id="4f46e-116">DirectXMath 3.13</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4f46e-117">Aggiornamento di Windows 10 (aprile 2018) SDK</span><span class="sxs-lookup"><span data-stu-id="4f46e-117">Windows 10 April 2018 Update SDK</span></span><br /><span data-ttu-id="4f46e-118">Windows 10 Fall Creators Update SDK</span><span class="sxs-lookup"><span data-stu-id="4f46e-118">Windows 10 Fall Creators Update SDK</span></span></td><td><span data-ttu-id="4f46e-119">DirectXMath 3.11</span><span class="sxs-lookup"><span data-stu-id="4f46e-119">DirectXMath 3.11</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4f46e-120">Windows 10 Creators Update SDK</span><span class="sxs-lookup"><span data-stu-id="4f46e-120">Windows 10 Creators Update SDK</span></span></td><td><span data-ttu-id="4f46e-121">DirectXMath 3.10</span><span class="sxs-lookup"><span data-stu-id="4f46e-121">DirectXMath 3.10</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4f46e-122">Windows 10 Anniversary SDK</span><span class="sxs-lookup"><span data-stu-id="4f46e-122">Windows 10 Anniversary SDK</span></span></td><td><span data-ttu-id="4f46e-123">DirectXMath 3.09</span><span class="sxs-lookup"><span data-stu-id="4f46e-123">DirectXMath 3.09</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4f46e-124">Windows 10 SDK (novembre 2015)</span><span class="sxs-lookup"><span data-stu-id="4f46e-124">Windows 10 SDK (November 2015)</span></span></td><td><span data-ttu-id="4f46e-125">DirectXMath 3.08</span><span class="sxs-lookup"><span data-stu-id="4f46e-125">DirectXMath 3.08</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4f46e-126">Windows SDK for Windows 8.1 (Spring 2015)</span><span class="sxs-lookup"><span data-stu-id="4f46e-126">Windows SDK for Windows 8.1 (Spring 2015)</span></span></td><td><span data-ttu-id="4f46e-127">DirectXMath 3.07</span><span class="sxs-lookup"><span data-stu-id="4f46e-127">DirectXMath 3.07</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4f46e-128">Windows SDK per Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4f46e-128">Windows SDK for Windows 8.1</span></span></td><td><span data-ttu-id="4f46e-129">DirectXMath 3.06</span><span class="sxs-lookup"><span data-stu-id="4f46e-129">DirectXMath 3.06</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4f46e-130">Windows SDK per Windows 8</span><span class="sxs-lookup"><span data-stu-id="4f46e-130">Windows SDK for Windows 8</span></span></td><td><span data-ttu-id="4f46e-131">DirectXMath 3.03</span><span class="sxs-lookup"><span data-stu-id="4f46e-131">DirectXMath 3.03</span></span></td>
 </tr>
</table>

<span data-ttu-id="4f46e-132">Per [altre informazioni, vedere Versioni di DirectXMath.](https://github.com/Microsoft/DirectXMath/releases)</span><span class="sxs-lookup"><span data-stu-id="4f46e-132">See [DirectXMath releases](https://github.com/Microsoft/DirectXMath/releases) for more information.</span></span>

## <a name="directxmath-differences-from-xna-math"></a><span data-ttu-id="4f46e-133">Differenze di DirectXMath rispetto a XNA Math</span><span class="sxs-lookup"><span data-stu-id="4f46e-133">DirectXMath differences from XNA Math</span></span>

<span data-ttu-id="4f46e-134">Ecco come la libreria DirectXMath differisce principalmente dalla libreria matematica XNA:</span><span class="sxs-lookup"><span data-stu-id="4f46e-134">Here is how the DirectXMath library primarily differs from the XNA Math library:</span></span>

-   <span data-ttu-id="4f46e-135">DirectXMath è solo C++ (spazi dei nomi, overload, nuovi modelli e così via).</span><span class="sxs-lookup"><span data-stu-id="4f46e-135">DirectXMath is C++ only (namespaces, overloads, new templates, and so on).</span></span>
-   <span data-ttu-id="4f46e-136">Richiede il supporto della libreria standard C++11, ovvero stdint.h e così via.</span><span class="sxs-lookup"><span data-stu-id="4f46e-136">Requires C++11 standard library support (that is, stdint.h, and so on).</span></span>
-   <span data-ttu-id="4f46e-137">Supporto degli intrinseci ARM-NEON per la Windows RT di lavoro.</span><span class="sxs-lookup"><span data-stu-id="4f46e-137">ARM-NEON intrinsics support for the Windows RT platform.</span></span>
-   <span data-ttu-id="4f46e-138">Nuova funzionalità di colore (conversioni dello spazio dei colori, costanti di colore .NET).</span><span class="sxs-lookup"><span data-stu-id="4f46e-138">New color functionality (color space conversions, .NET color constants).</span></span>
-   <span data-ttu-id="4f46e-139">Tipi di volume di delimitazione, una versione di cui in precedenza era presente l'intestazione XNACollision nell'esempio di collisione di DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="4f46e-139">Bounding volume types (a version of which was previously in the XNACollision header in the DirectX SDK Collision sample).</span></span>
-   <span data-ttu-id="4f46e-140">Nessuna Xbox 360 disponibile.</span><span class="sxs-lookup"><span data-stu-id="4f46e-140">No Xbox 360 version is available.</span></span> <span data-ttu-id="4f46e-141">Il Xbox 360 XDK continua a spedire XNAMath v2.x; rimozione di Xbox 360 tipi di dati e varianti di funzione specifici.</span><span class="sxs-lookup"><span data-stu-id="4f46e-141">The Xbox 360 XDK continues to ship XNAMath v2.x; removal of Xbox 360 specific data types and function variants.</span></span>
-   <span data-ttu-id="4f46e-142">Rielaborato [**XMVectorPermute per**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) migliorare l'ottimizzazione per gli intrinseci SSE e ARM-NEON.</span><span class="sxs-lookup"><span data-stu-id="4f46e-142">Reworked [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) for improved optimization for SSE and ARM-NEON intrinsics.</span></span>
-   <span data-ttu-id="4f46e-143">Il [**tipo XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) è completamente opaco.</span><span class="sxs-lookup"><span data-stu-id="4f46e-143">The [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) type is fully opaque.</span></span> <span data-ttu-id="4f46e-144">Per accedere ai singoli elementi **di XMMATRIX,** usare altri tipi, ad esempio [**XMFLOAT4X4.**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4)</span><span class="sxs-lookup"><span data-stu-id="4f46e-144">To access individual elements of **XMMATRIX**, use other types such as [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f46e-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4f46e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f46e-146">Guida per programmatori DirectXMath</span><span class="sxs-lookup"><span data-stu-id="4f46e-146">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> <dt>

[<span data-ttu-id="4f46e-147">Versioni di DirectXMath</span><span class="sxs-lookup"><span data-stu-id="4f46e-147">DirectXMath releases</span></span>](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
