---
title: Opzione/Zp
description: L'opzione/Zp è uguale all'opzione/Pack.
ms.assetid: ccdae6a5-e53c-4ddc-9f5f-2b2118709fdb
keywords:
- /ZP switch MIDL
topic_type:
- apiref
api_name:
- /Zp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553d99dee7dd08218680fc0b43e6e12237c4f8fa
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718160"
---
# <a name="zp-switch"></a><span data-ttu-id="0587e-104">Opzione/Zp</span><span class="sxs-lookup"><span data-stu-id="0587e-104">/Zp switch</span></span>

<span data-ttu-id="0587e-105">L'opzione **/ZP** è uguale all'opzione [**/Pack**](-pack.md) .</span><span class="sxs-lookup"><span data-stu-id="0587e-105">The **/Zp** switch is the same as the [**/pack**](-pack.md) option.</span></span>

``` syntax
midl /Zp packing_level
```

## <a name="switch-options"></a><span data-ttu-id="0587e-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="0587e-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="0587e-107">*livello di compressione \_*</span><span class="sxs-lookup"><span data-stu-id="0587e-107">*packing\_level*</span></span> 
</dt> <dd>

<span data-ttu-id="0587e-108">Specifica il livello di compressione delle strutture nel sistema di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0587e-108">Specifies the packing level of structures in the target system.</span></span> <span data-ttu-id="0587e-109">Il valore a livello di compressione può essere impostato su 1, 2, 4 o 8.</span><span class="sxs-lookup"><span data-stu-id="0587e-109">The packing-level value can be set to 1, 2, 4, or 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0587e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="0587e-110">Remarks</span></span>

<span data-ttu-id="0587e-111">L'opzione **/ZP** designa il livello di compressione delle strutture nel sistema di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0587e-111">The **/Zp** switch designates the packing level of structures in the target system.</span></span> <span data-ttu-id="0587e-112">Il valore a livello di compressione corrisponde al valore dell'opzione **/ZP** usato dal compilatore Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="0587e-112">The packing-level value corresponds to the **/Zp** option value used by the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="0587e-113">Per ulteriori informazioni, vedere la documentazione sulla programmazione in Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="0587e-113">For more information, see your Microsoft C/C++ programming documentation.</span></span>

<span data-ttu-id="0587e-114">Specificare lo stesso livello di compressione quando si richiama il compilatore MIDL e il compilatore C.</span><span class="sxs-lookup"><span data-stu-id="0587e-114">Specify the same packing level when you invoke the MIDL compiler and the C compiler.</span></span>

<span data-ttu-id="0587e-115">Il livello di compressione predefinito utilizzato quando non viene specificata né l'opzione **/ZP** né [**/Pack**](-pack.md) è 8 in tutti gli ambienti di compilazione.</span><span class="sxs-lookup"><span data-stu-id="0587e-115">The default packing level used when neither the **/Zp** nor [**/pack**](-pack.md) switch is specified is 8 in all build environments.</span></span>

> [!Note]  
> <span data-ttu-id="0587e-116">Non usare **/Zp1** o **/ZP2** su piattaforme MIPS o Alpha e non usare **/zp4** o **/ZP8** su piattaforme a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="0587e-116">Do not use **/Zp1** or **/Zp2** on MIPS or Alpha platforms and do not use **/Zp4** or **/Zp8** on 16-bit platforms.</span></span> <span data-ttu-id="0587e-117">A seconda del tipo di dati e della posizione di memoria assegnati dal compilatore C in fase di esecuzione, può verificarsi un'eccezione di allineamento dei dati sulle piattaforme MIPS e Alpha.</span><span class="sxs-lookup"><span data-stu-id="0587e-117">Depending on the data type and memory location assigned by the C compiler at run time, this can result in a data misalignment exception on MIPS and Alpha platforms.</span></span> <span data-ttu-id="0587e-118">Sulle piattaforme MS-DOS, il compilatore C non assicurerà l'allineamento a 4 o 8, quindi l'applicazione potrebbe terminare.</span><span class="sxs-lookup"><span data-stu-id="0587e-118">On MS-DOS platforms, the C compiler will not ensure the alignment at 4 or 8, and so the application may terminate.</span></span>

 

## <a name="examples"></a><span data-ttu-id="0587e-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="0587e-119">Examples</span></span>

<span data-ttu-id="0587e-120">**MIDL/zp4 nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="0587e-120">**midl /Zp4 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="0587e-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0587e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0587e-122">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="0587e-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="0587e-123">**/Pack**</span><span class="sxs-lookup"><span data-stu-id="0587e-123">**/pack**</span></span>](-pack.md)
</dt> </dl>

 

 




