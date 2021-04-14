---
title: opzione/header
description: L'opzione/header specifica il nome del file di intestazione.
ms.assetid: d36cb6c9-df57-4ef4-aff3-9968ac8ac001
keywords:
- /header switch MIDL
topic_type:
- apiref
api_name:
- /header
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816310f0b584f3c30d351e0d036e1f18c2f23962
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397878"
---
# <a name="header-switch"></a><span data-ttu-id="c2a1d-104">opzione/header</span><span class="sxs-lookup"><span data-stu-id="c2a1d-104">/header switch</span></span>

<span data-ttu-id="c2a1d-105">L'opzione **/header** specifica il nome del file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-105">The **/header** switch specifies the name of the header file.</span></span>

``` syntax
midl /header filename
```

## <a name="switch-options"></a><span data-ttu-id="c2a1d-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="c2a1d-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="c2a1d-107">*filename*</span><span class="sxs-lookup"><span data-stu-id="c2a1d-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="c2a1d-108">Specifica un nome di file di intestazione che esegue l'override del nome del file di intestazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-108">Specifies a header file name that overrides the default header file name.</span></span> <span data-ttu-id="c2a1d-109">I nomi di file possono essere racchiusi tra virgolette doppie (") per evitare che la shell interpreti caratteri speciali.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2a1d-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2a1d-110">Remarks</span></span>

<span data-ttu-id="c2a1d-111">Il nome file specificato sostituisce il nome file predefinito.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="c2a1d-112">Il nome file predefinito viene ottenuto sostituendo l'estensione del nome file IDL (in genere IDL) con l'estensione di file. h.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-112">The default file name is obtained by replacing the IDL file name extension (usually .idl) with the file name extension .h.</span></span> <span data-ttu-id="c2a1d-113">Per le interfacce OLE, l'opzione **/header** sostituisce il nome predefinito del file di intestazione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-113">For OLE interfaces, the **/header** switch overrides the default name of the interface header file.</span></span>

<span data-ttu-id="c2a1d-114">Quando si importano file, il nome file specificato si applica a un solo file di intestazione, ovvero il file di intestazione che corrisponde al file IDL specificato nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-114">When you are importing files, the specified file name applies to only one header file — the header file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="c2a1d-115">Se *filename* non include un percorso esplicito, il file viene scritto nella directory corrente o nella directory specificata dall'opzione [**/out**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="c2a1d-115">If *filename* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="c2a1d-116">Un percorso esplicito in *filename* esegue l'override della specifica del Commuter **/out** .</span><span class="sxs-lookup"><span data-stu-id="c2a1d-116">An explicit path in *filename* overrides the **/out** switch specification.</span></span>

## <a name="examples"></a><span data-ttu-id="c2a1d-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="c2a1d-117">Examples</span></span>

<span data-ttu-id="c2a1d-118">**MIDL/header "bar. h" nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="c2a1d-118">**midl /header "bar.h" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="c2a1d-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2a1d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2a1d-120">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="c2a1d-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="c2a1d-121">**/h**</span><span class="sxs-lookup"><span data-stu-id="c2a1d-121">**/h**</span></span>](-h.md)
</dt> <dt>

[<span data-ttu-id="c2a1d-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="c2a1d-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="c2a1d-123">**/out**</span><span class="sxs-lookup"><span data-stu-id="c2a1d-123">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="c2a1d-124">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="c2a1d-124">**/sstub**</span></span>](-sstub.md)
</dt> <dt>

[<span data-ttu-id="c2a1d-125">**/proxy**</span><span class="sxs-lookup"><span data-stu-id="c2a1d-125">**/proxy**</span></span>](-proxy.md)
</dt> </dl>

 

 




