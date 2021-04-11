---
title: ODJ_SID
description: Definizione di ODJ_SID IDL
ms.assetid: 1d06f725-6cd4-42cf-b171-c78a095690cb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: dd51f2e8a54eaf5be566e5a25f013ca1d87b9341
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "104047551"
---
# <a name="odj_sid-structure"></a><span data-ttu-id="a3c8f-103">Struttura ODJ_SID</span><span class="sxs-lookup"><span data-stu-id="a3c8f-103">ODJ_SID structure</span></span>

<span data-ttu-id="a3c8f-104">Contiene un ID di sicurezza (SID).</span><span class="sxs-lookup"><span data-stu-id="a3c8f-104">Contains a Security Identifier (SID).</span></span>

## <a name="syntax"></a><span data-ttu-id="a3c8f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3c8f-105">Syntax</span></span>

```C++
typedef struct _ODJ_SID
{
    UCHAR Revision;
    UCHAR SubAuthorityCount;
    SID_IDENTIFIER_AUTHORITY IdentifierAuthority;
    [size_is(SubAuthorityCount)] ULONG SubAuthority[*];
}   ODJ_SID, *PODJ_SID;
```

## <a name="members"></a><span data-ttu-id="a3c8f-106">Members</span><span class="sxs-lookup"><span data-stu-id="a3c8f-106">Members</span></span>

### <a name="revision"></a><span data-ttu-id="a3c8f-107">Revisione</span><span class="sxs-lookup"><span data-stu-id="a3c8f-107">Revision</span></span>

<span data-ttu-id="a3c8f-108">Deve essere impostato sulla revisione SID.</span><span class="sxs-lookup"><span data-stu-id="a3c8f-108">Must be set to the SID revision.</span></span>

### <a name="subauthoritycount"></a><span data-ttu-id="a3c8f-109">SubAuthorityCount</span><span class="sxs-lookup"><span data-stu-id="a3c8f-109">SubAuthorityCount</span></span>

<span data-ttu-id="a3c8f-110">Deve essere impostato sul numero di elementi nella sottoautorizzazione.</span><span class="sxs-lookup"><span data-stu-id="a3c8f-110">Must be set to the number of elements in SubAuthority.</span></span>

### <a name="identifierauthority"></a><span data-ttu-id="a3c8f-111">IdentifierAuthority</span><span class="sxs-lookup"><span data-stu-id="a3c8f-111">IdentifierAuthority</span></span>

<span data-ttu-id="a3c8f-112">Deve essere impostato sull'identificatore dell'autorità SID.</span><span class="sxs-lookup"><span data-stu-id="a3c8f-112">Must be set to the SID authority identifier.</span></span>

### <a name="subauthority"></a><span data-ttu-id="a3c8f-113">SubAuthority</span><span class="sxs-lookup"><span data-stu-id="a3c8f-113">SubAuthority</span></span>

<span data-ttu-id="a3c8f-114">Deve contenere una matrice di sottoautorità SID.</span><span class="sxs-lookup"><span data-stu-id="a3c8f-114">Must contain an array of SID sub authorities.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3c8f-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3c8f-115">See also</span></span>

[<span data-ttu-id="a3c8f-116">**Definizioni IDL di aggiunta al dominio offline**</span><span class="sxs-lookup"><span data-stu-id="a3c8f-116">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="a3c8f-117">**\_ \_ autorità identificatore SID \_ ODJ**</span><span class="sxs-lookup"><span data-stu-id="a3c8f-117">**ODJ\_SID\_IDENTIFIER\_AUTHORITY**</span></span>](odj-sid_identifier_authority.md)
