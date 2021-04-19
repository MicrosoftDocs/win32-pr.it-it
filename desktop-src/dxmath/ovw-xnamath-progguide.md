---
description: DirectXMath fornisce una soluzione matematica ottimizzata per Windows.
ms.assetid: c2a64435-b2fb-3638-2eea-3ed52f4c7cd5
title: Guida alla programmazione di DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df406787776f9fa5d1786e6ed6c5998e27a1c059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309305"
---
# <a name="directxmath-programming-guide"></a><span data-ttu-id="98c69-103">Guida alla programmazione di DirectXMath</span><span class="sxs-lookup"><span data-stu-id="98c69-103">DirectXMath programming guide</span></span>

<span data-ttu-id="98c69-104">DirectXMath fornisce una soluzione matematica ottimizzata per Windows.</span><span class="sxs-lookup"><span data-stu-id="98c69-104">DirectXMath provides a math solution optimized for Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="98c69-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="98c69-105">In this section</span></span>



| <span data-ttu-id="98c69-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="98c69-106">Topic</span></span>                                                             | <span data-ttu-id="98c69-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98c69-107">Description</span></span>                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98c69-108">Per iniziare</span><span class="sxs-lookup"><span data-stu-id="98c69-108">Getting Started</span></span>](pg-xnamath-getting-started.md)<br/>      | <span data-ttu-id="98c69-109">La libreria DirectXMath implementa un'interfaccia ottimale e portatile per operazioni aritmetiche e di algebra lineare su vettori a virgola mobile a precisione singola (2D, 3D e 4D) o matrici (3 × 3 e 4 × 4).</span><span class="sxs-lookup"><span data-stu-id="98c69-109">The DirectXMath Library implements an optimal and portable interface for arithmetic and linear algebra operations on single-precision floating-point vectors (2D, 3D, and 4D) or matrices (3×3 and 4×4).</span></span> <br/>                                                    |
| [<span data-ttu-id="98c69-110">Novità</span><span class="sxs-lookup"><span data-stu-id="98c69-110">What's New</span></span>](pg-xnamath-whatsnew.md)<br/>                  | <span data-ttu-id="98c69-111">La libreria DirectXMath si basa sulla [libreria XNA Math C++ SIMD della versione 2,04](https://walbourn.github.io/).</span><span class="sxs-lookup"><span data-stu-id="98c69-111">The DirectXMath library is based on the [XNA Math C++ SIMD library version 2.04](https://walbourn.github.io/).</span></span> <span data-ttu-id="98c69-112">Qui viene descritto come DirectXMath differisce da XNA Math e come le versioni di DirectXMath sono diverse.</span><span class="sxs-lookup"><span data-stu-id="98c69-112">Here we describe how DirectXMath differs from XNA Math and how DirectXMath versions differ.</span></span> <br/> |
| [<span data-ttu-id="98c69-113">Migrazione del codice</span><span class="sxs-lookup"><span data-stu-id="98c69-113">Code Migration</span></span>](pg-xnamath-migration.md)<br/>             | <span data-ttu-id="98c69-114">Questa panoramica descrive le modifiche necessarie per eseguire la migrazione del codice esistente usando la libreria Math XNA alla libreria DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="98c69-114">This overview describes the changes required to migrate existing code using the XNA Math library to the DirectXMath library.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="98c69-115">Uso di D3DXMath</span><span class="sxs-lookup"><span data-stu-id="98c69-115">Working with D3DXMath</span></span>](pg-xnamath-migration-d3dx.md)<br/> | <span data-ttu-id="98c69-116">D3DXMath è una libreria helper Math per le applicazioni Direct3D.</span><span class="sxs-lookup"><span data-stu-id="98c69-116">D3DXMath is a math helper library for Direct3D applications.</span></span> <br/>                                                                                                                                                                                                |
| [<span data-ttu-id="98c69-117">Ottimizzazione del codice</span><span class="sxs-lookup"><span data-stu-id="98c69-117">Code Optimization</span></span>](pg-xnamath-optimizing.md)<br/>         | <span data-ttu-id="98c69-118">In questo argomento vengono descritte le strategie e le considerazioni sull'ottimizzazione con la libreria DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="98c69-118">This topic describes optimization considerations and strategies with the DirectXMath Library.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="98c69-119">Elementi interni della libreria</span><span class="sxs-lookup"><span data-stu-id="98c69-119">Library Internals</span></span>](pg-xnamath-internals.md)<br/>          | <span data-ttu-id="98c69-120">In questo argomento viene descritta la progettazione interna della libreria DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="98c69-120">This topic describes the internal design of the DirectXMath library.</span></span><br/>                                                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="98c69-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="98c69-121">Related Topics</span></span>

<dl> <dt>

<span data-ttu-id="98c69-122"><span id="DirectXMath_Programming_Reference"></span><span id="directxmath_programming_reference"></span><span id="DIRECTXMATH_PROGRAMMING_REFERENCE"></span>[Guida di riferimento alla programmazione DirectXMath](ovw-xnamath-reference.md)</span><span class="sxs-lookup"><span data-stu-id="98c69-122"><span id="DirectXMath_Programming_Reference"></span><span id="directxmath_programming_reference"></span><span id="DIRECTXMATH_PROGRAMMING_REFERENCE"></span>[DirectXMath Programming Reference](ovw-xnamath-reference.md)</span></span>
<span data-ttu-id="98c69-123"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="98c69-123"></dt> <dd></dd> </dl></span></span>

## <a name="related-topics"></a><span data-ttu-id="98c69-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="98c69-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98c69-125">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="98c69-125">DirectXMath</span></span>](directxmath-portal.md)
</dt> </dl>

 

 




