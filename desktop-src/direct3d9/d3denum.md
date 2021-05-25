---
description: Flag di funzionalità del driver.
ms.assetid: 78ff4433-f0b5-4bbb-b2c0-bd389fbc31ce
title: D3DENUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 829d03bf596c24bfb6b3443ace859629f723a664
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343264"
---
# <a name="d3denum"></a><span data-ttu-id="ea1e8-103">D3DENUM</span><span class="sxs-lookup"><span data-stu-id="ea1e8-103">D3DENUM</span></span>

<span data-ttu-id="ea1e8-104">Flag di funzionalità del driver.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-104">Driver capability flag.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ea1e8-105">#Definire</span><span class="sxs-lookup"><span data-stu-id="ea1e8-105">#define</span></span></td>
<td><span data-ttu-id="ea1e8-106">Valore</span><span class="sxs-lookup"><span data-stu-id="ea1e8-106">Value</span></span></td>
<td><span data-ttu-id="ea1e8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea1e8-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ea1e8-108">D3DENUM_WHQL_LEVEL</span><span class="sxs-lookup"><span data-stu-id="ea1e8-108">D3DENUM_WHQL_LEVEL</span></span></td>
<td><span data-ttu-id="ea1e8-109">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="ea1e8-109">0x00000002L</span></span></td>
<td><span data-ttu-id="ea1e8-110">Test del driver Microsoft Windows Hardware Quality Labs (WHQL).</span><span class="sxs-lookup"><span data-stu-id="ea1e8-110">Microsoft Windows Hardware Quality Labs (WHQL) driver testing.</span></span> <span data-ttu-id="ea1e8-111">Si tratta di un test dispendioso in termini di tempo che richiede una penalità di un secondo o di due secondi.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-111">This is a time-consuming test requiring a one-second or two-second time penalty.</span></span> <span data-ttu-id="ea1e8-112">Questa costante viene usata dal membro WHQLLevel di <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-112">This constant is used by the WHQLLevel member of <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ea1e8-113">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-113">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="ea1e8-114">D3DENUM_WHQL_LEVEL è deprecato per Direct3D9Ex in esecuzione in Windows Vista, Windows Server 2008, Windows 7 e Windows Server 2008 R2 (o un sistema operativo più corrente).</span><span class="sxs-lookup"><span data-stu-id="ea1e8-114">D3DENUM_WHQL_LEVEL is deprecated for Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system).</span></span> <span data-ttu-id="ea1e8-115">Uno di questi sistemi operativi restituisce 1 per il livello WHQL senza controllare lo stato del driver.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-115">Any of these operating systems return 1 for the WHQL level without checking the status of the driver.</span></span> <br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="constant-information"></a><span data-ttu-id="ea1e8-116">Informazioni costanti</span><span class="sxs-lookup"><span data-stu-id="ea1e8-116">Constant Information</span></span>



| <span data-ttu-id="ea1e8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea1e8-117">Requirement</span></span>                         | <span data-ttu-id="ea1e8-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ea1e8-118">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="ea1e8-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea1e8-119">Header</span></span>                   | <span data-ttu-id="ea1e8-120">d3d9.h</span><span class="sxs-lookup"><span data-stu-id="ea1e8-120">d3d9.h</span></span>     |
| <span data-ttu-id="ea1e8-121">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="ea1e8-121">Minimum operating system</span></span> | <span data-ttu-id="ea1e8-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="ea1e8-122">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ea1e8-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ea1e8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea1e8-124">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="ea1e8-124">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




