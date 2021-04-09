---
title: Output del compilatore MIDL
description: Con i file IDL e ACF come input, il compilatore MIDL genera fino a cinque file di origine in linguaggio C.
ms.assetid: 151bd643-1da0-4b33-b8a3-3d7037e63319
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb45bb369ea9d5faa695bf2658f3bafe2b3cb3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044348"
---
# <a name="midl-compiler-output"></a><span data-ttu-id="996f4-103">Output del compilatore MIDL</span><span class="sxs-lookup"><span data-stu-id="996f4-103">MIDL Compiler Output</span></span>

<span data-ttu-id="996f4-104">Con i file IDL e ACF come input, il compilatore MIDL genera fino a cinque file di origine in linguaggio C.</span><span class="sxs-lookup"><span data-stu-id="996f4-104">With the IDL and ACF files as input, the MIDL compiler generates up to five C-language source files.</span></span> <span data-ttu-id="996f4-105">Per impostazione predefinita, il compilatore MIDL usa il nome del file di base del file IDL come parte dei file stub generati.</span><span class="sxs-lookup"><span data-stu-id="996f4-105">By default, the MIDL compiler uses the base file name of the IDL file as part of the generated stub files.</span></span> <span data-ttu-id="996f4-106">Quando nel nome del file di base sono presenti più di sei caratteri, è possibile che alcuni file System non accettino il nome dello stub completo.</span><span class="sxs-lookup"><span data-stu-id="996f4-106">When more than six characters are present in the base file name, some file systems may not accept the full stub name.</span></span> <span data-ttu-id="996f4-107">Nella tabella seguente vengono illustrate le convenzioni utilizzate per i nomi di file.</span><span class="sxs-lookup"><span data-stu-id="996f4-107">The following table shows conventions used for file names.</span></span>



| <span data-ttu-id="996f4-108">File</span><span class="sxs-lookup"><span data-stu-id="996f4-108">File</span></span>        | <span data-ttu-id="996f4-109">Parte predefinita del nome del file di base</span><span class="sxs-lookup"><span data-stu-id="996f4-109">Default portion of base file name</span></span> | <span data-ttu-id="996f4-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="996f4-110">Example</span></span>      |
|-------------|-----------------------------------|--------------|
| <span data-ttu-id="996f4-111">File IDL</span><span class="sxs-lookup"><span data-stu-id="996f4-111">IDL file</span></span>    | ---                               | <span data-ttu-id="996f4-112">Abcdefgh. idl</span><span class="sxs-lookup"><span data-stu-id="996f4-112">Abcdefgh.idl</span></span> |
| <span data-ttu-id="996f4-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="996f4-113">Header</span></span>      | <span data-ttu-id="996f4-114">.h</span><span class="sxs-lookup"><span data-stu-id="996f4-114">.h</span></span>                                | <span data-ttu-id="996f4-115">Abcdef. h</span><span class="sxs-lookup"><span data-stu-id="996f4-115">Abcdef.h</span></span>     |
| <span data-ttu-id="996f4-116">Stub client</span><span class="sxs-lookup"><span data-stu-id="996f4-116">Client stub</span></span> | <span data-ttu-id="996f4-117">\_c. c</span><span class="sxs-lookup"><span data-stu-id="996f4-117">\_c.c</span></span>                             | <span data-ttu-id="996f4-118">Abcdef \_ c. c</span><span class="sxs-lookup"><span data-stu-id="996f4-118">Abcdef\_c.c</span></span>  |
| <span data-ttu-id="996f4-119">Stub server</span><span class="sxs-lookup"><span data-stu-id="996f4-119">Server stub</span></span> | <span data-ttu-id="996f4-120">\_s. c</span><span class="sxs-lookup"><span data-stu-id="996f4-120">\_s.c</span></span>                             | <span data-ttu-id="996f4-121">Abcdef \_ s. c</span><span class="sxs-lookup"><span data-stu-id="996f4-121">Abcdef\_s.c</span></span>  |



 

 

 




