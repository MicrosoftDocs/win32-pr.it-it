---
title: Archiviazione di un valore a 64 bit
description: Per archiviare un valore di puntatore a 64 bit, utilizzare ULONG \_ ptr. Un \_ valore PTR ULONG è 32 bit quando viene compilato con un compilatore a 32 bit e 64 bit quando viene compilato con un compilatore a 64 bit.
ms.assetid: 0712e084-cf5e-470a-8f5d-0db2ef638f42
keywords:
- archiviazione dei valori a 64 bit programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cee4826caf93dbd464957fb5fb76f024bd9f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330031"
---
# <a name="storing-a-64-bit-value"></a><span data-ttu-id="94e72-105">Archiviazione di un valore a 64 bit</span><span class="sxs-lookup"><span data-stu-id="94e72-105">Storing a 64-bit Value</span></span>

<span data-ttu-id="94e72-106">Per archiviare un valore di puntatore a 64 bit, utilizzare **ULONG \_ ptr**.</span><span class="sxs-lookup"><span data-stu-id="94e72-106">To store a 64-bit pointer value, use **ULONG\_PTR**.</span></span> <span data-ttu-id="94e72-107">Un **valore \_ ptr ULONG** è 32 bit quando viene compilato con un compilatore a 32 bit e 64 bit quando viene compilato con un compilatore a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="94e72-107">A **ULONG\_PTR** value is 32 bits when compiled with a 32-bit compiler and 64 bits when compiled with a 64-bit compiler.</span></span>

<span data-ttu-id="94e72-108">Negli esempi seguenti viene usato codice reale che è stato trasferito in Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="94e72-108">The following examples use real-world code that has been ported to 64-bit Windows.</span></span> <span data-ttu-id="94e72-109">Il commento sulla procedura per rendere compatibile il codice a 64 bit è incluso.</span><span class="sxs-lookup"><span data-stu-id="94e72-109">Commentary on the steps to make the code 64-bit compatible is included.</span></span>

## <a name="example-1-getting-an-address"></a><span data-ttu-id="94e72-110">Esempio 1: recupero di un indirizzo</span><span class="sxs-lookup"><span data-stu-id="94e72-110">Example 1: Getting an Address</span></span>

<span data-ttu-id="94e72-111">Il codice seguente illustra un modo portatile per ottenere un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="94e72-111">The following code illustrates a portable way to get an address.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="94e72-112">Uso di ULONG (metodo solo a 32 bit)</span><span class="sxs-lookup"><span data-stu-id="94e72-112">Using ULONG (a 32-bit-only method)</span></span></td>
<td><pre class="syntax" data-space="preserve"><code>ULONG getAnAddress( )
Int *somePointer
Return( (ULONG) somePointer );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="94e72-113">Uso di ULONG_PTR (metodo portatile)</span><span class="sxs-lookup"><span data-stu-id="94e72-113">Using ULONG_PTR (the portable method)</span></span></td>
<td><pre class="syntax" data-space="preserve"><code>ULONG_PTR getAnAddress( )
Int *somePointer
Return( (ULONG_PTR) somePointer );</code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="example-2-calculating-an-address"></a><span data-ttu-id="94e72-114">Esempio 2: calcolo di un indirizzo</span><span class="sxs-lookup"><span data-stu-id="94e72-114">Example 2: Calculating an Address</span></span>

<span data-ttu-id="94e72-115">Il codice seguente illustra un modo portatile per calcolare un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="94e72-115">The following code illustrates a portable way to calculate an address.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="94e72-116">Uso di ULONG (metodo solo a 32 bit)</span><span class="sxs-lookup"><span data-stu-id="94e72-116">Using ULONG (a 32-bit-only method)</span></span></td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG)someOtherPointer + 0x20 );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="94e72-117">Uso di ULONG_PTR (metodo portatile)</span><span class="sxs-lookup"><span data-stu-id="94e72-117">Using ULONG_PTR (the portable method)</span></span></td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG_PTR)someOtherPointer + 0x20 );</code></pre></td>
</tr>
</tbody>
</table>



 

 

 




