---
description: Flag capacità driver.
ms.assetid: 78ff4433-f0b5-4bbb-b2c0-bd389fbc31ce
title: D3DENUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 059c2f9f1bf32275423bb9f2a9f484c12824bcda
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304793"
---
# <a name="d3denum"></a><span data-ttu-id="27d99-103">D3DENUM</span><span class="sxs-lookup"><span data-stu-id="27d99-103">D3DENUM</span></span>

<span data-ttu-id="27d99-104">Flag capacità driver.</span><span class="sxs-lookup"><span data-stu-id="27d99-104">Driver capability flag.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27d99-105">#definire</span><span class="sxs-lookup"><span data-stu-id="27d99-105">#define</span></span></td>
<td><span data-ttu-id="27d99-106">Valore</span><span class="sxs-lookup"><span data-stu-id="27d99-106">Value</span></span></td>
<td><span data-ttu-id="27d99-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27d99-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27d99-108">D3DENUM_WHQL_LEVEL</span><span class="sxs-lookup"><span data-stu-id="27d99-108">D3DENUM_WHQL_LEVEL</span></span></td>
<td><span data-ttu-id="27d99-109">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="27d99-109">0x00000002L</span></span></td>
<td><span data-ttu-id="27d99-110">Test del driver Microsoft Windows Hardware Quality Labs (WHQL).</span><span class="sxs-lookup"><span data-stu-id="27d99-110">Microsoft Windows Hardware Quality Labs (WHQL) driver testing.</span></span> <span data-ttu-id="27d99-111">Si tratta di un test che richiede molto tempo che richiede una riduzione del tempo di un secondo o di due secondi.</span><span class="sxs-lookup"><span data-stu-id="27d99-111">This is a time-consuming test requiring a one-second or two-second time penalty.</span></span> <span data-ttu-id="27d99-112">Questa costante viene utilizzata dal membro WHQLLevel del <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="27d99-112">This constant is used by the WHQLLevel member of <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27d99-113">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="27d99-113">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="27d99-114">D3DENUM_WHQL_LEVEL è deprecato per Direct3D9Ex in esecuzione in Windows Vista, Windows Server 2008, Windows 7 e Windows Server 2008 R2 (o più sistemi operativi correnti).</span><span class="sxs-lookup"><span data-stu-id="27d99-114">D3DENUM_WHQL_LEVEL is deprecated for Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system).</span></span> <span data-ttu-id="27d99-115">Uno di questi sistemi operativi restituisce 1 per il livello WHQL senza controllare lo stato del driver.</span><span class="sxs-lookup"><span data-stu-id="27d99-115">Any of these operating systems return 1 for the WHQL level without checking the status of the driver.</span></span> <br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="constant-information"></a><span data-ttu-id="27d99-116">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="27d99-116">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="27d99-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27d99-117">Header</span></span>                   | <span data-ttu-id="27d99-118">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="27d99-118">d3d9.h</span></span>     |
| <span data-ttu-id="27d99-119">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="27d99-119">Minimum operating system</span></span> | <span data-ttu-id="27d99-120">Windows 98</span><span class="sxs-lookup"><span data-stu-id="27d99-120">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="27d99-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="27d99-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27d99-122">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="27d99-122">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




