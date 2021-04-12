---
title: opzione/IID
description: L'opzione/IID specifica il nome del file dell'identificatore di interfaccia per un'interfaccia COM, eseguendo l'override del nome predefinito ottenuto aggiungendo \_ i. c al nome del file IDL.
ms.assetid: 051593f5-e612-4b19-94e5-d7885dbede21
keywords:
- /IID switch MIDL
topic_type:
- apiref
api_name:
- /iid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631a28f1bc5a1a24253c9416104df9941cd8da33
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397874"
---
# <a name="iid-switch"></a><span data-ttu-id="51e6e-104">opzione/IID</span><span class="sxs-lookup"><span data-stu-id="51e6e-104">/iid switch</span></span>

<span data-ttu-id="51e6e-105">L'opzione **/IID** specifica il nome del file dell'identificatore di interfaccia per un'interfaccia com, eseguendo l'override del nome predefinito ottenuto aggiungendo \_ i. c al nome del file IDL.</span><span class="sxs-lookup"><span data-stu-id="51e6e-105">The **/iid** switch specifies the name of the interface identifier file for a COM interface, overriding the default name obtained by adding \_i.c to the IDL file name.</span></span>

``` syntax
midl /iid filename
```

## <a name="switch-options"></a><span data-ttu-id="51e6e-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="51e6e-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="51e6e-107">*filename*</span><span class="sxs-lookup"><span data-stu-id="51e6e-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="51e6e-108">Specifica un nome di file dell'identificatore di interfaccia che sostituisce il nome del file dell'identificatore di interfaccia predefinito per un'interfaccia COM.</span><span class="sxs-lookup"><span data-stu-id="51e6e-108">Specifies an interface identifier file name that overrides the default interface identifier file name for a COM interface.</span></span> <span data-ttu-id="51e6e-109">I nomi di file possono essere racchiusi tra virgolette doppie (") per impedire alla shell di interpretare i caratteri speciali.</span><span class="sxs-lookup"><span data-stu-id="51e6e-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51e6e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="51e6e-110">Remarks</span></span>

<span data-ttu-id="51e6e-111">L'opzione **/IID** non influisce sulle interfacce RPC.</span><span class="sxs-lookup"><span data-stu-id="51e6e-111">The **/iid** switch does not affect RPC interfaces.</span></span>

<span data-ttu-id="51e6e-112">Se *filename* non include un percorso esplicito, il file viene scritto nella directory corrente o nella directory specificata dall'opzione [**/out**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="51e6e-112">If *filename* does not include an explicit path, the file is written to the current directory or to the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="51e6e-113">Un percorso esplicito in *filename* esegue l'override della specifica del Commuter **/out** .</span><span class="sxs-lookup"><span data-stu-id="51e6e-113">An explicit path in *filename* overrides the **/out** switch specification.</span></span>

## <a name="examples"></a><span data-ttu-id="51e6e-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="51e6e-114">Examples</span></span>

<span data-ttu-id="51e6e-115">**MIDL/IID "My \_ IID. c" nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="51e6e-115">**midl /iid "my\_iid.c" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="51e6e-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51e6e-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51e6e-117">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="51e6e-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="51e6e-118">**/header**</span><span class="sxs-lookup"><span data-stu-id="51e6e-118">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="51e6e-119">**/out**</span><span class="sxs-lookup"><span data-stu-id="51e6e-119">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="51e6e-120">**/proxy**</span><span class="sxs-lookup"><span data-stu-id="51e6e-120">**/proxy**</span></span>](-proxy.md)
</dt> </dl>

 

 




