---
description: .
ms.assetid: 719954bf-0d7d-f647-2d3f-a77d87df204e
title: DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f316939514d9a186fcd5ef36372f31709b69a7a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104352001"
---
# <a name="directxmath"></a><span data-ttu-id="dab49-103">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="dab49-103">DirectXMath</span></span>

## <a name="purpose"></a><span data-ttu-id="dab49-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="dab49-104">Purpose</span></span>

<span data-ttu-id="dab49-105">L'API di DirectXMath fornisce funzioni e tipi C++ intuitivi per l'algebra lineare comune e le operazioni matematiche grafiche comuni alle applicazioni DirectX.</span><span class="sxs-lookup"><span data-stu-id="dab49-105">The DirectXMath API provides SIMD-friendly C++ types and functions for common linear algebra and graphics math operations common to DirectX applications.</span></span> <span data-ttu-id="dab49-106">La libreria fornisce le versioni ottimizzate per Windows a 32 bit (x86), Windows 64-bit (x64) e Windows su ARM/ARM64 tramite SSE, AVX e il supporto degli intrinseci ARM-NEON nel compilatore Visual C++.</span><span class="sxs-lookup"><span data-stu-id="dab49-106">The library provides optimized versions for Windows 32-bit (x86), Windows 64-bit (x64), and Windows on ARM/ARM64 through SSE, AVX, and ARM-NEON intrinsics support in the Visual C++ compiler.</span></span>

<span data-ttu-id="dab49-107">Per gli sviluppatori che non hanno familiarità con DirectXMath, è consigliabile usare il wrapper SimpleMath in *DirectX Tool Kit* per [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929)  /  [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) come punto di partenza.</span><span class="sxs-lookup"><span data-stu-id="dab49-107">For developers new to DirectXMath, you may want to consider using the SimpleMath wrapper in the *DirectX Tool Kit* for [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929) / [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) as a starting point.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dab49-108">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="dab49-108">In this section</span></span>



| <span data-ttu-id="dab49-109">Argomento</span><span class="sxs-lookup"><span data-stu-id="dab49-109">Topic</span></span>                                                                     | <span data-ttu-id="dab49-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dab49-110">Description</span></span>                                                                      |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="dab49-111">Guida alla programmazione di DirectXMath</span><span class="sxs-lookup"><span data-stu-id="dab49-111">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)<br/>     | <span data-ttu-id="dab49-112">DirectXMath fornisce una soluzione matematica ottimizzata per Windows.</span><span class="sxs-lookup"><span data-stu-id="dab49-112">DirectXMath provides a math solution optimized for Windows.</span></span><br/>           |
| [<span data-ttu-id="dab49-113">Guida di riferimento alla programmazione DirectXMath</span><span class="sxs-lookup"><span data-stu-id="dab49-113">DirectXMath Programming Reference</span></span>](ovw-xnamath-reference.md)<br/> | <span data-ttu-id="dab49-114">Questa sezione contiene materiale di riferimento per la libreria DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="dab49-114">This section contains reference material for the DirectXMath Library.</span></span><br/> |



 

## <a name="developer-audience"></a><span data-ttu-id="dab49-115">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="dab49-115">Developer audience</span></span>

<span data-ttu-id="dab49-116">La libreria DirectXMath è progettata per gli sviluppatori C++ che lavorano su giochi e grafica DirectX in app di Windows Store, Xbox Games e applicazioni desktop tradizionali per Windows.</span><span class="sxs-lookup"><span data-stu-id="dab49-116">The DirectXMath library is designed for C++ developers working on games and DirectX graphics in Windows Store apps, Xbox games, and traditional desktop apps for Windows.</span></span>

## <a name="obtaining-directxmath"></a><span data-ttu-id="dab49-117">Recupero di DirectXMath</span><span class="sxs-lookup"><span data-stu-id="dab49-117">Obtaining DirectXMath</span></span>
 
<span data-ttu-id="dab49-118">Le intestazioni DirectXMath vengono fornite nella Windows SDK fornita con Visual Studio 2012 o versioni successive e come intestazione all inline non è presente alcuna DLL o libreria statica con cui eseguire il collegamento.</span><span class="sxs-lookup"><span data-stu-id="dab49-118">The DirectXMath headers ship in the Windows SDK that comes with Visual Studio 2012 or later, and as an all inline header there is no DLL or static library to link against.</span></span> <span data-ttu-id="dab49-119">È disponibile anche come pacchetto in [NuGet](https://www.nuget.org/packages/directxmath/).</span><span class="sxs-lookup"><span data-stu-id="dab49-119">It is also available as a package on [NuGet](https://www.nuget.org/packages/directxmath/).</span></span>

<span data-ttu-id="dab49-120">DirectXMath è open source con la [licenza mit](https://opensource.org/licenses/MIT) ospitata su [GitHub](https://github.com/Microsoft/DirectXMath).</span><span class="sxs-lookup"><span data-stu-id="dab49-120">DirectXMath is open source under the [MIT license](https://opensource.org/licenses/MIT) hosted on [GitHub](https://github.com/Microsoft/DirectXMath).</span></span>




