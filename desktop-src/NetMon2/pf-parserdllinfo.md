---
description: La \_ struttura PF PARSERDLLINFO definisce i parser presenti nella dll del parser.
ms.assetid: a7473b58-7767-4224-be3b-e96132d98adf
title: Struttura PF_PARSERDLLINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERDLLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ab4a3673c567a72cb5d0284a07d5603913e77550
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967895"
---
# <a name="pf_parserdllinfo-structure"></a><span data-ttu-id="725c7-103">\_Struttura PF PARSERDLLINFO</span><span class="sxs-lookup"><span data-stu-id="725c7-103">PF\_PARSERDLLINFO structure</span></span>

<span data-ttu-id="725c7-104">La struttura **PF \_ PARSERDLLINFO** definisce i parser presenti nella dll del parser.</span><span class="sxs-lookup"><span data-stu-id="725c7-104">The **PF\_PARSERDLLINFO** structure defines the parsers located in the parser DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="725c7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="725c7-105">Syntax</span></span>


```C++
typedef struct _PF_PARSERDLLINFO {
  DWORD         nParsers;
  PF_PARSERINFO ParserInfo[];
} PF_PARSERDLLINFO, *PPF_PARSERDLLINFO;
```



## <a name="members"></a><span data-ttu-id="725c7-106">Members</span><span class="sxs-lookup"><span data-stu-id="725c7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="725c7-107">**nParsers**</span><span class="sxs-lookup"><span data-stu-id="725c7-107">**nParsers**</span></span>
</dt> <dd>

<span data-ttu-id="725c7-108">Numero di parser nella DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="725c7-108">Number of parsers in the parser DLL.</span></span>

</dd> <dt>

<span data-ttu-id="725c7-109">**ParserInfo**</span><span class="sxs-lookup"><span data-stu-id="725c7-109">**ParserInfo**</span></span>
</dt> <dd>

<span data-ttu-id="725c7-110">Matrice di strutture [PF \_ PARSERINFO](pf-parserinfo.md) che descrivono ogni parser nella dll del parser.</span><span class="sxs-lookup"><span data-stu-id="725c7-110">Array of [PF\_PARSERINFO](pf-parserinfo.md) structures that describe each parser in the parser DLL.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="725c7-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="725c7-111">Remarks</span></span>

<span data-ttu-id="725c7-112">La struttura **PF \_ PARSERDLLINFO** viene restituita dalla funzione di esportazione [PARSERAUTOINSTALLINFO](parserautoinstallinfo.md) implementata nella dll del parser.</span><span class="sxs-lookup"><span data-stu-id="725c7-112">The **PF\_PARSERDLLINFO** structure is returned by the [ParserAutoInstallInfo](parserautoinstallinfo.md) export function that is implemented in the parser DLL.</span></span> <span data-ttu-id="725c7-113">La funzione **ParserAutoInstallInfo** identifica il numero di parser nella dll e usa una matrice di strutture [PF \_ PARSERINFO](pf-parserinfo.md) per descrivere ogni parser.</span><span class="sxs-lookup"><span data-stu-id="725c7-113">The **ParserAutoInstallInfo** function identifies the number of parsers in the DLL, and uses an array of [PF\_PARSERINFO](pf-parserinfo.md) structures to describe each parser.</span></span>

<span data-ttu-id="725c7-114">\_È necessario allocare la struttura PF PARSERDLLINFO usando **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="725c7-114">The PF\_PARSERDLLINFO structure must be allocated using **HeapAlloc**.</span></span>



| <span data-ttu-id="725c7-115">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="725c7-115">For information on</span></span>                                               | <span data-ttu-id="725c7-116">Vedere</span><span class="sxs-lookup"><span data-stu-id="725c7-116">See</span></span>                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="725c7-117">Quali sono i parser e come funzionano con Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="725c7-117">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="725c7-118">Parser</span><span class="sxs-lookup"><span data-stu-id="725c7-118">Parsers</span></span>](parsers.md)                                                      |
| <span data-ttu-id="725c7-119">I punti di ingresso inclusi nella DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="725c7-119">Which entry points are included in the parser DLL.</span></span>               | [<span data-ttu-id="725c7-120">Architettura DLL parser</span><span class="sxs-lookup"><span data-stu-id="725c7-120">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                      |
| <span data-ttu-id="725c7-121">L'implementazione di **ParserAutoInstallInfo**  include un esempio.</span><span class="sxs-lookup"><span data-stu-id="725c7-121">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="725c7-122">Implementazione di ParserAutoIstallInfo</span><span class="sxs-lookup"><span data-stu-id="725c7-122">Implementing ParserAutoIstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="725c7-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="725c7-123">Requirements</span></span>



| <span data-ttu-id="725c7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="725c7-124">Requirement</span></span> | <span data-ttu-id="725c7-125">Valore</span><span class="sxs-lookup"><span data-stu-id="725c7-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="725c7-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="725c7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="725c7-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="725c7-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="725c7-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="725c7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="725c7-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="725c7-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="725c7-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="725c7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="725c7-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="725c7-131"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="725c7-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="725c7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="725c7-133">PF \_ PARSERINFO</span><span class="sxs-lookup"><span data-stu-id="725c7-133">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> <dt>

[<span data-ttu-id="725c7-134">ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="725c7-134">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md)
</dt> </dl>

 

 




