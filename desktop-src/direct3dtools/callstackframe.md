---
description: Rappresenta le informazioni su un frame in stack.
MS-HAID: vspixengine.CallStackFrame
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura CallStackFrame
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50941BA0-968D-4341-8BF5-854FBDE8BD0C
api_name:
- CallStackFrame
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: fbe527c59a64e91f46a390344ea576c7560ef1f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304040"
---
# <a name="span-idvspixenginecallstackframespancallstackframe-structure"></a><span data-ttu-id="6a489-103"><span id="vspixengine.callstackframe"></span>Struttura CallStackFrame</span><span class="sxs-lookup"><span data-stu-id="6a489-103"><span id="vspixengine.callstackframe"></span>CallStackFrame structure</span></span>

<span data-ttu-id="6a489-104">Rappresenta le informazioni su un frame in stack.</span><span class="sxs-lookup"><span data-stu-id="6a489-104">Represents information about a frame on the callstack.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a489-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a489-105">Syntax</span></span>


```C++
} CallStackFrame;
```

## <a name="members"></a><span data-ttu-id="6a489-106">Members</span><span class="sxs-lookup"><span data-stu-id="6a489-106">Members</span></span>

<span data-ttu-id="6a489-107">**functionName**</span><span class="sxs-lookup"><span data-stu-id="6a489-107">**functionName**</span></span>  
<span data-ttu-id="6a489-108">Stringa COM contenente il nome della funzione associata.</span><span class="sxs-lookup"><span data-stu-id="6a489-108">A COM string containing the name of the associated function.</span></span>

<span data-ttu-id="6a489-109">**sourceFile**</span><span class="sxs-lookup"><span data-stu-id="6a489-109">**sourceFile**</span></span>  
<span data-ttu-id="6a489-110">Stringa COM contenente il percorso del file di origine associato.</span><span class="sxs-lookup"><span data-stu-id="6a489-110">A COM string containing the filepath of the associated source file.</span></span>

<span data-ttu-id="6a489-111">**moduleName**</span><span class="sxs-lookup"><span data-stu-id="6a489-111">**moduleName**</span></span>  
<span data-ttu-id="6a489-112">Stringa COM contenente il nome del modulo di codice associato.</span><span class="sxs-lookup"><span data-stu-id="6a489-112">A COM string containing the name of the associated code module.</span></span>

<span data-ttu-id="6a489-113">**lineNumber**</span><span class="sxs-lookup"><span data-stu-id="6a489-113">**lineNumber**</span></span>  
<span data-ttu-id="6a489-114">Numero di riga associato.</span><span class="sxs-lookup"><span data-stu-id="6a489-114">The associated line number.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a489-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a489-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6a489-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a489-116">Header</span></span></p></td><td><span data-ttu-id="6a489-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6a489-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



