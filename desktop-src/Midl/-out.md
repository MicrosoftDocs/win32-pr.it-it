---
title: /out (opzione)
description: L'opzione/out specifica la directory predefinita in cui il compilatore MIDL scrive i file di output.
ms.assetid: 37cfe989-137a-4336-8c66-e6b9c23473df
keywords:
- opzione/out MIDL
topic_type:
- apiref
api_name:
- /out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d688f17957170c6f3a8887030ea2c67140c0ff8c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299185"
---
# <a name="out-switch"></a><span data-ttu-id="04bc5-104">/out (opzione)</span><span class="sxs-lookup"><span data-stu-id="04bc5-104">/out switch</span></span>

<span data-ttu-id="04bc5-105">L'opzione **/out** specifica la directory predefinita in cui il compilatore MIDL scrive i file di output.</span><span class="sxs-lookup"><span data-stu-id="04bc5-105">The **/out** switch specifies the default directory where the MIDL compiler writes output files.</span></span>

``` syntax
midl /out path-specification
```

## <a name="switch-options"></a><span data-ttu-id="04bc5-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="04bc5-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="04bc5-107">*Specifica percorso*</span><span class="sxs-lookup"><span data-stu-id="04bc5-107">*path-specification*</span></span> 
</dt> <dd>

<span data-ttu-id="04bc5-108">Specifica il percorso della directory in cui vengono generati lo stub, l'intestazione e i file di commutazione.</span><span class="sxs-lookup"><span data-stu-id="04bc5-108">Specifies the path to the directory in which the stub, header, and switch files are generated.</span></span> <span data-ttu-id="04bc5-109">È possibile specificare una specifica di unità, un percorso di directory assoluto o entrambi.</span><span class="sxs-lookup"><span data-stu-id="04bc5-109">A drive specification, an absolute directory path, or both can be specified.</span></span> <span data-ttu-id="04bc5-110">I percorsi possono essere racchiusi tra virgolette doppie (") per impedire alla shell di interpretare i caratteri speciali.</span><span class="sxs-lookup"><span data-stu-id="04bc5-110">Paths can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04bc5-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="04bc5-111">Remarks</span></span>

<span data-ttu-id="04bc5-112">La directory di output può essere specificata con una lettera di unità, un nome di percorso assoluto o entrambi.</span><span class="sxs-lookup"><span data-stu-id="04bc5-112">The output directory can be specified with a drive letter, an absolute path name, or both.</span></span> <span data-ttu-id="04bc5-113">È possibile utilizzare l'opzione **/out** con una qualsiasi delle opzioni che consentono la specifica del singolo file di output.</span><span class="sxs-lookup"><span data-stu-id="04bc5-113">The **/out** option can be used with any of the switches that enable individual output file specification.</span></span>

<span data-ttu-id="04bc5-114">Se non si specifica l'opzione **/out** , i file vengono scritti nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="04bc5-114">When the **/out** switch is not specified, files are written to the current directory.</span></span>

<span data-ttu-id="04bc5-115">La directory predefinita specificata dall'opzione **/out** può essere sostituita da un nome di percorso esplicito specificato come parte dell'opzione [**/cstub**](-cstub.md), [**/header**](-header.md), [**/proxy**](-proxy.md)o [**/sstub**](-sstub.md) .</span><span class="sxs-lookup"><span data-stu-id="04bc5-115">The default directory specified by the **/out** switch can be overridden by an explicit path name specified as part of the [**/cstub**](-cstub.md), [**/header**](-header.md), [**/proxy**](-proxy.md), or [**/sstub**](-sstub.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="04bc5-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="04bc5-116">Examples</span></span>

<span data-ttu-id="04bc5-117">**MIDL/out c: \\ mydir \\ mysubdir \\ SubDir2 più profondo nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="04bc5-117">**midl /out c:\\mydir\\mysubdir\\subdir2 deeper filename.idl**</span></span>

<span data-ttu-id="04bc5-118">**MIDL/out c: filename. idl**</span><span class="sxs-lookup"><span data-stu-id="04bc5-118">**midl /out c: filename.idl**</span></span>

<span data-ttu-id="04bc5-119">**MIDL/out \\ mydir \\ mysubdir \\ un altro nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="04bc5-119">**midl /out \\mydir\\mysubdir\\another filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="04bc5-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04bc5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04bc5-121">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="04bc5-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="04bc5-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="04bc5-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="04bc5-123">**/header**</span><span class="sxs-lookup"><span data-stu-id="04bc5-123">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="04bc5-124">**/proxy**</span><span class="sxs-lookup"><span data-stu-id="04bc5-124">**/proxy**</span></span>](-proxy.md)
</dt> <dt>

[<span data-ttu-id="04bc5-125">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="04bc5-125">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




