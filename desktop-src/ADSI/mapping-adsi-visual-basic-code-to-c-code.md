---
title: Mapping del codice Visual Basic ADSI al codice C++
description: ADSI è costituito da più di 50 interfacce.
ms.assetid: 6316f504-265e-44d4-ba24-e6289065981b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c64a022569a95f38ec1da7a1cb7acf533eb04ca6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297666"
---
# <a name="mapping-adsi-visual-basic-code-to-c-code"></a><span data-ttu-id="40d22-103">Mapping del codice Visual Basic ADSI al codice C++</span><span class="sxs-lookup"><span data-stu-id="40d22-103">Mapping ADSI Visual Basic Code to C++ Code</span></span>

<span data-ttu-id="40d22-104">ADSI è costituito da più di 50 interfacce.</span><span class="sxs-lookup"><span data-stu-id="40d22-104">ADSI consists of more than 50 interfaces.</span></span> <span data-ttu-id="40d22-105">La maggior parte delle operazioni di directory può essere completata solo con cinque interfacce.</span><span class="sxs-lookup"><span data-stu-id="40d22-105">Most directory operations can be completed using only five interfaces.</span></span> <span data-ttu-id="40d22-106">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="40d22-106">They are:</span></span>

-   [<span data-ttu-id="40d22-107">**IADsOpenDSObject**</span><span class="sxs-lookup"><span data-stu-id="40d22-107">**IADsOpenDSObject**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)
-   [<span data-ttu-id="40d22-108">**IADs**</span><span class="sxs-lookup"><span data-stu-id="40d22-108">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
-   [<span data-ttu-id="40d22-109">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="40d22-109">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [<span data-ttu-id="40d22-110">**IDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="40d22-110">**IDirectoryObject**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [<span data-ttu-id="40d22-111">**IDirectorySearch**</span><span class="sxs-lookup"><span data-stu-id="40d22-111">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

<span data-ttu-id="40d22-112">La tabella seguente elenca i mapping dal codice ADSI VB/VBS al codice C++.</span><span class="sxs-lookup"><span data-stu-id="40d22-112">The following table lists mappings from ADSI VB/VBS code to C++ code.</span></span> <span data-ttu-id="40d22-113">Tenere presente che non si tratta di un elenco completo.</span><span class="sxs-lookup"><span data-stu-id="40d22-113">Be aware that this is not a complete list.</span></span>



| <span data-ttu-id="40d22-114">Codice VBS</span><span class="sxs-lookup"><span data-stu-id="40d22-114">VBS Code</span></span>                           | <span data-ttu-id="40d22-115">Codice VC</span><span class="sxs-lookup"><span data-stu-id="40d22-115">VC Code</span></span>                                                               |
|------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="40d22-116">Set obj = GetObject ()</span><span class="sxs-lookup"><span data-stu-id="40d22-116">Set obj = GetObject()</span></span>              | <span data-ttu-id="40d22-117">HR = AdsGetObject ()</span><span class="sxs-lookup"><span data-stu-id="40d22-117">hr = AdsGetObject()</span></span>                                                   |
| <span data-ttu-id="40d22-118">obj. Inserire obj. Ottiene obj. Padre</span><span class="sxs-lookup"><span data-stu-id="40d22-118">obj.Put obj.Get obj.Parent</span></span>         | <span data-ttu-id="40d22-119">IADs o IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="40d22-119">IADs or IDirectoryObject</span></span>                                              |
| <span data-ttu-id="40d22-120">obj. Creazione di obj. Elimina obj. MoveHere</span><span class="sxs-lookup"><span data-stu-id="40d22-120">obj.Create obj.Delete obj.MoveHere</span></span> | <span data-ttu-id="40d22-121">IADsContainer</span><span class="sxs-lookup"><span data-stu-id="40d22-121">IADsContainer</span></span>                                                         |
| <span data-ttu-id="40d22-122">Per ogni...</span><span class="sxs-lookup"><span data-stu-id="40d22-122">For each…</span></span> <span data-ttu-id="40d22-123">in...</span><span class="sxs-lookup"><span data-stu-id="40d22-123">in…</span></span>                      | <span data-ttu-id="40d22-124">AdsBuildEnumerator() ADsEnumerateNext()</span><span class="sxs-lookup"><span data-stu-id="40d22-124">AdsBuildEnumerator() ADsEnumerateNext()</span></span>                               |
| <span data-ttu-id="40d22-125">Connessione, comando, RecordSet</span><span class="sxs-lookup"><span data-stu-id="40d22-125">Connection, Command, RecordSet</span></span>     | <span data-ttu-id="40d22-126">IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="40d22-126">IDirectorySearch</span></span>                                                      |
| <span data-ttu-id="40d22-127">Descrittore di sicurezza, ACL, ACE</span><span class="sxs-lookup"><span data-stu-id="40d22-127">Security descriptor, ACL, ACE</span></span>      | <span data-ttu-id="40d22-128">IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="40d22-128">IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry</span></span> |



 

 

 




