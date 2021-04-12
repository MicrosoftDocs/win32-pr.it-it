---
title: /opzione di sistema
description: Il parametro/System indica al compilatore MIDL di generare una libreria dei tipi per il sistema specificato. Il valore predefinito è il sistema operativo corrente.
ms.assetid: 0fb69ffc-5ab4-49f3-b34d-859da776ce9e
keywords:
- /opzione di sistema MIDL
topic_type:
- apiref
api_name:
- / system
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e09f2cf97f8edb86ad831cff35420fad9a07d76
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334167"
---
# <a name="system-switch"></a><span data-ttu-id="20fe6-105">/<system> commutatore</span><span class="sxs-lookup"><span data-stu-id="20fe6-105">/<system> switch</span></span>

<span data-ttu-id="20fe6-106">L' **/<system>** opzione indica al compilatore MIDL di generare una libreria dei tipi per il sistema specificato.</span><span class="sxs-lookup"><span data-stu-id="20fe6-106">The **/<system>** switch directs the MIDL compiler to generate a type library for the specified system.</span></span> <span data-ttu-id="20fe6-107">Il valore predefinito è il sistema operativo corrente.</span><span class="sxs-lookup"><span data-stu-id="20fe6-107">The default is the current operating system.</span></span>

``` syntax
midl /{win32 | ia64 | amd64}
```

## <a name="switch-options"></a><span data-ttu-id="20fe6-108">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="20fe6-108">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span data-ttu-id="20fe6-109"><span id="win32"></span><span id="WIN32"></span>Win32 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="20fe6-109"><span id="win32"></span><span id="WIN32"></span>\*\*\*\*win32\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="20fe6-110">Windows 2000, Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="20fe6-110">Windows 2000, Windows XP, Windows Vista, Windows 7</span></span>

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span data-ttu-id="20fe6-111"><span id="ia64"></span><span id="IA64"></span>ia64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="20fe6-111"><span id="ia64"></span><span id="IA64"></span>\*\*\*\*ia64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="20fe6-112">Un ambiente Windows basato su Intel a 64 bit, ad esempio Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="20fe6-112">An Intel-based 64-bit Windows environment such as Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista, or Windows 7.</span></span>

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span data-ttu-id="20fe6-113"><span id="amd64"></span><span id="AMD64"></span>amd64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="20fe6-113"><span id="amd64"></span><span id="AMD64"></span>\*\*\*\*amd64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="20fe6-114">Un ambiente Windows a 64 bit basato sui dispositivi statunitensi, ad esempio Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="20fe6-114">An American Micro Devices-based 64-bit Windows environment such as Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista, or Windows 7.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20fe6-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="20fe6-115">Remarks</span></span>

<span data-ttu-id="20fe6-116">Lo **/<system>** Switch è funzionalmente uguale all'opzione MIDL [**/ENV**](-env.md) e viene riconosciuto dal compilatore MIDL esclusivamente per la compatibilità con le versioni precedenti di mktyplib.</span><span class="sxs-lookup"><span data-stu-id="20fe6-116">The **/<system>** switch is functionally the same as the MIDL [**/env**](-env.md) option and is recognized by the MIDL compiler solely for backward compatibility with MkTypLib.</span></span> <span data-ttu-id="20fe6-117">Se si sta generando un nuovo Makefile, usare l'opzione **/ENV** .</span><span class="sxs-lookup"><span data-stu-id="20fe6-117">If you are generating a new makefile, use the **/env** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="20fe6-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="20fe6-118">Examples</span></span>

<span data-ttu-id="20fe6-119">**MIDL/Win32 nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="20fe6-119">**midl /win32 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="20fe6-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20fe6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20fe6-121">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="20fe6-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="20fe6-122">**/ENV**</span><span class="sxs-lookup"><span data-stu-id="20fe6-122">**/env**</span></span>](-env.md)
</dt> </dl>

 

 




