---
description: DXGI
ms.assetid: 9565e874-5a8d-4b4b-a2a4-391e46922cc1
title: DXGI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b1e100d068d12f651c2602b29af75181607a038
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343496"
---
# <a name="dxgi"></a><span data-ttu-id="ade25-103">DXGI</span><span class="sxs-lookup"><span data-stu-id="ade25-103">DXGI</span></span>

<span data-ttu-id="ade25-104">Microsoft DirectX Graphic Infrastructure (DXGI) gestisce l'enumerazione delle schede grafiche, l'enumerazione delle modalità di visualizzazione, la selezione dei formati di buffer, la condivisione di risorse tra processi (ad esempio, tra applicazioni e Gestione finestre desktop (DWM) e la presentazione dei fotogrammi sottoposti a rendering in una finestra o in un monitor per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ade25-104">Microsoft DirectX Graphics Infrastructure (DXGI) handles enumerating graphics adapters, enumerating display modes, selecting buffer formats, sharing resources between processes (such as, between applications and the Desktop Window Manager (DWM)), and presenting rendered frames to a window or monitor for display.</span></span>

<span data-ttu-id="ade25-105">DXGI viene usato da Direct3D 10, Direct3D 11 e Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="ade25-105">DXGI is used by Direct3D 10, Direct3D 11 and Direct3D 12.</span></span>

<span data-ttu-id="ade25-106">Anche se la maggior parte della programmazione grafica viene eseguita con Direct3D, è possibile usare DXGI per presentare frame a una finestra, a un monitor o a un altro componente grafico per la composizione e la visualizzazione finale.</span><span class="sxs-lookup"><span data-stu-id="ade25-106">Though most graphics programming is done using Direct3D, you can use DXGI to present frames to a window, monitor, or other graphics component for eventual composition and display.</span></span> <span data-ttu-id="ade25-107">È anche possibile usare DXGI per leggere il contenuto su un monitor.</span><span class="sxs-lookup"><span data-stu-id="ade25-107">You can also use DXGI to read the contents on a monitor.</span></span>

<span data-ttu-id="ade25-108">Questo set di documentazione contiene informazioni sulla programmazione con DXGI.</span><span class="sxs-lookup"><span data-stu-id="ade25-108">This documentation set contains information about programming with DXGI.</span></span>



| <span data-ttu-id="ade25-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="ade25-109">Requirement</span></span>                                  | <span data-ttu-id="ade25-110">Valore</span><span class="sxs-lookup"><span data-stu-id="ade25-110">Value</span></span>                                                                                               |
|-----------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ade25-111">Ambienti di runtime supportati</span><span class="sxs-lookup"><span data-stu-id="ade25-111">Supported runtime environments</span></span>    | <dl> <span data-ttu-id="ade25-112"><dt>Windows/C++</dt></span><span class="sxs-lookup"><span data-stu-id="ade25-112"><dt>Windows/C++</dt></span></span> </dl>         |
| <span data-ttu-id="ade25-113">Linguaggi di programmazione consigliati</span><span class="sxs-lookup"><span data-stu-id="ade25-113">Recommended programming languages</span></span> | <span data-ttu-id="ade25-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="ade25-114">C/C++</span></span>                                                                                          |
| <span data-ttu-id="ade25-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ade25-115">Minimum supported Client</span></span>          | <dl> <span data-ttu-id="ade25-116"><dt>Windows Vista</dt></span><span class="sxs-lookup"><span data-stu-id="ade25-116"><dt>Windows Vista</dt></span></span> </dl>       |
| <span data-ttu-id="ade25-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ade25-117">Minimum supported Server</span></span>          | <dl> <span data-ttu-id="ade25-118"><dt>Windows Server 2008</dt></span><span class="sxs-lookup"><span data-stu-id="ade25-118"><dt>Windows Server 2008</dt></span></span> </dl> |



-   [<span data-ttu-id="ade25-119">Guida di programmazione per DXGI</span><span class="sxs-lookup"><span data-stu-id="ade25-119">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
-   [<span data-ttu-id="ade25-120">Informazioni di riferimento su DXGI</span><span class="sxs-lookup"><span data-stu-id="ade25-120">DXGI Reference</span></span>](d3d10-graphics-reference-dxgi.md)

 

 



