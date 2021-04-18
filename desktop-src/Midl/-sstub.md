---
title: opzione/sstub
description: L'opzione/sstub specifica il nome del file stub del server per un'interfaccia RPC.
ms.assetid: 8e695e81-7c1b-40c0-aeaa-5390512fa099
keywords:
- /sstub switch MIDL
topic_type:
- apiref
api_name:
- /sstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 131be3dd1890967f7107bea64c3dc2634833653d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299173"
---
# <a name="sstub-switch"></a><span data-ttu-id="de9e2-104">opzione/sstub</span><span class="sxs-lookup"><span data-stu-id="de9e2-104">/sstub switch</span></span>

<span data-ttu-id="de9e2-105">L'opzione **/sstub** specifica il nome del file stub del server per un'interfaccia RPC.</span><span class="sxs-lookup"><span data-stu-id="de9e2-105">The **/sstub** switch specifies the name of the server stub file for an RPC interface.</span></span>

``` syntax
midl /sstub stub_file_name
```

## <a name="switch-options"></a><span data-ttu-id="de9e2-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="de9e2-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="de9e2-107">*\_nome file \_ Stub*</span><span class="sxs-lookup"><span data-stu-id="de9e2-107">*stub\_file\_name*</span></span> 
</dt> <dd>

<span data-ttu-id="de9e2-108">Specifica un nome file che esegue l'override del nome del file stub del server predefinito.</span><span class="sxs-lookup"><span data-stu-id="de9e2-108">Specifies a file name that overrides the default server stub file name.</span></span> <span data-ttu-id="de9e2-109">I nomi di file possono essere racchiusi tra virgolette doppie (") per impedire alla shell di interpretare i caratteri speciali.</span><span class="sxs-lookup"><span data-stu-id="de9e2-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de9e2-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="de9e2-110">Remarks</span></span>

<span data-ttu-id="de9e2-111">Il nome file specificato sostituisce il nome file predefinito.</span><span class="sxs-lookup"><span data-stu-id="de9e2-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="de9e2-112">Per impostazione predefinita, il nome del file viene ottenuto aggiungendo \_ S. C al nome del file IDL.</span><span class="sxs-lookup"><span data-stu-id="de9e2-112">By default, the file name is obtained by adding \_S.C to the name of the IDL file.</span></span> <span data-ttu-id="de9e2-113">Questa opzione non influisce sulle interfacce OLE.</span><span class="sxs-lookup"><span data-stu-id="de9e2-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="de9e2-114">Quando si importano file, il nome file specificato si applica a un solo file stub, ovvero il file stub che corrisponde al file IDL specificato nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="de9e2-114">When you are importing files, the specified file name applies to only one stub file — the stub file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="de9e2-115">Se *il \_ \_ nome del file stub* non include un percorso esplicito, il file viene scritto nella directory corrente o nella directory specificata dall'opzione [**/out**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="de9e2-115">If *stub\_file\_name* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="de9e2-116">Un percorso esplicito *nel \_ \_ nome del file stub* esegue l'override della specifica del comcambio **/out** .</span><span class="sxs-lookup"><span data-stu-id="de9e2-116">An explicit path in *stub\_file\_name* overrides the **/out** switch specification.</span></span>

<span data-ttu-id="de9e2-117">L'opzione **/Server** None ha la precedenza sull'opzione **/sstub**</span><span class="sxs-lookup"><span data-stu-id="de9e2-117">The **/server** none switch takes precedence over the **/sstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="de9e2-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="de9e2-118">Examples</span></span>

<span data-ttu-id="de9e2-119">**MIDL/sstub My \_ sstub. c filename. idl**</span><span class="sxs-lookup"><span data-stu-id="de9e2-119">**midl /sstub my\_sstub.c filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="de9e2-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de9e2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de9e2-121">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="de9e2-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="de9e2-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="de9e2-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="de9e2-123">**/header**</span><span class="sxs-lookup"><span data-stu-id="de9e2-123">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="de9e2-124">**/out**</span><span class="sxs-lookup"><span data-stu-id="de9e2-124">**/out**</span></span>](-out.md)
</dt> </dl>

 

 




