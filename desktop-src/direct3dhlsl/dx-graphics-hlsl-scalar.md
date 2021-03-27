---
title: Tipi scalari
description: Tipi scalari
ms.assetid: bf24d27f-2720-4268-bc74-fc46afedb9aa
keywords:
- Tipi scalari HLSL
topic_type:
- apiref
api_name:
- Scalar Types
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 7198932c6edb91e6f797b232b6c980976f3696a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "103761896"
---
# <a name="scalar-types"></a><span data-ttu-id="15e6b-104">Tipi scalari</span><span class="sxs-lookup"><span data-stu-id="15e6b-104">Scalar Types</span></span>


<span data-ttu-id="15e6b-105">HLSL supporta diversi tipi di dati scalari:</span><span class="sxs-lookup"><span data-stu-id="15e6b-105">HLSL supports several scalar data types:</span></span>

-   <span data-ttu-id="15e6b-106">**bool** : true o false.</span><span class="sxs-lookup"><span data-stu-id="15e6b-106">**bool** - true or false.</span></span>
-   <span data-ttu-id="15e6b-107">intero con segno **int** a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="15e6b-107">**int** - 32-bit signed integer.</span></span>
-   <span data-ttu-id="15e6b-108">**uint** -Unsigned Integer a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="15e6b-108">**uint** - 32-bit unsigned integer.</span></span>
-   <span data-ttu-id="15e6b-109">**DWORD** -Unsigned Integer a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="15e6b-109">**dword** - 32-bit unsigned integer.</span></span>
-   <span data-ttu-id="15e6b-110">valore a virgola mobile a **metà** 16 bit.</span><span class="sxs-lookup"><span data-stu-id="15e6b-110">**half** - 16-bit floating point value.</span></span> <span data-ttu-id="15e6b-111">Questo tipo di dati viene fornito solo per la compatibilità con le lingue.</span><span class="sxs-lookup"><span data-stu-id="15e6b-111">This data type is provided only for language compatibility.</span></span> <span data-ttu-id="15e6b-112">Le destinazioni Direct3D 10 shader mappano tutti i tipi di dati a metà per i tipi di dati float.</span><span class="sxs-lookup"><span data-stu-id="15e6b-112">Direct3D 10 shader targets map all half data types to float data types.</span></span> <span data-ttu-id="15e6b-113">Non è possibile usare un tipo di dati Half in una variabile globale uniforme (usare il flag/GEC se si desidera questa funzionalità).</span><span class="sxs-lookup"><span data-stu-id="15e6b-113">A half data type cannot be used on a uniform global variable (use the /Gec flag if this functionality is desired).</span></span>
-   <span data-ttu-id="15e6b-114">**float** : valore a virgola mobile a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="15e6b-114">**float** - 32-bit floating point value.</span></span>
-   <span data-ttu-id="15e6b-115">valore a virgola mobile a 64 bit **doppio** .</span><span class="sxs-lookup"><span data-stu-id="15e6b-115">**double** - 64-bit floating point value.</span></span> <span data-ttu-id="15e6b-116">Non è possibile usare valori a precisione doppia come input e output per un flusso.</span><span class="sxs-lookup"><span data-stu-id="15e6b-116">You cannot use double precision values as inputs and outputs for a stream.</span></span> <span data-ttu-id="15e6b-117">Per passare valori a precisione doppia tra shader, dichiarare ogni **Double** come coppia di tipi di dati **uint** .</span><span class="sxs-lookup"><span data-stu-id="15e6b-117">To pass double precision values between shaders, declare each **double** as a pair of **uint** data types.</span></span> <span data-ttu-id="15e6b-118">Usare quindi la funzione [**asuint**](asuint.md) per comprimere ogni **Double** nella coppia di **uint** s e la funzione [**AsDouble**](asdouble.md) per decomprimere la coppia di **uint** di nuovo nel **valore Double**.</span><span class="sxs-lookup"><span data-stu-id="15e6b-118">Then, use the [**asuint**](asuint.md) function to pack each **double** into the pair of **uint** s and the [**asdouble**](asdouble.md) function to unpack the pair of **uint** s back into the **double**.</span></span>

<span data-ttu-id="15e6b-119">A partire da Windows 8 HLSL supporta anche i tipi di dati scalari con precisione minima.</span><span class="sxs-lookup"><span data-stu-id="15e6b-119">Starting with Windows 8 HLSL also supports minimum precision scalar data types.</span></span> <span data-ttu-id="15e6b-120">I driver grafici possono implementare tipi di dati scalari con precisione minima usando una precisione maggiore o uguale alla precisione dei bit specificata.</span><span class="sxs-lookup"><span data-stu-id="15e6b-120">Graphics drivers can implement minimum precision scalar data types by using any precision greater than or equal to their specified bit precision.</span></span> <span data-ttu-id="15e6b-121">Si consiglia di non basarsi sul comportamento di blocco o wrapping che dipende dalla precisione sottostante specifica.</span><span class="sxs-lookup"><span data-stu-id="15e6b-121">We recommend not to rely on clamping or wrapping behavior that depends on specific underlying precision.</span></span> <span data-ttu-id="15e6b-122">Ad esempio, il driver di grafica potrebbe eseguire operazioni aritmetiche su un valore **min16float** a una precisione completa a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="15e6b-122">For example, the graphics driver might execute arithmetic on a **min16float** value at full 32-bit precision.</span></span>

-   <span data-ttu-id="15e6b-123">**min16float** -valore minimo a virgola mobile a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="15e6b-123">**min16float** - minimum 16-bit floating point value.</span></span>
-   <span data-ttu-id="15e6b-124">**min10float** -valore a virgola mobile a 10 bit minimo.</span><span class="sxs-lookup"><span data-stu-id="15e6b-124">**min10float** - minimum 10-bit floating point value.</span></span>
-   <span data-ttu-id="15e6b-125">**min16int** -intero con segno a 16 bit minimo.</span><span class="sxs-lookup"><span data-stu-id="15e6b-125">**min16int** - minimum 16-bit signed integer.</span></span>
-   <span data-ttu-id="15e6b-126">**min12int** -valore intero con segno a 12 bit minimo.</span><span class="sxs-lookup"><span data-stu-id="15e6b-126">**min12int** - minimum 12-bit signed integer.</span></span>
-   <span data-ttu-id="15e6b-127">**min16uint** -unsigned integer minimo a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="15e6b-127">**min16uint** - minimum 16-bit unsigned integer.</span></span>

<span data-ttu-id="15e6b-128">Per ulteriori informazioni sui valori letterali scalari, vedere [grammatica](dx-graphics-hlsl-appendix-grammar.md).</span><span class="sxs-lookup"><span data-stu-id="15e6b-128">For more information about scalar literals, see [Grammar](dx-graphics-hlsl-appendix-grammar.md).</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="15e6b-129">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="15e6b-129">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="15e6b-130">In Direct3D 10 i tipi seguenti sono modificatori del tipo float.</span><span class="sxs-lookup"><span data-stu-id="15e6b-130">In Direct3D 10, the following types are modifiers to the float type.</span></span><br/>
<ul>
<li><span data-ttu-id="15e6b-131"><strong>russare float</strong> - IEEE a 32 bit con segno-float normalizzato nell'intervallo compreso tra 1 e 1.</span><span class="sxs-lookup"><span data-stu-id="15e6b-131"><strong>snorm float</strong> - IEEE 32-bit signed-normalized float in range -1 to 1 inclusive.</span></span></li>
<li><span data-ttu-id="15e6b-132"><strong>float unorm</strong> - IEEE a 32 bit senza segno: float normalizzato nell'intervallo compreso tra 0 e 1 inclusi.</span><span class="sxs-lookup"><span data-stu-id="15e6b-132"><strong>unorm float</strong> - IEEE 32-bit unsigned-normalized float in range 0 to 1 inclusive.</span></span></li>
</ul>
<span data-ttu-id="15e6b-133">Ecco ad esempio una dichiarazione con variabile float normalizzata a 4 componenti.</span><span class="sxs-lookup"><span data-stu-id="15e6b-133">For example, here is a 4-component signed-normalized float-variable declaration.</span></span><br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>snorm float4 fourComponentIEEEFloat;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 

## <a name="string-type"></a><span data-ttu-id="15e6b-134">Tipo di stringa</span><span class="sxs-lookup"><span data-stu-id="15e6b-134">String Type</span></span>

<span data-ttu-id="15e6b-135">HLSL supporta anche un tipo **stringa** , che è una stringa ASCII.</span><span class="sxs-lookup"><span data-stu-id="15e6b-135">HLSL also supports a **string** type, which is an ASCII string.</span></span> <span data-ttu-id="15e6b-136">Non sono presenti operazioni o Stati che accettano stringhe, ma gli effetti possono eseguire query su parametri e annotazioni di stringa.</span><span class="sxs-lookup"><span data-stu-id="15e6b-136">There are no operations or states that accept strings, but effects can query string parameters and annotations.</span></span>

## <a name="example"></a><span data-ttu-id="15e6b-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="15e6b-137">Example</span></span>

```c
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```

## <a name="see-also"></a><span data-ttu-id="15e6b-138">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="15e6b-138">See also</span></span>



* [<span data-ttu-id="15e6b-139">Dichiarazione di tipi scalari</span><span class="sxs-lookup"><span data-stu-id="15e6b-139">Declaring Scalar Types</span></span>](./dx-graphics-hlsl-writing-shaders-9.md#declaring-shader-variables)
* [<span data-ttu-id="15e6b-140">Tipi di dati (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="15e6b-140">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)