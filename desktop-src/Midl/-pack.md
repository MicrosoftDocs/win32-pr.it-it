---
title: opzione/Pack
description: L'opzione/Pack è uguale all'opzione/Zp.
ms.assetid: 381e3099-adb4-4219-bbb4-89c9e1dd3928
keywords:
- /Pack switch MIDL
topic_type:
- apiref
api_name:
- /pack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c807846148d81e0e59620046d9f24380fe647c11
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045860"
---
# <a name="pack-switch"></a><span data-ttu-id="03c58-104">opzione/Pack</span><span class="sxs-lookup"><span data-stu-id="03c58-104">/pack switch</span></span>

<span data-ttu-id="03c58-105">L'opzione **/Pack** è uguale all'opzione [**/ZP**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="03c58-105">The **/pack** switch is the same as the [**/Zp**](-zp.md) option.</span></span>

``` syntax
midl /pack packing_level
```

## <a name="switch-options"></a><span data-ttu-id="03c58-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="03c58-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="03c58-107">*livello di compressione \_*</span><span class="sxs-lookup"><span data-stu-id="03c58-107">*packing\_level*</span></span> 
</dt> <dd>

<span data-ttu-id="03c58-108">Specifica il livello di compressione delle strutture nel sistema di destinazione.</span><span class="sxs-lookup"><span data-stu-id="03c58-108">Specifies the packing level of structures in the target system.</span></span> <span data-ttu-id="03c58-109">Il valore a livello di compressione può essere impostato su 1, 2, 4 o 8.</span><span class="sxs-lookup"><span data-stu-id="03c58-109">The packing-level value can be set to 1, 2, 4, or 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03c58-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="03c58-110">Remarks</span></span>

<span data-ttu-id="03c58-111">L'opzione **/Pack** designa il livello di compressione delle strutture nel sistema di destinazione.</span><span class="sxs-lookup"><span data-stu-id="03c58-111">The **/pack** switch designates the packing level of structures in the target system.</span></span> <span data-ttu-id="03c58-112">Il valore a livello di compressione corrisponde al valore dell'opzione [**/ZP**](-zp.md) usato dal compilatore Microsoft C/C++ versione 7,0.</span><span class="sxs-lookup"><span data-stu-id="03c58-112">The packing-level value corresponds to the [**/Zp**](-zp.md) option value used by the Microsoft C/C++ version 7.0 compiler.</span></span> <span data-ttu-id="03c58-113">Per ulteriori informazioni, vedere la documentazione sulla programmazione in Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="03c58-113">For more information, see your Microsoft C/C++ programming documentation.</span></span>

<span data-ttu-id="03c58-114">Specificare lo stesso livello di compressione quando si richiama il compilatore MIDL e il compilatore C.</span><span class="sxs-lookup"><span data-stu-id="03c58-114">Specify the same packing level when you invoke the MIDL compiler and the C compiler.</span></span> <span data-ttu-id="03c58-115">Il livello di compressione predefinito utilizzato quando non viene specificata né l'opzione [**/ZP**](-zp.md) né **/Pack** è 8, in entrambi gli ambienti di compilazione.</span><span class="sxs-lookup"><span data-stu-id="03c58-115">The default packing level used when neither the [**/Zp**](-zp.md) nor **/pack** switch is specified is 8, in both all build environments.</span></span>

<span data-ttu-id="03c58-116">Per una descrizione dei potenziali rischi correlati all'uso di livelli di compressione non standard, vedere l'argomento della Guida di [**/ZP**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="03c58-116">For a discussion of the potential dangers in using nonstandard packing levels, see the [**/Zp**](-zp.md) help topic.</span></span>

## <a name="examples"></a><span data-ttu-id="03c58-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="03c58-117">Examples</span></span>

<span data-ttu-id="03c58-118">**MIDL/Pack 2 nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="03c58-118">**midl /pack 2 filename.idl**</span></span>

<span data-ttu-id="03c58-119">**MIDL/Pack 8 bar. idl**</span><span class="sxs-lookup"><span data-stu-id="03c58-119">**midl /pack 8 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="03c58-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03c58-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03c58-121">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="03c58-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="03c58-122">**/ENV**</span><span class="sxs-lookup"><span data-stu-id="03c58-122">**/env**</span></span>](-env.md)
</dt> <dt>

[<span data-ttu-id="03c58-123">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="03c58-123">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 




