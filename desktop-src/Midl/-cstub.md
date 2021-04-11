---
title: opzione/cstub
description: L'opzione/cstub specifica il nome del file stub client per un'interfaccia RPC.
ms.assetid: f2c9e083-3511-4e72-b1d1-14a3a662ffaf
keywords:
- /cstub switch MIDL
topic_type:
- apiref
api_name:
- /cstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 878f6eee47deaac3887c3f9936c18b0185cc807a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334572"
---
# <a name="cstub-switch"></a><span data-ttu-id="0d7a0-104">opzione/cstub</span><span class="sxs-lookup"><span data-stu-id="0d7a0-104">/cstub switch</span></span>

<span data-ttu-id="0d7a0-105">L'opzione **/cstub** specifica il nome del file stub client per un'interfaccia RPC.</span><span class="sxs-lookup"><span data-stu-id="0d7a0-105">The **/cstub** switch specifies the name of the client stub file for an RPC interface.</span></span>

``` syntax
midl /cstub stub_file_name
```

## <a name="switch-options"></a><span data-ttu-id="0d7a0-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="0d7a0-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="0d7a0-107">*\_nome file \_ Stub*</span><span class="sxs-lookup"><span data-stu-id="0d7a0-107">*stub\_file\_name*</span></span> 
</dt> <dd>

<span data-ttu-id="0d7a0-108">Specifica un nome file che esegue l'override del nome del file stub client predefinito.</span><span class="sxs-lookup"><span data-stu-id="0d7a0-108">Specifies a file name that overrides the default client stub file name.</span></span> <span data-ttu-id="0d7a0-109">I nomi di file possono essere racchiusi tra virgolette doppie (") per impedire alla shell di interpretare i caratteri speciali.</span><span class="sxs-lookup"><span data-stu-id="0d7a0-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d7a0-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d7a0-110">Remarks</span></span>

<span data-ttu-id="0d7a0-111">Il nome file specificato sostituisce il nome file predefinito.</span><span class="sxs-lookup"><span data-stu-id="0d7a0-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="0d7a0-112">Per impostazione predefinita, il nome del file viene ottenuto aggiungendo l'estensione \_ c. c al nome del file IDL.</span><span class="sxs-lookup"><span data-stu-id="0d7a0-112">By default, the file name is obtained by adding the extension \_c.c to the name of the IDL file.</span></span> <span data-ttu-id="0d7a0-113">Questa opzione non influisce sulle interfacce OLE.</span><span class="sxs-lookup"><span data-stu-id="0d7a0-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="0d7a0-114">Quando si importano file, il nome file specificato si applica a un solo file stub, ovvero il file stub che corrisponde al file IDL specificato nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="0d7a0-114">When you are importing files, the specified file name applies to only one stub file — the stub file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="0d7a0-115">Se *il \_ \_ nome del file stub* non include un percorso esplicito, il file viene scritto nella directory corrente o nella directory specificata dall'opzione [**/out**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="0d7a0-115">If *stub\_file\_name* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="0d7a0-116">Un percorso esplicito *nel \_ \_ nome del file stub* esegue l'override della specifica del comcambio **/out** .</span><span class="sxs-lookup"><span data-stu-id="0d7a0-116">An explicit path in *stub\_file\_name* overrides the **/out** switch specification.</span></span>

<span data-ttu-id="0d7a0-117">L'opzione **/client** None ha la precedenza sull'opzione **/cstub** .</span><span class="sxs-lookup"><span data-stu-id="0d7a0-117">The **/client** none switch takes precedence over the **/cstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="0d7a0-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="0d7a0-118">Examples</span></span>

<span data-ttu-id="0d7a0-119">**MIDL/cstub My \_ cstub. c filename. idl**</span><span class="sxs-lookup"><span data-stu-id="0d7a0-119">**midl /cstub my\_cstub.c filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="0d7a0-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d7a0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d7a0-121">**/header**</span><span class="sxs-lookup"><span data-stu-id="0d7a0-121">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="0d7a0-122">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="0d7a0-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="0d7a0-123">**/out**</span><span class="sxs-lookup"><span data-stu-id="0d7a0-123">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="0d7a0-124">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="0d7a0-124">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




