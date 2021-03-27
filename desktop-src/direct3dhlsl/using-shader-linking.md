---
title: Uso del collegamento shader
description: Viene illustrato come creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.
ms.assetid: 3A1597FF-F848-415E-BDF8-199C69C05C3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7528415f1bedb0364a9c4b09126a983222fc42b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729914"
---
# <a name="using-shader-linking"></a><span data-ttu-id="1e037-103">Uso del collegamento shader</span><span class="sxs-lookup"><span data-stu-id="1e037-103">Using shader linking</span></span>

<span data-ttu-id="1e037-104">Viene illustrato come creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1e037-104">We show how to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run-time.</span></span> <span data-ttu-id="1e037-105">Il collegamento dello shader è supportato a partire da Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="1e037-105">Shader linking is supported starting with Windows 8.1.</span></span>

<span data-ttu-id="1e037-106">**Obiettivo:** Informazioni su come usare il collegamento dello shader.</span><span class="sxs-lookup"><span data-stu-id="1e037-106">**Objective:** Learn how to use shader linking.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1e037-107">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="1e037-107">Prerequisites</span></span>

<span data-ttu-id="1e037-108">Partiamo dal presupposto che tu abbia familiarità con C++.</span><span class="sxs-lookup"><span data-stu-id="1e037-108">We assume that you are familiar with C++.</span></span> <span data-ttu-id="1e037-109">Devi inoltre avere un'esperienza di base dei concetti di programmazione di grafica.</span><span class="sxs-lookup"><span data-stu-id="1e037-109">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="1e037-110">**Tempo totale per il completamento:** 60 minuti.</span><span class="sxs-lookup"><span data-stu-id="1e037-110">**Total time to complete:** 60 minutes.</span></span>

## <a name="where-to-go-from-here"></a><span data-ttu-id="1e037-111">Dove proseguire</span><span class="sxs-lookup"><span data-stu-id="1e037-111">Where to go from here</span></span>

<span data-ttu-id="1e037-112">Vedere anche [API del compilatore HLSL](dx-graphics-d3dcompiler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="1e037-112">Also see [HLSL compiler APIs](dx-graphics-d3dcompiler-reference.md).</span></span>

<span data-ttu-id="1e037-113">Ti mostreremo come:</span><span class="sxs-lookup"><span data-stu-id="1e037-113">We show you how to:</span></span>

-   <span data-ttu-id="1e037-114">Compilare il codice dello shader</span><span class="sxs-lookup"><span data-stu-id="1e037-114">Compile your shader code</span></span>
-   <span data-ttu-id="1e037-115">Caricare il codice compilato in una libreria shader</span><span class="sxs-lookup"><span data-stu-id="1e037-115">Load the compiled code into a shader library</span></span>
-   <span data-ttu-id="1e037-116">Associare le risorse dagli slot di origine agli slot di destinazione</span><span class="sxs-lookup"><span data-stu-id="1e037-116">Bind the resources from source slots to destination slots</span></span>
-   <span data-ttu-id="1e037-117">Costrutto Function-linking-graphs (FLGs) per gli shader</span><span class="sxs-lookup"><span data-stu-id="1e037-117">Construct function-linking-graphs (FLGs) for shaders</span></span>
-   <span data-ttu-id="1e037-118">Collegare i grafici shader con una libreria shader per produrre un BLOB dello shader che può essere usato dal runtime Direct3D</span><span class="sxs-lookup"><span data-stu-id="1e037-118">Link shader graphs with a shader library to produce a shader blob that the Direct3D runtime can use</span></span>

<span data-ttu-id="1e037-119">Successivamente, si crea una libreria shader e si associano le risorse da slot di origine a slot di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1e037-119">Next we make a shader library and bind resources from source slots to destination slots.</span></span>

[<span data-ttu-id="1e037-120">Creazione del pacchetto di una libreria shader</span><span class="sxs-lookup"><span data-stu-id="1e037-120">Packaging a shader library</span></span>](pachaging-a-shader-library.md)

## <a name="related-topics"></a><span data-ttu-id="1e037-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1e037-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e037-122">Guida alla programmazione per HLSL</span><span class="sxs-lookup"><span data-stu-id="1e037-122">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[<span data-ttu-id="1e037-123">Grafica Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="1e037-123">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
</dt> <dt>

[<span data-ttu-id="1e037-124">DXGI</span><span class="sxs-lookup"><span data-stu-id="1e037-124">DXGI</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)
</dt> </dl>

 

 