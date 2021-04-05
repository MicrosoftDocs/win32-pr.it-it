---
title: /h (opzione)
description: L'opzione/h è equivalente dal punto di vista funzionale all'opzione/header.
ms.assetid: 1b74d5f2-6624-4b71-832d-fb55a0e84c86
keywords:
- /h switch MIDL
topic_type:
- apiref
api_name:
- /h
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ff2cd7aa5e4b8386e0c9faecfaccd860207403
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045837"
---
# <a name="h-switch"></a><span data-ttu-id="df146-104">/h (opzione)</span><span class="sxs-lookup"><span data-stu-id="df146-104">/h switch</span></span>

<span data-ttu-id="df146-105">L'opzione **/h** è equivalente dal punto di vista funzionale all'opzione [**/header**](-header.md) .</span><span class="sxs-lookup"><span data-stu-id="df146-105">The **/h** option is functionally equivalent to the [**/header**](-header.md) option.</span></span>

``` syntax
midl /h filename
```

## <a name="switch-options"></a><span data-ttu-id="df146-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="df146-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="df146-107">*filename*</span><span class="sxs-lookup"><span data-stu-id="df146-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="df146-108">Specifica un nome di file di intestazione che esegue l'override del nome del file di intestazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="df146-108">Specifies a header file name that overrides the default header file name.</span></span> <span data-ttu-id="df146-109">I nomi di file possono essere racchiusi tra virgolette doppie (") per evitare che la shell interpreti caratteri speciali.</span><span class="sxs-lookup"><span data-stu-id="df146-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df146-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="df146-110">Remarks</span></span>

<span data-ttu-id="df146-111">L'opzione **/h** specifica *filename* come nome di un file di intestazione che contiene tutte le definizioni contenute nel file IDL, senza la sintassi IDL.</span><span class="sxs-lookup"><span data-stu-id="df146-111">The **/h** switch specifies *filename* as the name for a header file that contains all the definitions contained in the IDL file, without the IDL syntax.</span></span> <span data-ttu-id="df146-112">Questo file può essere usato come file di intestazione C o C++.</span><span class="sxs-lookup"><span data-stu-id="df146-112">This file can be used as a C or C++ header file.</span></span>

## <a name="examples"></a><span data-ttu-id="df146-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="df146-113">Examples</span></span>

<span data-ttu-id="df146-114">**MIDL/h tlibhead. h nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="df146-114">**midl /h tlibhead.h filename.idl**</span></span>

<span data-ttu-id="df146-115">**MIDL/h "MIDL. h" nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="df146-115">**midl /h "midl.h" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="df146-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df146-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df146-117">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="df146-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="df146-118">**/header**</span><span class="sxs-lookup"><span data-stu-id="df146-118">**/header**</span></span>](-header.md)
</dt> </dl>

 

 




