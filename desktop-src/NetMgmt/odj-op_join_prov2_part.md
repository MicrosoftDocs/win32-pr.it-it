---
title: OP_JOINPROV2_PART
description: Definizione di OP_JOINPROV2_PART IDL
ms.assetid: c220627e-49bd-49f2-a03c-9cdef4b973ca
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8537b6ca9627a15470115a20f99082dae80e040
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "104118631"
---
# <a name="op_joinprov2_part-structure"></a><span data-ttu-id="70bb6-103">Struttura OP_JOINPROV2_PART</span><span class="sxs-lookup"><span data-stu-id="70bb6-103">OP_JOINPROV2_PART structure</span></span>

<span data-ttu-id="70bb6-104">Contiene informazioni aggiuntive utilizzate per la configurazione di un client aggiunto a un dominio.</span><span class="sxs-lookup"><span data-stu-id="70bb6-104">Contains additional information used for configuring a client joined to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="70bb6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70bb6-105">Syntax</span></span>

```C++
typedef struct _OP_JOINPROV2_PART
{
    DWORD     dwFlags;
    [string] wchar_t *lpNetbiosName;
    [string] wchar_t *lpSiteName;
    [string] wchar_t *lpPrimaryDNSDomain;
    DWORD             dwReserved;
    [string] wchar_t *lpReserved;
} OP_JOINPROV2_PART, *POP_JOINPROV2_PART;
```

## <a name="members"></a><span data-ttu-id="70bb6-106">Members</span><span class="sxs-lookup"><span data-stu-id="70bb6-106">Members</span></span>

### <a name="dwflags"></a><span data-ttu-id="70bb6-107">dwFlags</span><span class="sxs-lookup"><span data-stu-id="70bb6-107">dwFlags</span></span>

<span data-ttu-id="70bb6-108">Deve essere impostato su zero o su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="70bb6-108">Must be set to either zero or one of the following values:</span></span>

|<span data-ttu-id="70bb6-109">Valore</span><span class="sxs-lookup"><span data-stu-id="70bb6-109">Value</span></span>|<span data-ttu-id="70bb6-110">Significato</span><span class="sxs-lookup"><span data-stu-id="70bb6-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="70bb6-111">OP_JP2_FLAG_PERSISTENTSITE (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="70bb6-111">OP_JP2_FLAG_PERSISTENTSITE (0x00000001)</span></span>|<span data-ttu-id="70bb6-112">Il sito specificato in lpSiteName deve essere considerato il sito permanente per il client.</span><span class="sxs-lookup"><span data-stu-id="70bb6-112">The site specified in lpSiteName MUST be considered the permanent site for the client.</span></span>|

### <a name="lpnetbiosname"></a><span data-ttu-id="70bb6-113">lpNetbiosName</span><span class="sxs-lookup"><span data-stu-id="70bb6-113">lpNetbiosName</span></span>

<span data-ttu-id="70bb6-114">Contiene il nome NetBIOS dell'account del computer in formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="70bb6-114">Contains the Netbios name of the machine account in Unicode format.</span></span>

### <a name="lpsitename"></a><span data-ttu-id="70bb6-115">lpSiteName</span><span class="sxs-lookup"><span data-stu-id="70bb6-115">lpSiteName</span></span>

<span data-ttu-id="70bb6-116">Contiene il nome del sito Active Directory che il client deve utilizzare.</span><span class="sxs-lookup"><span data-stu-id="70bb6-116">Contains the name of the Active Directory site that the client should use.</span></span>

### <a name="lpprimarydnsdomain"></a><span data-ttu-id="70bb6-117">lpPrimaryDNSDomain</span><span class="sxs-lookup"><span data-stu-id="70bb6-117">lpPrimaryDNSDomain</span></span>

<span data-ttu-id="70bb6-118">Contiene il nome di dominio DNS primario che il client deve utilizzare.</span><span class="sxs-lookup"><span data-stu-id="70bb6-118">Contains the primary DNS domain name that the client should use.</span></span>

### <a name="dwreserved"></a><span data-ttu-id="70bb6-119">dwReserved</span><span class="sxs-lookup"><span data-stu-id="70bb6-119">dwReserved</span></span>

<span data-ttu-id="70bb6-120">Riservato per un utilizzo futuro e deve essere impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="70bb6-120">Reserved for future use and must be set to 0.</span></span>

### <a name="lpreserved"></a><span data-ttu-id="70bb6-121">lpReserved</span><span class="sxs-lookup"><span data-stu-id="70bb6-121">lpReserved</span></span>

<span data-ttu-id="70bb6-122">Riservato per utilizzi futuri e deve essere impostato su NULL.</span><span class="sxs-lookup"><span data-stu-id="70bb6-122">Reserved for future use and must be set to NULL.</span></span>

## <a name="see-also"></a><span data-ttu-id="70bb6-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70bb6-123">See also</span></span>

[<span data-ttu-id="70bb6-124">**Definizioni IDL di aggiunta al dominio offline**</span><span class="sxs-lookup"><span data-stu-id="70bb6-124">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
