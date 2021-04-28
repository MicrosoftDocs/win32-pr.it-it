---
description: DirectXMath
ms.assetid: 719954bf-0d7d-f647-2d3f-a77d87df204e
title: DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd35f1faf004bc55a6802da204a6c2fe4e7869b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113009"
---
# <a name="directxmath"></a><span data-ttu-id="17c46-103">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="17c46-103">DirectXMath</span></span>

## <a name="purpose"></a><span data-ttu-id="17c46-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="17c46-104">Purpose</span></span>

<span data-ttu-id="17c46-105">L'API DirectXMath fornisce tipi e funzioni C++ semplici da SIMD per operazioni matematiche e algebriche lineari comuni alle applicazioni DirectX.</span><span class="sxs-lookup"><span data-stu-id="17c46-105">The DirectXMath API provides SIMD-friendly C++ types and functions for common linear algebra and graphics math operations common to DirectX applications.</span></span> <span data-ttu-id="17c46-106">La libreria offre versioni ottimizzate per windows a 32 bit (x86), Windows a 64 bit (x64) e Windows in ARM/ARM64 tramite il supporto degli intrinseci SSE, AVX e ARM-NEON nel compilatore Visual C++.</span><span class="sxs-lookup"><span data-stu-id="17c46-106">The library provides optimized versions for Windows 32-bit (x86), Windows 64-bit (x64), and Windows on ARM/ARM64 through SSE, AVX, and ARM-NEON intrinsics support in the Visual C++ compiler.</span></span>

<span data-ttu-id="17c46-107">Per gli sviluppatori che non hanno a che fare con DirectXMath, è consigliabile usare il wrapper SimpleMath in *DirectX Tool Kit* per [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929)  /  [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) come punto di partenza.</span><span class="sxs-lookup"><span data-stu-id="17c46-107">For developers new to DirectXMath, you may want to consider using the SimpleMath wrapper in the *DirectX Tool Kit* for [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929) / [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) as a starting point.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="17c46-108">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="17c46-108">In this section</span></span>



| <span data-ttu-id="17c46-109">Argomento</span><span class="sxs-lookup"><span data-stu-id="17c46-109">Topic</span></span>                                                                     | <span data-ttu-id="17c46-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17c46-110">Description</span></span>                                                                      |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="17c46-111">Guida per programmatori DirectXMath</span><span class="sxs-lookup"><span data-stu-id="17c46-111">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)<br/>     | <span data-ttu-id="17c46-112">DirectXMath offre una soluzione matematica ottimizzata per Windows.</span><span class="sxs-lookup"><span data-stu-id="17c46-112">DirectXMath provides a math solution optimized for Windows.</span></span><br/>           |
| [<span data-ttu-id="17c46-113">Informazioni di riferimento sulla programmazione DirectXMath</span><span class="sxs-lookup"><span data-stu-id="17c46-113">DirectXMath Programming Reference</span></span>](ovw-xnamath-reference.md)<br/> | <span data-ttu-id="17c46-114">Questa sezione contiene materiale di riferimento per la libreria DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="17c46-114">This section contains reference material for the DirectXMath Library.</span></span><br/> |



 

## <a name="developer-audience"></a><span data-ttu-id="17c46-115">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="17c46-115">Developer audience</span></span>

<span data-ttu-id="17c46-116">La libreria DirectXMath è progettata per gli sviluppatori C++ che lavorano a giochi e grafica DirectX nelle app di Windows Store, nei giochi Xbox e nelle app desktop tradizionali per Windows.</span><span class="sxs-lookup"><span data-stu-id="17c46-116">The DirectXMath library is designed for C++ developers working on games and DirectX graphics in Windows Store apps, Xbox games, and traditional desktop apps for Windows.</span></span>

## <a name="obtaining-directxmath"></a><span data-ttu-id="17c46-117">Recupero di DirectXMath</span><span class="sxs-lookup"><span data-stu-id="17c46-117">Obtaining DirectXMath</span></span>
 
<span data-ttu-id="17c46-118">Le intestazioni DirectXMath sono disponibili nel Windows SDK fornito con Visual Studio 2012 o versione successiva e come intestazione all inline non è presente alcuna DLL o libreria statica a cui collegarsi.</span><span class="sxs-lookup"><span data-stu-id="17c46-118">The DirectXMath headers ship in the Windows SDK that comes with Visual Studio 2012 or later, and as an all inline header there is no DLL or static library to link against.</span></span> <span data-ttu-id="17c46-119">È disponibile anche come pacchetto in [NuGet.](https://www.nuget.org/packages/directxmath/)</span><span class="sxs-lookup"><span data-stu-id="17c46-119">It is also available as a package on [NuGet](https://www.nuget.org/packages/directxmath/).</span></span>

<span data-ttu-id="17c46-120">DirectXMath è open source con la [licenza MIT](https://opensource.org/licenses/MIT) ospitata su [GitHub.](https://github.com/Microsoft/DirectXMath)</span><span class="sxs-lookup"><span data-stu-id="17c46-120">DirectXMath is open source under the [MIT license](https://opensource.org/licenses/MIT) hosted on [GitHub](https://github.com/Microsoft/DirectXMath).</span></span>




