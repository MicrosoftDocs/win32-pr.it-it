---
title: pack_matrix direttiva pragma
description: Direttiva pragma che specifica l'allineamento di compressione per le matrici.
ms.assetid: e77dc007-d915-4d78-9fff-d44d4999e4da
keywords:
- pack_matrix direttiva pragma HLSL
topic_type:
- apiref
api_name:
- pack_matrix pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4bb5474702a1caba3f772002c34677601715caff
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045739"
---
# <a name="pack_matrix-pragma-directive"></a><span data-ttu-id="d547b-104">Pack \_ matrice pragma (direttiva)</span><span class="sxs-lookup"><span data-stu-id="d547b-104">pack\_matrix pragma Directive</span></span>

<span data-ttu-id="d547b-105">Direttiva pragma che specifica l'allineamento di compressione per le matrici.</span><span class="sxs-lookup"><span data-stu-id="d547b-105">Pragma directive that specifies packing alignment for matrices.</span></span>



| <span data-ttu-id="d547b-106">\#tabella pragma pack \_ ( *Alignment* )</span><span class="sxs-lookup"><span data-stu-id="d547b-106">\#pragma pack\_matrix( *alignment* )</span></span> |
|--------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="d547b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d547b-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d547b-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="d547b-108">Item</span></span></th>
<th><span data-ttu-id="d547b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d547b-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d547b-110"><span id="alignment"></span><span id="ALIGNMENT"></span><em>allineamento</em></span><span class="sxs-lookup"><span data-stu-id="d547b-110"><span id="alignment"></span><span id="ALIGNMENT"></span><em>alignment</em></span></span><br/></td>
<td><span data-ttu-id="d547b-111">Allineamento da impostare per le matrici.</span><span class="sxs-lookup"><span data-stu-id="d547b-111">Alignment to set for matrices.</span></span> <span data-ttu-id="d547b-112">Questo parametro può assumere uno dei valori elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d547b-112">This parameter can take one of the values listed in the following table.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d547b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="d547b-113">Value</span></span></th>
<th><span data-ttu-id="d547b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d547b-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d547b-115">column_major</span><span class="sxs-lookup"><span data-stu-id="d547b-115">column_major</span></span></td>
<td><span data-ttu-id="d547b-116">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="d547b-116">Default.</span></span> <span data-ttu-id="d547b-117">Imposta l'allineamento della compressione della matrice sulla colonna Major.</span><span class="sxs-lookup"><span data-stu-id="d547b-117">Sets the matrix packing alignment to column major.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d547b-118">row_major</span><span class="sxs-lookup"><span data-stu-id="d547b-118">row_major</span></span></td>
<td><span data-ttu-id="d547b-119">Imposta l'allineamento della compressione della matrice sulla riga principale.</span><span class="sxs-lookup"><span data-stu-id="d547b-119">Sets the matrix packing alignment to row major.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="d547b-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="d547b-120">Examples</span></span>

<span data-ttu-id="d547b-121">Nell'esempio seguente viene impostato l'allineamento della compressione della matrice sulla riga principale.</span><span class="sxs-lookup"><span data-stu-id="d547b-121">The following example sets the matrix packing alignment to row major.</span></span>


```
#pragma pack_matrix( row_major )
```



## <a name="see-also"></a><span data-ttu-id="d547b-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d547b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d547b-123">Direttive per il preprocessore (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d547b-123">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="d547b-124">\#pragma (direttiva) (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d547b-124">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





